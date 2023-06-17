in [[Java]]
>An `enum`  is a special "[[Classes-Objects in Java#Class|class]]" that represents a group of **constants** (unchangeable variables, like **[[Modifikatori u Javi#Access Modifikatori|final]]** variables).
To create an `enum`, use the `enum` keyword (instead of class or [[Metode u Javi#Interface|interface]]), and separate the constants with a comma. 
**Note** that they should be in uppercase letters:

```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}
```
You can access `enum` constants with the **dot** syntax:

```java
Level myVar = Level.MEDIUM;
```

==Loop Through an Enum==

```java
for (Level myVar : Level.values()) {
  System.out.println(myVar);
}
```

==Difference between Enums and Classes==

An `enum` can, just like a `class`, have attributes and methods. The only difference is that enum constants are `public`, `static` and `final` (unchangeable - cannot be overridden).

An `enum` cannot be used to create objects, and it cannot extend other classes (but it can implement interfaces).

==Why And When To Use Enums?==
#use
Use enums when you have values that you know aren't going to change, like month days, days, colors, deck of cards, etc.