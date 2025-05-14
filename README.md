
---

# 🎓 SmartForm – An AI-Driven Bicep Curl Counter Using Computer Vision

## 📖 Introduction

**SmartForm** is an innovative application of computer vision and artificial intelligence (AI) in the domain of fitness and human pose tracking. The system is designed to recognize, analyze, and count bicep curl repetitions in real-time using a webcam and without requiring any physical contact or wearable sensors. It aims to provide a cost-effective and accessible alternative to traditional personal training methods and smart gym equipment.

---

## 🎯 Project Objective

The main objectives of this project are:

* To develop a vision-based system capable of accurately detecting and analyzing human motion during bicep curls.
* To calculate elbow joint angles using body landmarks for identifying repetition stages.
* To automate repetition counting and provide live visual feedback to the user.
* To enhance the user’s form awareness, promoting safer and more effective exercise routines.

---

## 🧪 Methodology

1. **Pose Estimation with MediaPipe**
   The system utilizes **MediaPipe Pose**, a machine learning-based pose estimation framework developed by Google, which detects 33 key body landmarks from a video frame.

2. **Joint Angle Calculation**
   Using the detected coordinates of the shoulder, elbow, and wrist, the elbow angle is computed using vector mathematics and trigonometric functions. The angle is used as the primary metric for analyzing the bicep curl movement.

3. **Repetition Counting Logic**

   * When the elbow angle exceeds a certain threshold (e.g., 160°), the system interprets the motion as the **"down"** phase of the curl.
   * When the angle drops below a threshold (e.g., 30°), it marks the **"up"** phase.
   * A valid transition from "down" to "up" is counted as one complete repetition.

4. **Real-Time Feedback and Visualization**
   Visual feedback is provided directly on the video feed, including:

   * The numerical elbow angle at each frame.
   * The current stage of the motion (up/down).
   * The total repetition count.

---

## ⚙️ Tools and Technologies

* **Programming Language:** Python 3
* **Libraries Used:**

  * **MediaPipe:** For real-time pose estimation.
  * **OpenCV:** For capturing and displaying video frames.
  * **NumPy:** For numerical computations, especially in angle calculation.

---

## 📊 System Performance and Accuracy

The SmartForm system demonstrates high responsiveness and accuracy under well-lit conditions and a stable background. It is capable of:

* Providing instant visual feedback.
* Distinguishing valid repetitions with high precision.
* Supporting solo training sessions without the need for supervision.

---

## 📚 References and Resources

The development of this project was informed by the following resources:

* [MediaPipe Pose Documentation](https://google.github.io/mediapipe/solutions/pose.html)
* [OpenCV Library Documentation](https://docs.opencv.org/master/)
* Jiang, H. et al. *Estimating 3D Human Joint Angles from 2D Images*, International Conference on Computer Vision (ICCV), 2017.
* Zhang, T. et al. *Automatic Repetition Counting in Workout Videos*, IEEE Transactions on Multimedia, 2018.
* Sun, K. et al. *Deep High-Resolution Representation Learning for Human Pose Estimation*, IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI), 2019.

---

## 🚀 Future Scope

Future extensions of this project may include:

* Support for multiple exercises such as squats, push-ups, and lunges.
* Real-time audio feedback and correction suggestions using speech synthesis.
* Integration with mobile applications and fitness tracking dashboards.
* Use of historical workout data to provide progress analysis and adaptive workout plans.

---

## 📌 Conclusion

SmartForm effectively demonstrates the potential of computer vision in the field of fitness tracking and human-computer interaction. By automating form correction and repetition counting, it contributes to a more engaging, independent, and data-driven fitness experience for users of all levels.

---
