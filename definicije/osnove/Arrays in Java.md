in [[Java]]

```java
String[] cars;
```
```java
int[] myNum;
```

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
```
printuje "Volvo"

To find out how many elements an array has, use the `length` property:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
```
dobijes 4

### Loop
ima nekoliko opcij da se [[Loops in Java | loop]] kroz niz

[[Loops in Java#For | standardni nacin]]
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.length; i++) {
  System.out.println(cars[i]);
}
```

[[Loops in Java#For-Each | for-each nacin]]

```java
for (type variable : arrayname) {
  ...
}
```

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

# Vise Dimenzijonalni Nizovi

```java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };


System.out.println(myNumbers[1][2]); // Outputs 7

myNumbers[1][2] = 9;

System.out.println(myNumbers[1][2]); // Outputs 9 instead of 7

```

### Loop kroz vise dimenzijonalne

moraju da se koriste [[Loops in Java#Nested Loops | nested loops]]
```java
for (int i = 0; i < myNumbers.length; ++i) {
      for(int j = 0; j < myNumbers[i].length; ++j) {
        System.out.println(myNumbers[i][j]);
    }
}
```
