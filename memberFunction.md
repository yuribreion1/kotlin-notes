# Member functions in Kotlin

Function is the first level citizen in Kotlin as we know, but can be used as well to create functions as part of classes to execute specific activities.

The example below displays a simple function inside the class to print out data:

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
         
         fun customerAsString(): String {
             return("Id: $id - Name: $name")
         }
}
```
