---
cssclass:
- t-w
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Java Memory Management|HOME [Java]]]**

---
### Options for heap sizes
|                                              | <center>Definition</center>                                                       |
| -------------------------------------------- | --------------------------------------------------------------------------------- |
| <center>`-Xmx`</center>                      | set the maximum heap size                                                         |
| <center>`-Xms`</center>                      | set the starting heap size                                                        |
| <center>`-XX:MaxMetaspaceSize=size`</center> | sets the maximum amount of native memory that can be allocated for class metadata |
| <center>`-Xmn`</center>                      | set the size of the young generation                                              |
| <center>`-XX:HeapDumpOnOutOfMemory`</center> | creates a heap dump file                                                          | 

```
k - kilobyte
m - megabyte
g - gigabyte

-Xmx512m - Xms150m
-XX:MaxMetaspaceSize=250M
-Xmn256m
```

<br>

### Options for monitoring GC
|                               | <center>Definition</center> |
| ----------------------------- | --------------------------- |
| <center>`verbose:gc`</center> | print to console when a GC takes places                            |

```
-Xmx50m -verbose:gc
```

<br>

# 
---
- [java (oracle.com)](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/java.html)