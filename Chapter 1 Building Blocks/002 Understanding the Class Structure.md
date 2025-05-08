- in java classes are the basic building blocks 
- When defining a class, you describe all the parts and characteristics of one of those building blocks.
- To use a class, an object has to be created 
- An object is a runtime instance of a class in memory
- instance...single representation of the class 
- objects represent the state of the program 
- A reference is a variable that points to an object.

# Fields and Methods 
- classes consist of methods and fields(which are the members of the class)
	- variables hold the state of the program
	- methods(functions)...perform actions on the state 
- simple java class 
```java 
public class Animal{
	String name;
	public String getName(){
		return name;
	}

	public void setName(String newName){
		name = newName;
	}
}
```
- class 
	- indicates the definition of a class 
- Animal 
	- name of the class 
- String name 
	- field 
	- String is also a class provided by Java 
- methods
	- public...can be called from any class 
	- return type...string or void 
	- void doesn't return anything but requires a parameter to be provided 
- method name and parameters are know as the signature 

- Example
```java 
public int numberVisitors(int month){
	return 10
}
```
- parameter...month, which is of type int
- method...numberVisitors 
- method signature is numberVisitors(int)

# Comments 
```java 
//single line comment

/*
* multi line comment 
*/

/**
* javadoc 
* @author Victor Mpala
*/
```
- the javadoc tools can interpret the javadoc comments 
- this comment won't compile
```java
/*
* /* ferret */
*/
```

# Classes and Source Files 
- each class is defined in it;s own .java file
- A top-­level type is a data structure that can be defined independently within a source file
- public
	- any code can call it 
	- public is not really necessary but the class name has to match the file name 

```java 
class Animal(){
	String name;
}
```
- 2 types can be used but the top level type has to be public 

```java 
public class Animal {
	private String name;
}
```
