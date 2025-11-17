🐭 Animal Behavior Prediction Using Machine Learning

This repository contains the full implementation of my Master’s Thesis project:
“Animal Behavior Prediction Using Machine Learning Methods” (UPM, 2023).
The project applies computer vision and unsupervised machine learning to understand and classify mouse behavior from pose estimation, video data, and audio features.

🚀 Project Overview

The goal of this research is to automatically predict and cluster animal behavior (mice) using:
Pose estimation (AlphaTracker & SLEAP keypoints)
Tracking analysis (MOTA, HOTA, Track-mAP, IDF1)
Unsupervised clustering (K-Means)
Audio-based feature extraction (MFCC, spectral centroid)
Dimensionality reduction (PCA)
The project ultimately identifies behavioral clusters by combining image data + audio data.

🧠 Key Components

1️⃣ Pose Estimation & Tracking
The mice were tracked using AlphaTracker, based on:
Bounding box detection
Keypoint estimation (nose, ears, hips, tail base, etc.)
Tracking consistency across frames
We evaluated model accuracy using:
  1. Metric	Purpose
  2. IoU	Overlap quality between predicted & ground truth boxes
  3. MOTA	Multi-object tracking accuracy (FP, FN, ID switches)
  4. HOTA	Balanced metric for detection & identity association
  5. IDF1	Identity preservation quality
  6. Track-mAP	Tracking mean average precision.

2️⃣ Audio Feature Extraction
Audio files (.wav) were processed using Librosa, extracting:
MFCC coefficients
Spectral centroid
Spectral contrast
Zero-crossing rate
Mel spectrogram
These features were later merged with image-based features for clustering.

3️⃣ Clustering Analysis
We applied K-Means Clustering, with:
PCA for dimensionality reduction
Elbow method & Silhouette score for K selection
Combined feature space (pose + audio)
➡️ Final result: 2 dominant behavioral clusters

🛠️ Technologies Used
Python
Numpy / Pandas
Scikit-Learn
Librosa
Matplotlib / Seaborn
Google Colab (GPU)
AlphaTracker (Deep Learning)
JSON-based annotation datasets

📊 Example Visualizations


