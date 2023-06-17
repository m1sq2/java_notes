try...Catch in [[Java]]

>The `try` statement allows you to define a block of code to be tested for errors while it is being executed.

>The `catch` statement allows you to define a block of code to be executed, if an error occurs in the try block.

>The `try` and `catch` keywords come in pairs:

```java
try {
  //  Block of code to try
}
catch(Exception e) {
  //  Block of code to handle errors
}
```

>The `finally` statement lets you execute code, after `try...catch`, regardless of the result

>The `throw` statement allows you to create a custom error.

The `throw` statement is used together with an **exception type**. There are many exception types available in Java: `ArithmeticException`, `FileNotFoundException`, `ArrayIndexOutOfBoundsException`, `SecurityException`, etc: