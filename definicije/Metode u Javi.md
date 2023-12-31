[[Java]]

>A **method** is a block of code which only runs when it is called.
You can pass data, known as parameters, into a method.
Methods are used to perform certain actions, and they are also known as **functions**.

```java
public class Main {
  static void myMethod(ParametarDataType parametarName) {
    // code to be executed
  }
}
```
`static` govori da metodu main() mozemo da koristimo nevezano od class Main
`void` nam govori koj tip class vraca metoda, i u ovom slucaju je prazna, odnosno ne vraca nista kad se pozove, moze biti zamenjno sa bilo kojim [[Vriable u javi#Data Types|Data Type]]

### Tips

multiple methods can have the same name with different parameters:
```java
int myMethod(int x)
float myMethod(float x)
double myMethod(double x, double y)
```
Multiple methods can have the same name as long as the number and/or type of parameters are different.

#scope
In Java, variables are only accessible inside the region they are created. This is called **scope**.
Variables declared directly inside a method are available anywhere in the method following the line of code in which they were declared:
A block of code refers to all of the code between curly braces `{}`.

# Interface
>An `interface` is a completely "**[[Inheritance in Java#Abstraction|abstract class]]**" that is used to group related methods with empty bodies:

```java
// interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void run(); // interface method (does not have a body)
}
```

To access the interface methods, the interface must be "implemented" (kinda like inherited) by another class with the `implements` keyword (instead of `extends`). The body of the interface method is provided by the "implement" class.
- Like **abstract classes**, interfaces **cannot** be used to create objects (in the example above
- Interface methods do not have a body - the body is provided by the "implement" class
- On implementation of an interface, you must override all of its methods
- Interface methods are by default `abstract` [[Modifikatori u Javi#Non-Access Modifikatori|and]] `public`
- Interface attributes are by default `public`, `static`[[Modifikatori u Javi#Access Modifikatori|and]] `final`
- An interface cannot contain a constructor (as it cannot be used to create objects)

#use
 Why And When To Use Interfaces?

1) To achieve security - hide certain details and only show the important details of an object (interface).
2) Java does not support "multiple inheritance" (a class can only inherit from one superclass). However, it can be achieved with interfaces, because the class can **implement** multiple interfaces. 
**Note:** To implement multiple interfaces, separate them with a comma .

```java
interface FirstInterface {
  public void myMethod(); // interface method
}

interface SecondInterface {
  public void myOtherMethod(); // interface method
}

class DemoClass implements FirstInterface, SecondInterface {
  public void myMethod() {
    System.out.println("Some text..");
  }
  public void myOtherMethod() {
    System.out.println("Some other text...");
  }
}

class Main {
  public static void main(String[] args) {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```