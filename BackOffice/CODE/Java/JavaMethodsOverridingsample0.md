---
aliases:
tags:
---
**[[JavaMethodsOverriding|BACK]]**

---
Where a Bank is a class that provides functionality to get the rate of interest. However, the rate of interest varies according to banks. For example, SBI, ICICI and AXIS banks could provide 8%, 7%, and 9% rate of interest.

![[JavaMethodsOverridingsample0image0.png|center]]
>[!aside|show-title right]+ RESULT:
> SBI Rate of Interest: 8  
> ICICI Rate of Interest: 7
> AXIS Rate of Interest: 9

```java
class Bank {
    int getRateOfInterest() {
        return 0;
    }
}

class SBI extends Bank {
	@Override
    int getRateOfInterest() {
        return 8;
    }
}

class ICIC extends Bank {
	@Override
    int getRateOfInterest() {
        return 7;
    }
}

class AXIS extends Bank {
	@Override
    int getRateOfInterest() {
        return 9;
    }
}

public class Proto1 {
    public static void main(String[] args) {
        SBI sub1 = new SBI();
        ICIC sub2 = new ICIC();
        AXIS sub3 = new AXIS();

        System.out.printf("SBI Rate of Interest: %d%n", sub1.getRateOfInterest());
        System.out.printf("ICICI Rate of Interest: %d%n", sub2.getRateOfInterest());
        System.out.printf("AXIS Rate of Interest: %d", sub3.getRateOfInterest());
    }
}
```