# Project Title: Customer Salary Prediction

## Overview
This project aims to predict the salary of customers based on various features using a regression model. The dataset used in this project is derived from a customer churn dataset and includes features such as Geography, Gender, Age, Tenure, Balance, and more. The project involves data preprocessing, model training, and deployment using Streamlit, making it accessible as a web application.

## Files in the Repository
- `app.py`: The main application script that loads the model, preprocesses the input data, and predicts customer salary. It also includes the code to deploy the application using Streamlit.
- `regression_model.h5`: The trained regression model saved in HDF5 format.
- `label_encoder_gender.pkl`: Label encoder used for encoding the 'Gender' feature.
- `onehot_encoder_geo.pkl`: One-hot encoder used for encoding the 'Geography' feature.
- `scaler.pkl`: Standard scaler used to normalize the features before feeding them into the model.
- `Churn_Modelling.csv`: The dataset used for training and testing the model.
- `.gitignore`: Specifies files and folders to be ignored by Git, such as model files and logs.
- `LICENSE`: Apache License 2.0 under which this project is licensed.
- `requirements.txt`: A file listing all the Python dependencies required to run the project.

## Project Structure
- `app.py`: Contains the logic to load the trained model and preprocess the input data using the provided encoders and scaler. It then predicts the salary based on the provided features. The script is also set up for deployment with Streamlit.
- `regression_model.h5`: The machine learning model trained on the dataset to predict customer salary.
- `label_encoder_gender.pkl`, `onehot_encoder_geo.pkl`, `scaler.pkl`: Serialized objects for encoding and scaling features to match the format used during model training.
- `Churn_Modelling.csv`: Dataset containing customer information, including features such as Geography, Gender, Age, Tenure, Balance, Number of Products, etc.
- `logs/`: A folder to store regression logs, capturing details about the model's performance during training and testing phases.
- `.gitignore`: Configured to ignore files that should not be tracked by version control, such as environment files, cached files, and serialized model artifacts.
- `LICENSE`: Contains the Apache License 2.0 under which this project is licensed.
- `requirements.txt`: Lists the dependencies required for running the project, including `streamlit`, `tensorflow`, `pandas`, and others.

## Installation
To run this project locally, follow these steps:

1. **Clone the repository:**  
   `git clone https://github.com/yourusername/churn-prediction.git`  
   `cd churn-prediction`

2. **Create a virtual environment and activate it:**  
   `python -m venv venv`  
   `source venv/bin/activate`  *(On Windows use `venv\Scripts\activate`)*

3. **Install the required dependencies:**  
   `pip install -r requirements.txt`

## Usage

### Running the Streamlit App
You can run the Streamlit app to interact with the model:

`streamlit run app.py`

### Model Training and Evaluation
You can explore the model training and evaluation process using the Jupyter notebooks provided:

- **notebook.ipynb:** Contains exploratory data analysis and the model training process.
- **prediction.ipynb:** Contains the code for making predictions using the trained model.

## Model Details
The model is a deep learning neural network built using TensorFlow/Keras. It includes the following steps:

- **Data Preprocessing:** Scaling, encoding categorical variables, and handling missing values.
- **Model Architecture:** A neural network with multiple layers, designed to predict churn.
- **Evaluation:** The model is evaluated using various metrics like accuracy, precision, recall, and F1-score.

## Deployment on Streamlit Cloud
You can easily deploy this project to Streamlit Cloud by following these steps:

1. **Fork the repository** *(if you haven't already):*  
   Go to the GitHub repository and click on the "Fork" button to create a copy of the repository in your GitHub account.

2. **Deploy to Streamlit Cloud:**  
   Sign in to [Streamlit Cloud](https://streamlit.io/cloud) with your GitHub account.  
   Click on "New app" and choose the repository and branch you want to deploy.  
   Specify the `app.py` as the entry point for the app.  
   Click "Deploy."

3. **Environment Variables (if required):**  
   If your app requires any environment variables, you can set them in the Streamlit Cloud settings under the "Advanced Settings" tab.

4. **Access your deployed app:**  
   Once deployed, Streamlit will provide you with a URL where your app is live and accessible to others.

## License
This project is licensed under the Apache License 2.0 - see the `LICENSE` file for details.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## Acknowledgments
This project was developed as part of a data science project. Special thanks to the udemy course instructor and the open-source community for the tools and libraries used in this project.
