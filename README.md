# WayZT (Way to Zero Trash)

> An intelligent iOS application to identify your waste and find the nearest recycling centers, guiding you on your journey to zero trash.

> [!NOTE]
> This app is built for iOS and utilizes native frameworks like SwiftUI, MapKit, and Core ML. A physical device is recommended to test all features, especially the AI-powered camera scanner.

## What is WayZT?

**WayZT (Way to Zero Trash)** is an iOS application designed to simplify and encourage recycling for everyone. By leveraging the power of Artificial Intelligence and geolocation, WayZT removes the guesswork from recycling. Users can instantly identify what type of material their trash is and find the most convenient location to recycle it properly.

The application's main goals are to:
1.  **Identify Waste:** Use the device's camera to scan an item and let the built-in Core ML model classify it (e.g., plastic, glass, cardboard).
2.  **Locate Centers:** Display a comprehensive map of nearby recycling centers, with details on what materials they accept.
3.  **Provide Guidance:** Connect the identified waste type to the appropriate recycling centers on the map.
4.  **Educate Users:** Offer helpful articles and tips to promote a more sustainable, zero-waste lifestyle.

## Key Features

- **AI-Powered Waste Scanner:** Integrates a custom Core ML model (`WasteClassification-v3.mlmodel`) that analyzes images from the camera in real-time to classify different types of recyclable materials.
- **Interactive Recycling Map:** Uses Apple's MapKit to display user's location and nearby recycling points of interest (POIs). Users can filter centers based on the materials they accept.
- **Material-Specific Directions:** After scanning an item, the app suggests the best local centers that accept that specific material.
- **Educational Content:** Features a dedicated section (`ArticlesView`) with articles and guides on recycling, reducing waste, and other environmental topics.
- **User Profiles:** Includes a profile section (`ProfileView`) where users might track their recycling progress and contributions.
- **Modern & Native UI:** Built entirely with SwiftUI, offering a responsive, clean, and modern user interface that feels at home on iOS.

## Application Screens

This section will showcase the main user interfaces of the application.

*(You can add your screenshots here later)*

1.  **Splash Screen:** An initial launch screen with the app's logo and animation.
2.  **Main Map View:** The central hub of the app, showing a map with recycling centers. Includes a search bar and filtering options.
3.  **AI Waste Scanner:** The live camera view (`CameraView`) where users point at an item to have it identified.
4.  **Identification Result View:** A screen that appears after a scan, showing the identified material and options to find a place to recycle it.
5.  **Recycling Articles View:** A list or grid of educational articles for users to read.
6.  **User Profile View:** A dedicated screen for user-related information.

## Technology Stack 🧑‍💻

[![Made with Swift](https://img.shields.io/badge/Made%20with-Swift-F05138.svg?style=for-the-badge&logo=swift)](https://www.swift.org)
[![Built with SwiftUI](https://img.shields.io/badge/Built%20with-SwiftUI-027AFF.svg?style=for-the-badge&logo=swift)](https://developer.apple.com/xcode/swiftui/)
[![Uses Core ML](https://img.shields.io/badge/Uses-Core%20ML-333333.svg?style=for-the-badge&logo=apple)](https://developer.apple.com/documentation/coreml)
[![Uses MapKit](https://img.shields.io/badge/Uses-MapKit-34A853.svg?style=for-the-badge&logo=apple)](https://developer.apple.com/documentation/mapkit)

- **Language:** Swift
- **UI Framework:** SwiftUI
- **Mapping & Geolocation:** MapKit
- **Artificial Intelligence:** Core ML for on-device image classification.

## Project Structure

The project is organized into logical groups to maintain a clean architecture:
-   `SplashScreen/`: Handles the initial app launch view.
-   `Model/`: Contains the data structures for the app (e.g., `Articulo`, `PointOfInterest`, `Profile`).
-   `Views/`: Holds all the major SwiftUI views for each screen.
-   `Map/`: Contains specific logic and sub-views related to the MapKit implementation.
-   `Helpers/`: A collection of reusable SwiftUI components (e.g., `SearchBar`, custom buttons).
-   `Animation/`: Stores custom animations used throughout the app.

### Quickstart Guide ⚡️

Follow these steps to run the project in your local environment.

1.  **Prerequisites**
    - macOS (Ventura or newer recommended)
    - Xcode (15.0 or newer recommended)
    - A physical iPhone is required to test the camera scanning feature.

2.  **Clone the repository**

    ```bash
    # Replace the URL with your repository's URL
    $ git clone https://your-repo-url/wayzt-app.git
    $ cd wayzt-app
    ```

3.  **Open the project**

    Find the `Waste Manager.xcodeproj` file in the project directory and double-click it to open it in Xcode.

4.  **Configure Signing & Capabilities**

    - In Xcode, select the `Waste Manager` project in the Project Navigator.
    - Go to the "Signing & Capabilities" tab.
    - Select your development team from the "Team" dropdown menu. This is required to build the app on a physical device.

5.  **Build and Run**

    - Select your target device (an iPhone or an iOS Simulator) from the scheme menu at the top of the Xcode window.
    - Press the "Run" button (▶) or use the shortcut `Cmd + R`.
    - The app will build and launch on your selected device or simulator.
