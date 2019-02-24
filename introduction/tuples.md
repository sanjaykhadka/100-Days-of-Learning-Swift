# Tuples
Tuples can contain multiple different type of values in a single variable. We can use parenthesis ```()``` to define a tuple. 

Tuples aren't collections, but like collections, they also group multiple values. The values stored in a tuple don't need to be of the same type. In tuple we normally store values that form a sensible multipart.

```swift
var currency = ("EUR", 0.81)
var time = (Date(), "This is my message.")
var email = ("Sanjay Khadka", "test@example.com")
var person = ("Sanjay", 15)
print(person)
print(person.0)
print(person.1)
```

```
("Sanjay", 15)
Sanjay
15
```

Also, we can define tuple by associating name to each values i.e. by giving named index to the values.

```swift
var person1 = (name: "Ramu", age: 10)
print(person1)
print(person1.0)
print(person1.name)
print(person1.age)
```

```
(name: "Ramu", age: 10)
Ramu
Ramu
10
```

We can decompose the tuple into separate constants or variables and access the values.

```swift
let httpError = (404, "Page Not Found")
let (statusCode, statusMessage) = httpError
print(httpError.0)
print("The status code is \(statusCode)")
print("The status message is \(statusMessage)")
```

```
404
The status code is 404
The status message is Page Not Found
```

Also, we can partly decompose the value of tuples and ignore others. We can use underscore ```_``` for that.

```swift
// to get only code
let(code, _) = httpError
print(code)
// or to get message only
let(_, message) = httpError
print(message)
```

```
404
Page Not Found
```

Although tuple seems like an array, but it is different to an array in the following ways-
* Unlike an array, tuples are fixed in sized, ie once created, we can't add or remove items from the tuple.
* We can change the value of tuple but not the type of values ie the type-casting of tuple values are not allowed.