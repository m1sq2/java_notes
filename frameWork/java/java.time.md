vreme u [[Java]]
# .time

```java
import java.time.LocalTime; // import the LocalTime class

public class Main {
  public static void main(String[] args) {
    LocalTime myObj = LocalTime.now();
    System.out.println(myObj);
  }
}
```

![[Pasted image 20230601030108.png]]
![[Pasted image 20230601030237.png]]
```java
DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss")
```
