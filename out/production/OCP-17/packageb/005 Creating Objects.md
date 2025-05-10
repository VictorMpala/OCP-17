- an object is an instance of a class
- constructors, object fields, instance initializers, and the order in which values are
initialized.

# Calling Constructors
```java
Park p = new Park();
```
- declare the type...Park 
- variable name...p
- new Park()...to actually create the object
- Park()...is It’s called a constructor, which is a special type of method that creates a new object.

- constructor
```java
public class Chick {
	public Chick() {
	System.out.println("in constructor");
	}
}
```
- key points 
	- the name of the constructor matches the name of the class
	- no return type 

```java
public class Chick {
	public void Chick() { } //not a constructor
}
```
==When you see a method name beginning with a capital letter and having a return type,==
==pay special attention to it. It is not a constructor since there’s a return type. It’s a regular==
==method that does compile but will not be called when you write new Chick().==
- purpose of a constructor is to initialize fields
- Another way to initialize fields is to do so directly on the line on which they’re declared.

```java
public class Chicken {
	int numEggs = 12; // initialize on line
	String name;

public Chicken() {
	name = "Duke"; // initialize in constructor
	}
 }
```

# Reading and Writing Member Fields
