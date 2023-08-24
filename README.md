# Xylophone iOS13 App Readme

The **Xylophone iOS13** app is a simple iOS application developed using the Swift programming language and the UIKit framework. This app allows users to play musical notes when they tap on virtual xylophone keys displayed on the screen. Each xylophone key represents a different musical note.

## Table of Contents

- introduction
- app-components
- how-it-works
- usage
- conclusion

## Introduction

The **Xylophone iOS13** app showcases how to create a virtual xylophone experience on iOS devices. Users can enjoy playing musical notes by interacting with the colorful xylophone keys displayed on the screen.

## App Components

The app consists of the following main components:

1. **ViewController**: This is the main view controller of the app. It's responsible for managing the UI elements and responding to user interactions.

2. **AVAudioPlayer**: An instance of the `AVAudioPlayer` class is used to play musical notes. It's responsible for loading and playing the audio files corresponding to each note.

3. **UIButtons**: The app UI includes multiple buttons, each representing a different musical note. These buttons are created using `UIButton` instances and are connected to the `cKeyPressed` IBAction.

## How It Works

When the app is launched, the main view controller (`ViewController`) is loaded. The view contains colorful buttons that mimic the appearance of xylophone keys. The `playSound` function is responsible for playing the corresponding note when a button is tapped.

1. **View Loading**: The `viewDidLoad` method is called when the view controller's view is loaded. However, this method is empty in the provided code.

2. **Button Interaction**: Each button is linked to the `cKeyPressed` IBAction using Interface Builder. When a button is tapped, the `cKeyPressed` function is triggered.

3. **Note Playback**:
    - The `playSound` function takes a `soundName` parameter, which represents the name of the audio file corresponding to a musical note.
    - Inside the `playSound` function, the app attempts to find the audio file with the given name and the `.wav` extension in the app's main bundle.
    - If the audio file is found, an `AVAudioPlayer` instance is created with the URL of the audio file.
    - The app configures the audio session to allow for playback and activates it.
    - The `AVAudioPlayer` instance is then used to play the musical note.

4. **Button Animation**:
    - After a xylophone key is tapped, its alpha (opacity) is briefly reduced to 0.5 to provide visual feedback to the user.
    - The use of `DispatchQueue.main.asyncAfter` delays the change in alpha back to 1.0, creating a quick animation effect.

## Usage

1. Launch the app on an iOS device or simulator.

2. You will see a virtual xylophone on the screen, with colorful keys resembling a real xylophone.

3. Tap on a xylophone key to play the corresponding musical note. The key's alpha will briefly decrease and then return to normal, mimicking the press of a physical key.

## Conclusion

The **Xylophone iOS13** app demonstrates the process of creating an interactive xylophone experience on iOS devices using Swift and the `AVFoundation` framework. Users can enjoy playing musical notes in a playful and visually appealing manner. This app serves as a foundation and can be extended with additional features, such as more notes, different instrument sounds, and user interface enhancements.
