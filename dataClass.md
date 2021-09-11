# Kotlin Data Classes

We usually create access methods in Java such as getters and setters, hash codes or toStrings, and it creates many boilerplate codes. In Kotlin, there is a simple
option to work with data inside classes in a pretty way, which is the usage of data classes.

Let's set up a customer class like the example below:

``` kotlin
data class Customer(var id: Int, var name: String, var email: String)

fun main() {
	val customer = Customer(1, "Yuri", "yuribreion@mail.com")
    println(customer)
}
```

We've the following output:

`Customer(id=1, name=Yuri, email=yuribreion@mail.com)`

Is possible to copy initialized objects to new ones:

``` kotlin
// is possible to copy
val customer3 = customer1

// other option to copy, but you can change values of parameters
val customer4 = customer1.copy(email = "test@test.com")
```

If you want, you can override methods like `toString` using the keywork `override`, follow an example below that convert the output to JSON format:

``` kotlin
data class Customer(var id: Int, var name: String, var email: String) {
    override fun toString(): String {
        return "{\"id\": \"$id\", \"name\": \"$name\", \"email\": \"$email\" }"
    }
}
```
