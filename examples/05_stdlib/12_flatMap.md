# flatMap

Returns a single list of all the elements yielded from the results of a transform function being invoked on each element of the original collection.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val numbers = listOf(1, 2, 3)                        // 1

    val tripled = numbers.flatMap { listOf(it, it, it) } // 2
//sampleEnd

    println("Numbers: $numbers")
    println("Transformed: $tripled")
}
```

</div>

1. Define a collection of numbers.
2. Transform the collection repeating each element three times.
