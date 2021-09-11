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
class Customer(var id: Int, var name: String)
```

- Is possible to create initialization block, allowing you to give special instructions for the variables

``` kotlin
class Customer(val id: Int, var name: String) {
    init {
        name = name.uppercase()
    }
}
```

- Ability to create special parameters as the example below of social security number:

``` kotlin
class Customer(val id: Int, var name: String) {
    init {
        name = name.uppercase()
    }
    
    var socialSecurityNumber: String = ""
    	 set(value) {
             if (!value.startsWith("SN")) {
                 throw IllegalArgumentException("Social security number should start with SN")
             }
             field = value
         }
}
```
Is important to consider the line with `field` keyword which is used to pass forward the information
