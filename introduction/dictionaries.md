# Dictionaries
Dictionary is a collection of similar type of data just like an array, but unlike an array which uses index to store values, we can store values in dictionary using anything we want. Commonly we use string as a index name to store values.

```swift
let person = [
    "fname": "Sanjay",
    "lname": "Khadka"
]
```

We use colon ```:``` to separate the value and identifier. The identifiers are called ```keys```. So we use ```key:value``` pair to store information in a dictionary. And we can use ```key``` while accessing the value from the dictionary. ```Keys``` must be unique.

```swift
print(person["fname"]!)
```

Note ```!``` here, we are force unwrapping the value. By force unwrapping, we are guaranteeing that it does have a value. To read more, see [optional & unwrapping](https://github.com/sanjaykhadka/learn-swift-coding/blob/master/optionals-unwrapping-typecasting)

We can also use type annotation to indicate type for ```key``` and ```value``` of dictionary. Example: ```[String: String]``` or ```[String: Int]```

## Syntax:
Dictionary is similar to array, except that you need to specify the type for both keys and values. The following example shows the ways to declare a dictionary.

```swift
var dict1: Dictionary<String, Int>
var dict2: [String: Int]
var dict3 = [
    "one": 1, 
    "two": 2, 
    "three": 3
]
```

```swift
var animals = [String: String]() // creates an empty array
animals = [
    "cow": "farm animal",
    "sheep": "farm animal",
    "horse": "pet animal"
]
dump(animals) // dump is similar to print, except that it display in pretty format
animals["dog"] = "pet animal"
animals["zebra"] = "wild animal"
print(animals) // unreadable so we use dump
dump(animals)
```
```
▿ 3 key/value pairs
  ▿ (2 elements)
    - key: "sheep"
    - value: "farm animal"
  ▿ (2 elements)
    - key: "cow"
    - value: "farm animal"
  ▿ (2 elements)
    - key: "horse"
    - value: "pet animal"

["cow": "farm animal", "sheep": "farm animal", "horse": "pet animal", "zebra": "wild animal", "dog": "pet animal"]

▿ 5 key/value pairs
  ▿ (2 elements)
    - key: "horse"
    - value: "pet animal"
  ▿ (2 elements)
    - key: "cow"
    - value: "farm animal"
  ▿ (2 elements)
    - key: "sheep"
    - value: "farm animal"
  ▿ (2 elements)
    - key: "dog"
    - value: "pet animal"
  ▿ (2 elements)
    - key: "zebra"
    - value: "wild animal"
```

## Dictionary Default Values
We can access the value of dictionary using its ```key```. But if the key doesn't exists, Swift will send back ```nil```. While it is good to get nil, we can also provide a default value for the ```keys``` that is missing.

```swift
let addresses: [String: String] = [
    "Ramu": "Kathmandu",
    "Shyam": "Bhaktapur",
    "Sita": "Lalitpur"
]

// access Ramu's address
print(addresses["Ramu"])

// But if we try to access, address of a person that is not in our dictionary
print(addresses["Shiva"])

// In such cases, we can provide a default value
let na = addresses["Aaron", default: "Unknown"]
print("The address of Aaron is \(na)")
```

```
Optional("Kathmandu")
nil
The address of Aaron is Unknown
```
