**Fake Currency Detection using Machine Learning**

**Overview**

This project implements a fake currency detection system using machine learning techniques, as described in the research paper Comparative Study of Machine Learning Classifiers for Fake Currency Detection by Anadi Krishna Jain and Krishiv Panchal. The system processes images of Indian currency notes (₹50, ₹100, ₹200, ₹500) to classify them as genuine or counterfeit. It leverages image processing for feature extraction and evaluates twelve machine learning classifiers, achieving high accuracy with Naive Bayes (98.08% single split, 96.92% cross-validation) and Random Forest (98.08% single split, 96.54% cross-validation).

**Project Structure**

**Dataset:** A synthetic dataset of 460 images (400 real, 60 fake) across four denominations (₹50, ₹100, ₹200, ₹500).

**Methodology:**

**Data Generation:** Real images (50 per denomination, front and back) and fake images (15 per denomination, front only) with modifications to security features.

**Image Processing:** Cropping using Canny edge detection, scaling to a uniform 600-pixel width, and feature extraction (8 features: security thread edge density, watermark gradient magnitude, microlettering contrast, microlettering energy, identification mark edge density, security thread intensity variance, watermark intensity mean, whole image entropy).

**Classifiers:** Twelve machine learning models (SVM, ANN, KNN, Logistic Regression, Gradient Boosting, Naive Bayes, Gradient Descent for Logistic Regression, XGBoost, Random Forest, DCNN, Decision Tree, Ridge Linear Classifier).

**Evaluation:** Single train-test split (80:20) and 5-fold cross-validation with metrics (accuracy, precision, recall, F1-score)

**Feature Importance:** Permutation-based analysis for SVM and Random Forest to identify discriminative features.

**Implementation:** MATLAB R2023a with Image Processing and Statistics and Machine Learning Toolboxes.

**Results**

**Top Performers:**

**Naive Bayes:** 98.08% accuracy (single split), 96.92% (cross-validation), 93.00% F1-score.

**Random Forest:** 98.08% accuracy (single split), 96.54% (cross-validation), 92.00% F1-score.

**ANN:** 98.08% accuracy (single split), 96.15% (cross-validation), 91.00% F1-score.

**Key Features:** Security thread edge density, microlettering contrast, and whole image entropy were highly discriminative.

**Limitations:** Synthetic dataset, limited fake images (60 vs. 400 real), front-side-only feature extraction, and reliance on handcrafted features.
