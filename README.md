<img src="River vs Non-River.png" alt="Alt text" width="800" />
# River vs Non-River Classification of Satellite Data using Bayes Decision Rule

This project implements a classifier to distinguish between satellite images containing river scenes and those without. The classification is based on statistical analysis of pixel intensity values using the Bayes decision rule and multivariate normal distribution modeling.

## Overview

The goal of this project is to automate the classification of satellite images into two categories: images depicting river scenes and images depicting non-river scenes. This distinction is crucial for applications such as environmental monitoring, urban planning, and natural resource management.

## Methodology
1. Data Collection
River Dataset: Gather satellite images containing visible river scenes. Ensure variations in river widths, surroundings, and seasons to capture diverse scenarios.

Non-River Dataset: Collect satellite images without visible river scenes, focusing on landscapes, urban areas, and diverse natural environments.

2. Data Preprocessing
Image Preprocessing: Convert images to grayscale to simplify intensity analysis. Resize images to a standardized resolution for consistency.

Feature Extraction: For each grayscale image:

Extract pixel intensity values.
Compute mean and variance matrices to characterize the statistical distribution of pixel intensities for both river and non-river datasets.
3. Statistical Modeling
Bayes Decision Rule: Utilize the Bayes decision rule for classification:

Calculate the posterior probability of an image belonging to either the river or non-river class based on the observed pixel intensity values.
The decision rule considers the prior probabilities of river and non-river classes, which can be estimated from the dataset or assumed equal if no prior information is available.
Multivariate Normal Distribution:

Model the distribution of pixel intensities for river and non-river images using multivariate normal distribution:
Mean Vector (μ): Represents the average pixel intensity values across all images in each class.
Covariance Matrix (Σ): Describes the variation of pixel intensities within each class.
4. Implementation Details
Programming Language: Implement the classifier in Python for flexibility and efficiency.

Libraries: Use NumPy for numerical operations and matrix manipulations, avoiding reliance on external machine learning libraries.

5. Training and Testing
Training Phase:
Fit the statistical models (mean and covariance matrices) using the training dataset.
Testing Phase:
Evaluate the classifier's performance on a separate set of test images:
Input test images, extract pixel intensities.
Apply the Bayes decision rule to classify each test image as either river or non-river.
6. Evaluation Metrics
Accuracy: Measure the percentage of correctly classified images compared to the total number of test images.

Confusion Matrix: Analyze true positive, true negative, false positive, and false negative classifications to understand classifier performance in detail.

7. Future Enhancements
Feature Engineering: Explore advanced image features beyond pixel intensities for improved classification accuracy.

Model Optimization: Fine-tune parameters and assumptions in the Bayes decision rule for better performance across diverse satellite image datasets.

Real-Time Classification: Adapt the classifier to process and classify streaming satellite data for near real-time applications.



Two datasets are required for training and testing:
- **River Dataset:** Contains satellite images with visible river scenes.
- **Non-River Dataset:** Contains satellite images without visible river scenes.

For each image:
- Pixel intensity values are extracted and used to compute mean and variance matrices for both river and non-river datasets.

### Statistical Modeling

The classifier utilizes the Bayes decision rule:
- **Multivariate Normal Distribution:** Models are built based on the mean and variance matrices derived from the datasets.

### Implementation Details

- **Language:** Implemented in Python.
- **Libraries:** Uses NumPy for efficient numerical operations.

