[[Java]]
![[Pasted image 20230531142815.png]]


# Class
>A Class is like an object constructor, or a "blueprint" for creating objects.

```java
public class Main {
  int x = 5;
}
```
You can also create an object of a class and access it in another class. This is often used for better organization of classes (one class has all the attributes and methods, while the other class holds the `main()` method (code to be executed)).

Remember that the name of the java file should match the class name. In this example, we have created two files in the same directory/folder

```java
public class Main {
  int x = 5;
}
```

```java
class Second {
  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

```bash
$ javac Main.java
$ javac Second.java
$ java Second
```
output: 5

### Atributi classe
>class attributes are variables within a class

```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

dakle pristupamo atributu tako sto `myObj.x` odnosno imeObjekta.imeAtributa

>moze im biti dodeljena vrednost,
>ako se koristi keyword `final` onda ne moze da im se dodeli vrednost

```java
public class Main {
  final int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // will generate an error: cannot assign a value to a final variable
    System.out.println(myObj.x);
  }
}
```

### Inner classes
bukvalno nested classes
- The purpose of nested classes is to group classes that belong together, which makes your code more readable and maintainable.

```java
class OuterClass {
  int x = 10;

  class InnerClass {
    public int myInnerMethod() {
      return x;
    }
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.myInnerMethod());
  }
}

// Outputs 10
```

u slucaju [[Modifikatori u Javi#Access Modifikatori]]
`private` ili `protected` je ucini da samo njena outer class moze  da je koristi
`static`  je ucini da mozes da je korists bez da zoves njenu outer class


# Objects
>object is an instance of a class. It represents a specific entity or data structure that is created based on the class's blueprint.

```java
Main myObj = new Main();
```
- prvo je tip, odnosno klassa na kojoj zasnivamo objekat
- zatim ide ime objekta
- =
- new , keyword da kreiramo novi objekat
- Main(), konstruktor koji koristimo

konstruktor je metoda koja je malo specificna jer se koristi za kreiranje objekata

