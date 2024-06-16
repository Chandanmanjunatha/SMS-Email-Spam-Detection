Here's the README file for the SMS/Email Spam Detection project. This file provides a detailed overview of the project, including instructions on setting up the environment, running the application, and understanding the components of the project.

---

# SMS/Email Spam Detection

This project involves the development of a machine learning model to classify SMS or email messages as spam or not spam. The project includes data preprocessing, model training, and a web application for predicting the nature of the message. The application is built using Streamlit for the user interface.

## Table of Contents
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Data Preprocessing](#data-preprocessing)
- [Model Building and Evaluation](#model-building-and-evaluation)
- [Web Application](#web-application)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
SMS-Email-Spam-Detection/
│
├── app.py                 # Streamlit web application script
├── sms-spam-detection.ipynb  # Jupyter Notebook for data processing and model training
├── vectorizer.pkl         # Pre-trained TF-IDF vectorizer
├── model.pkl              # Pre-trained machine learning model
├── requirements.txt       # List of dependencies
└── README.md              # Project documentation
```

## Installation

To get started with this project, follow the steps below:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repository/sms-email-spam-detection.git
   cd sms-email-spam-detection
   ```

2. **Set up a virtual environment**:
   ```bash
   python -m venv env
   source env/bin/activate   # On Windows use `env\Scripts\activate`
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

   Alternatively, you can manually install the necessary packages listed in the `requirements.txt` file.

4. **Download NLTK data**:
   Open a Python shell and run the following commands to download necessary NLTK datasets:
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   ```

## Usage

### Running the Web Application

1. **Run the Streamlit application**:
   ```bash
   streamlit run app.py
   ```

2. **Open your web browser** and navigate to `http://localhost:8501`. You should see the interface for the Spam Classifier.

3. **Input a message** in the text area and click on the "Predict" button to classify it as "Spam" or "Not Spam".

### Notebook Exploration

To explore the data processing and model training steps, open the Jupyter Notebook:

1. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

2. **Open `sms-spam-detection.ipynb`** and follow the step-by-step analysis and model building process.

## Data Preprocessing

The data preprocessing involves several steps to clean and prepare the data for model training:

1. **Data Cleaning**:
   - Removing unnecessary columns.
   - Handling missing values.
   - Removing duplicates.

2. **Text Processing**:
   - Converting text to lowercase.
   - Tokenization (splitting text into words).
   - Removing non-alphanumeric characters.
   - Removing stop words and punctuation.
   - Stemming (reducing words to their base form).

3. **Feature Engineering**:
   - Adding features such as the number of characters, words, and sentences.

## Model Building and Evaluation

The notebook `sms-spam-detection.ipynb` covers the following:

1. **Vectorization**:
   - Converting text into numerical features using TF-IDF vectorizer.

2. **Model Training**:
   - Training different models including Naive Bayes, SVM, Logistic Regression, and others.

3. **Evaluation**:
   - Evaluating models based on accuracy, precision, and other metrics.
   - Comparing performance of different classifiers.

4. **Model Selection**:
   - Choosing the best performing model for deployment.

## Web Application

The web application is built using Streamlit and allows users to input a message and get a prediction on whether it is spam or not. The application flow includes:

1. **Text Input**: User inputs the message in a text area.
2. **Prediction**:
   - The text is preprocessed using the same steps as during training.
   - The pre-trained TF-IDF vectorizer transforms the text into numerical features.
   - The trained model predicts whether the message is spam.
3. **Display Result**: The prediction result is displayed as "Spam" or "Not Spam".

## Contributing

Contributions are welcome! If you have suggestions or improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to customize this README further to match your specific repository and any additional instructions or information you may want to provide.

## OUTPUT:

![Screenshot (41)](https://github.com/Chandanmanjunatha/SMS-Email-Spam-Detection/assets/97020983/c8e1fc20-cfaf-4ed0-a407-507a620763af)
