# PCOS Predictor

## About The Project
Polycystic Ovary Syndrome (PCOS)--recently renamed Polyendocrine Metabolic Ovarian Syndrome (PMOS)--is a hormonal disorder that causes a range of health symptoms, from hormonal fluctuations to abnormal hair growth. There is no single test to determine if patients have PCOS. This project explores a clinical dataset to determine which reproductive and comprehensive health features are most correlated with PCOS, and with that information, designs and evaluates machine learning models to classify whether a patient has PCOS based on the features analyzed.

## Project Goals
- Identify which reproductive and comprehensive health features are best to identify if a woman has PCOS
- Visualize and analyze the data to explore patterns and correlations between PCOS and focus features
- Compare different machine learning models to determine the most accurate classifier


## Dataset
- Dataset: [Polycystic ovary syndrome (PCOS)](https://www.kaggle.com/datasets/prasoonkottarathil/polycystic-ovary-syndrome-pcos) dataset sourced from Kaggle
- Size: 540 entries, 40 columns after cleaning
- Key features: Follicle count (left/right), LH (luteinizing hormone), AMH (Anti-Müllerian hormone), FSH (follicle-stimulating hormone), TSH (thyroid-stimulating hormone), cycle length, endometrium (mm), weight gain, hair growth, skin darkening
- Target variable: PCOS (1 = diagnosed with PCOS, 0 = not diagnosed)

## Methodology
<b>Data Cleaning</b>
- Dropped blank/unnecessary columns
- Removed empty entries
- Standardized labels to camelCase_units for continuity
- Fixed incorrect cells (incorrect decimal place)
- Rounded off values

<b>Feature Engineering</b>
- Derived new features (BMI, FSH/LH, waistHipRatio)
- Created a new dataset to use for the machine learning models that only included patients who weren't pregnant
- Added a total follicle count column combining left follicle count + right follicle count

<b>Visualization</b>
- Correlation heat maps for reproductive and comprehensive health factors
- Bar graphs of PCOS feature counts by PCOS Diagnosis for comprehensive health factors (weight gain, hair growth, skin darkening, hair loss, and pimples)
- Scatterplot of left follicle count vs. right follicle count
- Boxplot FSH/LH by PCOS diagnosis and luteinizing hormone by PCOS diagnosis

<b>Modeling</b>
- Tested both a Decision Tree model and K-Nearest Neighbors (KNN) Model
- Used a grid search to determine 6 neighbors as the optimal K for KNN 
- Visualized the ROC curve and confusion matrix for model evaluation

## Key Insights
- Increased follicle count positively correlates with a PCOS diagnosis, and combining left/right follicle counts preserves this finding
- KNN outperformed the Decision Tree model, which suggests that proximity-based patterns best capture the relationship between features and diagnosis
- Weight gain, hair growth, and skin darkening were all comprehensive features reported by a greater percentage of patients with PCOS than without. When added as focus features in the model, the model increased in accuracy

## Limitations
- The dataset didn't include androgens, which is one of the three criteria needed to determine if a patient has PCOS

## Tech Stack
- Python
- Pandas
- Numpy
- Seaborn
- MatPlotLib
- Scikit-Learn

## Project Structure
```text
pcos-analysis-python/
├── PCOS_Project.ipynb
└── README.md
```
## Author
<b>Kate Passwater</b>
<ul>
  <li>GitHub: <a href="https://github.com/katepass">@katepass</a></li>
  <li>LinkedIn: <a href="https://linkedin.com/in/katepasswater">in/katepasswater</a></li>
</ul>


  

  




