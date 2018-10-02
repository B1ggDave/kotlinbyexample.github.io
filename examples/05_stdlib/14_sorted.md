# sorted

`sorted` returns a list of all the elements sorted according to their natural ascending sort order.

`sortedBy` returns a list of all the elements sorted according to the natural sort order of the value returned by specified selector function.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val shuffled = listOf(5, 4, 2, 1, 3)     // 1
    val natural = shuffled.sorted()          // 2
    val inverted = shuffled.sortedBy { -it } // 3
//sampleEnd

    println("Shuffled: $shuffled")
    println("Natural order: $natural")
    println("Inverted natural order: $inverted")
}
```

</div>

1. Define a collection of shuffled numbers.
2. Sort it in their natural ascending order.
2. Sort it in their natural descending order.
