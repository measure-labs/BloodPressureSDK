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

let sdk = BloodPressureSDK(
    key: {YOUR_SDK_KEY}, 
    onCancel: { 
        // Handle user cancellation...
    },
    onResult: { bp, error in 
        guard error == nil else { 
            // Handle error...
            return
        }
        
        // Handle blood pressure values...        
        let systolic: Double = bp.systolic
        let diastolic: Double = bp.diastolic
    }
        
)
```

#### Present the SDK

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
