# External declarations

The *external* keyword allows us to declare existing JavaScript API in a type-safe way.

<div class="language-kotlin" theme="idea" data-min-compiler-version="1.3" data-target-platform="js">

```kotlin
external fun alert(msg: String)   // 1

fun main() {
  alert("Hi!")                    // 2
}
```

</div>

1. Declare an existing JavaScript function `alert` which takes a single `String` argument
2. Use it as if it were regular Kotlin.

Note that Kotlin checks during compilation that an exact single argument of type `String` is passed.
That prevents a number of bugs even when using a pure JavaScript API - same as with regular Kotlin.

Please [refer to the docs](https://kotlinlang.org/docs/reference/js-interop.html#external-modifier) in order 
to learn more about describing the existing JavaScript API.
