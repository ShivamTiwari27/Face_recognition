# Face_recognition
This repository features the implementation of the Principal Component Analysis (PCA) algorithm from scratch, followed by the development of a face recognition system using PCA.


Here's a refined version of the README.md file for your GitHub repository:

---

# Facial Recognition using PCA

This repository contains an implementation of a facial recognition system using Principal Component Analysis (PCA). The system projects face images onto a feature space, known as the "face space," represented by Eigenfaces. Eigenfaces are the eigenvectors of a set of face images, which capture the most significant variations among distinct faces.

## Objective

The objective of this project is to recognize a person's face by comparing it to a pre-existing database of faces and identifying the closest match. We implement PCA to create Eigenfaces, which represent the principal components of the face dataset.

## Dataset

We use the AT&T face dataset, which consists of grayscale face images with dimensions 92x112. The dataset comprises 40 directories, each corresponding to a different subject (labeled as s1 to s40). Each subject directory contains ten different images (labeled as 1.pgm to 10.pgm) of that subject, captured under varying conditions such as lighting, facial expressions, and facial details.

[AT&T face dataset](https://git-disl.github.io/GTDLBench/datasets/att_face_dataset/)

## Tasks Performed

1. **Loading and Splitting Dataset:** We load the dataset and divide it into training and test sets, ensuring that one image from each subject is included in the test dataset.

2. **Implementation of PCA:** We implement the PCA algorithm from scratch to extract Eigenfaces from the training dataset.

3. **Image Reconstruction:** We reconstruct images using Eigenfaces and visualize the differences for different numbers of components.

4. **Visualizing Mean (Eigenface):** We visualize the mean face, also known as the Eigenface generated by PCA.

5. **Face Recognition Module:** We evaluate the performance of the PCA-based face recognition module by obtaining accuracy scores for different numbers of principal components.

## Steps for Implementation of PCA Algorithm

1. **Standardize the Data:** Scale the input data to have zero mean and unit variance.
2. **Compute Covariance Matrix:** Calculate the covariance matrix of the standardized data.
3. **Compute Eigenvectors and Eigenvalues:** Find the eigenvectors and eigenvalues of the covariance matrix.
4. **Select Principal Components:** Choose the top k eigenvectors based on their corresponding eigenvalues.

## Steps for Implementation of Image Reconstruction from Eigenfaces

1. **Load the Image:** Load the image to be reconstructed.
2. **Vectorize the Image:** Convert the grayscale image into a 1D vector.
3. **Standardize the Data:** Scale the vectorized image.
4. **Compute Eigenvectors and Eigenvalues:** Find the eigenvectors and eigenvalues of the covariance matrix.
5. **Select Principal Components:** Choose the top k eigenvectors.
6. **Project onto Lower-Dimensional Space:** Project the standardized vector onto the selected eigenvectors.
7. **Reconstruct the Image:** Multiply the lower-dimensional representation by the eigenvectors and add the mean of the standardized vector.

## Advantages and Limitations of PCA

### Advantages

- **Dimensionality Reduction:** Reduces the number of variables while retaining important information.
- **Interpretability:** Transforms variables into uncorrelated components with clear interpretations.
- **Visualization:** Facilitates visualization of high-dimensional data in lower-dimensional space.

### Limitations

- **Assumes Linearity:** Assumes linear relationships between variables, may not capture non-linear relationships effectively.
- **Sensitive to Outliers:** Susceptible to outliers, which can significantly impact results.
- **Data Scaling Required:** Requires variables to be scaled, which may be challenging if variables have different scales.

In the context of face recognition, PCA has additional limitations:

- **Limited Facial Variations:** May not capture all facial variations effectively, such as changes in lighting or expression.
- **Limited Accuracy:** May not be accurate enough for high-security applications.
- **Computationally Expensive:** Can be computationally expensive, especially for large datasets.

For further details, refer to the provided [paper on Eigenfaces](https://sites.cs.ucsb.edu/~mturk/Papers/mturk-CVPR91.pdf).

---

This README.md file provides comprehensive information about the project, including its objectives, tasks performed, implementation steps, dataset details, and the advantages and limitations of PCA in facial recognition. Feel free to customize it further to suit your specific requirements and preferences. If you have any questions or need further assistance, please let me know!
