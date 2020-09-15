[![Release](https://jitpack.io/v/badoualy/animatedsvg-composable.svg)](https://jitpack.io/#badoualy/animatedsvg-composable)

# <img src="https://github.com/badoualy/animatedsvg-composable/blob/master/ART/web_hi_res_512.png" width="32"> AnimatedSVG Composable
<img src="https://github.com/badoualy/animatedsvg-composable/blob/master/ART/preview.gif" width="300">

Setup
----------------

First, add jitpack in your build.gradle at the end of repositories:
 ```gradle
repositories {
    // ...
    maven { url "https://jitpack.io" }
}
```

Then, add the library dependency:
```gradle
compile 'com.github.badoualy:animatedsvg-composable:1.0.0'
```


Now go do some awesome stuff!

Usage
----------------

(See MainActivity sample)
```kotlin
val state = remember { AnimationState(isRunningInitially = true) }
AnimatedSvg(
    strokes = strokes,
    box = RectF(0f, 0f, 109f, 109f),
    modifier = Modifier
        .fillMaxSize()
        .clickable(onClick = { state.restart() }),
    animationState = state
)
```