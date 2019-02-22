# Complex Data Types
## Arrays
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
