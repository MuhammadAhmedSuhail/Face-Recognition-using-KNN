# Face Recognition Using KNN

## Project Description

In this project, I used a simplified version of the CMU Pose, Illumination, and Expression (PIE) Dataset to implement a k-Nearest Neighbors (k-NN) classifier for face recognition. The dataset consisted of 10 subjects spanning five near-frontal poses, and there were 170 images for each individual. In addition, all the images were resized to 32x32 pixels. The dataset was provided in the form of a CSV file with 1700 rows and 1024 columns. Each row was an instance and each column a feature. The first 170 instances belonged to the first subject, the next 170 to the second subject, and so on.

## Methodology
I followed the following methodology to complete the project:
- **Pre-processing:**
The first step is to normalize each face image vector to unit length by dividing each vector by its magnitude. This is to ensure that the images have the same scale and to prevent features with high magnitude from dominating the distance calculation.
Next, I randomly select 150 images for training and use the remaining 20 for testing for each of the 10 subjects.
- **k-NN Classifier:**
I implement a k-NN classifier using the training set.
For distance calculation, I implement two distance measures: Euclidean and cosine similarity.
I use different values of k (i.e., k=2, 5, 7, 11) and evaluate the performance of the classifier for each distance measure and k value on the test set.
I also experiment with fewer training images (i.e., 100 training images and 70 test images per subject) and report the results.
- **Comparison with Sklearn classifiers:**
I use Sklearn to apply SVM and GaussianNB classifiers on the pre-processed dataset.
I compare the accuracy of the k-NN classifier with the accuracy of the SVM and GaussianNB classifiers.
- **Dimensionality Reduction:**
I perform dimensionality reduction on the pre-processed dataset using Principal Component Analysis (PCA).
I visualize the reduced dataset in 3-D space using matplotlib or Seaborn.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
You will need to have Python 3.x installed on your machine. You can download the latest version of [Python](https://www.python.org/downloads/) here.
</br>
You will also need to have Anaconda on your machine. You can download the latest version of [Anaconda](https://www.anaconda.com/) here.

### Installing
Clone this repository onto your local machine.
```
git clone https://github.com/MuhammadAhmedSuhail/Face-Recognition-using-KNN.git
```
## Running the Program
To run the program, simply execute the juypter notebook to run the KNN Classifier

## Built with:
- Python3 - Programming Language Used
- Sklearn - Library used for Classifer and ML models
- Matplotlib - Library used for displaying the plots

## Results for KNN classifier
- Euclidean distance

  | K  | Accuracy |
  | ------------- | ------------- |
  | 2       |                   95%  |
  | 5       |                   94%  |
  | 7       |                   93%  |
  | 11      |                   89%  |
  
- Cosine Distance

  | K  | Accuracy |
  | ------------- | ------------- |
  | 2       |                   95%  |
  | 5       |                   94%  |
  | 7       |                   93%  |
  | 11      |                   89%  |

## Sklearn classifiers
I used Sklearn to apply SVM and GaussianNB on the dataset and evaluated their performance.

| Classifer  | Accuracy |
| ------------- | ------------- |
| SVM       |                   100%  |
| GausianNB       |                   92%  |

## Dimensionality reduction using PCA
I performed dimensionality reduction on the training and testing datasets and visualized them in 3-D space using PCA and matplotlib.

![Plot](https://user-images.githubusercontent.com/72251313/233627223-487b082d-6981-4e3f-8757-95a920202bb8.png)

## Conclusion
In this project, I implemented the Lazy Snapping algorithm and the k-NN classifier from scratch and evaluated their performance on the provided datasets. I also used Sklearn to apply SVM and GaussianNB on the dataset for comparison. I found that Lazy Snapping provided good segmentation results for the test images, and that k-NN with cosine similarity distance metric and k=5 provided the best classification results for the face recognition task. PCA visualization showed that the dataset is separable in 3-D space.

## Author:
- Muhammad Ahmed Suhail

## Acknowledgments:
- This project was completed as an assignment for **Data Mining** at FAST - NUCES Islamabad.







