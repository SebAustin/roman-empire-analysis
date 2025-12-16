#Blog : https://medium.com/@henry.sebastien1982usa/the-most-dangerous-job-in-history-what-data-science-reveals-about-roman-emperors-0481d4f68481
#Github : https://github.com/SebAustin/roman-empire-analysis

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

This section answers five key research questions about Roman Emperors, following a structured approach with hypothesis, results, visual evidence, and conclusions.

### Question 1: What Factors Influenced Emperor Reign Length?

**Hypothesis**: Age at ascension and dynasty would significantly impact reign duration.

**Results**:
- Average reign length: **7.62 years** (median: 3.81 years)
- Longest reign: 30.83 years
- Age at reign start showed positive correlation with reign length
- Dynasty affiliation showed significant variation in stability

**Visual Evidence**:  
See `images/eda_reign_analysis.png` - Four-panel analysis showing distributions, dynasty comparisons, death causes, and age relationships

**Conclusion**: ✅ **Hypothesis Confirmed**. Both age and dynasty were strong predictors of reign length. Emperors in their 30s-50s reigned longer than young heirs.

---

### Question 2: What Were the Patterns of Power and Violence?

**Hypothesis**: Expected high rates of violence in succession (>50% assassinated).

**Results**:
- **36.8%** of emperors were assassinated
- Only **30.9%** died of natural causes
- Most emperors seized power through military force
- Median reign: just 3.81 years

**Visual Evidence**:  
See `images/death_and_rise_patterns.png` - Pie chart (death causes) and bar chart (rise to power methods)

**Conclusion**: ✅ **Hypothesis Supported**. While not 60%+, violence was endemic. Being a Roman Emperor was extraordinarily dangerous.

---

### Question 3: What Relationships Exist Between Emperor Characteristics?

**Hypothesis**: Expected correlations between age, reign length, dynasty, and survival.

**Results**:
- Age at reign start correlates with reign length
- Dynasty and era significantly influence outcomes
- **Surprising**: Military leaders who seized power had MORE stable reigns than heirs

**Visual Evidence**:  
See `images/correlation_matrix.png` - Heatmap showing relationships between age, death, and reign variables

**Conclusion**: ✅ **Hypothesis Confirmed with Surprises**. Complex interrelationships exist, but the power paradox was unexpected.

---

### Question 4: How Accurate Is the Predictive Model?

**Hypothesis**: Machine learning could predict reign length with reasonable accuracy (R² > 0.5).

**Results**:
- Model: Random Forest Regressor
- R² Score: **-0.39** (negative indicates poor predictive power)
- Mean Absolute Error: **6.45 years**
- Despite clear patterns, individual outcomes remained unpredictable

**Visual Evidence**:  
See `images/model_predictions.png` - Scatter plots of predicted vs actual values  
See `images/feature_importance.png` - Bar chart of feature significance

**Conclusion**: ❌ **Hypothesis Refuted**. Roman politics was inherently chaotic. This finding itself is valuable—it reveals that chance, personal rivalries, and random events played huge roles.

---

### Question 5: What Would Happen in a Predictive Scenario?

**Hypothesis**: Can use model to predict reign lengths for hypothetical emperors.

**Predictive Scenarios**:
- **Ideal emperor** (age 35, natural death expected): ~15.3 years
- **Young heir** (age 18, assassination threats): ~10.2 years
- **Military commander** (age 50): ~11.2 years
- Historical average: 7.6 years

**Visual Evidence**:  
See `images/prediction_scenarios.png` - Bar chart comparing three scenarios with historical average

**Conclusion**: ✅ **Predictions Align with Patterns**. Even under ideal circumstances, predicted reign is modest (15.3 years), demonstrating inherent instability of Roman leadership.

---

### Blog Post

For a non-technical summary of these findings, read the accompanying blog post:  
**Medium**: [Link to be added after publication]  
**GitHub**: `blog_post_medium.md`

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

