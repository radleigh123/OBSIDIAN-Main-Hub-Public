---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Network Programming|HOME [Java]]]**

---
## The Stock Quote Program
![[JavaNetworkStockQuote.png|right hs-med]]
In this section you’ll learn how to write a program that can read stock market price quotes from the Internet. There are many Internet sites providing such quotes; the Internet portal Yahoo! is one of them.

Visit `http://finance.yahoo.com`, enter the symbol of any stock, MOT for example, and press the Get Quotes button. You’ll see the pricing information about Motorola, Inc. — a fragment of this web page is depicted on Figure 18-1.

But what’s more interesting for our goal is the URL that is displayed in the Web browser:
```java
http://finance.yahoo.com/q?s=MOT
```

Right-click this web page and select View Source from the pop-up menu to see the HTML contents of this page; you’ll see lots of HTML tags, and the information about MOT will be buried somewhere deep inside. Modify the line in the class `WebSiteReader` from Listing 18-1 to have it print the content of this page on the system console:
```java
url = new URL(”http://finance.yahoo.com/q?s=MOT”);
```

You can also store the whole page in a Java String variable instead of printing the lines. Just modify the while loop in Listing 18-1:
```java
String theWholePage;
String txt;

while (txt =buff.readLine() != null ){
	theWholePage=theWholePage + txt;
}
```

If you add some smart tokenizing (splitting into parts based on the specified tokens as in Listing 18-4) of `theWholePage`, to get rid of all HTML tags and everything but Last Trade info, you can create your own little Stock Quote program. While this approach is useful to sharpen your tokenizing skills, it may not be the best solution, especially if Yahoo! changes the wording it uses on this page. That’s why we’ll be using another URL that provides stock quotes in a cleaner comma-separated values (CSV) format. Here’s the URL that should be used for the symbol MOT:
```
http://quote.yahoo.com/d/quotes.csv?s=MOT&f=sl1d1t1c1ohgv&e=.csv
```

This URL produces a string that includes the stock symbol, last trade, date and time of the price quote, earning per share (EPS), opening price, day’s range, and volume. Compare the CSB line below with the data shown in Figure 18-1 — they are the same (the date is not shown on Figure 18-1).
```
“MOT”,7.81,”8/16/2010”,”4:00PM”,0.17,7.63,7.86,7.58,25934265
```

Now the task of tokenizing the entire web page comes down to parsing a short CSV line. The `StockQuote` class from Listing 18-4 does exactly this: It accepts the stock symbol from the command line, gets the data from Yahoo!, tokenizes the received CSV line, and prints the price quote on the console.
```java
import java.net.*;
import java.io.*;
import java.util.StringTokenizer;

public class Main {
    static void printStockQuote(String symbol) {
        String csvString;
        URL url = null;
        URLConnection urlConn = null;
        InputStreamReader inStream = null;
        BufferedReader buff = null;
        try {
            url = new URL("http://quote.yahoo.com/d/quotes.csv?s=" + symbol + "&f=sl1d1t1c1ohgv&e=.csv");
            urlConn = url.openConnection();
            inStream = new InputStreamReader(urlConn.getInputStream());
            buff = new BufferedReader(inStream);

            // get the quote as a csv string
            csvString = buff.readLine();
            // parse the csv string
            StringTokenizer tokenizer = new StringTokenizer(csvString, ",");
            String ticker = tokenizer.nextToken();
            String price = tokenizer.nextToken();
            String tradeDate = tokenizer.nextToken();
            String tradeTime = tokenizer.nextToken();

            System.out
                    .println("Symbol: " + ticker + " Price: " + price + " Date: " + tradeDate + " Time: " + tradeTime);
        } catch (MalformedURLException e) {
            System.out.println("Please check the spelling of "
                    + "the URL: " + e.toString());
        } catch (IOException e1) {
            System.out.println("Can’t read from the Internet: " + e1.toString());
        } finally {
            try {
                inStream.close();
                buff.close();
            } catch (Exception e) {
                System.out.println("StockQuote: can’t close streams" +
                        e.getMessage());
            }
        }
    }

    public static void main(String args[]) {
        if (args.length == 0) {
            System.out.println("Sample Usage: java StockQuote IBM");
            System.exit(0);
        }

        printStockQuote(args[0]);
    }
}
```

If you’ve gone through all the previous lessons in this book, reading and understanding the code in Listing 18-4 should be a piece of cake for you. Test the StockQuote program by running it from Eclipse (enter MOT as an argument in the Run Configuration window) or run it from a command window as follows:
```
java StockQuote MOT
```