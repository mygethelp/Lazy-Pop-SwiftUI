# Lazy Pop SwiftUI

Swiping on any part of the screen starts an interruptible pop animation to the previous view.

<p align="center"><img src="https://github.com/joehinkle11/Lazy-Pop-SwiftUI/raw/master/demo.gif"/></p>

Forked from https://github.com/rishi420/SwipeRightToPopController and adapted for SwiftUI.

Also thanks to [lyinsteve on this Reddit comment](https://www.reddit.com/r/iOSProgramming/comments/e4zeoi/i_made_a_swiftui_component_so_you_can_drag/f9gkllt/) for suggesting I turn this into modifier.

# Use

To make your view lazily poppable, just add the `LazyPop()` modifer to it.

```swift
struct DetailsViewWithLazyPop: View {
    var body: some View {
        Text("Lazy pop enabled. Swipe anywhere to dismiss.")
        .lazyPop()
    }
}
```
If you would like to toggle when the lazy pop is enabled, just pass it a boolean state.

```swift
struct DetailsViewWithToggleableLazyPop: View {
    @State var isEnabled: Bool = true
    var body: some View {
        Toggle(isOn: $isEnabled) {
            Text("Toggle lazy pop")
        }
        .lazyPop(enabled: $isEnabled)
    }
}
```

# Install

Just inlude the three files under `LazyPop` in this repo. Here's a link to them https://github.com/joehinkle11/Lazy-Pop-SwiftUI/tree/master/Lazy%20Pop%20SwiftUI/Lazy%20Pop

If this gets enough use, I'll put this in a Swift Package or a Cocopod.
