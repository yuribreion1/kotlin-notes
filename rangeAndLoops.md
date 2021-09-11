# Range and Loops

The examples below represent some applications of range and loops. 

``` kotlin
fun main() {
    
    // specify a range
	val number = 1 .. 100
	
    // desc loop
    for (a in 100 downTo 1) println(a)
    
    // desc loop 5 by 5
    for (b in 100 downTo 1 step 5) {
        println(b)
    }
    
    // iterating a loop
    val capitals = listOf("London","Paris","Roma","Madrid")
    for (capital in capitals) {
        println(capital)
    }
    
    // breaking loops
    loop@ for (i in 1..100) {
        for (j in 1..100) {
            break@loop
        }
    }
}
```
