## Data Types

A data type is an attribute of data which tells the compiler or interpreter how the programmer intends to use the data.



#### 1 Numbers

##### 1.1 int

An integer number.

```dart
int age = 18;
int ageInHex = 0x12;
print(age); // 18
print(ageInHex); // 18
```

##### 1.2 double

A double-precision floating point number.

```dart
double pi = 3.14;
double piMorePrecise = 3.1415926;
print(pi); // 3.14
print(piMorePrecise); // 3.1415926
print(double.parse(piMorePrecise.toStringAsFixed(2))); // 3.14, round it to 2 decimal places
```



#### 2 Booleans

To represent boolean values.

``` dart
bool skyIsBlue = true;
bool earthIsACube = false;
print(skyIsBlue); // true
print(earthIsACube); // false
print(!earthIsACube); // true
```



#### 3 Strings

A sequence of UTF-16 code units. You can use either single or double quotes to create a string.

``` dart
String dartOne = 'dart';
String dartTwo = "dart";
String dartThree = "dart 3";
print(dartOne == dartTwo); // true
print(dartOne == dartThree); // false
```



#### 4 Collections

A **collection** (**container**) is a grouping of some variable number of data items.

##### 4.1 Lists

An **indexable** collection of objects with a length.

``` dart
List<int> numbers = [1, 2, 3, 4, 5];
print(numbers.length); // 5, list length
print(numbers[0]); // 1, first element 
print(numbers[numbers.length - 1]); // 5, last element
numbers.add(3); // add a new element
print(numbers); // [1, 2, 3, 4, 5, 3]
numbers.sort(); // sort the list 
print(numbers); // [1, 2, 3, 3, 4, 5]
```

##### 4.2 Sets

A **unordered** collection of objects in which each object can occur only once.

``` dart
Set<int> numbers = {1, 2, 3, 4, 5, 5, 5};
print(numbers); // {1, 2, 3, 4, 5}
print(numbers.length); // 5, set length
print(numbers[0]); // error!
```

##### 4.3 Maps

A collection of **key/value** pairs, from which you retrieve a value using its associated key.

``` dart
Map<String, Object> myPersonalInfo = {
    'first name': 'Boom', 
    'last name': 'Tiramisu',
    'age' : 18,
    'email' : "hello@missouri.edu"
  };
print(myPersonalInfo.length); // 4
myPersonalInfo['gender'] = 'female';
print(myPersonalInfo['gender']); // female
print(myPersonalInfo.length); // 5
myPersonalInfo.clear();
print(myPersonalInfo.length); // 0
```

