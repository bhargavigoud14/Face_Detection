
# Face Comparison Using DeepFace in Google Colab

## 📌 Introduction

This project enables you to compare two images of human faces and determine if they belong to the same person. It uses a pre-trained deep learning model from the DeepFace library to perform facial recognition. The process works directly in Google Colab, making it easy to use without needing to set up a local environment. The script will show the images side-by-side, perform the comparison, and then display a similarity score between 0% and 100%. If no faces are detected, the script will handle it and provide an appropriate error message.

---

## 🚀 What It Does

- Accepts two face images as input.
- **Detects** faces from the images.
- **Compares** the faces using a pre-trained deep learning model.
- Outputs a **similarity score** that tells you how likely it is that the faces belong to the same person.
- Displays both images side by side for easy comparison.
- Handles several edge cases:
  - If no face is detected in one or both images.
  - If multiple faces are detected, the largest face is chosen for comparison.
  - If there are errors in reading or processing the images.

---

## 🧠 Technologies Used

- **Python**: The core language for this project.
- **DeepFace**: A deep learning library that provides state-of-the-art models for face recognition.
- **OpenCV**: A computer vision library used to load and process images.
- **Matplotlib**: A library for displaying images side by side.
- **Google Colab**: An online platform for running the code without setting up a local environment.

---

## 🧪 How It Works (Code Overview)

1. **Image Upload**: The images are uploaded into the Colab environment using the file upload feature.
2. **Image Preprocessing**: The images are read using OpenCV and converted to RGB for proper display using Matplotlib.
3. **Face Detection & Comparison**: DeepFace is used to verify whether the faces in the images match. The face verification process involves using a deep learning model (like `VGG-Face`) to extract features from the images and compare them.
4. **Similarity Calculation**: A similarity score is computed based on the distance between the features extracted from the images. A higher similarity percentage indicates that the faces are more likely to match.
5. **Error Handling**: The script checks for cases where images cannot be loaded, no faces are detected, or other issues occur. It provides appropriate messages to guide the user.

---

## 🧩 Key Features

- **Face Detection**: The script automatically detects faces in the input images, even if multiple faces are present.
- **Similarity Scoring**: The result shows a similarity percentage, indicating how similar the two faces are.
- **Error Handling**: The script gracefully handles cases where no face is found or if the images are invalid.
- **User-Friendly**: The images are displayed side by side with the similarity score for easy interpretation.

---

## 📂 How to Use in Google Colab

1. Upload the images using Google Colab's file upload feature.
2. Install the DeepFace library using `!pip install deepface`.
3. Run the script, providing the image file paths as input to the `compare_faces` function.

---

## ✅ Output Example

- **Matched Faces**:  
  If the faces are similar, the script will output something like:
  `✅ Faces match with 85.37% confidence.`

- **Non-Matched Faces**:  
  If the faces don't match, you will see:
  `❌ Faces do NOT match. Similarity: 34.45%`

- **Error Handling**:  
  If no faces are detected or if there's an issue with the image, the script will notify you:
  `❌ Error: Face not found in one or both images.`


