## MLOPS Project - Network security system for Phising Data

"Phishing data" refers to sensitive personal information like passwords, bank details, or credit card numbers that cybercriminals attempt to acquire through deceptive means.

### **MLOps Project: Building a Network Security System with ETL Pipelines**

This project focuses on building an **MLOps-based network security system** to detect phishing attempts by classifying data as malicious or non-malicious. The system leverages **ETL pipelines**, **machine learning models**, and **cloud deployment** to create a robust and scalable solution. Below is a detailed summary of the project:

---

#### **Objective**
The goal was to predict whether phishing data (sensitive information like passwords, bank details, etc.) is malicious or not, using a structured MLOps workflow. The project emphasizes automation, scalability, and reproducibility.

---

#### **Key Components and Workflow**
1. **Data Pipeline**:
   - Created ETL pipelines to load data into MongoDB instance.
   - **Data Ingestion**: Phishing data was ingested from a **MongoDB database** and split into train and test datasets, stored as **data ingestion artifacts**.
   - **Data Validation**: Validated the data using **data drift parameters** to ensure consistency and quality.
   - **Data Transformation**: Transformed the data and generated a **preprocessor.pkl file** for preprocessing steps.

3. **Model Development**:
   - **Model Training**: Multiple models were trained, including **Logistic Regression, KNN, AdaBoost, Decision Tree, and Random Forest**.
   - **Model Evaluation**: Models were evaluated, and the best-performing model was selected, resulting in a **final model.pkl file**.
   - **Training and Batch Prediction Pipelines**: Created separate pipelines for training and batch prediction to streamline the process.

4. **Experiment Tracking and Artifact Management**:
   - Used **DagsHub** (an MLOps tool) with **MLflow** to log metrics, track experiments, and select the best model.
   - Artifacts (e.g., preprocessor.pkl, model.pkl) were pushed to **AWS S3 buckets** for storage and versioning.

5. **Web Application**:
   - Developed a **FastAPI-based web application** for real-time predictions.

6. **Cloud Deployment**:
   - **Dockerization**: Created a Docker image and pushed it to the **AWS Elastic Container Registry (ECR)**.
   - **CI/CD Pipelines**: Automated the deployment workflow using **GitHub Actions**.
   - **Deployment**: Deployed the Docker image to an **AWS EC2 instance** for scalable and reliable model serving.

---

#### **Technologies and Tools Used**
- **Data Storage**: MongoDB, AWS S3
- **MLOps Tools**: DagsHub, MLflow
- **Machine Learning**: Scikit-learn (Logistic Regression, KNN, AdaBoost, Decision Tree, Random Forest)
- **Web Framework**: FastAPI
- **Cloud Services**: AWS (EC2, ECR, S3)
- **Automation**: GitHub Actions (CI/CD pipelines)
- **Containerization**: Docker

---

#### **Outcome**
The project successfully built an end-to-end MLOps pipeline for phishing detection, integrating data ingestion, model training, evaluation, and deployment. The use of **DagsHub**, **MLflow**, and **AWS** ensured reproducibility, scalability, and efficient model management. The system is now deployed on **AWS EC2**, ready for real-world phishing detection.

---

