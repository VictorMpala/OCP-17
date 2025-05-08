- thousands of built in classes 
- without importing them you get erros such as cannot find symbol 

```java
import java.util.Random;  
  
public class NumberPicker {  
public static void main(String[] args) {  
    Random r = new Random();  
    System.out.println(r.nextInt(10));  
}  
}
```
# Packages
- detailed packages are called child packages 
- java. 
- com.wiley.java.
- after the website name, you can add anything
- seperated by periods .

# Wildcards 
- * to import all the classes in a package 
- importing many packages does not slow down the program

```java 
import java.utl.*
```

# Redundant Imports 
- java.lang is automatically imported 

```java
public class InputImports {
	public void read(Files files) {
	Paths.get("name");
}
}


import java.nio.*;// NO GOOD -­a wildcard only matches
// class names, not "file.Files"
import java.nio.*.*;// NO GOOD -­you can only have one wildcard
// and it must be at the end
import java.nio.file.Paths.*; // NO GOOD -­you cannot import methods
// only class names

// solutions that work
import java.nio.file.*;
import java.nio.file.Files;
import java.nio.file.Paths;
```

# Naming Conflicts 
- eg multiple implementations of date 
- java.util.Date and java.sql.Date
```java
import java.util.*;
import java.sql.*; // causes Date declaration to not compile

//this is the solution
import java.util.Date;
import java.sql.*;

// ambigious imports 
import java.util.Date;
import java.sql.Date;

// if you really want to use both, use the fully qualified class name
public class Conflicts {
	java.util.Date date;
	java.sql.Date sqlDate;
}

```
- If you explicitly import a class name, it takes precedence over any wildcards present

# Creating a new package 
- default package 
	- for throwaway code 
- the directory structure relates to the package name 
```java
package packagea;
public class ClassA {}

package packageb;
import packagea.ClassA;
public class ClassB {
	public static void main(String[] args) {
		ClassA a;
		System.out.println("Got it");
}
}
```

# Compiling and Running Code with Packages

```bash
javac packagea/ClassA.java packageb/ClassB.java
```

# Compiling with Wildcards
- using a wildcard 
```bash
javac packagea/*.java packageb/*.java
```
- wildcards for sub directories won't work 
```bash
javac *.java //specify the packages 
```

- to run the classB 
```bash 
java packageb.ClassB
```
![[Pasted image 20250508153114.png]]

# Compiling to another directory 
- y default, the javac command places the compiled classes in the same directory as the source code
- the -d option specifies this target directory.
![[Pasted image 20250508154105.png]]
- To run the program, you specify the classpath so Java knows where to find the classes.
```bash
java -­cp classes packageb.ClassB
java -­classpath classes packageb.ClassB
java -­-­class-­path classes packageb.ClassB
```
![[Pasted image 20250508154711.png]]

# Compiling with JAR files 
- A Java archive (JAR) file is like a ZIP file of mainly Java class files.
- 