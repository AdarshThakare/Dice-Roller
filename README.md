# Dice-Roller App
#### Hii ! This is my first basic functional Android App that I built using Kotlin Programing Language and Jetpack Compose.

---

## Logic
```kotlin
 var result by remember { mutableStateOf(1) }
    val imageResource = when (result) {
        1 -> R.drawable.dice_1
        2 -> R.drawable.dice_2
        3 -> R.drawable.dice_3
        4 -> R.drawable.dice_4
        5 -> R.drawable.dice_5
        else -> R.drawable.dice_6
    }
```
- This piece of code initially preserves the state of result even after recomposition using `remember function` and sets it to 1.
---
```kotlin
Image(
        painter = painterResource(imageResource) ,
        contentDescription = result.toString())
        Spacer(modifier = Modifier.height(16.dp) )
        Button(onClick = {result = (1..6).random()}) {
            Text(text = stringResource(id = R.string.die_roll))
        }
```
___

- After the `ROLL` button in clicked , the onclick lambda is executed and sets the result value randomly from 1 to 6.
- Depending on the result value,`imageResource` variable fetches the respective dice image

___
## Demo

https://github.com/AdarshThakare/Dice-Roller/assets/112002059/f0744916-06f2-429b-9ebe-9feda348c6ce

