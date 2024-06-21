# River-Classifier-
This project implements a classifier to distinguish between images containing river scenes and those without, based on statistical analysis of pixel intensity values. The classifier utilizes the concept of multivariate normal distribution to model the pixel intensity distributions of both river and non-river images.
# River vs Non-River Classification of Satellite Data using Bayes Decision Rule

This project implements a classifier to distinguish between satellite images containing river scenes and those without. The classification is based on statistical analysis of pixel intensity values using the Bayes decision rule and multivariate normal distribution modeling.

## Overview

The goal of this project is to automate the classification of satellite images into two categories: images depicting river scenes and images depicting non-river scenes. This distinction is crucial for applications such as environmental monitoring, urban planning, and natural resource management.

## Methodology

### Data Collection and Preprocessing

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

### How to Use

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/River-non-river-classification.git
   cd River-non-river-classification
