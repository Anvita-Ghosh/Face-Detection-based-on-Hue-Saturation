# Face-Detection-based-on-Hue-Saturation
Face detection and clustering using OpenCV and K-Means. This project extracts HSV features from detected faces, performs unsupervised clustering, and classifies a template image into the learned clusters. Includes visualisations, distance-based analysis, and practical implementation of feature-based image grouping.

# Overview

This project implements a complete computer vision pipeline that:
- Detects faces using OpenCV Haar Cascades
- Extracts HSV-based color features (Hue & Saturation)
- Applies K-Means clustering to group similar faces
- Classifies a new template image into the learned clusters
- Visualizes clustering results in feature space

# Aim
The objective of this lab is to:

1. Detect faces from an input image.
2. Extract numerical features from face regions.
3. Apply K-Means clustering for grouping similar faces.
4. Classify a new template image based on learned clusters.
5. Visualize results to interpret clustering behaviour.

# Methodology
1. Face Detection
- Haar Cascade classifier is used to detect faces in the input image.  
- Detected face regions are extracted.  
- Bounding boxes are drawn around each detected face.

2. Feature Extraction (HSV Space)

- The image is converted from BGR to HSV color space.  
- Mean Hue and Mean Saturation values are computed for each detected face.  
- Each face is represented as a 2D feature vector

3. K-Means Clustering

- K-Means clustering is applied to the extracted HSV features.  
- Faces are grouped based on similarity in color distribution.  
- Cluster centroids are computed and visualized.  
- Separation between clusters is observed in a 2D feature space.

4. Template Classification

- A new template image (`Dr_Shashi_Tharoor.jpg`) is:
  - Converted to HSV
  - Feature vector extracted (Mean Hue, Mean Saturation)
- The trained K-Means model predicts its cluster label.
- The template image is plotted in the same feature space for comparison.

# Key findings
- Faces with similar color distributions cluster together.  
- HSV features provide a simple yet effective low-dimensional representation.  
- K-Means forms separable clusters in the 2D feature space.  
- Template classification works based on proximity to learned centroids.  
- Performance depends on:
  - Proper feature scaling  
  - Choice of number of clusters (K)  
  - Lighting and image conditions
 
# Conclusions

This project demonstrates how simple color-based features combined with K-Means clustering can group similar face regions and classify new inputs without requiring labeled data.

Although effective in controlled scenarios, improvements could include:
- Adding texture-based features  
- Using deep feature embeddings  
- Applying dimensionality reduction  
- Evaluating optimal K using Silhouette score  


