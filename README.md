# CinematicOnboardingView-SwiftUI

A cinematic onboarding flow built in SwiftUI

[![Watch the video](https://adamlyttleapps.com/demo/OnboardingCinematicView/demo-preview.png)](https://adamlyttleapps.com/demo/OnboardingCinematicView/demo.mp4)

## Overview

CinematicOnboardingView-SwiftUI is a SwiftUI-based onboarding framework designed for apps that want a bold, animated, and cinematic first impression. With layered animations, progress tracking, testimonials, and rich visuals, this component enhances user engagement from the very start.

## Features

* SwiftUI Architecture: Built natively with SwiftUI and animation support  
* Cinematic Graphics: Support for full-screen hero images and animated overlays  
* Animated Step Transitions: Smooth fade and scale transitions between onboarding steps  
* AI-Powered Messaging: Copy and visuals tailored for AI/vision-based use cases  
* Testimonial View: Rotating, animated user quotes with star ratings  
* Reusable Components: Modular views for animation, header, footer, and content  
* Dark Mode Optimized: Fully styled for dark mode aesthetics  

## Usage

1. **Add the Onboarding Files to Your Project**

Drag the Swift files into your project:
- `OnboardingCinematicView.swift`
- `CustomAnimationFishPhotoView.swift`
- `CustomAnimationDigitalSharkView.swift`
- Any related views or assets used inside

2. **Add Required Assets to Assets.xcassets**

Include the following images:
- `hero-header`, `hero-footer`
- `onboarding-fish-wireframe`, `onboarding-hand-animation-1/2/3`
- `onboarding-shark`
- `award-leaves`, `avatar-1`, `avatar-2`, etc.

3. **Present Onboarding View Fullscreen**

```swift
struct ContentView: View {
    @State private var isPresented = true
    var body: some View {
        Text("Hello, world!")
            .fullScreenCover(isPresented: $isPresented) {
                OnboardingCinematicView(
                    isPresented: $isPresented
                )
            }
    }
}
```

4. **Customize Testimonials**

```swift
@State private var testimonials: [OnboardingTestimonial] = [
    OnboardingTestimonial(id: 1, title: "Such a good app", description: "I never thought identifying insects could be this fun!"),
    OnboardingTestimonial(id: 2, title: "Super useful in the field", description: "Quick, reliable, and even shows me local species."),
]
```

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request on the [GitHub repository](https://github.com/your-username/OnboardingCinematicView).

## MIT License

This project is licensed under the MIT License. See the LICENSE file for more details.
