[[Java]] inheritance of [[Classes-Objects in Java#Class|Class]] attributes and methods

We group the "inheritance concept" into two categories:

- **subclass** (child) - the class that inherits from another class
- **superclass** (parent) - the class being inherited from

To inherit from a class, use the `extends` keyword.

```java
class Vehicle {
  ...
}

class Car extends Vehicle {
  ...
}
```

mozes da koristi [[Modifikatori u Javi#Non-Access Modifikatori|final]] na klasi da ne moze da bude nasledjna
```java
final class Vehicle {
  ...
}

class Car extends Vehicle {
  ...
}
```

```
`Main.java:9: error: cannot inherit from final Vehicle   class Main extends Vehicle {                     ^   1 error)`
```

# Polymorphism
>Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.

bukvalno samo naziv za to sto ces extendovati classu u novu classu i onda je modifikovati tako sto joj das nove atribute i metode, nista posebno iskreno

# Abstraction

>class namenja iskljucivo da bude nasledjivana

Data **abstraction** is the process of hiding certain details and showing only essential information to the user.  
Abstraction can be achieved with either **abstract classes** or **[[Metode u Javi#Interface|Interface]]**

The `abstract` keyword is a [[Modifikatori u Javi#Non-Access Modifikatori|non-access modifier]], used for classes and methods:
- **Abstract class:** is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
- **Abstract method:** can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).

#use
*To achieve security - hide certain details and only show the important details of an object.
