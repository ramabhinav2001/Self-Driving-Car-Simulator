# 🚗 Self-Driving Car Simulation using Udacity Simulator
## 🎥 Demo

📹 Simulation video attached in this repository (Udacity Simulator output)

https://github.com/user-attachments/assets/ce7acb37-629f-4b82-a7f6-f607a1c580f5

---

## 📌 Overview

This project implements an end-to-end deep learning pipeline for autonomous driving using the Udacity Self-Driving Car Simulator. The model predicts steering angles from camera images using a Convolutional Neural Network (CNN), enabling autonomous navigation in a simulated environment.

---

## 🧠 Key Features

* End-to-end behavioral cloning model
* Image preprocessing (cropping, grayscale, resizing, smoothing)
* Data balancing to handle steering angle bias
* CNN-based regression model for steering prediction
* Real-time inference in Udacity simulator

---

## 🗂️ Dataset

* Collected using Udacity Simulator
* ~36,000+ driving samples
* Reduced to ~12,500 samples after balancing
* Includes:

  * Center, Left, Right camera images
  * Steering angle, throttle, brake, speed

---

## ⚙️ Data Preprocessing

* Removed excessive zero steering angles
* Applied:

  * Cropping (remove irrelevant regions)
  * Gaussian blur (noise reduction)
  * Grayscale conversion
  * Resizing to (200 × 66)
* Data augmentation:

  * Zoom
  * Width/Height shift

---

## 🧱 Model Architecture

Inspired by NVIDIA’s end-to-end self-driving architecture:

* 5 Convolutional Layers (ELU activation)
* Fully Connected Layers with Dropout
* Output: Steering angle regression

**Model Size:** ~251K parameters

---

## 🏋️ Training Details

* Loss Function: Mean Squared Error (MSE)
* Optimizer: Adam (lr = 0.0001)
* Batch Size: 32
* Epochs: 30 (with early stopping)

### 📊 Performance

* Validation Loss: ~0.197
* Mean Absolute Error: ~0.34

---

## 🚀 Tech Stack

* **Language:** Python
* **Libraries:** TensorFlow, Keras, OpenCV, NumPy, Pandas, Matplotlib, Scikit-learn

---

## 📁 Project Structure

```
├── self driving car.ipynb   # Main training + preprocessing notebook
├── model.h5                # Trained model
├── README.md
├── driving_log.csv         # Create your own Training Data or Download it form Kaggle
└── demo_video.mp4 / link
```

---

## ▶️ How to Run

### 1. Clone the repo

```bash
git clone https://github.com/ramabhinav2001/Self-Driving-Car-Simulator.git
```

### 2. Install dependencies

```bash
pip install tensorflow keras opencv-python numpy pandas matplotlib scikit-learn jupyter
```

### 3. Run Notebook

```bash
jupyter notebook "self driving car.ipynb"
```

### 4. Run in Udacity Simulator

* Open simulator
* Select autonomous mode
* Load trained model (`model.h5`)

---

## 📈 Future Improvements

* Implement advanced augmentation (brightness, flipping)
* Use transfer learning (ResNet/EfficientNet)
* Optimize for real-time deployment

---

## 👤 Author

**Done by:** Vishweshwar Parmeshwar Bhatt
             Ram Abhinav Vedant Madabushi

---

## 🙌 Acknowledgements

* Udacity Self-Driving Car Simulator
* NVIDIA End-to-End Learning for Self-Driving Cars
