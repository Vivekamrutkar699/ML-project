# End to End Machine Learning Project

A complete machine learning project featuring data preprocessing, model training, and a Flask web application for predictions.

## Project Overview

This project implements a machine learning pipeline for predicting student performance based on various features including gender, ethnicity, parental education level, lunch type, test preparation course, reading score, and writing score.

**Author:** Vivek Amrutkar  
**Email:** vivekamrutkar2066@gmail.com

---

## 📁 Project Structure

```
ML-project/
├── notebook/                  # Jupyter notebooks for data exploration and analysis
├── src/                       # Source code for the ML pipeline
│   └── pipeline/
│       └── predict_pipeline.py   # Prediction pipeline
├── artifacts/                 # Trained models and preprocessors
├── templates/                 # HTML templates for Flask app
├── app.py                     # Flask application for web interface
├── setup.py                   # Package setup configuration
├── requirement.txt            # Project dependencies
├── README.md                  # Project documentation
└── .gitignore                 # Git ignore rules
```

---

## 🛠️ Installation

### Prerequisites
- Python 3.x
- pip (Python package manager)

### Step 1: Clone the Repository
```bash
git clone https://github.com/Vivekamrutkar699/ML-project.git
cd ML-project
```

### Step 2: Create a Virtual Environment
```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirement.txt
```

### Step 4: Install the Package
```bash
pip install -e .
```

---

## 📦 Dependencies

The project uses the following libraries:

| Library | Purpose |
|---------|---------|
| `pandas` | Data manipulation and analysis |
| `numpy` | Numerical computing |
| `scikit-learn` | Machine learning algorithms |
| `xgboost` | Gradient boosting model |
| `catboost` | Gradient boosting model |
| `matplotlib` | Data visualization |
| `seaborn` | Statistical data visualization |
| `Flask` | Web framework for predictions |
| `dill` | Serialization library |

---

## 📊 Project Workflow

### Step 1: Data Exploration & Analysis
- Explore the dataset using Jupyter notebooks in the `notebook/` directory
- Understand feature distributions and relationships
- Identify outliers and missing values

### Step 2: Data Preprocessing
- Clean and preprocess the data
- Handle missing values
- Encode categorical variables
- Scale numerical features using `StandardScaler`

### Step 3: Model Training
- Train multiple machine learning models (XGBoost, CatBoost, etc.)
- Perform hyperparameter tuning
- Evaluate model performance
- Save the best model and preprocessor in the `artifacts/` directory

### Step 4: Prediction Pipeline
- Create a prediction pipeline using the trained model
- Handle input data transformation
- Use the `CustomData` and `PredictPipeline` classes for predictions

### Step 5: Web Application
- Deploy predictions through a Flask web interface
- Access the prediction form at `/predictdata`
- Get real-time predictions on new data points

---

## 🚀 Usage

### Running the Flask Web Application

```bash
python app.py
```

The application will start on `http://0.0.0.0:5000/`

### Routes

| Route | Method | Purpose |
|-------|--------|---------|
| `/` | GET | Home page |
| `/predictdata` | GET | Display prediction form |
| `/predictdata` | POST | Submit data and get predictions |

### Making Predictions

1. Navigate to `http://localhost:5000/`
2. Click on "Predict Data" or go to `/predictdata`
3. Fill in the form with:
   - Gender
   - Race/Ethnicity
   - Parental Level of Education
   - Lunch Type
   - Test Preparation Course
   - Reading Score
   - Writing Score
4. Submit the form to receive the prediction

---

## 📋 Input Features

- **gender**: Student's gender
- **race_ethnicity**: Race/ethnicity category
- **parental_level_of_education**: Parent's education level
- **lunch**: Type of lunch (standard/free-reduced)
- **test_preparation_course**: Completion status of test prep course
- **reading_score**: Student's reading score
- **writing_score**: Student's writing score

---

## 🔧 Configuration

### Setup Configuration
The `setup.py` file contains package metadata:
- **Name:** ML-Project
- **Version:** 0.0.1
- **Author:** Vivek Amrutkar

To modify project metadata, edit `setup.py` accordingly.

---

## 📈 Model Artifacts

Trained models and preprocessors are stored in the `artifacts/` directory:
- Preprocessed data scalers
- Trained machine learning models
- Model evaluation metrics

---

## 📝 Jupyter Notebooks

The `notebook/` directory contains Jupyter notebooks for:
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model experimentation
- Performance comparison

---

## 🔒 Git Configuration

The `.gitignore` file excludes unnecessary files from version control:
- Virtual environments
- Cache and compiled files
- IDE settings
- Model artifacts (optional)

---

## 🐛 Troubleshooting

### Common Issues

**Issue:** Module not found errors
```bash
# Solution: Reinstall dependencies
pip install -r requirement.txt -r --force-reinstall
```

**Issue:** Port 5000 already in use
```bash
# Solution: Change the port in app.py
# Modify: app.run(host="0.0.0.0", port=5001, debug=True)
```

**Issue:** Flask app crashes on prediction
- Check that all artifacts are present in the `artifacts/` directory
- Verify input data format matches training data

---

## 📚 Additional Resources

- [Flask Documentation](https://flask.palletsprojects.com/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [CatBoost Documentation](https://catboost.ai/)

---

## 📄 License

This project is open source and available for educational purposes.

---

## 👤 Contact

For questions or suggestions, please reach out to:
- **Email:** vivekamrutkar2066@gmail.com
- **GitHub:** [Vivekamrutkar699](https://github.com/Vivekamrutkar699)

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

---

**Last Updated:** May 2026
