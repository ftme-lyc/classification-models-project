# Student Performance Classification Project

This project aims to develop a machine learning model that predicts student performance categories (Excellent, Good, Average, Poor) using academic, behavioral, and demographic data. The goal is to help educators identify students at risk of academic underperformance and enable timely interventions.

## Business Use Cases  
- **Student Support Officers:** Identify at-risk students early and provide targeted support.  
- **Academic Advisors:** Guide students with personalized interventions based on predictions.  
- **University Staff:** Enhance strategies to improve overall student success.

## Key Objectives  
- Build reliable classification models to predict semester-end student performance.  
- Identify and analyze key features influencing performance (e.g., GPA, attendance, study hours).  
- Achieve interpretable models with F1-score and Recall above 80%.  
- Provide actionable insights aligned with stakeholder needs.

## Dataset  
- Contains 1,009 student records with 45 features related to academic, behavioral, and demographic aspects.  
- Data cleaning included correcting errors, handling missing values, and feature engineering such as GPA change and study efficiency.  
- Addressed imbalanced classes using SMOTE for improved minority class prediction.

## Modeling Approach  
- Evaluated multiple classification algorithms:  
  - Support Vector Classifier (SVC)  
  - Decision Tree Classifier  
  - Extra Trees Classifier  
- Conducted extensive hyperparameter tuning using grid search for all models.  
- Applied feature engineering and label encoding to reduce dimensionality and improve performance.

## Evaluation Results  
| Model           | F1 Score (Test) | Recall (Test) | Notes                                   |
|-----------------|-----------------|---------------|-----------------------------------------|
| Dummy Classifier | 0.36            | 0.37          | Baseline model                          |
| SVC             | 0.72            | 0.72          | Reasonable performance but limited      |
| Decision Tree   | 0.94            | 0.94          | High performance but possible overfitting |
| Extra Trees     | **0.82**        | **0.81**      | Best balanced model; meets project goals|

- Extra Trees demonstrated strong generalization and balanced performance.  
- Key predictive features include GPA, attendance, and study hours.  
- Misclassifications mainly occurred between adjacent performance categories, reducing the negative impact.

## Conclusion  
- The Extra Trees model is the most effective and interpretable, providing reliable early detection of at-risk students.  
- The project successfully addresses stakeholder requirements and achieves the desired performance metrics.  
- Limitations include a relatively narrow dataset and potential generalization issues; broader and more recent data are recommended for future work.  
- Future improvements may involve expanding the dataset, testing across academic terms, and exploring additional ensemble methods.

## License
This project is for educational and research purposes.

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ftme-lyc/classification-models-project.git
   cd classification-models-project
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Upload the dataset:

   Place students_performance.csv in the same directory as the notebooks, or upload them to your Drive if using Colab.
5. Run the notebooks:

   Open the following files in Jupyter Notebook or VS Code:
   - 36106_25au_at2_25589351_experiment_0.py
   - 36106_25au_at2_25589351_experiment_1.py
   - 36106_25au_at2_25589351_experiment_2.py
   - 36106_25au_at2_25589351_experiment_3.py
   - 36106_25au_at2_25589351_experiment_4.py

