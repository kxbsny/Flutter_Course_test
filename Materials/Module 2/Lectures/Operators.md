## Operators

An operator is a symbol that tells the compiler or interpreter to perform specific mathematical, relational or logical operation and produce final result.



### 1 Arithmetic Operators

| Operator | Meaning                                                      |
| -------- | :----------------------------------------------------------- |
| `+`      | Add                                                          |
| `–`      | Subtract                                                     |
| `-expr`  | Unary minus, also known as negation (reverse the sign of the expression) |
| `*`      | Multiply                                                     |
| `/`      | Divide                                                       |
| `~/`     | Divide, returning an integer result                          |
| `%`      | Get the remainder of an integer division (modulo)            |

#### 1.1 Example

``` dart
var x = 10;
var y = 5;

print(x + y); // 15
print(x - y); // 5
print(- x); // -10
print(x * y); // 50
print(x / y); // 2.0
print(x ~/ y); // 2
print(x % y); // 0
```



### 2 Equality and relational operators

| Operator | Meaning                     |
| -------- | --------------------------- |
| `==`     | Equal; see discussion below |
| `!=`     | Not equal                   |
| `>`      | Greater than                |
| `<`      | Less than                   |
| `>=`     | Greater than or equal to    |
| `<=`     | Less than or equal to       |

#### 2.1 Example

``` dart
var x = 10;
var y = 5;

print(x == y); // false
print(x != y); // true
print(x > y); // true
print(x < y); // false
print(x >= y); // true
print(x <= y); // false
```



### 3 Logical operators

| Operator | Meaning                                                      |
| -------- | ------------------------------------------------------------ |
| `!expr`  | inverts the following expression (changes false to true, and vice versa) |
| `||`     | logical OR                                                   |
| `&&`     | logical AND                                                  |

#### 3.1 Example

``` dart
print(! true); // false
print(! false); // true

print(true || true); // true
print(true || false); // true
print(false || true); // true
print(false || false); // false

print(true && true); // true
print(true && false); // false
print(false && true); // false
print(false && false); // false
```



### 4 Bitwise and shift operators

| Operator | Meaning                                               |
| -------- | ----------------------------------------------------- |
| `&`      | AND                                                   |
| `|`      | OR                                                    |
| `^`      | XOR                                                   |
| `~expr`  | Unary bitwise complement (0s become 1s; 1s become 0s) |
| `<<`     | Shift left                                            |
| `>>`     | Shift right                                           |

#### 4.1 Example

``` dart

```



### 5 Assignment operators

| Operator | Meaning                                                      |
| -------- | ------------------------------------------------------------ |
| `=`      | assign value to a variable                                   |
| `??=`    | assign value to a variable if the variable is null; otherwise, the variable stays the same value |

#### 5.1 Example

``` dart
int a = 0;
a = 10;
print(a); // 10

int b;
print(b); // null
b ??= 20;
print(b); // 20
b ??= 30;
print(b); // 20
```



###  6 Compound Assignment Operators

| `=`  | `-=` | `/=`  | `%=`  | `>>=` | `^=` |
| ---- | ---- | ----- | ----- | ----- | ---- |
| `+=` | `*=` | `~/=` | `<<=` | `&=`  | `|=` |

|                           | Compound assignment | Equivalent expression |
| ------------------------- | ------------------- | --------------------- |
| **For an operator *op*:** | `a op= b`           | `a = a op b`          |
| **Example:**              | `a += b`            | `a = a + b`           |

#### 6.1 Example

``` dart

```



### 7 Type test operators

| Operator | Meaning                                    |
| -------- | ------------------------------------------ |
| `as`     | Typecast                                   |
| `is`     | True if the object has the specified type  |
| `is!`    | False if the object has the specified type |

#### 7.1 Example

``` dart
int a = 0;
if (a is int) {
	print("a is type of int");
} else {
	print("a is not type of int");
} // a is type of int

double b = 1.1;
if (b is! int) {
	print("b is not type of int");
} else {
	print("b is type of int");
} // b is not type of int
```



### 8 Conditional Expressions

| Expression                  | Meaning                                                      |
| --------------------------- | ------------------------------------------------------------ |
| `condition ? expr1 : expr2` | If condition is true, evaluates expr1 (and returns its value); otherwise, evaluates and returns the value of expr2. |
| `expr1 ?? expr2`            | If expr1 is non-null, returns its value; otherwise, evaluates and returns the value of expr2. |

#### 8.1 Example

``` dart
String str ;
str = true ? 'ab' : 'bc';
print(str); // ab
str = false ? 'ab' : 'bc';
print(str); // bc

String name;
print(name); // null
name = 'good' ?? 'bad'; 
print(name); // good
name = null ?? 'bad';
print(name); // bad
```



### 9 Cascade Notation

Cascades (`..`) allow you to make a sequence of operations on the same object. In addition to function calls, you can also access fields on that same object. This often saves you the step of creating a temporary variable and allows you to write more fluid code.

#### 9.1 Example



### 10 Assignment operators

#### 10.1 Example

