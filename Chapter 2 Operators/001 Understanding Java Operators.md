- use of operators to evaluate variables

# Understanding Java Operators
- A Java operator is a special symbol that can be applied to a set of variables, values, or literals—­referred to as operands—­ and that returns a result
- operand refers to the value or variable the operator is being applied to
![[Pasted image 20250222000623.png]]
- = is the assignment operator 

# Types of Operators 
- unary, binary, ternary
- can be applied to one, two, or three operands, respectively
- reward evaluates to 9.0
```java
public class Operator {  
    public static void main(String[] args) {  
        int cookies = 4;  
        double reward = 3 + 2 * --cookies;  
        System.out.print("Zoo animal receives: "+reward+" reward points");  
    }}
```

# Operator Precedence
![[Pasted image 20250222001455.png]]
- if equal evaluation is from left to right 
- -> lambda operator

# Applying Unary Operators 
- requires exactly one operand 
![[Pasted image 20250222001938.png]]

# Complement and Negation Operators 
- logical complement operator !
```java
boolean isAnimalAsleep = false;
System.out.print(isAnimalAsleep); // false
isAnimalAsleep = !isAnimalAsleep;
System.out.print(isAnimalAsleep); // true
```

- bitwise complement operator (~)
	- flips all of the 0s and 1s in a number
- only be applied to integer numeric types such as byte, short, char, int, and long

```java
int value = 3;
int complement = ~value;
System.out.println(value);
System.out.println(complement);
```
- to find the bitwise complement of a number, multiply it by negative one and then subtract one.

- negration operator  - 
```java
	double zooTemperature = 1.21;
	System.out.println(zooTemperature); // 1.21
	zooTemperature = -­zooTemperature;
	System.out.println(zooTemperature); // -­1.21
	zooTemperature = -­(-­zooTemperature);
	System.out.println(zooTemperature); // -­1.21
```

- more examples
```java
int pelican = !5; // DOES NOT COMPILE
boolean penguin = -­true; // DOES NOT COMPILE
boolean peacock = !0; // DOES NOT COMPILE
```
- cannot perform a logical inversion of a numeric value
- cannot numerically negate a boolean value
- cannot take the logical complement of a numeric value, nor can you assign an integer to a boolean variable.
- in Java, 1 and true are not related in any way, just as 0 and false are not related.

# Increment and Decrement Operators 
- applied first in the expression 
![[Pasted image 20250222004858.png]]
- For the exam, it is critical that you know the difference between expres-sions like parkAttendance++ and ++parkAttendance. The increment and decrement operators will be in multiple questions, and confusion about which value is returned could cause you to lose a lot of points on the exam.