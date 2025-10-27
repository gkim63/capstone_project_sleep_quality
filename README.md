# capstone_project_sleep_quality
Analysis of the Impact of Occupational and Lifestyle Factors on Sleep Quality

This project analyzes the impact of occupational and lifestyle factors on sleep quality using the **Sleep_Disorder_Diagnosis_Dataset** from Kaggle.

## Dataset
- Source: [Kaggle - Sleep Disorder Diagnosis Dataset](https://www.kaggle.com/datasets/varishabatool/disorder)  
- Format: CSV  
- Contents: Occupation, sleep duration, sleep quality, physical activity, stress level  
- Notes: No personally identifiable information included.  

## Data Processing
1. **Data Extraction**
   - Loaded the CSV file into a Jupyter Notebook using Pandas.
2. **Data Preparation**
   - Selected relevant variables: occupation, sleep duration, sleep quality, physical activity, and stress level.
   - Removed occupations with fewer than 10 samples.
   - Removed outliers in sleep quality using the IQR method.
   - No missing values in key variables; no further cleaning required.

## Tools Used
- **Pandas**: Data cleansing and processing
- **Jupyter Notebook / VS Code**: Analysis and visualization
- **Matplotlib / Seaborn**: Visualizations
- **Scikit-learn**: Regression modeling

## Data Analysis Results

### Statistical Significance

| Hypothesis | Test | Metrics | Conclusion |
|------------|------|---------|------------|
| **A: Sleep quality differs by occupation** | One-way ANOVA | F = 41.65, p = 0.00 | Reject null hypothesis. Nurses and salespeople had the lowest median sleep quality (6), engineers, lawyers, and accountants the highest (8-9). |
| **B: Stress has the strongest correlation** | Pearson Correlation | Stress r = -0.91, Physical Activity r = 0.15, Sleep Duration r = 0.88 | Stress has the strongest absolute correlation; reject null hypothesis. |
| **C: Predictive model sufficiency** | Multiple Linear Regression | R² = 0.8856, MSE = 0.1470 | Model shows high predictive accuracy; reject null hypothesis. |

### Practical Significance
- Sleep quality varies by occupation; work-related stress can negatively impact sleep.
- Stress has the strongest negative correlation with sleep quality; managing stress can significantly improve sleep.
- Predictive model is accurate; lifestyle factors can be used to forecast sleep quality and recommend improvements.

### Visualizations for Storytelling
- **Box Plot:** Compared distribution of sleep quality by occupation.
- **Scatter Plot with Jitter:** Showed relationships between stress, sleep duration, physical activity, and sleep quality.
- Visualizations helped identify key factors and support conclusions.

## Recommended Actions
1. **Implement Stress Management Programs**
   - Tailored programs for high-stress occupations (e.g., nurses, salespeople) such as yoga, counseling, or relaxation techniques.
2. **Sleep Education and Health Campaigns**
   - Promote healthy sleep habits for occupations with shorter sleep duration or low physical activity.
   - Expected outcomes: improved employee productivity, mental health, and organizational efficiency.

## Conclusion
- Sleep quality significantly differs across occupations.
- Stress is the most influential factor negatively impacting sleep quality.
- Multiple linear regression predicted sleep quality with ~88.5% accuracy.
- Results provide actionable insights for occupation-specific wellness and stress management programs.

## Installation & Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/gkim63/capstone_project_sleep_quality.git
2. Open in VS Code
  - Open the project folder in Visual Studio Code.
  - Open the analysis.ipynb file to explore and run the analysis.
  - Make sure your Python interpreter is properly set.
3. Install dependencies
  - Run the following command in the terminal to install required libraries:
    ```bash
    pip install -r requirements.txt
4. Run the notebook
   - Use VS Code’s Jupyter extension to run cells interactively, or Launch Jupyter Lab from the terminal:
     '''bash
     jupyter lab


