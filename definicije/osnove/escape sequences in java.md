escape sequences in  ==[[Java]]==


-   `\"`: Double quote
-   `\'`: Single quote
-   `\\`: Backslash
-   `\n`: Newline (line feed)
-   `\r`: Carriage return
-   `\t`: Tab
-   `\b`: Backspace
-   `\f`: Form feed
-   `\uXXXX`: Unicode escape sequence, where `XXXX` represents a hexadecimal value for a Unicode character

```java
public class EscapeSequences {
    public static void main(String[] args) {
        System.out.println("Hello, \"Java\"!"); // Output: Hello, "Java"!
        System.out.println("I\'m learning\tJava."); // Output: I'm learning    Java.
        System.out.println("This is a backslash: \\"); // Output: This is a backslash: \
        System.out.println("Line 1\nLine 2"); // Output: Line 1
                                                //         Line 2
        System.out.println("Hello\rWorld"); // Output: World
        System.out.println("Hello\bWorld"); // Output: HellWorld
        System.out.println("Hello\t\tWorld"); // Output: Hello      World
        System.out.println("Hello\fWorld"); // Output: Hello
                                             //         World
        System.out.println("\u0048\u0065\u006C\u006C\u006F"); // Output: Hello
    }
}

```

