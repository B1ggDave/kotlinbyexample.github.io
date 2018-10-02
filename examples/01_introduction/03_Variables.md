# Variables

Kotlin has powerful type inference. While you can explicitly declare the type of a variable, you'll usually let the
compiler do the work by inferring it. Kotlin does not enforce immutability, though it is recommended.
In essence use *val* over *var*.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {
//sampleStart
    var a: String = "initial"  // 1
    println(a)
    val b: Int = 1             // 2
    val c = 3                  // 3
//sampleEnd
}
```

</div>

1. Declare a mutable variable and initialize it
2. Declare an immutable variable and initialize it
3. Declare an immutable variable and initialize it. The compiler infers the type.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun main() {
//sampleStart
    var e: Int  // 1
    println(e)  // 2
//sampleEnd
}
```

</div>

1. Declare a variable, but don't initialize it.
2. Produces compiler error: Variable 'e' must be initialized

Variable initialization can be postponed, but it must be initialized before the first read.
 
<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3">

```kotlin
fun someCondition() = true 

fun main() {
//sampleStart
    val d: Int  // 1
    
    if (someCondition()) {
        d = 1   // 2
    } else {
        d = 2   // 2
    }
    
    println(d) // 3
//sampleEnd
}
```

</div>

1. Declare a variable, but don't initialize it.
2. Initialize the variable with different values depending on some condition.
3. The first use of the variable.
