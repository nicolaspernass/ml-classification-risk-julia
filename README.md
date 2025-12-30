# Machine Learning Classification Under Risk (Julia)

## Project Overview
End-to-end machine learning classification project focused on decision-making under asymmetric risk.
The objective was to compare multiple supervised learning models and select suitable approaches by prioritizing the reduction of high-cost classification errors rather than relying solely on overall accuracy.

## Dataset
- Real-world binary classification dataset (UCI Sonar)
- Task: distinguish between two classes based on numerical signal features
- Error costs are asymmetric:
  - False negatives are more critical than false positives
- Dataset characteristics influenced model selection and evaluation metrics

## Methodology

### Data Exploration & Preprocessing
- Exploratory analysis to understand feature distributions and class behavior
- Normalization using Min-Max scaling
- Consistent preprocessing applied across all models for fair comparison

### Model Training
All models were implemented and evaluated using Julia:

- Neural Networks
- Support Vector Machines (SVM)
- k-Nearest Neighbors (kNN)
- Decision Trees
- DoME (custom symbolic learning algorithm)

Hyperparameters were adjusted to analyze performance trade-offs.

### Evaluation Strategy
Models were evaluated using:
- F1-score
- Sensitivity (Recall)

These metrics were prioritized due to the asymmetric cost of errors, where missing critical cases is more severe than false alarms.

Cross-validation was used to ensure robustness and reduce overfitting.

## Model Selection
Several models achieved similar performance.
Final selection prioritized:
- Sensitivity to high-cost errors
- Stability across validation folds
- Balanced trade-offs between performance and risk

The project emphasizes metric-driven decision-making aligned with real-world constraints.

## Results
- Comparable F1-scores across multiple models
- Models prioritizing sensitivity were favored
- Explicit analysis of trade-offs between complexity, interpretability, and performance

## Tools
- Julia
- Machine Learning libraries
- Statistical evaluation and visualization tools

## Key Takeaways
- Model selection should reflect operational or business risk
- Accuracy alone is insufficient when error costs are asymmetric
- Comparing diverse models improves decision quality

## Notes
This project was developed as part of an academic machine learning course and is presented as an example of applied ML reasoning and decision-oriented evaluation.
