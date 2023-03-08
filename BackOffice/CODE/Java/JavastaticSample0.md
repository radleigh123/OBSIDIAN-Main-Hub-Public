---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/static
- Java/Methods
---
**[[Javastatic|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> 37.05555555555556

```java
class WeatherReport {
    static double convertValue(double x) {
        return ((x - 32) * 5 / 9);
    }
}

public class Proto {

    public static void main(String[] args) {
	    // calling the function w/out instantiating the class
        double y = WeatherReport.convertValue(98.7);

        System.out.println(y);
    }
}
```