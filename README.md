# 🖐️ Gesture Math: Hand Detection via Geometry
A Computer Vision project using OpenCV to count fingers without Deep Learning.

## 🧠 The Math Behind the Project
Unlike modern AI, this project uses **Spatial Geometry** to understand shapes:

1. **Sklansky’s Algorithm:** Used to generate a **Convex Hull** (a mathematical "rubber band") around the hand contour.
2. **Convexity Defects:** Identified the "valleys" between fingers by calculating the distance between the hull and the contour.
3. **The Law of Cosines:** To filter out noise, every finger gap is verified using:
   $$cos(\theta) = \frac{a^2 + b^2 - c^2}{2ab}$$
   If the angle is $< 90^\circ$, it is mathematically classified as a finger gap.

## 🛠️ Requirements
- Python 3.x
- OpenCV
- NumPy
