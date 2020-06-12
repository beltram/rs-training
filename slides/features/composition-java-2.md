## Composition over inheritance 

```kotlin
// 2050
abstract class Vehicle {
    abstract fun drive()
    abstract fun fly()
}
class Twingo : Vehicle() {
    override fun drive() = println("Vroom")
    override fun fly() = println("I'm screwed")
}
```
