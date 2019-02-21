# Getting Started
The secret to getting ahead is getting started. In this section we will get our hands dirty by learning about variables, constants and simple data types.

## Variables
Variables can be considered as the places where we can store program data. They are called variables because their values can vary. You are free to change their values.

Now lets launch XCode app, and it will ask you what you want to do. 
* Choose "Get started with a Playground" (This is a play area for your codes where you can play with your swift codes for testing purpose and here you can see immediate results unline in Xcode IDE where you need actual device or simulator to see your output.)
* Choose "blank" and click "next" and create to save it whereever you like. For example save it to your desktop. 

In your playground area, you will see a line of code

```swift
var str = "Hello, playground"
```

> Output: Hello, playground

This creates a new variable called ``str`` with the value ``Hello, playground``. You can see the output as ``Hello, playground`` in the right side. 

As the name suggests, we can change the value of ``str`` because it is a variable.

```swift
str = "Hello, world!"    
```

> Output: Hello, world!

Now this time we don't need the keyword ```var```, because the variable has already been created and we are just changing its value. 

Similarly if you want to create another variable, just follow the above code with the code below,

```swift
var name = "Sanjay Khadka"
print(name)
```

> Output: Sanjay Khadka

If you have set the playground to run automatically at the bottom side of the playground(also recommended), then you will see the output at the right side of the playground once the execution completes. 
![execute image](https://github.com/sanjaykhadka/learn-swift-coding/blob/master/images/execute.gif)

Here print is used to print the output to the bottom console of the playground.

![Playground Image](https://github.com/sanjaykhadka/learn-swift-coding/blob/master/images/playground.png)

