SymptoPredict – AI Symptom to Disease Predictor
SymptoPredict is an AI-based chatbot designed to predict diseases based on user-entered symptoms. Built using Flask, this project leverages machine learning techniques, particularly Support Vector Machines (SVM), to provide accurate disease predictions. The system parses the user's symptom descriptions using NLP techniques and provides a comprehensive diagnosis, including preventive measures, medications, diets, and workouts.

Technologies Used:
Python
Flask
Scikit-learn (SVM)
Pandas
NLP
HTML/CSS for Web Interface
Google Colab for Model Training

Features:
Symptom-Based Prediction: Users can input a list of symptoms, and the system predicts the most likely disease.
Disease Description: Provides a detailed description of the predicted disease.
Precautions: Suggests preventive measures for the identified disease.
Medications: Recommends medications based on the disease.
Diet Suggestions: Provides diet recommendations to aid recovery.
Workout Suggestions: Suggests appropriate workouts for disease management (if applicable).

Installation:
1. Clone this repository:
bash
Copy
Edit
git clone https://github.com/Rohith1234-sarikela/MediBOT.git
cd SymptoPredict
2. Install Dependencies:
Make sure you have Python 3.8 or higher installed. Then, install the required dependencies:
bash
Copy
Edit
pip install -r requirements.txt

3. Download Model and Dataset Files:
Ensure you have the following files in the datasets/ and models/ directories:
datasets/symtoms_df.csv
datasets/description.csv
datasets/medications.csv
datasets/diets.csv
datasets/precautions_df.csv
datasets/workout_df.csv
models/svc.pkl (Trained SVM model)

4. Run the Application:
Start the Flask app:
bash
Copy
Edit
python app.py
Visit the application at http://127.0.0.1:5000/ in your browser.

How it Works:
User Input:
The user enters their symptoms into a text field, separated by commas. For example: "fever, cough, headache".
Symptom Parsing:
The application processes the user input and splits it into individual symptoms.
The symptoms are then matched with a predefined list of known symptoms stored in the system.
Feature Vector Creation:
Each symptom is converted into a binary feature vector, where each feature corresponds to the presence or absence of a specific symptom from the predefined list.
Disease Prediction:
The feature vector is passed to a pre-trained Support Vector Machine (SVM) model, which has been trained on a dataset of diseases and their associated symptoms.
The model outputs the predicted disease based on the user's symptoms.
Disease Information:
After predicting the disease, the system retrieves additional information about the disease, including:
Description: An explanation of the disease.
Precautions: A list of preventive measures for the disease.
Medications: Suggested medications for treatment.
Diet: Diet recommendations to help manage or recover from the disease.
Workouts: Suggested workouts (if applicable) for maintaining health during recovery.
Output Display:The predicted disease, along with the relevant information, is displayed to the user on the web interface.

Contributing:
Feel free to fork the repository, raise issues, and create pull requests.

License:
This project is licensed under the MIT License.

Contact:
If you have any questions or feedback, feel free to reach out.

