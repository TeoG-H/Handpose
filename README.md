# Enhanced Hand Gesture Tracker & Analyzer


## 📸 Screenshots & Demos

| | | |
|:---:|:---:|:---:|
| <img src="Output%20Images/palma.jpg" height="220"> | <img src="Output%20Images/left_right.jpg" height="220"> | <img src="Output%20Images/angle_detection.jpg" height="220"> |
| **Normal Detection** | **Left & Right Classification** | **Angle Analysis** |
| <img src="Output%20Images/3-degete.jpg" height="220"> | <img src="Output%20Images/peace.jpg" height="220"> | <img src="Output%20Images/rock.jpg" height="220"> |
| **Finger Counter** | **Gesture: Peace** | **Gesture: Rock** |

---


An advanced real-time hand tracking and gesture recognition system built using **MediaPipe** and **OpenCV**. This project extends basic hand tracking with finger counting, angle calculation, and custom gesture detection.

## 🚀 Key Features

* **Dual Hand Tracking:** Detects and tracks up to 2 hands simultaneously.
* **Hand Classification:** Accurately labels hands as **Left** or **Right** with confidence scores.
* **Gesture Recognition:** Identifies specific gestures:
    * **Palma** (Open Palm)
    * **Pumn** (Fist)
    * **Peace**
    * **OK**
    * **Rock**
    * **Pointing**
* **Finger Counter:** Real-time counting of raised fingers.
* **Kinematic Analysis:** Calculates real-time **angles** for each finger joint (using NumPy).
* **Pinch Detection:** Detects when the thumb and index finger meet.
* **Visual UI:** Includes an FPS counter, semi-transparent overlay, and screenshot functionality.
## ✋ Implementation Details

The project uses MediaPipe’s 21-landmark hand detection model to map the full hand structure and enable gesture analysis and kinematic calculations.

## 🛠️ Installation

1. **Clone this repository:**

**Bash**
```
git clone https://github.com/TeoG-H/Handpose.git
```
2. **Install required dependencies:**

**Bash**

```
pip install opencv-python mediapipe numpy matplotlib
```
## 🎮 How to Use

Run the main script or the Jupyter Notebook. Once the webcam starts:

* **Show your hands:** The system automatically detects hand landmarks and computes joint angles.
* **Perform gestures:** The interface displays the detected gesture name (e.g., Palm, Rock, Peace) in the top-left corner.
* **Keyboard controls:**
    * **S:** Save a screenshot of the current frame to the `Output Images/` folder.
    * **Q:** Quit the application and release the camera.

## 🧪 Technical Details

This project includes advanced kinematic analysis and gesture recognition techniques:

* **Gesture Mapping:** Uses custom logic to compare fingertip positions relative to lower joints to determine whether each finger is raised or folded.
* **Trigonometry:** Uses `np.arctan2` to compute precise flexion angles between three key landmarks of each finger.
* **Pinch Detection:** Measures the Euclidean distance between the thumb tip and index finger tip to trigger a pinch event.
* **FPS & UI Overlay:** Includes an FPS counter and a semi-transparent interface overlay for clearer visualization of data.

## 🙏 Credits

Development of this project was inspired and guided by the resources and tutorials from:

* **Nicholas Renotte** - [AI Hand Pose Estimation with MediaPipe and Python](https://www.youtube.com/watch?v=vQZ4IvB07ec)
* **Nicholas Renotte** - [Detect Left and Right Hand + Calculate Angles](https://www.youtube.com/watch?v=EgjwKM3KzGU)
