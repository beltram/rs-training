## Composition over inheritance 

```kotlin
// 2020
abstract class Vehicle {
    abstract fun drive()
}
class Twingo : Vehicle() {
    override fun drive() = println("Vroom")
}
```
