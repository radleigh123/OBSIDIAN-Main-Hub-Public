---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Network Programming|HOME [Java]]]**

---
## The Stock Quote Server w/ Sockets
Before: [[JavaNetworkStockQuote|The Stock Quote Program]]

Let’s build a socket-based client/server application that emulates both a server providing fake price quotes for requested stocks and a client consuming this data.

The server will start and listen to requests on `port 3000` (see Listing 18-5). The method accept() of the `SocketServer` class is the one that waits for the client’s requests. As soon as it starts you’ll see the message “*Waiting for a quote request*” on the system console, and nothing else will happen until the request comes in from the client. Creating a `SocketServer` instance binds it to the specified port, but if this port is already in use by another process you’ll get a `BindException`.
```java
import java.io.*;
import java.net.*;

public class Main {
    public static void main(java.lang.String[] args) {
        ServerSocket serverSocket = null;
        Socket client = null;
        BufferedReader inbound = null;
        OutputStream outbound = null;
        try {
            // Create a server socket
            serverSocket = new ServerSocket(3000);
            System.out.println("Waiting for a quote request");
            while (true) {
                // Wait for a request
                client = serverSocket.accept();
                // Get the streams
                inbound = new BufferedReader(new InputStreamReader(client.getInputStream()));
                outbound = client.getOutputStream();

                String symbol = inbound.readLine();
                // Generete a random price
                String price = (new Double(Math.random() * 100)).toString(); // DEPRECATED
                outbound.write(("\n The price of " + symbol + " is " + price + "\n").getBytes());

                System.out.println("Request for " + symbol + " has been processed. The price is " + price);
                outbound.write("End\n".getBytes());
            }
        } catch (IOException ioe) {
            System.out.println("Error in Server: " + ioe);
        } finally {
            try {
                inbound.close();
                outbound.close();
            } catch (Exception e) {
                System.out.println("StockQuoteServer: cant close streams" + e.getMessage());
            }
        }
    }
}
```
When a client connects to the socket, the server gets references to its I/O streams and sends randomly generated quotes for the requested stock. In the real world this server would have to be connected to another program providing real-time market data, but for our purposes generating random numbers as “*price quotes*” will suffice. The client program shown in Listing 18-6 has to be started with a command-line parameter such as IBM or MSFT to produce a price quote.
```java
import java.io.*;
import java.net.*;

public class Main {
    public static void main(java.lang.String[] args) {
        if (args.length == 0) {
            System.out.println("Usage: java Client Symbol");
            System.exit(0);
        }
        OutputStream outbound = null;
        BufferedReader inbound = null;
        Socket clientSocket = null;
        try {
            // Open a client socket connection
            clientSocket = new Socket("localhost", 3000);
            System.out.println("Client: " + clientSocket);
            // Get the streams
            outbound = clientSocket.getOutputStream();
            inbound = new BufferedReader(new InputStreamReader(clientSocket.getInputStream()));
            // Send stock symbol to the server
            outbound.write((args[0] + "\n").getBytes());
            outbound.write("End\n".getBytes());
            String quote;
            while (true) {
                quote = inbound.readLine();
                if (quote.equals("End")) {
                    break;
                }
                System.out.println("Got the quote for " + args[0] + ":" + quote);
            }
        } catch (UnknownHostException uhe) {
            System.out.println("UnknownHostException: " + uhe);
        } catch (IOException ioe) {
            System.err.println("IOException: " + ioe);
        } finally {
            // Close the streams
            try {
                outbound.close();
                inbound.close();
                clientSocket.close();
            } catch (IOException e) {
                System.out.println("Can not close streams..." +
                        e.getMessage());
            }
        }
    }
}
```
Have you noticed that `StockQuoteServer` appends the word `End` to indicate that the price quote has ended? The class `Client` also checks for this word. This is an example of a very simple custom-made networking protocol.