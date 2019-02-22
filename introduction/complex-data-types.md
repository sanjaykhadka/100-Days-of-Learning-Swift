# Complex Data Types

## Tuples
Tuples can contain multiple different type of values in a single variable. We can use parenthesis ```()``` to define a tuple. 

**Example**
```swift
var person = ("Sanjay", 15)
print(person)
print(person.0)
print(person.1)
```

*Output:*
```
("Sanjay", 15)
Sanjay
15
```

Also, we can define tuple by associating name to each values ie by giving named index to the values.

**Example**
```swift
var person1 = (name: "Ramu", age: 10)
print(person1)
print(person1.0)
print(person1.name)
print(person1.age)
```

*Output:*
```
(name: "Ramu", age: 10)
Ramu
Ramu
10
```

We can decompose the tuple into separate constants or variables and access the values.

**Example**
```swift
let httpError = (404, "Page Not Found")
let (statusCode, statusMessage) = httpError
print(httpError.0)
print("The status code is \(statusCode)")
print("The status message is \(statusMessage)")
```

*Output:*
```
404
The status code is 404
The status message is Page Not Found
```

Also, we can partly decompose the value of tuples and ignore others. We can use underscore ```_``` for that.

**Example**
```swift
// to get only code
let(code, _) = httpError
print(code)
// or to get message only
let(_, message) = httpError
print(message)
```

*Output*
```
404
Page Not Found
```

Although tuple seems like an array, but it is different to an array in the following ways-
* Unlike an array, tuples are fixed in sized, ie once created, we can't add or remove items from the tuple.
* We can change the value of tuple but not the type of values ie the type-casting of tuple values are not allowed.

## Collection Types: Arrays, Sets, Dictionaries
### Arrays
Arrays are a collection of similar values. Lets say, while variable can only store a single value at a time, and there is no other way we can use a variable to store multiple values, we can use an array as a variable or a constant that can store multiple value at a time. 

**Example**
```swift
let p1 = "Ram"
let p2 = "Shyam"
let p3 = "Hari"
let p4 = "Sita"

// array of strings
let persons = [p1, p2, p3, p4]

// array of numbers
let numbers = [10, 20, 30, 40]

print(numbers)
print(numbers)
```

*Output:*
```
[10, 20, 30, 40]
[10, 20, 30, 40]
```

In the code above, ```persons``` is an array of strings while ```numbers``` is an array of integers. 

We can also define an array explicitly, by using type annotations.

**Example**
```swift
let colors:[String] = ["red", "green", "blue"]
let happiness:[Bool] = [true, false]
let digits:[Int] = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print(colors)
print(happiness)
print(digits)
```

*Output*
```
["red", "green", "blue"]
[true, false]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

We can access the values from an array by using the index of each values. For example, an array index always starts from 0. So to read the first value of our ```persons``` array, we can write ```persons[0]```

**Example**
```swift
print(persons[0]) 
print(persons[2])
```

*Output:*
```
red
blue
```

## Sets

## Arrays vs Sets vs Tuples

## Dictionaries

## Dictionary Default Values

## Creating Empty Collections

## Enumerations

## Enum associated values

## Enum raw values