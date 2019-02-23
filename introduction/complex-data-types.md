# Complex Data Types

## Tuples
Tuples can contain multiple different type of values in a single variable. We can use parenthesis ```()``` to define a tuple. 

Tuples aren't collections, but like collections, they also group multiple values. The values stored in a tuple don't need to be of the same type. In tuple we normally store values that form a sensible multipart.

**Example**
```swift
var currency = ("EUR", 0.81)
var time = (Date(), "This is my message.")
var email = ("Sanjay Khadka", "test@example.com")
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

Also, we can define tuple by associating name to each values i.e. by giving named index to the values.

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
Swift provides three primary collection types- arrays, sets and dictionaries for storing collection of values.
* Arrays are ordered collections of values. 
* Sets are unordered collections of unique values.
* Dictionaries are unordered collections of key-value associations.

### Arrays
Arrays are ordered collection of values. An array stores values of the same type in an ordered list with the index of the order always starting from 0.

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

In the code above, ```persons``` is an array of string type while ```numbers``` is an array of integers. 

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

Normally array stores the same type of data, but if we want to store different type of data in an array, we can use ```Any``` type while creating an array.

**Example**
```swift 
let arr:[Any] = ["Ram", 10, "Shyam"]
print(arr[0])
print(arr[1])
```

*Output*
```
Ram
10
```

#### Array Type Shorthand Syntax
In Swift, the syntax of array type can be written as
```Array<Element>```,
where ```Element``` is th. type of values
Also the shorthand form can be written as 
```[Element]```.
The shorthand form is preferred in swift while referring to the type of an array.

We can create an empty array like this:

```swift
var a = Array<String>() // creates an empty array a
var b = [Int]() // creates an empty array b
a.append("hello") // adds item hello to array a
b.append(10) // adds item 10 to array b
print(a, b)
```
*Output*
```
["hello"] 
[10]
```

#### Default value
```repeating``` and ```count``` can be used inside an Array initializer to form an array with default values.

```swift
var defaultDoubles = Array(repeating: 0.0, count: 3)
print(defaultDoubles)
```

*Output*
```
[0.0, 0.0, 0.0]
```

#### Adding two arrays
We can form a third array by adding two arrays, only if the type of those array are same. For example, we cannot add two arrays if one is String, and another is an integer. The resulting array will automatically be of the same type.

```swift
let firstArray: [Int] = [10, 20]
let secondArray: [Int] = [30, 40, 50]
let thirdArray = firstArray + secondArray
print(thirdArray)
```

```
Output
[10, 20, 30, 40, 50]
```

#### Modify an array
We can use some methods as shown in example below to play with an array.

**Example**
```swift
var cart = [String]() // creates an empty array
cart.append("apple") // adds first item as apple
cart.append("banana") // appends banana
cart.insert("orange", at: 1) // inserts orange at index 1
cart += ["grapes", "guava", "Eggs", "Tomato"] // appends these 4 items at the end
print(cart)
cart[2...5] = ["Mango", "Potato"] // removes index 2 to 5 items and replaces them with mango and potato
print(cart)
cart.remove(at: 0) // removes 0 index item
print(cart)
cart.removeLast()
print(cart)
print(cart.count)
```

*Output:*
```
["apple", "orange", "banana", "grapes", "guava", "Eggs", "Tomato"]
["apple", "orange", "Mango", "Potato", "Tomato"]
["orange", "Mango", "Potato", "Tomato"]
["orange", "Mango", "Potato"]
3
```

#### Iterate through an array
We can use loops to iterate through an entire array values. For further information regarding loop, go to [loops](https://github.com/sanjaykhadka/learn-swift-coding/blob/master).

Lets use ```for-in``` loop to play with our cart.

```swift
for item in cart {
  print(item)
}
```

```
**Output:**
*outout*
orange
Mango
Potato
```




## Sets

## Arrays vs Sets vs Tuples

## Dictionaries

## Dictionary Default Values

## Creating Empty Collections

## Enumerations

## Enum associated values

## Enum raw values