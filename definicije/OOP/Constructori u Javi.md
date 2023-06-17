[[Java]]
>A constructor in Java is a **special method** that is used to initialize objects. The constructor is called when an [[Classes-Objects in Java#Objects|Objects]] of a [[Classes-Objects in Java#Class|Class]] is created. It can be used to set initial values for object attributes

- constructor name must **match the class name**, and it cannot have a **return type** (like `void`).
- constructor is called when the object is created.
- All classes have constructors by default: if you do not create a class constructor yourself, Java creates one for you.
- 
```java
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }
```


# Parametri

>konsturktori mogu da zahtevaju parametri, i mozes da imas vise konstruktora tako da pokrijes razlicite opcije parametara koje mozes korisnik da unese

