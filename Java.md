#java #OOP

>Java is a high-level, object-oriented programming language that is designed to be platform-independent, meaning it can run on different operating systems without requiring major modifications.

>Java offers features such as automatic memory management, strong type checking, exception handling, and a rich set of libraries and frameworks, making it a popular choice for building reliable and scalable software solutions.

1. napisi program u javi
2. compajluj code u bytes
3. tako compailovan moze da bude pokrenut na bilo kojoj mashin koja ima Java Virtual Machine

instaliranje JVM zavisi od Operativnog Sistema do Operativnog Sistema, prilagodjeno je tako da moze da korisit resurse

***

```java
public class Main{
	public static void main(String[] args){
		//ovo je komentar
		
		System.out.println("Hello, World!");
		
		/*
		ovo
		je
		blok
		komentar
		*/
	}
}
```

pravilo definisanja ide:
	- prvo se definise da li je javno/prvivatno/ili vec
	- zatim sta je (klasa, metoda...)
	- i slucaju metoda, i koj tip podatka vraca
	- i na kraju ime definicije

`public` govori da je javno
`class` govori da je klasa (objekat)
`Main` govori ime klase

`static` govori da metodu main() mozemo da koristimo nevezano od class Main, npr:
```java
main() //kada se koristi static
Main.main() //kad ne bi bilo statica
```
`void` nam govori koj tip class vraca metoda, i u ovom slucaju je prazna, odnosno ne vraca nista kad se pozove 
`String[]` koji se nalazi unutar main( ) nam govori da metoda main() uzima za variablu niz Stringova, `args` je ime te variable

`System` je classa predefinisana od starane java i nudi pristup razlicitim mogucnostima sistema
`out` je variabla definisana unutar class `System` , type `PrintStream` i predstavlja standardni output za system
`println` je metoda unutar classe `System` koja za variablue uzima String i onda ga outputuje u CLI, razlika izmedju `print` i `println` je sto `println` dodaje `\n` ([[escape sequences in java | tip]]) na kraju svakog Stringa

komentare compiler ignorise

- - -


>nakon sto smo napisali ovakav program, mozemo da ga comailujemu u CLI i onda pokrenemo

```bash
$ javac Main.java
$ java Main
```

---
---

>>DOKUMENTACIJA

1. [[Classes-Objects in Java]]
	1. [[Classes-Objects in Java#Class|Class]]
		1. [[Classes-Objects in Java#Atributi classe|Atributi]]
		2. [[Constructori u Javi]]
		3.  [[Wrapper Classes in java|Wrapper]]
		4. [[Classes-Objects in Java#Inner classes|inner]]
	2. [[Classes-Objects in Java#Objects|Objects]]
		1. [[Modifikatori u Javi|Modifikatori]]
		2. [[Arrays in Java|Arrays]]
		3. [[String in Java|Strings]]
		4. [[java.util#.ArrayList]]
		5. [[java.util#.LinkedList]]
		6. [[java.util#.HashMap]]
		7. [[java.util#.HashSet]]
		8. [[java.util#.Iterator]]
		9. [[java.util#.regex]]
		10. [[java.util#.Consumer]]
	3. [[Metode u Javi]]
		1. [[Metode u Javi|Interface]]
		2. [[Threads in java| Threads]]
	4. [[Inheritance in Java|Inheritance]]
		1. [[Inheritance in Java#Abstraction| Abstraktne classes]]
		2. [[Enums u Javi|Enums]]
2. [[Vriable u javi|Data/Value manipulation]]
	1. [[Vriable u javi#Data Types|Data Types]]
		1. [[Operacije u javi|Operation]]
		2. [[Math in java|Math]]
		3. [[escape sequences in java|Escape Sequences]]
	2. [[Loops in Java|Loops]]
		1. [[If Else Switch u Javi|If Else Switch]]
		2. [[Break and Continue in Java|Break/Continue]]
		3. [[Exceptions in Java|Try...Catch]]
3. [[Import for java| Packages]]
	1. Frameworks
		1. Java
			1. [[java.util]]
			2. [[java.io]]
			3. [[java.time]]
			4. [[java.net]]
		2. Javax
			1. [[javax.swing]]
4. [[tips for java| TIPS]]

