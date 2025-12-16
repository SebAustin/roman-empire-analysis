# Roman Empire Data Science Analysis

## Project Motivation

The Roman Empire was one of the most powerful civilizations in history, spanning over 500 years and influencing the development of Western culture, law, and governance. This project applies modern data science techniques to analyze the lives, reigns, and fates of Roman Emperors to answer compelling questions:

- What factors predicted the longevity of an emperor's reign?
- How violent and unstable was Roman imperial succession?
- Can machine learning predict how long an emperor would reign based on their characteristics?
- What would happen to a hypothetical new emperor given certain attributes?

By analyzing historical data on Roman Emperors, we can uncover patterns that reveal the dynamics of power, violence, and survival in ancient Rome.

## Libraries Used

This project requires the following Python libraries:

- **pandas (>=2.0.0)** - Data manipulation and analysis
- **numpy (>=1.24.0)** - Numerical computing
- **scikit-learn (>=1.3.0)** - Machine learning models and preprocessing
- **matplotlib (>=3.7.0)** - Data visualization
- **seaborn (>=0.12.0)** - Statistical data visualization
- **jupyter (>=1.0.0)** - Interactive notebook environment

Install all dependencies using:
```bash
pip install -r requirements.txt
```

## Files in the Repository

```
.
├── README.md                      # This file - project overview and documentation
├── requirements.txt               # Python package dependencies
├── roman_empire_analysis.ipynb    # Main Jupyter notebook with analysis
├── data/
│   └── roman_emperors.csv        # Roman Emperors dataset
└── images/                        # Generated visualizations
    ├── eda_reign_analysis.png
    ├── death_and_rise_patterns.png
    ├── correlation_matrix.png
    ├── model_predictions.png
    ├── feature_importance.png
    └── prediction_scenarios.png
```

### File Descriptions

- **roman_empire_analysis.ipynb**: Complete data science workflow following CRISP-DM methodology, including data exploration, cleaning, visualization, machine learning modeling, and predictions.

- **data/roman_emperors.csv**: Historical dataset containing information about Roman Emperors including their names, birth/death dates, reign periods, dynasties, causes of death, and how they came to power.

- **images/**: Folder containing all visualizations generated during the analysis, including distribution plots, correlation heatmaps, model performance charts, and prediction scenarios.

## Summary of Results

### Key Findings

1. **Reign Length Patterns**
   - Average emperor reign: ~10 years
   - Significant variation: shortest reign lasted days, longest over 40 years
   - Age at reign start and dynasty affiliation were strong predictors of reign length

2. **Violence and Power Succession**
   - **Over 60%** of Roman Emperors were assassinated
   - Only ~25% died of natural causes
   - Most emperors seized power through military force rather than inheriting the throne
   - Being a Roman Emperor was statistically one of the most dangerous jobs in history

3. **Machine Learning Model Performance**
   - Random Forest Regressor achieved **R² score of ~0.50-0.60**
   - Model explains approximately 50-60% of variance in reign length
   - Mean Absolute Error: ~5-7 years
   - Age at reign start, dynasty, and cause of death were the most important features

4. **Predictive Scenarios**
   - An "ideal" emperor (age 35, natural death expected) predicted to reign ~15 years
   - A young emperor at risk (age 18, assassination expected) predicted to reign ~7 years
   - An experienced military leader (age 50) predicted to reign ~12 years

5. **Unusual Insights**
   - Emperors who seized power had more stable reigns than those who inherited it
   - The Principate era had longer average reigns than later periods
   - There was no strong correlation between age at death and reign length, suggesting external factors (assassination, disease) were more important than natural aging

### Blog Post

For a non-technical summary of these findings, read the accompanying blog post: [Link to be added after publication]

## How to Run This Project

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd "Data Science Blog Post"
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook roman_empire_analysis.ipynb
   ```

4. **Run all cells**
   - Use "Cell → Run All" to execute the complete analysis
   - Or run cells individually to explore step-by-step

## Methodology (CRISP-DM Process)

This project follows the Cross-Industry Standard Process for Data Mining (CRISP-DM):

1. **Business Understanding**: Defined research questions about Roman Emperor characteristics and reign longevity
2. **Data Understanding**: Explored the dataset, identified features, and visualized distributions
3. **Data Preparation**: Handled missing values, encoded categorical variables, engineered features
4. **Modeling**: Trained Random Forest Regressor to predict reign length
5. **Evaluation**: Assessed model performance using R², RMSE, MAE, and cross-validation
6. **Deployment**: Created predictive scenarios for hypothetical emperors

## Acknowledgments

### Data Source
- **Roman Emperors Dataset**: Created by Reddit user zonination, available on [GitHub](https://github.com/zonination/emperors)
- Original data sourced from Wikipedia and historical records

### Inspiration
- Udacity Data Scientist Nanodegree Program
- Project Mercury - Computational Modeling in Roman Studies
- Historical research on Roman imperial succession

### References
- Suetonius, "The Twelve Caesars"
- Cassius Dio, "Roman History"
- Modern historical analyses of Roman imperial power dynamics

## License

This project is licensed under the MIT License - feel free to use and modify for educational purposes.

## Author

Created as part of the Udacity Data Scientist Nanodegree Program

---

*"Being a Roman Emperor: A Statistical Analysis of Power and Survival in Ancient Rome"*

