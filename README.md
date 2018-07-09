# Personal Swift Guide
Swift's personal study repository

![Swift](/images/swift.png "Swift")

# Index
- [x] [Intro](#Intro)
- [x] [Xcode](#Xcode)
- [x] [Interface](#Interface)
    - [x] [Toolbar](#Toolbar)
    - [x] [Navigator area](#Navigator-Area)
    - [x] [Editor area](#Editor-Area)
    - [x] [Utilities area](#Utilities-Area)
    - [x] [Debug area](#Debug-Area)
- [x] [Storyboard and Interface Builder](#Storyboard-and-Interface-Builder)
- [x] [Playground](#Playground)
- [x] [Swift](#Swift)
    - [ ] What's new in Swift 4.2
    - [x] [Variables Types](#Variables-Types)
    - [x] [Optionals](#Optionals)
        - [x] [Unwrap](#Unwrap)
    - [x] [Operators](#Operators)
        - [x] [Assignment Operators](#Assignment-Operators)
        - [x] [Arithmetic Operators](#Arithmetic-Operators)
        - [x] [Compound Operators](#Compound-Operators)
        - [x] [Comparison Operators](#Comparison-Operators)
        - [x] [Equality Operators](#Equality-Operators)
        - [x] [Inequality Operators](#Inequality-Operators)
        - [x] [Logical Operators](#Logical-Operators)
        - [x] [Ternary Operators](#Ternary-Operators)
    - [x] [Conditional Structures](#Conditional-Structures)
    - [x] [Collections Types](#Collections-Types)
        - [x] [Arrays](#Arrays)
            - [x] [Actions in arrays](#Actions-in-arrays)
        - [x] [Dictionaries](#Dictionaries)
        - [x] [Set](#Set)
        - [x] [Tuples](#Tuples)
    - [x] [Control Flow](#Control-Flow)
        - [x] [For Statement](#For-Statement)
        - [x] [While Statement](#While-Statement)
    - [x] [Enums](#Enums)
    - [x] [Structs](#Structs)
    - [x] [Functions](#Functions)
        - [x] [First Class Citizen](#First-Class-Citizen)
    - [x] [Closures](#Closures)
    - [x] [Error Handling](#Error-Handling)
- [x] [Tips](#Tips)
    - [x] [Border radius](#Border-radius)
    - [x] [Alignment centered on borders with Autolayout](#Alignment-centered-on-borders-with-Autolayout)
    - [x] [Leading and Trailing](#Leading-and-Trailing)
    - [x] [Hide keyboard](#Hide-keyboard)
    - [x] [Guard let](#guard-let)
    - [x] [Invoke IBAction without element](#Invoke-IBAction-without-element)
    - [x] [Declaration Info](#Declaration-Info)
    - [x] [Keyword Info](#Keyword-Info)

## Intro
To develop for iOS you need an Apple machine (Macbook, Mac Mini, iMac, etc). The Apple environment is not [multiplatform](https://en.wikipedia.org/wiki/Cross-platform), that means, the tools are not shared between the platforms. In addition, submitting the application to [store](https://www.apple.com/ios/app-store/) must be done through a macOS.

The main development language is ~~Objective-C~~ [Swift](https://www.apple.com/swift/).

## Xcode
![Welcome to Xcode](/images/welcome-to-xcode.png "Welcome to Xcode")

An [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) is the set of tools that helps the development. Unlike text editors such as [Visual Studio Code](https://code.visualstudio.com/), an IDE has a whole toolkit for application management, screen configuration (visual part), automation of debugging tasks, compilers that transforms the code into an IPA.

Xcode is the only IDE used for the development of all applications in the Apple ecosystem. That means, all applications are developed by Xcode, there is no other alternative.

In Xcode it is possible to create projects for iOS, watchOS, tvOS, macOS and Cross-Plataform (which works on all platforms). Among the development templates that each category offers there is no limitation between one and another. These templates are the first access to development. Regardless of which template you choose, you can change it normally. Your goal is just to start an application.

## Interface
Xcode is divided into several categories, among them:

### Toolbar
![Toolbar](/images/toolbar.png "Toolbar")

It has options to run and stop the application. Device or simulator where it will be executed. The simulators solve many problems and serve very well in development. Some operations such as [Push Notifications](https://en.wikipedia.org/wiki/Push_technology) and [Accelerometer](https://en.wikipedia.org/wiki/Accelerometer) can only be tested in a physical device.

In the center is the **View Activity** that displays current information about the application, if there is any error or warning and the current state of the application.

On the right is the Configuration Area that display the editor and sidebar.

### Navigator Area
![Navigator Area](/images/navigation.png "Navigator Area")

Structure area of the project files. It is a representation of the files that are saved in the directory in the operating system. It has several tabs that will be approached later.

### Editor Area
![Editor Area](/images/editor.png "Editor Area")

Code location. This is a Content Sensitive area, meaning your work is based on the developer's attitude.

### Utilities Area
![Utilities Area](/images/utilities.png "Utilities Area")

Area that displays options for the selected file. For visual files, options for changing layout, positioning, connections and various visual components are displayed.

### Debug Area

![Debug Area](/images/debug.png "Debug Area")

Displays all outputs in our code, both generated by the IDE itself and by us through the console.

## Storyboard and Interface Builder
![Storyboard](/images/storyboard.png "Storyboard")

Storyboards are used to create scenes from Views. Scene is the graphical representation of each screen, where all visual components are organized. When you select a `.storyboard` file in the Sidebar Utilities, all the native components of the operating system are available to use. Interface Builder is the individual representation of a scene. The Storyboard has all the IBs of the application working flow.

Storyboard has several advantages and drawbacks. The main advantage is the ease of identifying and visualizing both the graphic interface and the overall flow of the project. But when there are other developers involved in the project this process can get very stressful, especially when used with code versioning system.

Other alternatives are to create the visual representation through the code. Great post in portuguese exemplifying the differences and advantages of each alternative: https://www.concrete.com.br/2018/06/08/curso-ios-view-code/

## Playground
Ideal place to test code snippets so you do not need to create a new experiment project. Much more than simple code, in the Playground you can use all Apple APIs and other services. As an example, when creating a new Playground file it is possible to choose a Map model that when running the project the map is rendered emulating an iOS application. It is also a great source for study and programming knowledge for beginners in the language.

![Playground](/images/playground.png "Playground")

## Swift
**In Swift prioritize English in creating and declaring variables, functions, methods, classes.**

Launched in 2014, currently in version 4.2. It is a great language for beginners, especially for children. An example is due to the possibility of using emojis in declaration and code creation.

It is a [Case Sensitive](https://en.wikipedia.org/wiki/Case_sensitivity) language.

In Swift, `Variables` are called **mutable** information, that is, they have the value changed during execution.
`Constants` are the **immutable** ones that have the same value in their life cycle.

The Swift language makes the inference of the type, so it is not necessary to define its type during creation.

Declaration of variables with explicit type.
```swift
var swiftIsCool: Bool = true
```

Declaration of variables without explicit type.
```swift
var swiftIsCool = true
```
Since the variable is true, it will be `Bool`.

Swift is strongly typed. **Never, ever a variable will have its type changed after declaration or attributionKK)**.

### Variables Types
Always pay attention to the variable type before reserved a variable to preserve less memory, because on mobile devices memory is very precious.

Main types: `Int`,` Float`, `Double`,` Character`, `String` and` Bool`.

Another important type is `UInt`. This type only receives positive integers.

```swift
let firstName = "John"
let lastName = "Doe"
```

Give preference for variable **interpolation** instead of **concatenation**.

Concatenation.
```swift
let fullName = firstName + " " + lastName
```

Interpolation.
```swift
let fullName = "\(firstName) \(lastName)"
```

Another way to concatenate strings is to use the comma after a statement followed by the variable. A whitespace will be inserted automatically.
```swift
var name: String = "John"
print("My name is", name)
```

### Optionals
They serve to declare a variable without initializing it. Its value will be set to `nil` until it receives some assignment. The `interrogation (?)` signal is used to define an Optional.

Optional Statement.
```swift
var opt: Type?

var driverLicense: Int?
driverLicense = 12345678
```

When trying to access this variable `Optional` its value will be an `Optional of Int`. This is the safety way Swift found to access a variable that may be empty `nil`.
```swift
optional(12345678)
```

**A case where the return will always be Optional**: The conversion from one type into another always returns an `Optional`. In the example below the conversion from String "100" to Int will be an `Int Optional`, cause the conversion can get wrong if the String were "100-A" for example.
```swift
let addressNumber = Int("100")
```

#### Unwrap
To unwrap this variable can use the exclamation mark `!`.
```swift
driverLicense!
```

**However, this is the unsafe method and is not recommended for doing this unwrap, since the varivable may be empty and a fatal error will be throw and the app will close. It is an inadmissible mistake**.

**Optional binding** is the safe method for doing the unwrap of variables.
```swift
if let driverLicense = driverLicense {
    print("My driver's license is:", driverLicense)
} else {
    print("I do not have a driver's license")
}
```

You can use the same name of the constant in the verification, because within the validation block the constant that will be accessed will be the new one that was declared.

**Nil Coaliscing Operator**, is another way to do the unwrap. The function of this operator is to set a value if the variable is `nil`. In the example, if the conversion of text "123" is not possible its return will be 0, instead of fatal error.
```swift
// Returns 123
let addressNumber = Int("123") ?? 0

// Returns 0 because it is not possible to convert char A to Int
let addressNumber = Int("123-A") ?? 0
```

**Implicit Unwrapped Optinal** is another form of unwrap. Just use the exclamation mark `!` after the variable type. When you access the variable, even if it has no value assigned, the return will succeed. But **careful**, if we try to manipulate this variable by invoking some method, for example, the return will be **fatal error**.
```swift
// Using Implicit Unwrapped
var name: String!

// Accessing the return is Nil
print(name)

// FATAL ERROR. Does not allow manipulation since it has no value
print(name.count)
```

Way of doing the `unwrap` of this and the other types of `Optionals`.
```swift
if name != nil {
    print(name)
}
```

### Operators
#### Assignment Operators
It is represented by the `=`.

```swift
let pi = 3.14
var (name, age) = ("John", 22)
```

#### Arithmetic Operators
They are the mathematical operation: sum, subtraction, multiplication, division and Module (%).
**An arithmetic operator is only executed when conditions have the same type**. That means, it is only possible to operate `Int` with` Int`, `Double` with` Double`, `Float` with` Float`, among others. And consequently the return will be of the same type.

#### Compound Operators
Assigns and operates at the same time: `+=`, `-=`, `*=`, `/=`, `%=`.
The `++` and `--` signals were removed in version 3 of Swift.

```swift
let grade1 = 7.5
let grade2 = 9
grade1 += grade2
```

#### Comparison Operators
Comparison between two values and always returns a bool: `<`, `>`, `<=`, `>=`.

```swift
let grade1 = 7.5
let grade2 = 9
let compare = grade1 >= grade2
```

#### Equality Operators
The sign used is: `==`.

Remembering that Swift is case sensitive. This also applies to text values. To work around this type of comparison you can use the String methods: `.lowercased()` or `.uppercased()`.

```swift
let name1 = "John"
let name2 = "john"
let sameName = name1 == name2   // Returns false
```

#### Inequality Operators
```swift
let sameName = name1 != name2
```

#### Logical Operators
Operators `&&`, `||`, `!`.

#### Ternary Operators
Alternative to replace `if..else` in some situations using the `ternary (?)`.
```swift
var grade = 7.5
var result = (grade >= 7.0) ? "Approved" : "Disapproved"
```

```swift
var number = 11
var type = (number % 2 == 0) ? "Even" : "Odd"
```

### Conditional Structures
IF, Switch statements.

```swift
let number = 20
if number % 2 == 0 {
    print("Even")
} else {
    print("Odd")
}
```

**ClosedRange e Half-Closed Range**
ClosedRange defined by the `...` signal: Range of a lower bound to, and including, an upper bound.

```swift
let range0_10 = 0...10
```

Half-Closed Range defined by the `..<` signal: Interval between two boundaries.

```swift
let range0_9 = 0..<10
```

### Collections Types

### Arrays
**ORDERED** collection of objects of the same type. Ways to create arrays.

```swift
var names = ["Name 1", "Name 2", "Name 3", "Name 4"]
var ages: [UInt8] = [28, 19, 35, 33]    // Int bits up to 8 bits (255)
var numbers = [Int] = []
var phoneNumbers = [String]?
```

#### Actions in arrays

```swift
// Gets the total
names.count

// Valid if empty
names.isEmpty

// Retrieve by index
let secondeName = names[1]

// Handle by index
names[1] = "Name 5"

// Handle by scope
names[0...1] = ["Name 6", "Name 7", "Name 8"]

// Common array methods
names.first
names.last
names.append("Name 9")
names.insert("Name 10", at: 2)
names.removeFirst()
names.removeLast()
names.remote(at: 3)
names.removeAll()
names.contains("Name 3")
```

### Dictionaries
Similar to a real-world dictionary, Swift Dictionaries are collections of definitions associated with values. Unlike Arrays, Dictionaries are collections of unmatched objects of the same type that are accessed through braces.

```swift
var names = ["N1": "Name 1", "N2": "Name 2", "N3": "Name 3"]

// Type explicit. First Key after Value and empty value
var phoneNumbers = [String: Int] = [:]

// Including values
phoneNumbers["Phone 1"] = 2222-3333

// Replace a value and save the old one
let oldPhone = phoneNumbers.updateValue(4444-5555, forKey: "Phone 1")
print(oldPhone)     // Returns 4444-5555 in the Keys "Phone 1"

// Recover by key
let myPhone = phoneNumbers["Phone 1"]   // Return will be an optional()

// Optional unwrap
if let myPhone = myPhone {
    print(myPhone)
}

// Create Key Arrays or Dictionary Values
let keys = Array(phoneNumbers.keys)
let values = Array(phoneNumbers.values)
```

### Set
Set is in a way a mix of Array and Dictionary because it is composed by characteristics of both collections and has its particularity. It is a **NOT ORDERED** collection of objects of the same type, which can not be repeated. Therefore, it is not possible to enter an already existing value within in the Set. All its elements must be unique, have no key or index. Its declaration is similar to the Array, however it is mandatory to define the **Set** type.

```swift
var names: Set<String> = ["Name 1", "Name 2", "Name 3", "Name 4"]

var ages: Set<UInt> = [28, 19, 35, 33]
```

The insert method of the Set returns a `Tuple` with two properties. Therefore, the return constant will be a `Tuple` that indicates whether the value was entered and displays the value itself.

```swift
let result = names.Insert("Name 1")
print(result.Inserted)      // Bool has been inserted or not
print(result.MemberAfterInsert)     // The value itself
```

The methods used in Arrays and Dictionaries, which are not oriented by index or keys, are shared in Set.

```swift
names.remove("Name 2")
names.removeAll()

if names.contains("Name 3") {
    print("This name exists on the Set")
}
```

Since there is no index, to use a set you use repetition structures.
```swift
for name in names {
    print(name)
}
```

Other Set methods.
```swift
var school1Ages: Set<UInt> = [10, 9, 12, 11]
var school2Ages: Set<UInt> = [11, 13, 12, 14]

// To compare values between Sets
let sameAges = school1Ages.intersection(school2Ages)
print(sameAges)     // Return will be 11 and 12

// To join the values of the Sets
let allAges = school1Ages.union(school2Ages)
print(sameAges)     // Returns all ages without repeating

// Remove values between Sets
let allAges = school1Ages.subtracting(school2Ages)
print(sameAges)     // Returns values that do not repeat
```

### Tuples
With tuples you can combine values of different types.

Ways to declare tuples.
```swift
let firstPerson = ("Felipe", "Mendes", 26, "111.222.333-44", "Brazil")

let secondPerson: (String, String, UInt, String, String) = ("John", "Doe", 30, "555.666.777-88", "Brazil")

let thirdPerson: (firstName: String, lastName: String, age: UInt, cpf: String, country: String) = ("Joe", "Tarantino", 33, "888-999-111-22", "Brazil")
```

To access the values.
```swift
print(firstPerson.3)

print(secondPerson.0, secondPerson.2)

print(thirdPerson.firstName, thirdPerson.lastName)
```

Transform the values of a Tuple into variables.
```swift
let (firstName, lastName, age, cpf, country) = thirdPerson
print(firstName)
print(age)

// If no value is needed, use the _
let (firstName, lastName, age, _, _) = thirdPerson
```

### Control Flow
Flow Control is for executing instructions in order.

For all types of loops you can use the `break` to stop the repet.

### For Statement
Ways to declare and use the For statement.
```swift
for number in 1...10 {
    print("Printing the number \(number)")
}

// If the signature constant is not used, you can omit
for _ in 1...20 {
    print("Printing 20 times")
}

// Scrolling through a collection
var names = ["Name 1", "Name 2", "Name 3", "Name 4"]
for name in names {
    print("Print the name", \(name))
}

// Returning the characters of a String
// In version 4 the characteres method is not necessary
let language = "Swift"
for letter in language.characteres {
    print(letter)
}

// Returning a Tuple
// The return will be the index and the element
for letter in name.enumerated() {
    print(letter)
}

// Ways to separate values
for (index, letter) in name.enumerated() {
    print(index, letter)
}
```

### While Statement
While declaring ways.
```swift
var value = 0
while value <= 5 {
    print(value)
    value += 1
}
```

There is also variation with Repeat While.
```swift
var value = 0
repeat {
    print("Repeat:", value)
    value += 1
} while value <= 5
```

### Enums
Enums allows the representation of a set or a named group of options that can have associated values. Swift recommends to make the statements using [CamelCase](https://en.wikipedia.org/wiki/Camel_case). For the Enum name use **UpperCamelCase** and for its values **lowerCamelCase** (when name is compounded). And for the values use the name in the singular for easy reading.

Ways to declare Enum.
```swift
enum CompassPoint {
    case north
    case east
    case west
    case south
}

enum Planet {
    case mercury, venus, earth, mars, jupiter, saturn, uranus, neptune
}
```

Accessing the Enum values.
```swift
var directionToHead: CompassPoint = CompassPoint.north
var directionToHead2: CompassPoint = .north
var directionToHead3 = CompassPoint.north
```

Once the enum is accessed you can use the shorter syntax to change the value.
```swift
directionToHead1 = .east
```

Using enum with `switch` to define values.
```swift
directionToHead = .south
switch directionToHead {
case .north:
    print("Lots of planets have a north")
case .south:
    print("Watch out for penguins")
case .east:
    print("Where the sun rises")
case .west:
    print("Where the skies are blue")
}
// Prints "Watch out for penguins"
```

To define a type to the enum we use **Raw Values**. It can be any existing type.

In this example the type **Raw Value** is `Character` and represents [ASCII](https://en.wikipedia.org/wiki/ASCII) codes as enum values.
```swift
enum ASCIIControlCharacter: Character {
    case tab = "\t"
    case lineFeed = "\n"
    case carriageReturn = "\r"
}
```

Using **Raw Values** to change the enum index.

By default, the enum index starts with `0`. But since January is the month `1` we can change only its default value that the other months follow the order.
```swift
enum Months: Int {
    case january = 1
    case february   // It will be 2
    case march      // It will be 3
    case april      // It will be 4
    ...
}
```

To view the associated **Raw Value**.
```swift
Month.march.rawValue
```

**Associated Values** are used to store the type of enum values. Each value can have distinct types within the same enum and its access is done separately.

The **Associated Values** type declaration is made after the value name. In this case `Double`, `Int` and a `Tuple` are used.
```swift
enum Measure {
    case weight(Double)
    case age(Int)
    case size(width: Double, height: Double)
}
```

Assigning value to enum.
```swift
let measure: Measure = .weigth(0.70)
measure = .age(22)
measure = .size(width: 0.5, heigth: 1.60)
```

### Structs
Structs are used to create custom types. Structs are very similar to OOP classes. In Swift you can use definitions.

Structs have code blocks, properties, initializations, methods that add functionality to the structure.

Statement of **structs**.
```swift
struct SomeStructure {
    // structure definition goes here
}

struct Resolution {
    var width: Int
    var height: Int
}
```

Defining values to a struct.
```swift
var resolution = Resolution(width: 30, height: 15)
resolution.height = 20
```

To remove the mandatory property we can use `optionals` in the declaration and set the value to `nil` in instantiation. You can also set a default value for a property.
```swift
struct Person {
    var name: String
    var age: UInt?
    var phone: String = "(11) 1111-1111"
}
var person = Person(name: "John", age: nil, phone: nil)
```

If not defined the `init` method is implicitly created with all the properties as parameters forcing to define all the properties when instantiating.

If we create the `init` method only this will exist. To assign the value of a parameter to a property we use the `self` keyword before the property name.
```swift
struct Person {
    var name: String
    var age: UInt?

    init(name: String) {
        self.name = name
    }
}
```

To remove the mandatory property we can use `optionals` in the declaration and set the value to `nil` in instantiation. You can also set a default value for a property.
```swift
struct Person {
    var name: String
    var age: UInt?

    func seyHello() {
        print("Hello")
    }

    mutating func incrementAge() {
        age += 1
    }
}
```

**Computed Properties** are properties that return some embedded logic. In the example the `fahrenheit` property is calculated from the `celsius` property, which makes it a Computed Properties.
```swift
struct Temperature {
    var celsius: Double
    var fahrenheit: Double {
        return celsius * 1.8 + 32
    }
}

var temperature = Temperature(celsius: 25)
print(temperature.celsius)      // Returns 25.0
print(temperature.fahrenheit)   // Returns 77.00
```

### Functions
Functions are blocks of code that perform a certain task. Structure of a function.
```swift
func name(argumentLabel parameterName: Type) -> ReturnType {
    // Code
    return ReturnType
}
```

Function examples.
```swift
func greet(person: String) -> String {
    let greeting = "Hello, " + person + "!"
    return greeting
}
print(greet(person: "Anna"))
```

When executing a function, it is necessary to enter the name of the argument. In the function signature you can create the different **argument name** and **parameter name**. To remove the requirement to enter the argument name in the call, use the `_` sign as the external name.
```swift
func multiply(_ number1: Int, by number2: Int) -> Int {
    return number1 * number2
}
multiply(10, by 5)  // 50
```

Receiving more than one value in a single parameter. Use the `...` sign after the name.
```swift
func sum(_ initialValue: Int, withValues values:Int...) -> Int {
    var result = initialValue
    for value in values {
        result += value
    }
    return result
}
sum(5, withValues: 3, 6, 10, 8, 15)     // 47
```

Using `tuple` as a function return. Just enter the return types and use **dot syntax** to access the values separately.
```swift
func fullName(_ first: String, _ last: String) -> (firstName: String, lastName: String) {
    return (firstName, lastName)
}
let person("John", "Doe")
person.firstName
person.lastName
```

`In-Out` parameter types are used to change the value of a parameter during the execution of a function. Without the use of `In-Out` Swift returns an error if the value sent as argument is changed in the body of the method. To work around this need include the `inout` keyword before the parameter type.

The function below changes the values between the parameters. `A` will be worth` B` and vice versa.
```swift
func swapTwoInts(_ a: inout Int, _ b: inout Int) {
    let temporaryA = a
    a = b
    b = temporaryA
}
```

#### First Class Citizen
A **First Class Citizen** object supports all basic types of operations. This means that the object can be a function argument, function return, executed during a function, assigned to a variable.

To pass a **function as a parameter** to another function, simply type the function of the source function. Function type is defined by the parameter types plus the return type of your signature.
```swift
func sum(_ a: Int, _ b: Int) -> Int {   // The type is `(Int, Int) -> Int`
    return a + b
}
```

With the type of the function in hand it suffices to inform in the type of the parameter.
```swift
func applyOperation(_ a: Int, _ b: Int, operation: (Int, Int) -> Int) -> Int {
    return operation(a, b)
}
```

For ease reading, we can use the `typealias` keyword to create a alias for a value.
```swift
typealias Op = (Int, Int) -> Int
```

Whenever it is necessary to use type `(Int, Int) -> Int` you can use the alias `Op`. So the same function would look this way.
```swift
func applyOperation(_ a: Int, _ b: Int, operation: Op) -> Int {
    return operation(a, b)
}
```

Performing this function.
```swift
let result = applyOperation(10, 20, operation: sum)
```

Defining a **function as a return** in another function.
```swift
func getOperation(_ operation: String) -> Op {      // Using typealias for (Int, Int) -> Int
    switch {
        case "sum"
            return sum
        default
            return nil
    }
}
```

Assigning a variable to a function using the concept of **First Class Citizen**. Therefore the `operation` variable receives the `sum` function.
```swift
var operation = getOperation("sum")
```

Now the `operation` variable has the behavior of a function. With this, it is enough to inform the necessary arguments for its execution.
```swift
opertion(30, 20)    // Returns 50
```

### Closures
They are the **anonymous** functions of the language. That is, functions that have no name and are executed directly in the code without the invocation. It is the same behavior of **lambda** that exists in other programming languages.

Closure expression syntax.
```swift
{ (parameters) -> return type in
    statements
}
```

`Closure` declaration.
```swift
func calculate(_ a: Int, _ b: Int, operation: (Int, Int) -> Int) -> Int {
    return operation(a, b)
}

// Using closure in argument passing
calculate(10, 20, operation: {(a: Int, b: Int) -> Int in
    return a + b
})
```

Simplifying the `closure` usage.
```swift
// Since in Swift there is type inference we can omit the types
calculate(10, 20, operation: {(a, b) -> Int in
    return a + b
})

// The return is also implicit, so it can remove the return type
calculate(10, 20, operation: {a, b in
    return a + b
})

// Since the argument expects two `Int` we can replace them with the constant created by the language:`$ + index`
calculate(10, 20, operation: {
    return $0 + $1
})

// If the body has only one line it can remove the keyword `return`
calculate(10, 20, operation: {$0 + $1})
// or
calculate(10, 20) {$0 + $1}

// If the operation is binary and `closure` is the last parameter you can remove the constants
calculate(10, 20, operation: +)
```

**Methods that uses closures**. Arrays in Swift have useful methods that use the concept of closures. Some are: `map`, `filter`, `reduce`.

**Map**
```swift
var names = ["John", "Joe"]
let uppercasedNames = names.map({$0.uppercased()})
print(uppercasedNames)
```

**Filter**
```swift
let newNames = names.filter({$0.count <= 3})
print(newNames)
```

**Reduce**
```swift
let sumLetters = names.reduce(0, {$0 + $1.count})
print(sumLetters)
```

## Error Handling
Error handling helps to inform the developer or user what problem was reported during the execution of a statement. Without due treatment the user only receives a generic message like `true` or `false`.

The possible errors that a code can trigger can be stored in an `enum`. Example of a login treatment. The `enum` type must be `Error`.
```swift
enum LoginError: Error {
    case wrongUsername
    case wrongPassword
}
```

At the signature of the validation method you must enter the keyword `throws` before the return type where it indicates that the error handling will be used. At each error trigger use the `throw` keyword and the` enum` error type.
```swift
func login(username: String, password: String) throws -> Bool {
    if username != "Test" {
        throw LoginError.wrongUsername
    }
    if password != "123" {
        throw LoginError.wrongPassword
    }
    return true
}
```

To safely execute a method that has `throws` error handling, use the `do`, `catch` blocks and `try` keyword before the method name.
```swift
do {
    let loginResult = try login(username: "Test", password: "987")
} catch {
    print(error)
}
```

Improving the return of the error using the `enum` of errors. Create a catch block for each case in the collection.
```swift
do {
    let loginResult = try login(username: "Test", password: "987")
} catch LoginError.wrongUsername {
    print("Wrong username. Please, try again.")
} catch LoginError.wrongPassword {
    print("Wrong password. Please, try again.")
}
```

Unsecured forms to execute a method that has `throws` error handling. Useful for testing because it has no validations.

Using the `?` signal after `try` to unwrap optional safely. If there are any errors the return will be `nil` otherwise the method runs normally.
```swift
let loginResult = try? login(username: "Test", password: "987")
```

Using the `!` signal will force optional wrapping without security. In case of error the return will be `Fatal Error`.
```swift
let loginResult = try! login(username: "Test", password: "987")
```

## Tips
Session with general code tips, layout, tools and other useful information.

### Border radius
In User Defined **Runtime Attributes** at sidebar **Identity Inspector** set the values to:

| Key path           | Type          | Value  |
| ------------------ |:-------------:| ------:|
| layer.cornerRadius | Number        | 10     |

### Alignment centered on borders with Autolayout
To center a component out of the `0` value of the X axis, apply the Autolayout **Horizontally in Container** on the component, select the x-axis line of the component in the scene. In **Attributes Inspector** set the value **Constant** to the desired:

![Align](/images/align.png "Align")

### Leading and Trailing
Apple could not simply name these values for Left and Right because it has to make sense for layout orientation. But **Leading and Trailing** are the same as **left-to-right** and **right-to-left**.
These are the Autolayout settings for one component to follow the orientation of another element based on one or both sides. Thus, for different screen sizes, an element will always have its behavior changed according to the position of a reference component.
To set a Leading or Trailing, simply press the Control key on the element and drag it to the reference component.

### Hide keyboard
To hide the keyboard after entering value in a TextField you can use the following methods.
```swift
// Applies directly to TextField
[someTextField].resignFirstResponder()

// Applies to View
self.view.endEditing(true)
```

Stackoverflow answer that explains the difference of both: https://stackoverflow.com/a/29882902/6736283

### Guard let
The **guard let {expression}** retains its value after the check block. Other than the **if let** value only exists inside the block.
```swift
guard let temperature = Double(tbValue!) else { return }
print(temperature)
```

### Invoke IBAction without element
Every IBAction receives as a parameter the type of the element from which it was created. However, it is possible to invoke this action without element, just use the **Optional** in the parameter and send **nil**.
```swift
myAction(nil)
@IBAction func myAction(_ sender: UIButton?) {
    print("Test")
}
```

### Declaration Info
To view type, return and method data and declarations use the `Option` key on the name that will display a box with all the useful information.

### Keyword Info
Clicking on reserved words with the `Command` key pressed Xcode displays actions with useful information such as navigating to the word definition.

![Command Action](/images/command-action.png "Command Action")