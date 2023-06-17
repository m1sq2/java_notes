in [[Java]]

# While
```java
while (condition) {
  // code block to be executed
}
```

example:
```java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

## Do/While
```java
do {
  // code block to be executed
}
while (condition);
```

example:
```java
int i = 0;do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

# For
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```
- **Statement 1** is executed (one time) before the execution of the code block.
- **Statement 2** defines the condition for executing the code block.
- **Statement 3** is executed (every time) after the code block has been executed.

example:
```java
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```

## Nested Loops
```java
// Outer loop
for (int i = 1; i <= 2; i++) {
  System.out.println("Outer: " + i); // Executes 2 times
  
  // Inner loop
  for (int j = 1; j <= 3; j++) {
    System.out.println(" Inner: " + j); // Executes 6 times (2 * 3)
  }
} 
```
loop unutar loopa

# For-Each
```java
for (type variableName : arrayName) {
  // code block to be executed
}
```

example:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```
