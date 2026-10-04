# Practical-6: Frame-by-Frame Animation and Splash Screen

## 📌 Aim

Create an Android application to demonstrate **Frame-by-Frame Animation** and a **Splash Screen using Tween Animation**.

## 📝 Description

This practical demonstrates different animation techniques in Android using Kotlin and XML. The application contains a main screen with an `ImageView` to display frame-by-frame animation and a splash screen that uses tween animations to animate UI elements before opening the main Activity.

Frame-by-frame animation displays a sequence of images one after another to create the illusion of movement. Tween animation applies transformations such as scaling, translating, rotating, and fading to a view.

## 🎯 Objectives

* To understand frame-by-frame animation.
* To understand tween animation.
* To create a splash screen for an Android application.
* To use `ImageView` to display images.
* To implement `AnimationDrawable`.
* To create a gradient background using XML.
* To apply scale, translate, rotate, and alpha animations.
* To understand immersive mode and edge-to-edge display.
* To learn about animation listeners and Activity transitions.
* To convert SVG images into Android XML drawable resources.

## 🛠️ Technologies Used

* **Programming Language:** Kotlin
* **IDE:** Android Studio
* **UI Design:** XML
* **Platform:** Android
* **Animation:** XML Animation Resources and `AnimationDrawable`

## 📚 Practical Tasks

### 1. Main Activity

Create `MainActivity` according to the given UI design. It displays the required UI elements and demonstrates frame-by-frame animation using an `ImageView`.

### 2. Splash Activity

Create `SplashActivity` according to the practical's reference video. The splash screen displays the application logo or other visual elements with tween animations before navigating to the main screen.

### 3. Gradient Background

Create a rectangular gradient background for the splash screen using the `<gradient>` tag inside a `<shape>` tag.

Required properties:

* Shape: Rectangle
* Gradient type: Radial
* Center X: `0.9`
* Center Y: `0.9`
* Gradient radius: `1500`
* Start color: Pink
* End color: Blue

### 4. Frame-by-Frame Animation

Use a sequence of images to create an animation. The images can represent an alarm, a heart, or the UVPCE logo.

The `<animation-list>` resource defines the sequence of drawable images and their durations.

Important attributes and elements:

* `<animation-list>`
* `android:oneshot`
* `AnimationDrawable`

### 5. Tween Animation

Use tween animation to apply transformations to the splash screen elements.

The following XML tags must be demonstrated:

| XML Tag       | Purpose                    |
| ------------- | -------------------------- |
| `<set>`       | Groups multiple animations |
| `<scale>`     | Changes the size of a view |
| `<translate>` | Moves a view               |
| `<rotate>`    | Rotates a view             |
| `<alpha>`     | Changes transparency       |

Important animation attributes:

* `android:startOffset="100"`
* `android:duration="1000"`

### 6. Animation and Activity Methods

The practical covers the following methods and classes:

* `AnimationUtils`
* `loadAnimation()`
* `setAnimationListener()`
* `onWindowFocusChanged()`
* `overridePendingTransition()`
* `finish()`

These are used to load animations, handle animation events, control immersive display behavior, and manage Activity transitions.

## 📖 Theory

### What is Frame-by-Frame Animation?

Frame-by-frame animation displays a series of drawable images in sequence. Each image acts as one frame, and displaying them quickly creates the effect of movement.

In Android, it can be implemented using `AnimationDrawable` and an XML `<animation-list>` resource.

### What is Tween Animation?

Tween animation applies transformations to a view over a specified duration. It can change the view's position, size, rotation, or transparency.

The four basic tween animations are:

1. **Scale:** Changes the size of a view.
2. **Translate:** Moves a view from one position to another.
3. **Rotate:** Rotates a view.
4. **Alpha:** Changes the transparency of a view.

### What is Edge-to-Edge Display?

Edge-to-edge display allows application content to extend behind the system status bar and navigation bar. Appropriate window insets should be handled so that important content is not hidden behind system bars.

### What is Immersive Mode?

Immersive mode allows an application to hide system bars temporarily, providing a full-screen experience. It is useful for splash screens and applications that require an uninterrupted visual display.

## 📂 Suggested Project Structure

```text
Practical-6/
│
├── README.md
│
└── app/
    └── src/
        └── main/
            ├── java/
            │   └── com.example.practical6/
            │       ├── MainActivity.kt
            │       └── SplashActivity.kt
            │
            ├── res/
            │   ├── anim/
            │   │   ├── scale.xml
            │   │   ├── translate.xml
            │   │   ├── rotate.xml
            │   │   ├── alpha.xml
            │   │   └── splash_animation.xml
            │   │
            │   ├── drawable/
            │   │   ├── gradient_background.xml
            │   │   └── animation_list.xml
            │   │
            │   ├── drawable-nodpi/
            │   │   └── animation_frames/
            │   │
            │   ├── layout/
            │   │   ├── activity_main.xml
            │   │   └── activity_splash.xml
            │   │
            │   └── values/
            │
            └── AndroidManifest.xml
```

*Note: This is a suggested structure. Actual filenames and resource locations may differ depending on your implementation.*

## ▶️ How to Run

1. Open Android Studio.
2. Create or open the Practical-6 project.
3. Select Kotlin as the programming language.
4. Create `MainActivity` and `SplashActivity`.
5. Add the required image resources to the project.
6. Create the frame animation using an `<animation-list>` resource.
7. Create the gradient background using a drawable XML file.
8. Add tween animation XML files inside `res/anim`.
9. Implement the animation logic in Kotlin.
10. Configure the launcher Activity in `AndroidManifest.xml`.
11. Connect an Android device or start an emulator.
12. Run the application and observe the splash screen and animations.

## 🧪 Testing

| Test                 | Expected Result                                    |
| -------------------- | -------------------------------------------------- |
| Launch application   | Splash screen appears                              |
| Splash animation     | UI elements animate as expected                    |
| Splash completion    | Main Activity opens                                |
| Frame animation      | Images play in sequence                            |
| Scale animation      | View changes size                                  |
| Translate animation  | View changes position                              |
| Rotate animation     | View rotates                                       |
| Alpha animation      | View fades in or out                               |
| Gradient background  | Pink-to-blue radial gradient appears               |
| Edge-to-edge display | Content extends behind system bars when configured |

## 📸 Screenshots

Add your application screenshots after completing the practical.

### 1. Splash Screen

*Add splash screen screenshot here.*

### 2. Tween Animation

*Add screenshot showing the animation here.*

### 3. Main Activity

*Add main screen screenshot here.*

### 4. Frame-by-Frame Animation

*Add screenshot showing the frame animation here.*

## 🧠 Key Learning Outcomes

After completing this practical, we understand:

* The difference between frame-by-frame and tween animation.
* How to display animations using `ImageView`.
* How to use `AnimationDrawable`.
* How to create a radial gradient background.
* How to apply scale, translate, rotate, and alpha animations.
* How to load animations using `AnimationUtils`.
* How to handle animation events using listeners.
* How to navigate between Activities after a splash screen.
* How to configure immersive mode and edge-to-edge display.
* How to use drawable and animation resources in Android.

## ✅ Conclusion

This practical demonstrates frame-by-frame animation and tween animation in an Android application using Kotlin and XML. It covers splash screen creation, gradient backgrounds, image sequences, view transformations, and Activity transitions. It helps develop an understanding of animation techniques used to make Android applications more interactive and visually appealing.
