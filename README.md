<a name="top"></a>
# 🏒 Air Hockey using OpenCV & Hand Detection
This is a fun Air Hockey game built with Python and OpenCV where two players can control paddles using hand movements detected via the webcam.

## ✨ Features
- 🎮 Real-time paddle control using color-based hand detection
- 🧠 Simple collision detection for ball and paddle interactions
- 🔁 Auto speed increment on every paddle hit
- 🏆 Win condition based on score (default: 5)
- 🖼️ OpenCV GUI with live tracking and score display

## 📦 Requirements
- Python 3.x
- OpenCV (cv2)
- NumPy
  
Install required libraries using:
```bash
pip install opencv-python numpy
```

## 🛠️ Folder Structure
```bash
├── main.py
├── utils/
│   ├── Ball.py
│   ├── Paddle.py
│   ├── Score.py
│   ├── collision.py
│   ├── constants.py
│   └── hand_detection.py
```
## 🚀 How to Run
- Clone this repo or copy the files.
- Make sure your webcam is working.
- Run the main file:
```bash
python main.py
```

Use colored objects (like gloves or paper) for hand detection and move your hands up/down to control the paddles.

## 🎮 Controls
- Left Paddle: Left hand (first detected centroid)
- Right Paddle: Right hand (second detected centroid)
- Quit Game: Press q

## ⚙️ Customization
You can edit the following in utils/constants.py:
```python
BALL_VEL = 2             # Initial ball speed
BALL_RADIUS = 15         # Ball size
MAX_SCORE = 5            # Score needed to win
PADDLE_WIDTH = 20        # Paddle width
PADDLE_HEIGHT = 100      # Paddle height
```
- Also, tune HSV values in the "Trackbars" window to match your colored object for better detection.

## 🧠 How It Works
- Uses OpenCV to track color (HSV range via trackbars)
- Detects contours and calculates their centroids
- Maps those centroids to paddle Y-axis positions
- Ball moves and bounces with increasing speed on paddle collision
- Score is tracked and displayed in real-time

## 📌 Note
- Make sure you have decent lighting for color tracking.
- Avoid background colors similar to your paddle color object.

## 👩‍💻 Author
- Made with ❤️ by Charul192
- Feel free to fork, clone, or contribute!
  
## ⭐ Support the Project
If you found this project useful or interesting, please give it a star on GitHub — it helps others discover it too!
<br/>
[⬆ Back to Top](#top)
