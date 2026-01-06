

# 🖐️ 3D Gesture Emoji Action

A real-time Computer Vision application that detects hand gestures using a **CNN (Convolutional Neural Network)** and triggers **animated 3D-style emojis** with physics-based motion.

## 🚀 Features

* **CNN Classification:** High-accuracy detection of 5 gestures: Palm, Fist, Thumbs Up, Peace, and OK.
* **Temporal Stability:** Uses a **Voting System** (Rolling History) to prevent flickering and false triggers.
* **3D Action Animations:** Emojis don't just appear; they "pop" and "float" using Sine-wave mathematics.
* **Automatic Data Collection:** Includes a script to capture and pre-process 1,000+ training images automatically.

## 📂 Project Structure

```text
.
├── assets/               # 3D-style transparent PNG emojis
│   ├── palm.png
│   ├── fist.png
│   └── ...
├── data/                 # Collected training images (organized by folder)
│   ├── palm/
│   ├── fist/
│   └── ...
├── emotions.ipynb         # The final real-time application
└── gesture_model.h5      # The trained brain (generated)

```

## 🛠️ Installation & Setup

1. **Install Dependencies:**
```bash
pip install opencv-python tensorflow numpy

```


1. **Collect Data:**`,
   change the `target_gesture` name, and press **'s'** to auto-capture 200 images per sign.
2. **Train the Brain:**
 This will process your colored images into grayscale and save `gesture_model.h5`.
3. **Run the App:**
  and show your hand to the camera!

## 🧠 How the "Action" Works

The project uses **Alpha Blending** to overlay transparent emojis onto the webcam feed. The "3D feel" is created by two math functions:

* **Scaling:**  for a fast "pop-in" effect.
* **Bouncing:**  to make the emoji float smoothly.

## 🎮 Controls

* **'s'**: Start auto-capturing (in collector script).
* **'q'**: Quit the application.
* **Hand in Box**: Triggers the 1-second 3D emoji action.

