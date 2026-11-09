# Student Final Mathematics Grade Prediction Using Linear Regression

A beginner-friendly Python mini-project that predicts students' final Mathematics grades (`G3`, 0-20) using non-grade student characteristics and study-related factors.

## Project design
- Dataset: UCI Student Performance - Mathematics file `student-mat.csv` (395 student records).
- Target: `G3`.
- Algorithm: scikit-learn Linear Regression.
- Predictors: demographic, family, school, lifestyle and study-related features.
- Excluded predictors: `G1` and `G2`, because these are earlier grades and the project deliberately studies prediction without earlier grade inputs.
- Split: 80% training / 20% testing, with `random_state=42`.
- Preprocessing: median imputation for numeric columns; most-frequent imputation and one-hot encoding for categorical columns. Preprocessing is kept inside a pipeline to reduce data leakage.
- Evaluation: R², MAE and RMSE on training and test sets.

## Run in Google Colab
1. Upload `student_grade_prediction.ipynb` to https://colab.research.google.com/.
2. Run all cells from top to bottom.
3. Keep internet access enabled for the first data download.
4. Inspect the charts and the actual evaluation results.

## Run locally
```bash
python -m pip install -r requirements.txt
jupyter notebook
```
Open `student_grade_prediction.ipynb` and run all cells.

## Outputs
The notebook creates: `plots/01_target_distribution.png`, `02_correlation_heatmap.png`, `03_selected_features_vs_grade.png`, `04_actual_vs_predicted.png`, `05_residual_plot.png`, and `06_model_coefficients.png`. It also writes `results/evaluation_metrics.csv`, `model_coefficients.csv`, `test_predictions.csv`, and a serialized model file.

## Important interpretation note
The scores must be taken from an actual notebook run; no performance value is assumed in advance. A coefficient or correlation is an association, not evidence of causation. Model predictions are estimates and must not be used as the sole basis for decisions about individual students.

## Limitations
The data come from two Portuguese schools and should not automatically be generalized to other schools or countries. Linear Regression may not capture nonlinear patterns, and test results can vary with the split. Cross-validation is a possible extension.

## Dataset citation
Cortez, P. (2008). *Student Performance* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5TG7T

Official source: https://archive.ics.uci.edu/dataset/320/student-performance

## Presentation
[View Project PPT](https://github.com/2026aib1074-oss/Student-Grade-Prediction/blob/main/AI%20GROUP%2020%20PPT%20(3)%20(4).pptx)
https://github.com/2026aib1074-oss/Student-Grade-Prediction/blob/main/AI%20GROUP%2020%20PPT%20(3)%20(4)%20(2)%20(1)%20(2).pptx


## Team Roles
| Team Member | Name | Responsibility |
|---|---|---|
| Member 1 | Sajal Choudhary | Setup and execution instructions |
| Member 2 | Rajarshi Ghosh | Presentation (PPT) |
| Member 3 | Madhav Gupta | GitHub Collaboration and Documentation |
| Member 4 | Jaipal Nayak | Project Demonstration Video |
