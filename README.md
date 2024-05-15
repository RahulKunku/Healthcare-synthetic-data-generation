# Enhancing Patient Privacy with Synthetic Data Generation

## Links
1. All code, presentation, poster files are available here: [https://qrco.de/bevxN8](https://qrco.de/bevxN8)
2. Video Presentation available here: [https://youtu.be/_vCb8h40J9s](https://youtu.be/_vCb8h40J9s)

## Overview

This project aims to create a privacy-focused technological solution that permits responsible and safe data sharing in the healthcare industry. By developing a novel approach to synthetic data generation that maintains the statistical characteristics and predictive ability of actual patient data while providing strong privacy assurances, we assist our client in utilizing the potential of data analytics while maintaining patient confidentiality.

## Project Goals and Objectives

### Goals
- Develop a synthetic data generation methodology that retains the utility of healthcare data for analytical purposes.
- Ensure robust privacy protections for patients, adhering to regulatory frameworks like HIPAA.
- Create a cost-effective alternative to traditional data anonymization techniques.

### Objectives
- Generate synthetic data that mimics real patient data.
- Train machine learning models using synthetic data and compare their performance with models trained on real data.
- Evaluate privacy preservation and utility of the generated synthetic data.

## Process and Methodology

### Data
The dataset for this project was synthetically generated according to the HL7 FHIR dataset format. It includes clinical information, healthcare utilization, and patient demographics, capturing the multifaceted nature of healthcare data.

### Methodology
1. **Data Preprocessing**: Involves exploratory data analysis (EDA), handling outliers and missing values, and feature engineering.
2. **Synthetic Data Generation**: Using techniques such as DataSynthesizer, Variational Autoencoder (VAE), Gaussian Copula, CTGAN, and Copula GAN.
3. **Model Training**: Training models on real and synthetic data, using techniques like Logistic Regression, and evaluating their performance.
4. **Privacy Verification**: Ensuring the synthetic data does not infringe upon individual privacy.
5. **Iterative Refinement**: Adjusting synthetic data generation parameters to balance utility and privacy.

### Predictive Model
- **Training**: Models were trained separately on real and synthetic data.
- **Testing**: Models were tested against unseen real test data.
- **Model Used**: Logistic Regression with a maximum iteration parameter set to 10,000.

### Model Evaluation Metrics
- **ROC AUC Curve**: Evaluates the model's ability to classify correctly.
- **Epsilon (ε)**: Measures the trade-off between privacy and utility in differential privacy.
- **Correlation Matrix**: Assesses the preservation of dependencies and relationships among variables.

## Noise Addition for Differential Privacy
1. **Laplace Noise for Continuous Columns**: Adds noise following a symmetric double exponential distribution.
2. **Salt-and-Pepper Noise for Binary Columns**: Introduces variability by randomly flipping binary values.
3. **Adaptive Noise Addition Using Feature Importance**: Scales noise according to the importance of each feature.

## Models and Results

### Evaluated Models
1. **Generative Adversarial Networks (GANs)**
2. **Variational Autoencoders (VAEs)**
3. **Copula-based Methods**
4. **Conditional Tabular Generative Adversarial Networks (CTGAN)**

### Best Results
- **CTGAN** emerged as the top performer, balancing predictive performance and privacy preservation.
- **Performance Metrics**: ROC AUC, accuracy, and privacy level (ε).
- **CTGAN Advantages**: Generates synthetic data that mirrors the statistical properties of real data while maintaining privacy.

## Key Insights and Takeaways
- The right combination of properties and algorithms is key to generating effective synthetic data.
- Balancing utility and privacy is crucial for the applicability of synthetic data in real-world scenarios.
- CTGAN-generated synthetic data offers significant benefits for healthcare analytics, providing a cost-effective, ethical, and compliant solution.

## Conclusion
The project successfully demonstrated the feasibility and benefits of using synthetic data to balance data utility with privacy concerns in healthcare. By adopting advanced synthetic data generation models, we provided a viable solution to the challenges faced by healthcare providers and researchers, paving the way for further innovations in the field.
