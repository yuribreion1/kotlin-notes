# Conditional execution with if and when in Kotlin

## Unit

The application of `if` statement is pretty much the same as other languages. But there is a concept of Unit, which is like a void method in Java or C#. 

``` kotlin
val result = if (myString != "") {
        "Not empty"
    } else {
        "Empty"
    }
```
On the example above, `result` receives the result of the variable, which is a unit. It's just important to provide an `else` ever, because in this case, is mandatory to have an exit.

## When

Is the `case` equivalent in Kotlin, which can be used for multiple applications. Follow an example:

``` kotlin
var myString = "Start value"
    val result = if (myString != "") {
        "Not empty"
    } else {
        "Empty"
    }
    
    when (result) {
        is String -> println("Excelent")
        "Value" -> "This line wont be executed"
    }
```

The code above present a scenario that compare the unit, when the value is a String. Print the work `Excelent`. **Is important to consider that, each when condition executes just one statement and break, it not allow multiple lines per condition.**

You can assign the `when` condition to an expression, keep in mind to give an exit to your code. Follow an example: 

``` kotlin
val result = "Value"
    val whenValue = when (result) {
        "Value" -> {
            println("It's a value")
            println("Second statement")
        }
        is String -> println("Excelent")
        else -> println("It came to this?")
    }
    println(whenValue)
```
In other words, is necessary to use the `else` to give an exit if the condition is not true. 

If I change the value of `"Value"` to anything different, the clause inside the `when` is not considered.
