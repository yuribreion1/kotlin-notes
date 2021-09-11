# Functions

Kotlin in a functional language which able you to work just with this kind of nomenclature, different from Java, you can programming in Kotlin just declaring functions. 

The example below is a function without parameters(void in Java), which is known as Unit: 

``` kotlin
fun hello() {
    println("Hello")
}

or 

fun hello(): Unit {
    println("Hello")
}
```

If you want a function that returns a specific type, you need to declate it: 

``` kotlin
fun returnAnFour(): Int {
    return 4
}
```

Is possible as well to create a function with multiple parameters: 

``` kotlin
fun sum(x: Int, y: Int): Int {
    return x + y
}
```
Kotlin compiler works with type inference, then, is no necessary to specify `Int` as the return of the fuction, follow a simplified version of the function above:

``` kotlin
fun sum(x: Int, y: Int) = x + y
```

Is possible to have functions with initialized parameters that you could not specify during the execution: 

``` kotlin
fun printDetails(name: String, email: String, phone: String = "") {
    println("name: $name - email: $email - phone $phone")
}
```

The example above, notice that `phone` is initialized as blank, if we execute the function, we can use in this way:

``` kotlin
fun main() {
    printDetails("Yuri", email = "yuribreion@mail.com")
}
```
In the nutshell, named parameters able us to change the order of values.
