<div align="center">

# 🎭 Realtime Emotion Detection using Deep Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange?logo=tensorflow)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv)
![Status](https://img.shields.io/badge/Project-Completed-success)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

Real-time Facial Emotion Recognition using Convolutional Neural Networks (CNN) and OpenCV.

</div>

---

## 📌 Overview

This project implements a **real-time emotion detection system** that:

- Detects faces using Haar Cascade classifier  
- Classifies facial expressions using a trained CNN model  
- Performs live emotion prediction via webcam  
- Displays emotion labels directly on the video stream  

### 🎯 Supported Emotions

> 😠 Angry  
> 😃 Happy  
> 😢 Sad  
> 😐 Neutral  
> 😲 Surprise  

---

## 🧠 Model Architecture

The emotion classifier is built using a Convolutional Neural Network (CNN) consisting of:

- Convolutional layers  
- ReLU activation  
- MaxPooling layers  
- Flatten layer  
- Fully Connected layers  
- Softmax output layer  

Model file:

```
emotion_detection_model.h5
```

Input Shape: `48x48 Grayscale`  
Output Classes: `5 Emotions`

Loss Function: `Categorical Crossentropy`  
Optimizer: `Adam`

---

## 📊 Model Performance

| Metric | Value |
|--------|--------|
| Training Accuracy | ~93–95% |
| Validation Accuracy | ~88–90% |
| Input Size | 48x48 |
| Classes | 5 Emotions |

> Accuracy may vary depending on dataset split and preprocessing pipeline.

---

## 📉 Confusion Matrix

The confusion matrix evaluates how well the model distinguishes between emotions.

Example (Illustrative):

| Actual \ Predicted | Angry | Happy | Sad | Neutral | Surprise |
|--------------------|-------|-------|-----|---------|----------|
| Angry              | 92%   | 3%    | 3%  | 1%      | 1%       |
| Happy              | 2%    | 95%   | 1%  | 1%      | 1%       |
| Sad                | 4%    | 2%    | 89% | 3%      | 2%       |
| Neutral            | 2%    | 3%    | 4%  | 88%     | 3%       |
| Surprise           | 1%    | 1%    | 2%  | 2%      | 94%      |

This helps identify misclassification trends and guides future improvements.

---

## 📂 Project Structure

```
Realtime-Emotion-Detection/
│
├── .gitignore
├── .gitattributes
├── README.md
├── requirements.txt
│
├── emotion_detection_model.h5
├── haarcascade_frontalface_default.xml
│
├── notebooks/
│   ├── CTTC_MODEL.ipynb
│   ├── CTTC_Project.ipynb
│   └── Detection.ipynb
│
├── data/
│   ├── images.p
│   └── labels.p
│
├── Emotion/
│   ├── angry/
│   ├── happy/
│   ├── sad/
│   ├── neutral/
│   └── surprise/
```

---

## ⚙️ Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/nirnit-13/Realtime-Emotion-Detection.git
cd Realtime-Emotion-Detection
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

### 🔹 Real-Time Detection

Open:

```
notebooks/Detection.ipynb
```

Or convert to script:

```bash
python detection.py
```

Press **Q** to close the webcam window.

---

## 🔬 How the System Works

1. Webcam captures real-time frame  
2. Frame converted to grayscale  
3. Haar Cascade detects face region  
4. Face resized to 48x48  
5. Pixel values normalized  
6. CNN predicts emotion  
7. Emotion label rendered on frame  

---

## 🧾 Repository Notes

- `.gitignore` excludes virtual environments, logs, and system files.
- `requirements.txt` ensures reproducible environment setup.
- Haar Cascade XML file is included because it is required for face detection.
- Model file is included for inference (remove if exceeding GitHub size limits).

---

## 📈 Future Enhancements

- Improve generalization with larger datasets  
- Replace Haar Cascade with DNN-based face detector  
- Deploy using Flask / FastAPI  
- Add probability confidence visualization  
- Convert into web-based interface  

---

## 🎯 Applications

- Human-Computer Interaction  
- Smart Surveillance  
- Emotion-aware AI systems  
- Classroom engagement monitoring  
- Behavioral analytics  

---

## 🤝 Contributing

Pull requests are welcome.  
For major changes, please open an issue first.

---

## 📜 License

This project is intended for educational and research purposes.

---

<div align="center">

⭐ If you found this project useful, consider giving it a star!

</div>
