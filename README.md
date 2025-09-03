# 🧙‍♂️ Harry Potter Invisibility Cloak using OpenCV

This project recreates the famous **Invisibility Cloak** effect from Harry Potter using Python and OpenCV.  
When you cover yourself with a red cloth (or any chosen color), the cloth is replaced with the static background, making it appear as if you are invisible.

---

## ✨ Features
- Capture a clean background image from your webcam.
- Detect a red-colored cloak using **HSV color space**.
- Replace the detected cloak area with the background.
- Real-time video feed with the invisibility effect.
- Quit anytime with the `q` key.

---

## 🛠️ Requirements
- Python 3.x  
- OpenCV  
- NumPy  

Install dependencies:
```bash
pip install opencv-python numpy
````

---

## 📷 How it Works

1. **Background Capture**

   * Run the first part of the code (`capture_background.py`).
   * Stay out of the camera view and press `q` to save the background image (`image.jpg`).

2. **Cloak Effect**

   * Run the second part of the code (`invisible_cloak.py`).
   * Wear/hold a red cloak (or change HSV values for another color).
   * The cloak area will be replaced with the saved background, creating the invisibility effect.

---

## 🧩 Code Structure

* `capture_background.py` → Captures and saves a static background image.
* `invisible_cloak.py` → Runs the invisibility cloak effect.

---

## 🎨 Change Cloak Color

By default, the cloak color is **red** (HSV ranges defined in the code).
To change the cloak color, adjust the HSV values:

```python
# Example for blue cloak
lower_blue = np.array([94, 80, 2])
upper_blue = np.array([126, 255, 255])
mask = cv2.inRange(hsv_frame, lower_blue, upper_blue)
```

---

## 🚀 Run

```bash
# Step 1: Capture background
python capture_background.py

# Step 2: Start cloak effect
python invisible_cloak.py
```

---

## 📌 Notes

* Ensure good lighting for best results.
* Avoid wearing clothes of the same color as the cloak.
* Tune the HSV ranges if the cloak is not detected properly.

---

## 📜 License

This project is open-source and free to use for educational purposes.

```

---

👉 Do you want me to also **separate your code into two clean files** (`capture_background.py` and `invisible_cloak.py`) so that it matches this README structure?
```
