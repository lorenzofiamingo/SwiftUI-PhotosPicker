# SwiftUI PhotosPicker 🌇

`PhotosPicker` is a photos picker sheet, based on `PHPickerViewController`. Currently supports only iOS and Mac Catalyst.

## Usage

`PhotosPicker` has similar API and behavior as other [Presentation Modifiers](https://developer.apple.com/documentation/swiftui/view-presentation).
```swift
import SwiftUI
import PhotosPicker

struct ContentView: View {
    
    @State private var showingPicker = false
    
    var body: some View {
        Button("Choose image") {
            showingPicker = true
        }
        .photosPicker(isPresented: $showingPicker) { photos in
            if photos.count > 0 {
                print("Selected \(photos)")
            }
        }
    }
}
```

## Installation

1. In Xcode, open your project and navigate to **File** → **Swift Packages** → **Add Package Dependency...**
2. Paste the repository URL (`https://github.com/lorenzofiamingo/SwiftUI-PhotosPicker`) and click **Next**.
3. Click **Finish**.


## Other projects

[SwiftUI MapItemPicker 🗺️](https://github.com/lorenzofiamingo/SwiftUI-MapItemPicker)

[SwiftUI CachedAsyncImage 🗃️](https://github.com/lorenzofiamingo/SwiftUI-CachedAsyncImage)

[SwiftUI VerticalTabView 🔝](https://github.com/lorenzofiamingo/SwiftUI-VerticalTabView)

[SwiftUI SharedObject 🍱](https://github.com/lorenzofiamingo/SwiftUI-SharedObject)
