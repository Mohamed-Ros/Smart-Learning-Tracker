# Smart Learning Tracker 🎓📈

## Overview
**Smart Learning Tracker** is a comprehensive, machine learning-powered educational analytics system. It is designed to track student progress throughout their courses, analyze their performance on quizzes and lectures, identify common mistake types, and provide actionable recommendations for the "next step" in their learning journey.

Whether determining if a student is ready for the next lecture or if they need to review specific topics, this system leverages data-driven insights to personalize and enhance the educational experience.

## ✨ Features
- **Data Generation & Preprocessing**: Robust Jupyter notebooks to generate synthetic student performance data and preprocess it for machine learning pipelines.
- **Predictive Machine Learning Models**:
  - `predict_next_action`: Recommends the optimal next learning step (e.g., *Proceed to Next Lecture*, *Review Material*, *Take Practice Quiz*) based on the student's score, time spent, and specific mistakes made.
  - `lesson_evaluation`: Evaluates the overall difficulty and effectiveness of various lessons/modules.
  - `next_step_engine`: A customized recommendation engine mapping performance to personalized learning paths.
- **Rich Data Visualizations**: Generates detailed, shareable insights into average quiz scores, mistake distributions, and student performance levels across different educational stages.
- **End-to-End ML Pipeline**: Covers the entire lifecycle from raw data generation to feature engineering, model training, persistence (saving models), and inference.

## 📂 Project Structure
```text
Smart Learning Tracker/
├── data/
│   ├── raw/                      # Generated raw datasets (CSVs)
│   └── processed/                # Preprocessed data ready for model training
├── models/
│   ├── saved_models/             # Serialized ML models (joblib)
│   ├── train_ml_pipeline.ipynb   # End-to-end ML model training pipeline
│   ├── predict_next_action.ipynb # Model inference for next action prediction
│   ├── next_step_engine.ipynb    # Logic for recommending learning next steps
│   └── lesson_evaluation.ipynb   # Analytics model for lesson effectiveness
├── scripts/
│   ├── generate_raw_data.ipynb   # Synthetic student data generation notebook
│   ├── preprocess_data.ipynb     # Data cleaning, encoding, and feature engineering
│   └── visualizations.ipynb      # Code to generate and export performance charts
├── visualizations/               # Output charts and graphs (PNGs)
│   ├── Average Quiz Score per Stage.png
│   ├── Mistake Types Distribution per Stage.png
│   ├── Student Performance Levels per Stage (Lecture).png
│   └── Detailed Analysis for Stage Lecture 1-5.png
└── requirements.txt              # Standard Python dependencies
```

## 🚀 Setup & Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Mohamed-Ros/Smart-Learning-Tracker.git
   cd smart-learning-tracker
   ```

2. **Create a virtual environment (Recommended):**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Usage Guide

1. **Step 1: Data Generation & Preprocessing**
   - Navigate to the `scripts/` directory.
   - Run `generate_raw_data.ipynb` to create your initial dataset in `data/raw/`.
   - Run `preprocess_data.ipynb` to clean and format the data, saving the results to `data/processed/`.

2. **Step 2: Model Training**
   - Navigate to the `models/` directory.
   - Execute `train_ml_pipeline.ipynb` to train the classification models (e.g., Random Forest or Logistic Regression). 
   - The trained models and scalers will be automatically exported to the `models/saved_models/` folder.

3. **Step 3: Analytics & Predictions**
   - Use `predict_next_action.ipynb` or `next_step_engine.ipynb` to test live predictions on individual student records.
   - Simply load the saved model and input new test data to see the recommended academic actions.

4. **Step 4: Generate Visualizations**
   - Open and run `scripts/visualizations.ipynb` to parse the processed data and generate graphical insights. 
   - All plots will be saved as high-quality PNG images in the `visualizations/` folder.

## 🛠️ Technologies Used
- **Python 3** 🐍
- **Pandas & NumPy** (Data Manipulation and Aggregation)
- **Scikit-Learn** (Building and Evaluating Machine Learning Models)
- **Jupyter Notebook** (Interactive Development and Prototyping)
- **Joblib** (Efficient Model Serialization)
- **Matplotlib & Seaborn** (Static and Statistical Data Visualizations)

## 🤝 Contributing
Contributions, issues, and feature requests are welcome!
## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
