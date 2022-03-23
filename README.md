## Drug Classification 

README traduzido para Português/BR [aqui](https://github.com/leticiaplang/drug_classification/blob/main/README_ptBR.md)

### Content & access
* This educational project was designed for classification model construction
* The original dataset can be find at [Kaggle](https://www.kaggle.com/prathamtripathi/drug-classification)
* You can access the original code by:
    - After openning it at GitHub, click on 'open in colab'
    - Make a Raw copy and save it in .ipynb format
    - Open it with https link

### Business problem
One of the biggest pain at healthcare services is the medication and prescription errors. According Rayhan A. and collegue's [article](https://www.ncbi.nlm.nih.gov/books/NBK519065/) the ordering/prescribing errors include 50% of the total medications errors. It's harms not only the patient, familly and professionals, as the company, once it's esteemed an bigger cost of $40 billion each year to look after these patients.
This algorithm is the first step to construct an MVP looking for help at secure medication presciption. After that we are going analyse dosage data and a bigger sample for better results.

### Goals
* Looking for insigths about association e correlation between variables at exploratory analysis
* Construct classification model to predict which drug is prescripted

### Modeling method
* Target: Drug
* Continuous features: Age and Na_to_K
* Categorical features: Sex, BP, Cholesterol
* 3 functions created: run scenarios, run models and create histograms
* performance metrics: accuracy(principal), precision, recall and F1-score
* ML models: dummy classifer(baseline), logistic regression, KNN, decision tree, random forest

### Conclusion
1. Model
* Baseline was dummy classifer with accuracy equal to 0.5
* Best performance was logistic regression with accuracy equal to 0.89
* Decision tree and random forest probably with overfitting
* It can be used as MVP

2. Insights

Age:
* Drug A was prescribed for younger than 50 years old
* Drug B was prescribed for older than 50 years old

Blood Pressure:
* Drug A and drug B was prescribed for people with high blood pressure
* Drug C was prescribed for people with normal blood pressure
* Drug X was prescribed for people with low and normal blood pressure

Cholesterol:
* Drug C was prescribed for people with high cholesterol

Na to K:
* Drug Y was prescribed for people with > 15mEq/24h

Sex: Is it a irrelevant feature?

### Next steps
* Tuning the decision tree and random forest, including overfitting analysis.
* Calculate ANOVA to analyse variable correlation or feature importance to inderstand which are more important.
* Apply SMOTE to embalanced data.
* As possible, insert dosage information to get greater data granularity and have more security to help treatment prescription.
