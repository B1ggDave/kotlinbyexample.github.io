# any, all, none

These extension functions answer the questions about the existence element(s) in collection based on given predicate.

### Function `any`

Function `any` returns `true` if the collection contains at least one element matching the given predicate.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val numbers = listOf(1, -2, 3, -4, 5, -6)            // 1
    
    val anyNegative = numbers.any { it < 0 }             // 2
    
    val anyGT6 = numbers.any { it > 6 }                  // 3
//sampleEnd

    println("Numbers: $numbers")
    println("Is there any number less than 0: $anyNegative")
    println("Is there any number greater than 6: $anyGT6")
}
```

</div>

1. Define collection of numbers.
2. Whether there is an element less than `0`.
3. Whether there is an element greater than `6`. 


### Function `all`

Function `all` returns `true` if all the elements in the collection match the given predicate.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val numbers = listOf(1, -2, 3, -4, 5, -6)            // 1
    
    val allEven = numbers.all { it % 2 == 0 }            // 2
    
    val allLess6 = numbers.all { it < 6 }                // 3
//sampleEnd

    println("Numbers: $numbers")
    println("All numbers are even: $allEven")
    println("All numbers are less than 6: $allLess6")
}
```

</div>

1. Define collection of numbers.
2. Whether all elements are even.
3. Whether all elements less than `6`.


### Function `none`

Function `none` returns `true` if there are no elements in the collection matching the given predicate.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {

//sampleStart
    val numbers = listOf(1, -2, 3, -4, 5, -6)            // 1
    
    val allEven = numbers.none { it % 2 == 1 }           // 2
    
    val allLess6 = numbers.none { it > 6 }               // 3
//sampleEnd

    println("Numbers: numbers")
    println("All numbers are even: $allEven")
    println("No element greater than 6: $allLess6")
}
```

</div>

1. Define the collection of numbers.
2. Whether there an odd element which means all elements are even.
3. If there is no element greater than 6.
 
