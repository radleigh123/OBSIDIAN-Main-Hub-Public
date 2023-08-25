---
title: JavaAudio
creation-date: 2023-02-21
aliases:
tags:
- Java
- Java/javax.sound.sampled
- Java/java.io.File
- Java/AudioInputStream
- Java/Clip
- Java/Clip/open
- Java/Clip/close
- Java/Clip/setMicrosecondPosition
- Java/Clip/stop
- Java/toUpperCase
---
**[[Java#I/O Stream|HOME [Java]]]**

---
# Audio
**e.g.**
```java
import java.io.File;
import java.io.IOException;
import java.util.Scanner;

import javax.sound.sampled.*;

public class Proto {
    public static void main(String[] args) throws UnsupportedAudioFileException, IOException, LineUnavailableException {
        Scanner sc = new Scanner(System.in);
        File file = new File("sound.wav");
        AudioInputStream audioStream = AudioSystem.getAudioInputStream(file);
        Clip clip = AudioSystem.getClip();

        clip.open(audioStream);

        String response = "";

        while (!response.equals("Q")) {
            System.out.println("P - play  S - stop  R - reset  Q - quit");
            System.out.print("Enter choice: ");

            response = sc.next();
            response = response.toUpperCase();

            switch (response) {
                case ("P"):
                    clip.start();
                    break;
                case ("S"):
                    clip.stop();
                    break;
                case ("R"):
                    clip.setMicrosecondPosition(0);
                    break;
                case ("Q"):
                    clip.close();
                    break;
                default:
                    System.out.println("Not a valid response");
            }
        }

        System.out.println("Bye");
        sc.close();
    }
}
```

<br>

# 
---
- **AudioInputStream** - https://docs.oracle.com/javase/7/docs/api/javax/sound/sampled/AudioInputStream.html
- https://www.baeldung.com/java-play-sound