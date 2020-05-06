## Variables

Variables are the names you give to computer memory locations which are used to store values in a computer program.



### 1 Explicit Typed Variable

``` dart
// declare a explicit typed variable
Variable_Type Variavle_Name = Variable_Value;

// uninitialized variables have an initial value of null
Variable_Type Variavle_Name;
```

#### 1.1 Example

``` dart
String universityName = 'Mizzou';
int foundedYear = 1839;
double campusAreaInSqMi = 31.3;

String a; // null
int b; // null
double c; // null
```



### 2 Type Inference Variable

Type inference is that the compiler can figure out the static types for you so you don't have to type them.

``` dart
// declare a type inference variable
var/dynamic/const/final Variavle_Name = Variable_Value;
```

#### 2.1 var

The **var** keyword is used to declare variables of **static** type.

- You can change the **value** after it was declared.
- You cannot change the **type** after it was declared with a different type of value.

##### 2.1.1 Example

``` dart
var year = 10;
print(year.runtimeType); // int
year = 5;
year = 10.5; // Error: A value of type 'double' can't be assigned to a variable of type 'int'.
year = '10'; // Error: A value of type 'String' can't be assigned to a variable of type 'int'.
```

#### 2.2 dynamic

The **dynamic** keyword is used to declare variables of **non-static** type.

- You can change the **value** after it was declared.
- You can change the **type** after it was declared with a different type of value.

##### 2.2.1 Example

``` dart
dynamic year = 10;
print(year.runtimeType); // int
year = 10.5;
print(year.runtimeType); // double
year = '10';
print(year.runtimeType); // String
```

#### 2.3 final & const

The **final** and **const** keyword are used to declare constants.

* You cannot change the **value** after it was declared.
* The **const** keyword is used to represent a compile-time constant.
* The **final** keyword is used to represent a run-time constant.

##### 2.3.1 Example

``` dart
const year = 10;
print(year.runtimeType); // int
print(year); // 10
year = 5; // Error: Setter not found: 'year'.
```

``` dart
final year = 10;
print(year.runtimeType); // int
print(year); // 10
year = 5; // Error: Setter not found: 'year'.
```

**final** vs. **const**

For example, functions are acquired dynamically at runtime.

``` dart
void main() {
  const name = getName(); // Error: Method invocation is not a constant expression.
}
String getSchoolName() {
  return 'Mizzou';
}
```

``` dart
void main() {
  final name = getSchoolName();
  print(name); // Mizzou
}
String getSchoolName() {
  return 'Mizzou';
}
```



