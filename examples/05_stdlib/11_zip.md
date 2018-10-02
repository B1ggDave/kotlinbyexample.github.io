# zip

Merge a collection with another collection to make a new collection. The returned collection contains either a `Pair` of elements from source collection with the same indexes or the result of a given transformation of elements with the same indexes. Let's take a look!

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val A = listOf("a", "b", "c")                  // 1
    val B = listOf(1, 2, 3, 4)                     // 1

    val resultPairs = A zip B                      // 2
    val resultReduce = A.zip(B) { a, b -> "$a$b" } // 3
//sampleEnd

    println("A to B: $resultPairs")
    println("\$A\$B: $resultReduce")
}
```

</div>

1. Define two collections.
2. Zip them into pairs using infix notation.
3. Zip them concatinating them together.
