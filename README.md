# Cervical-cancer-risk-assessment-using-XGBoost

## Overview
This project aims to assess the risk of cervical cancer based on various health and lifestyle factors. Using a machine learning model (XGBoost), the system takes user inputs through a simple front-end and predicts whether the individual is at high or low risk of developing cervical cancer. This project also highlights the importance of early detection and is developed as a proof-of-concept and educational tool, not a replacement for professional medical assessment.

---

## Dataset
The dataset used is the [UCI Machine Learning Repository Cervical Cancer Risk Factors dataset](https://archive.ics.uci.edu/ml/datasets/Cervical+cancer+%28Risk+Factors%29). This dataset contains features related to patient medical and lifestyle history, which may correlate with the risk of developing cervical cancer.

Key attributes used:
- Age
- Number of sexual partners
- Age of first sexual intercourse
- Number of pregnancies
- Smoking duration
- Hormonal contraceptive usage
- Number of STDs
- Cancer diagnosis
- HPV diagnosis

---

## Project Structure
The project contains the following main files and folders:
- **train_and_save_model.py**: Script to preprocess data, train the model, and save the trained model as `xgb_model.pkl`.
- **app.py**: Flask application script to handle the frontend, get user inputs, and make predictions using the saved model.
- **templates/**: Contains the HTML files for the frontend.
    - `home.html`: Provides general information and an introduction to cervical cancer.
    - `index.html`: Form for users to enter health-related data for risk assessment.
    - `result.html`: Displays the prediction result.
- **static/**: Contains styles (`styles.css`) and images.

---

## Methodology
1. **Data Preprocessing**:
   - Loaded the dataset and replaced missing values with the mean for continuous variables.
   - Dropped columns with minimal relevance or excessive missing values.
   - Converted data to a format suitable for model training.

2. **Model Training**:
   - Used the XGBoost classifier due to its effectiveness in handling imbalanced data and complex relationships.
   - The model is trained with an 80/20 train-test split, with hyperparameters optimized for accuracy and interpretability.

3. **Prediction Flow**:
   - User inputs health-related information via a web form.
   - Inputs are formatted and passed to the model to predict risk status.
   - Result (High/Low Risk) is displayed on the `result.html` page.

## Model Selection
The **XGBoost** algorithm was selected for its strong performance in handling imbalanced data and ability to model non-linear relationships. The classifier was fine-tuned to improve precision and recall, critical metrics for health-risk prediction models.

## Frontend
The frontend is built using HTML/CSS with Flask as the backend framework. The `home.html` page introduces the project, and the `index.html` page collects user input for prediction. 

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/cervical-cancer-risk-assessment.git
   cd cervical-cancer-risk-assessment
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python app.py
   ```

The application will run on `http://127.0.0.1:5000/`.

## Usage
- Access the home page and learn about cervical cancer risks.
- Navigate to the risk assessment form, fill in the health-related details, and submit.
- View the risk prediction (High or Low) along with a disclaimer.

---

## Disclaimer
This project is intended for educational purposes only and is not a substitute for professional medical advice. Always consult healthcare providers for a thorough medical examination and assessment.

## Future Work
1. Improve model accuracy by using additional data and exploring alternative models.
2. Add visualizations to provide insights into the features impacting risk assessment.
3. Extend the frontend for better interactivity and user experience.
4. Deploy the app on a cloud platform for accessibility.

## Contributors
- **Pratyusha R Yarlapati**: Developer and project owner
