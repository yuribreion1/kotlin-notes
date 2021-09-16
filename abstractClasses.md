# Abstract class

The same way as Java, Kotlin supports abstract classes, follow an simple implementation:

``` kotlin
abstract class StoredEntity {
  val isActive = true
  abstract fun store() {
    return isActive.toString()
  }
}

class Employee: StoredEntity() {
  override fun store() {
    ?
  //something here
}

fun main(args: Array<String> {
  val se  = Employee()
  se.isActive
}
```

The example above allow to access members from extract classes and inherit abstract classes as well
