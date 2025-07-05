# Real-Time Face Recognition for Modern Android

This is a fully modernized, high-performance face recognition application for Android, built using the latest development tools and libraries. It provides a robust foundation for implementing real-time, on-device face recognition in any modern Android project.

This project was developed by **Danush Gopal**. The core functionality is based on creating and comparing unique facial embeddings, allowing for fast, accurate, and offline recognition.

## Key Features
- **Fast and Accurate:** Utilizes a lightweight MobileFaceNet model for high-speed performance on mobile devices.
- **Modern Tech Stack:** Built with the latest versions of Android Studio, Gradle, and modern Jetpack libraries.
- **No Re-training Required:** New faces can be added dynamically without needing to retrain the underlying model.
- **Real-Time & Offline:** All processing, from face detection to recognition, happens entirely on the device. No internet connection is required.
- **Simple and Intuitive UI:** A clean interface for adding, managing, and recognizing faces.
- **Save & Manage Recognitions:** Easily save recognized faces with names and manage them through an intuitive list interface.

## Core Technologies & Frameworks
- **Development Environment:** Android Studio (Hedgehog | 2023.1.1 or newer)
- **Language:** Java
- **Build System:** Gradle 8.x
- **Core Libraries:**
  - **CameraX:** For a modern, lifecycle-aware camera implementation.
  - **ML Kit (Face Detection):** Used for efficiently locating faces in the camera feed.
  - **TensorFlow Lite:** For running the machine learning model that generates face embeddings.
  - **Android Jetpack:** Includes Navigation Component for UI flow and other modern architecture components.

## How It Works
The application follows a sophisticated pipeline to achieve real-time recognition:

1.  **Face Detection:** The CameraX feed is analyzed in real-time by Google's ML Kit to detect the presence and location of a face.
2.  **Image Processing:** Once a face is detected, it is cropped and resized to the required 112x112 pixel input size for the model.
3.  **Embedding Generation:** The processed face image is fed into a pre-trained **MobileFaceNet** model running via TensorFlow Lite. The model generates a **192-number vector (an "embedding")**, which serves as a unique mathematical signature for that face.
4.  **Recognition via Comparison:** This new embedding is compared against a list of previously saved embeddings. The app calculates the **Euclidean distance** to find the closest match. If the distance is below a set threshold, the name associated with the saved embedding is displayed.

## The Machine Learning Model
- **Model Architecture:** **MobileFaceNet**
- **Research Paper:** [ArcFace: Additive Angular Margin Loss for Deep Face Recognition](https://arxiv.org/abs/1801.07698)
- **Note:** The model used in this app is **pre-trained**. The training process happened on large-scale academic datasets. This app focuses on using the model for inference (generating embeddings), not training.

## Getting Started

To get this project running on your own machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Danush6123/Face_Recognition_TFlite_Android_Application
    ```

2.  **Open in Android Studio:**
    - Launch Android Studio (version Hedgehog or newer is recommended).
    - Select `Open` and navigate to the cloned project folder.
    - Android Studio will automatically sync the Gradle project.

3.  **Run the App:**
    - Connect an Android device (with USB debugging enabled) or start an Android Emulator.
    - Click the 'Run' button (▶️) in Android Studio.

## Contribution
Pull requests are welcome! For major changes or feature suggestions, please open an issue first to discuss what you would like to change.

## Developer
**atharvakale** - https://github.com/atharvakale31

Updated by - **Danush Gopal**

---
*This project has been fully updated and modernized to ensure compatibility and performance with the current Android development ecosystem.*
