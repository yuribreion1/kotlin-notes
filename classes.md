# Classes

``` kotlin
class Customer {
  var id = 0
  var name: String = 0
}
```

Similar as other languages, you can use classes in Kotlin, with some key differences as: 
- No need to use `new` keyword to instancialize an object of the class
- Instead of initianize a variable in the first moment, you can add as constructor

``` kotlin
class Customer(var id: Int, var name: String) {
  
}
```
