- main() is the entry point which the JVM looks for 
- a java program begins execution with the main() method

# Creating a main() Method 
- main() lets the JVM call our code 

```java 
public class Zoo{
	public static void main(String[] args){
		System.out.println("Hello World");
	}
}
```

```bash
javac Zoo.java 
java Zoo
```

- public 
	- access modifier
		- methods level of exposure to potential callers in the program 
- static
	- binds a method to its class so it can be called by just the class name
	- for example, Zoo.main(). Java doesn’t need to create an object to call the main() method
- void 
	- return type
- A method that returns no data returns control to the caller silently
- . In general, it’s good practice to use void for methods that change an object’s state. In that sense, the main() method changes the program state from started to finished
- parameter list 
	- String[] args
	- String options[]
	- String... friends
		- any of these are acceptable 
- variable name args 
	- refers to arguments to arguments that were read when the JVM started
-  [] represent an array 
- ...
	- variable argument list 

## Optional Modifiers 
```java
public final static void main(final String[] args) {}
```
- final modifiers are optional 

# Passing Parameters to a Java Program 
- sending data to the main() method 

```java 
public class Zoo{
public static void main(String[] args) {
// System.out.println("Hello World");
	System.out.println(args[0]);
	System.out.println(args[1]);
}
}
```

```bash
javac Zoo.java
java Zoo Bronx Zoo
```
- positional arguments 
- if the second argument isn't provided, an error is generated 
```bash
Bronx
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 1 out of bounds for length 1
        at Zoo.main(Zoo.java:5)
```

# Single-File Source-Code
```bash
java Zoo.java Bronx Zoo
```
- skipping the compilation, hence the .java extension has to be included 