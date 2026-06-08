# Basketball Shot Detector & Security Control 🏀🔐

This is a Computer Vision project developed in Python that combines a secure access control system via a visual passcode interface and a real-time basketball shot detector/counter powered by a custom **YOLOv8** object detection model.

## 📋 Project Structure

* **`main.py`**: The main script that manages the application workflow (toggling between the security interface and the basketball detection mode).
* **`utils.py`**: Contains helper functions for image processing, UI rendering, and detection logic.
* **`best.pt`**: Custom YOLOv8 model weights optimized to accurately detect the basketball and the hoop.
* **`limits.json`**: Stores coordinates and spatial limits (Zones of Interest) used to track the ball and determine if a shot was successfully scored.

---

## 🚀 Key Features

### 1. Security Control Panel 🛡️
* **Restricted Access:** Before launching the game detector, the application deploys an interactive graphical interface on the screen that acts as a digital keypad.
* **Credentials Validation:** The user must enter the correct passcode by interacting with the visual system. If an incorrect PIN is provided, the system remains locked. Once the correct passcode is entered, the sports analytics module is unlocked.

### 2. Real-Time Shot Detector (YOLOv8) 🏀
* **Object Detection & Identification:** Utilizes a custom-trained YOLOv8 model (`best.pt`) to locate the basketball hoop and the ball with high precision in every frame.
* **Automated Tracking & Counting:** By defining geometric boundaries stored in `limits.json`, the system monitors the ball's trajectory. When the ball crosses the hoop's critical zone in the correct downward direction, the scoreboard automatically updates in real-time.

---

## 🛠️ Requirements & Technologies

The project is developed using the following core technologies:

* **Python 3.x**
* **OpenCV (`cv2`)**: For video capture, on-screen UI rendering, and drawing text boxes/buttons.
* **Ultralytics (YOLOv8)**: For deep learning model inference and object detection.
* **NumPy**: For efficient mathematical operations on frame matrices.

---

## 📦 Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/jorgemartinb/Basketball-Shot-Detector.git](https://github.com/jorgemartinb/Basketball-Shot-Detector.git)
    cd Basketball-Shot-Detector
    ```

2.  **Install the required dependencies:**
    Make sure your `pip` is updated and install the main libraries:
    ```bash
    pip install opencv-python ultralytics numpy
    ```

---

## 💻 Usage

To run the application, simply execute the main file from your terminal:

```bash
python main.py