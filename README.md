# AI in Software Development: StackOverflow 2024 Developer Survey Analysis

This project analyzes the 2024 StackOverflow Developer Survey to understand AI tool adoption patterns among developers. The analysis follows the CRISP-DM methodology and includes machine learning models, SHAP interpretability analysis, and Aequitas bias/fairness auditing.

## Blog Post

The Medium blog post accompanying this repo can be found [here](https://medium.com/@andaluri/the-ai-revolution-in-software-development-what-65-000-developers-reveal-about-the-future-of-coding-41aa8e0a433f
).

## Project Summary

- **Dataset**: 2024 StackOverflow Developer Survey (65,437 respondents, 114 features)
- **Key Finding**: 61.8% of developers now use AI tools in their workflow
- **Models**: Random Forest Classifier (AI adoption) and Regressor (salary prediction)
- **Interpretability**: SHAP (Shapley) values for feature importance
- **Fairness**: Aequitas bias analysis across demographic groups

## 1. Cloning the Repository

```bash
git clone https://github.com/<username>/udacity-datascience-project-blog.git
cd udacity-datascience-project-blog
```

## 2. Install `uv` (Recommended Package Manager)

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Or using pip
pip install uv
```

## 3. Prerequisites

- Python 3.9+
- Jupyter Notebook or JupyterLab

## 4. Create Virtual Environment

```bash
uv venv
source .venv/bin/activate  # Linux/macOS
# or
.venv\Scripts\activate     # Windows
```

## 5. Install Dependencies

```bash
uv pip install -r requirements.txt
```

Or using pip directly:
```bash
pip install -r requirements.txt
```

## 6. Decompress Data

```bash
gunzip -k data/survey_results_public.csv.gz
```

## 7. Run the Notebook

```bash
jupyter notebook developer_survey_analysis.ipynb
```

Or with JupyterLab:
```bash
jupyter lab developer_survey_analysis.ipynb
```

## 8. Project Structure

```
udacity-datascience-project-blog/
├── data/
│   └── survey_results_public.csv.gz    # Compressed survey data
├── figures/                             # Generated visualizations
│   ├── ai_adoption.png
│   ├── ai_adoption_predictors.png
│   ├── ai_adopter_comparison.png
│   ├── ai_sentiment.png
│   ├── aequitas_bias_experience.png
│   ├── jobsat_comparison.png
│   ├── language_ai_adoption.png
│   ├── missing_values.png
│   ├── salary_by_ai_adoption.png
│   ├── salary_distribution.png
│   ├── salary_predictors.png
│   ├── shap_beeswarm_classification.png
│   ├── shap_importance_classification.png
│   ├── shap_importance_salary.png
│   └── shap_vs_rf_importance.png
├── developer_survey_analysis.ipynb      # Main analysis notebook
├── requirements.txt                     # Python dependencies
├── .gitignore
└── README.md
```

## 9. Business Questions Answered

1. **What factors predict whether a developer uses AI tools?**
   - Years of experience is the strongest predictor (32.7%)
   - TypeScript usage correlates with higher adoption (10.8%)

2. **How does AI usage correlate with job satisfaction?**
   - No significant difference between AI adopters and non-adopters

3. **Which programming languages have highest AI adoption?**
   - TypeScript: 69.4%
   - JavaScript: 65.4%
   - Python: 64.1%

4. **What predicts developer compensation?**
   - Years of experience dominates salary prediction
   - AI adoption is not a significant salary predictor

5. **Key differences between AI adopters vs non-adopters?**
   - Adopters: Median 6 years experience
   - Non-adopters: Median 10 years experience

## 10. Model Performance

| Model | Task | Metric | Value |
|-------|------|--------|-------|
| Random Forest Classifier | AI Adoption Prediction | Accuracy | 64.0% |
| Random Forest Classifier | AI Adoption Prediction | Cross-Val | 64.1% |
| Random Forest Regressor | Salary Prediction | R² | 0.11 |
| Random Forest Regressor | Salary Prediction | MAE | $44,580 |

## 11. Requirements

```
aequitas==1.1.0
jupyter==1.1.1
matplotlib==3.10.8
notebook==7.6.0
numpy==2.4.0
pandas==2.3.3
scikit-learn==1.9.0
seaborn==0.13.2
shap==0.52.0
```

## 12. Data Source

[2024 StackOverflow Developer Survey](https://survey.stackoverflow.co/2024/)

License: Open Database License (ODbL)

## 13. Acknowledgments

- StackOverflow for the annual developer survey
- Udacity Data Science Nanodegree program
