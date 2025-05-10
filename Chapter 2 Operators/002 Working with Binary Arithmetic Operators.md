- take two operands 
- perform mathematical operations on variables, create logical expressions, and perform basic variable assignments

# Arithmetic Operators
- operate on numeric values 
![[Pasted image 20250222010435.png]]
- also include ++ and -- 
```java
//evaluates to 14
int price = 2 * 5 + 3 * 4 -­8;
```
- can be applied to primitives except boolean 
- + can be applied to String for concatenation purposes 

# Adding Parentheses
- changing the order of operation using parenthesis
```java
//evaluates to 48
int price = 2 * ((5 + 3) * 4 -­8);
```
# Verifying Parentheses Syntax 
- imbalanced parentheses 
	- no matching parentheses 
```java
// both don't applu
long pigeon = 1 + ((3 * 5) / 3;
int blueJay = (9 + 2) + 3) / (2 * 4;
// DOES NOT COMPILE
// DOES NOT COMPILE
```

- [] cannot be used in place of parentheses
```java
short robin = 3 + [(4 * 2) + 4];
// DOES NOT COMPILE
```

# Division and Modulus Operators

```java
System.out.println(9 / 3); // 3
System.out.println(9 % 3); // 0

System.out.println(10 / 3); // 3
System.out.println(10 % 3); // 1

System.out.println(11 / 3); // 3
System.out.println(11 % 3); // 2

```
- floor value is 4 for each of the values 4.0, 4.5, and 4.9999999.
- floor is different from rounding 
- modulus can also be applied to negative numbers 

# Numeric Promotion
- 