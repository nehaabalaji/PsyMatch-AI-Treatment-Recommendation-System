# PsyMatch: AI-Powered Treatment Recommendation System for Mental Health

## Overview

This project implements a comprehensive AI-powered system to provide personalized, data-driven treatment recommendations for mental health conditions. The system analyzes treatment effectiveness patterns from real patient data to help clinicians make evidence-based decisions.

## Getting Started with Google Colab

### Step 1: Open the Notebook
1. Go to [Google Colab](https://colab.research.google.com/)
2. Click **File** → **Upload notebook**
3. Upload `PsyMatch_AI_Treatment_Recommendation.ipynb`

### Step 2: Upload Your Data
1. When you run the data loading cell (Phase 2), a file upload dialog will appear
2. Upload your `mental_health_diagnosis_treatment_.xlsx` file
3. The notebook will automatically load and process the data

### Step 3: Run All Cells
- Click **Runtime** → **Run all** to execute the entire notebook
- Or run cells sequentially by clicking the play button on each cell

## Project Structure

The notebook is organized into 12 phases:

1. **Environment Setup**: Install required packages
2. **Data Loading & Exploration**: Load and understand the data
3. **Data Preprocessing**: Feature engineering and data preparation
4. **Treatment Effectiveness Analysis**: Calculate and visualize treatment outcomes
5. **Association Rule Mining**: Discover treatment patterns using Apriori algorithm
6. **Causal Inference**: Estimate treatment effects with propensity score matching
7. **Predictive Modeling**: Build ML models for personalized recommendations
8. **Recommendation System**: Generate treatment recommendations
9. **Interactive Interface**: User-friendly widget-based interface
10. **Advanced Visualizations**: Interactive charts and heatmaps
11. **Clinical Decision Support**: Generate comprehensive reports
12. **Summary & Findings**: Key insights and statistics

## Key Features

### 1. Association Rule Mining
- Discovers frequent, effective treatment patterns
- Identifies rules like: "Diagnosis=MDD, Age=20-30, High_Stress=True → SSRIs + CBT"

### 2. Causal Inference
- Estimates Average Treatment Effects (ATE)
- Controls for confounding variables
- Compares treatment effectiveness rigorously

### 3. Personalized Recommendations
- Predicts outcome probability for each treatment option
- Considers patient demographics, symptoms, and behavioral markers
- Provides top 3 recommendations with confidence scores

### 4. Interactive Interface
- Easy-to-use widgets for entering patient information
- Real-time recommendation generation
- Visual display of results with color-coded confidence levels

### 5. Clinical Decision Support
- Comprehensive reports with:
  - Expected improvement probabilities
  - Evidence from similar patients
  - Key insights and mechanisms
  - Monitoring suggestions
  - Contraindications and warnings

## Usage Example

```python
# Define a patient profile
patient_profile = {
    'diagnosis': 'Major Depressive Disorder',
    'age': 35,
    'gender': 'Female',
    'symptom_severity': 7,
    'mood_score': 4,
    'sleep_quality': 4,
    'physical_activity': 3,
    'stress_level': 8,
    'ai_emotional_state': 'Anxious'
}

# Get recommendations
recommendations = get_treatment_recommendations(patient_profile, top_n=3)

# Generate clinical report
report = generate_clinical_report(patient_profile, recommendations)
print(report)
```

## Data Requirements

Your Excel file should contain the following columns:
- Patient ID
- Age
- Gender
- Diagnosis
- Symptom Severity (1-10)
- Mood Score (1-10)
- Sleep Quality (1-10)
- Physical Activity (hrs/week)
- Medication
- Therapy Type
- Treatment Start Date
- Treatment Duration (weeks)
- Stress Level (1-10)
- Outcome (Improved/No Change/Deteriorated)
- Treatment Progress (1-10)
- AI-Detected Emotional State
- Adherence to Treatment (%)

## Outputs

The system generates:
1. **Treatment Effectiveness Heatmaps**: Visual comparison of medication-therapy combinations
2. **Top Treatment Recommendations**: Ranked list with improvement probabilities
3. **Clinical Reports**: Comprehensive decision support documents
4. **Statistical Insights**: Key findings about treatment effectiveness patterns

## Ethical Considerations

⚠️ **Important Disclaimers:**
- Recommendations are based on retrospective data analysis
- Not a substitute for clinical judgment
- Consider patient preferences, comorbidities, and contraindications
- Sample sizes vary by treatment combination
- Individual patient responses may vary

## Technical Requirements

- Python 3.7+
- Required packages (automatically installed in Colab):
  - pandas, numpy
  - matplotlib, seaborn, plotly
  - scikit-learn
  - mlxtend
  - statsmodels
  - ipywidgets
  - openpyxl

## Support

For questions or issues, please refer to the project guide or check the notebook comments for detailed explanations of each phase.

## License

This project is for educational and research purposes. Please ensure compliance with healthcare data regulations (HIPAA, GDPR, etc.) when using real patient data.

