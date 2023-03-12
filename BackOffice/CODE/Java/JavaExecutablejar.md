---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
---
**[[Java|HOME [Java]]]**

---
## Executable (.jar)
Compile java
```cmd
javac fileName.java
```

Manifest file (**.MF**)
```
Main-Class: fileName
(empty)
```

Creating jar file
```
jar -cvfm fileName.jar manifestFile.MF fileName.class
```

Running the jar
```
java -jar Proto.jar
```

<br>

# 
---
- https://dev.to/rohitk570/create-an-executable-jar-file-on-vs-code-n-command-line-154b