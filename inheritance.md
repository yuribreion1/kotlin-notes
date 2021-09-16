# Inheritance

Similar as other object-oriented languages, Kotlin supports inheritance: 

``` kotlin
open class Person 
  open fun validate() {
    
  } 
}

class Customer: Person() {
  override fun validate()
}
```

Is important to mention that `open` keyword is required to access the Person class or the class that is inherited. It is applicable for members as well. 

## Final keyword

The usage of final is a little different in Kotlin, if you have a class called `SpecialCustomer` and you do not want to access the function validate from `Person` class
you need to speficy the keyword `final` at the Customer override function:

``` kotlin
open class Person 
  open fun validate() {
   
  } 
}

class Customer: Person() {
  final override fun validate()
}

class SpecialCustomer: Customer() {

} 
```
