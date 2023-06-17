[[Java]] [[Import for java#Java libs|libs]] JSL utilitis

# .Scanner
```java
import java.util.Scanner;

public class Main{
	public static void main(String[] args){
		
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Unesi teskt");
		String tekst = scanner.nextLine();
		
		System.out.println(tekst);
	}
}
```
![[Pasted image 20230601025944.png]]


# .ArrayList

>The difference between a built-in [[Arrays in Java]] and an `ArrayList` in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one). While elements can be added and removed from an `ArrayList` whenever you want. The syntax is also slightly different:

```java
import java.util.ArrayList; // import the ArrayList class

ArrayList<String> cars = new ArrayList<String>(); // Create an ArrayList object
```
umesto `String` mozes da stavis bilo koji [[Vriable u javi#Data Types|data type]]

- add()
- get()
- set()
- remove()
- size()
- sort()

# .LinkedList

>slicno ArrayList

>The `LinkedList` class has all of the same methods as the `ArrayList` class because they both implement the `List` interface. This means that you can add items, change items, remove items and clear the list in the same way.


==How the ArrayList works==

The `ArrayList` class has a regular array inside it. When an element is added, it is placed into the array. If the array is not big enough, a new, larger array is created to replace the old one and the old one is removed.

==How the LinkedList works==

The `LinkedList` stores its items in "containers." The list has a link to the first container and each container has a link to the next container in the list. To add an element to the list, the element is placed into a new container and that container is linked to one of the other containers in the list.
#use an `ArrayList` for storing and accessing data, and `LinkedList` to manipulate data.
![[Pasted image 20230601031439.png]]

# .HashMap

>A `HashMap` however, store items in "**key**/**value**" pairs, bukvalno je dnevnik kao iz pythonda

key/value mogu da budu bilo koj [[Vriable u javi#Data Types|data type]]
```java
HashMap<String, String> capitalCities = new HashMap<String, String>();
```
- put()
- get()
- remove()
- clear()
- size()
**Note:** Use the `keySet()` method if you only want the keys, and use the `values()` method if you only want the values

==[[Loops in Java#For|loop]] through a HashMap==
```java
// Print keys
for (String i : capitalCities.keySet()) {
  System.out.println(i);
}
```
```java
// Print values
for (String i : capitalCities.values()) {
  System.out.println(i);
}
```
```java
// Print keys and values
for (String i : capitalCities.keySet()) {
  System.out.println("key: " + i + " value: " + capitalCities.get(i));
}
```

# .HashSet
>A HashSet is a collection of items where every item is unique

svi items su objekti tkd mogu biti bilo koji [[Vriable u javi#Data Types|data type]]
```java
HashSet<String> cars = new HashSet<String>();
```
- add()
- contains()
- remove()
- clear()
- size()

==[[Loops in Java]]==
```java
for (String i : cars) {
  System.out.println(i);
}
```

# .Iterator

>An `Iterator` is an object that can be used to loop through collections, like [ArrayList](https://www.w3schools.com/java/java_arraylist.asp) and [HashSet](https://www.w3schools.com/java/java_hashset.asp). It is called an "iterator" because "iterating" is the technical term for looping.

==[[Loops in Java]]==
```java
while(it.hasNext()) {
  System.out.println(it.next());
}
```
- remove()
**Note:** Trying to remove items using a **for loop** or a **for-each loop** would not work correctly because the collection is changing size at the same time that the code is trying to loop.

# .regex

>A regular expression is a sequence of characters that forms a search pattern. When you search for data in a text, you can use this search pattern to describe what you are searching for.

- `Pattern` Class - Defines a pattern (to be used in a search)
- `Matcher` Class - Used to search for the pattern
- `PatternSyntaxException` Class - Indicates syntax error in a regular expression pattern

```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
  public static void main(String[] args) {
    Pattern pattern = Pattern.compile("w3schools", Pattern.CASE_INSENSITIVE);
    Matcher matcher = pattern.matcher("Visit W3Schools!");
    boolean matchFound = matcher.find();
    if(matchFound) {
      System.out.println("Match found");
    } else {
      System.out.println("Match not found");
    }
  }
}
// Outputs Match found
```
Flags in the `compile()` method change how the search is performed. Here are a few of them:

- `Pattern.CASE_INSENSITIVE` - The case of letters will be ignored when performing a search.
- `Pattern.LITERAL` - Special characters in the pattern will not have any special meaning and will be treated as ordinary characters when performing a search.
- `Pattern.UNICODE_CASE` - Use it together with the `CASE_INSENSITIVE` flag to also ignore the case of letters outside of the English alphabet

![[Pasted image 20230601034001.png]]
![[Pasted image 20230601034028.png]]
![[Pasted image 20230601034044.png]]

# .Consumer

>Use Java's `Consumer` interface to store a lambda expression in a variable:

```java
import java.util.ArrayList;
import java.util.function.Consumer;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(5);
    numbers.add(9);
    numbers.add(8);
    numbers.add(1);
    Consumer<Integer> method = (n) -> { System.out.println(n); };
    numbers.forEach( method );
  }
}
```