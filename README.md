# BloodPressureSDK

MeasureLabs BloodPressure SDK for iOS

## Installation

### Xcode Projects

Select `File` -> `Swift Packages` -> `Add Package Dependency` and enter `https://github.com/measure-labs/BloodPressureSDK`.

### Swift Package Manager

You can add `BloodPressureSDK` as a package dependency in your `Package.swift` file:

```swift
let package = Package(
    //...
    dependencies: [
        .package(
            url: "https://github.com/measure-labs/BloodPressureSDK",
            .exact("1.0.0")
        ),
    ],
    //...
)
```

Then simply `import BloodPressureSDK` where you plan to use it.

## Usage

Note: An example project demonstrating a complete integration with this SDK is forthcoming.

### Initialize the SDK

```
import BloodPressureSDK

let sdk = BloodPressureSDK(key: {YOUR_SDK_KEY})
```

#### Present the Blood Pressure Measurement View

##### UIKit
```
viewController.present(sdk.viewController, animated: true)
```

##### SwiftUI
```
NavigationLink(destination: sdk.view) { ... }
```

Questions?
Email justin@measurelabs.com
