# Pokémon Mega Evolution Prediction

**Group 7**: Bradley Stoller, Samuel Martinez Koss, Xigang Zhang, and Zhiwei Guo

**Machine Learning Operations Final Project** | December 2025

## Project Overview

This project applies machine learning operations to predict whether a Pokémon has a Mega Evolution form based on its stats and characteristics. Using a dataset of 721 Pokémon from Generations 1-6, we built a binary classification ML pipeline incorporating AWS AutoML, MLflow experimentation, AWS deployment, and Evidently AI model monitoring.

**Key Highlights:**
- AWS AutoML: 97% accuracy with XGBoost/Gradient Boosting
- MLflow optimized model: 88% training accuracy  
- Successful drift detection with Evidently AI monitoring

## Repository Organization

- **`eda.ipynb`** - Exploratory Data Analysis including feature distributions, class imbalance analysis, and type-based statistics
- **`modeling.ipynb`** - Steps 1-9 of the final project assignment including:
  - Train/Test Splitting (SMOTE for class balancing)
  - AWS AutoML experimentation
  - MLflow hyperparameter tuning (10 models via random search)
  - AWS inference deployment
  - Evidently AI drift monitoring setup 
  - Model monitoring validation with changed test data
- **`presentation.pdf`** - Presentation slides (PDF)
- **`presentation.pptx`** - Presentation slides (includes demo video)

## Technical Approach

**Pipeline:** Raw Data -> SMOTE -> AWS AutoML -> MLflow Optimization -> AWS Deployment -> Evidently AI Monitoring

**Evaluation Metric:** Accuracy (balanced dataset post-SMOTE, equal cost for false positives/negatives)

**Model Monitoring:** Implemented data and prediction drift detection using Evidently AI integrated with AWS SageMaker and S3 for record archiving

## Results

The deployed gradient boosting model successfully detected drift when test data was intentionally modified (swapping and randomizing features), with accuracy dropping from 88% to 74%, which confirms the effectiveness of our monitoring approach.

## Team Contributions

This project was a collaborative effort with clearly defined responsibilities:

### Bradley Stoller
- AWS SageMaker model deployment
- Evidently AI model monitoring implementation
- S3 integration for record archiving
- Model inference endpoint setup

### Samuel Martinez Koss
- SMOTE implementation for class balancing
- Data preprocessing and feature engineering
- Train/test splitting strategy
- MLflow experimentation and hyperparameter tuning (10 model configurations via random search)

### Zhiwei Guo
- Exploratory Data Analysis (EDA)
- Statistical analysis (ANOVA, Tukey's HSD, effect size calculations)
- Data visualization and insights generation
- Presentation development

### Xigang Zhang
- Dataset research and sourcing
- Exploratory Data Analysis (EDA)
- Feature analysis and documentation
- Presentation development


