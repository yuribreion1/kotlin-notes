# Enum classes

Kotlin allows us to create enum classes like Java enum classes, with some improvements, let's check the example below: 

``` kotlin
enum class Priority(val value: Int) {
    MINOR(-1),
    NORMAL(0),
    MAJOR(1),
    CRITICAL(10)
}
```

Notice above, that you can set a value for each item. That can be called as well using the keyword `value`: `println(priority.value)`

Follow an example of the list of priorities: 

``` kotlin
for (priority in Priority.values()) { println(priority) }
```

It's possible as well to override the values of each element of enum, the example below applies this concept: 

``` kotlin
enum class Priority(val value: Int) {
    MINOR(-1){
        override fun text(): String {
            return "Minor priority"
        }
    },
    NORMAL(0) {
        override fun text(): String {
            return "Normal priority"
        }
    },
    MAJOR(1) {
        override fun text(): String {
            return "Major priority"
        }
    },
    CRITICAL(10) {
        override fun text(): String {
            return "Critical priority"
        }
    };
    
    abstract fun text(): String
}

fun main() {
	for (priority in Priority.values()) { println(priority.text()) }
}
```

Notice that all items should be formated in sense of return a `text()` function as well and the `abstract fun text(): String` is required.
