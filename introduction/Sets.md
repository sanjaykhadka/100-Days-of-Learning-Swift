## Sets
A set is a collection of values similar to array except they have 2 differences,
* items are stored in random order, ie they don't have any fixed order.
* all items in a set must be unique. No item can appear more than once in a set.

The type of set is written as ```Set<Element>```, where ```Element``` is the type. And unline arrays, sets don't have equivalent shorthand form.

```swift
let colors = Set(arrayLiteral: "red", "green", "blue")
let names = Set(["Ram", "Shyam", "Hari"])

print(colors)
print(colors[0]) // will give an error
```

Because sets are unordered, they don't have indices bound for each items unlike array, and we cannot use numerical positions unlike array to access the value of set.

### Initializing an Empty Set and Set with an Array Literal

```swift
// Creating and Initializing an empty set
var genres = Set<String>()
genres.insert("Rock")
genres.insert("Classical")

// Set with an Array Literal
var favGenres: Set<String> = ["Metal", "Melody"]

print(genres)
print(favGenres)

// ["Classical", "Rock"]
// ["Melody", "Metal"]
```

### Reading and Modifying a Set
Sets have its methods to access and modify its values.

```swift
var numbers: Set<Int> = [10, 20]
numbers.insert(30) // inserts 30 at the end of set
print(numbers)
numbers.insert(10) // since set only can store unique number, this will be ignored
print(numbers)
numbers.remove(10)
numbers.insert(40)
print(numbers)

if let removed = numbers.remove(30) {
    print("Removed item is \(removed)")
} else {
    print("Item doesnot exists, cannot remove")
}

print(numbers)
print(numbers.count)

if numbers.contains(40) {
    print("The number exists on the set")
} else {
    print("The number doesnot exists")
}
```

```
[10, 30, 20]
[10, 30, 20]
[40, 30, 20]
Removed item is 30
[40, 20]
2
The number exists on the set
```

### Iterating through a set
We can use ```for-in``` to iterate over the values of a set.

```swift
// insert new genre metal
genres.insert("Metal")

print("Normal loop though set")
// access values in loop normally
for value in genres {
    print(value)
}

print("\nSorted genres loop")
// sorted genres
for value in genres.sorted() {
    print(value)
}

print("\nEnumerated genres loop")
// Set also supports enumerated like array
for (i, g) in genres.enumerated() {
    print("\(i + 1). \(g)")
}
```

```
Normal loop though set
Metal
Rock
Classical

Sorted Genres loop
Classical
Metal
Rock

Enumerated genre loop
1. Metal
2. Rock
3. Classical
```
### Choosing between Arrays, Sets and Tuples
Arrays, Sets and Tuples seem to be very similar, but they have distinct usage. To help you know which choose, here are some rules-
* If a fixed and specific collection of related value is needed, then use a tuple.

```swift
let address = (city: "Kathmandu", street: "Aloknagar, Binayak Samjhana Marg", house: 333)
```
* If a collection of values must be unique, then we should use a set.

```swift
let cities = Set(["Kathmandu", "Bhaktapur", "Lalitpur"])
```
* If a collection of values can contain duplicate values, and should be ordered, then an array should be used.

```swift
let persons = ["Ram", "Shyam", "Hari", "Shyam", "Ram", "Sita"]
```
