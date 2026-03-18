# H1N1 Vaccine Uptake Prediction Using Machine Learning

## Overview

This project applies machine learning techniques to predict whether individuals are likely to receive the H1N1 vaccine. By analyzing demographic characteristics, health behaviors, and public perceptions, the project aims to uncover patterns that influence vaccination decisions.

The goal of this analysis is to support data-driven public health strategies that improve vaccination uptake and resource allocation.

---

## Business and Data Understanding

### Business Problem

Despite the availability of vaccines, a significant portion of the population does not get vaccinated. This presents a major challenge for public health organizations, as low vaccination rates increase the risk of disease transmission and strain healthcare systems.

Public health authorities often lack the ability to identify individuals or groups that are less likely to vaccinate, making it difficult to design targeted and effective vaccination campaigns.

This project addresses the following key question:

**Can we predict vaccination behavior using demographic, behavioral, and perception-based data?**

---

### Stakeholders

The insights from this project are relevant to:

- Kenya Ministry of Health — responsible for vaccination programs and public health policy  
- Africa Centres for Disease Control and Prevention (Africa CDC) — supports disease prevention strategies across the continent  
- World Health Organization (WHO) — guides global vaccination efforts and public health initiatives  

These stakeholders can use predictive insights to improve vaccination outreach and intervention strategies.

---

### Dataset

The dataset is derived from the National 2009 H1N1 Flu Survey and contains responses from over 26,000 individuals.

It includes:

- Demographic information (age, education, income)  
- Health behaviors (preventive actions, healthcare access)  
- Opinions and perceptions about vaccines  
- Vaccination status (target variable)  

The target variable is binary:

- 1 → Received H1N1 vaccine  
- 0 → Did not receive H1N1 vaccine  

---

## Modeling

An iterative modeling approach was used to build and improve classification models.

### Baseline Model

A Logistic Regression model was used as the baseline. This model utilized all available features and provided a benchmark for performance.

While the baseline model achieved high accuracy, it showed limited ability to identify vaccinated individuals due to class imbalance.

---

### Improved Model

An improved Logistic Regression model was developed by:

- Applying class weighting to address class imbalance  
- Tuning regularization parameters  

This resulted in a significant improvement in recall for the vaccinated class, allowing the model to better capture vaccination behavior.

---

### Model Comparison

| Metric | Baseline Model | Improved Model |
|--------|--------------|----------------|
| Accuracy | 83.7% | 77.0% |
| Recall (Vaccinated) | 44% | 72% |
| Precision | 68% | 47% |
| AUC | 0.83 | 0.83 |

Although the improved model shows slightly lower accuracy, it provides a much better balance by correctly identifying a higher proportion of vaccinated individuals.

---

## Evaluation

Model performance was evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC-AUC  

Due to class imbalance, **recall** was prioritized as the key metric, as it measures the model’s ability to correctly identify individuals who received the vaccine.

Both models achieved similar ROC-AUC scores (~0.83), indicating similar overall predictive capability. However, the improved model demonstrated significantly better recall, making it more suitable for this problem.

---

## Key Findings

The analysis identified several important factors influencing vaccination behavior:

- Doctor recommendation strongly increases the likelihood of vaccination  
- Belief in vaccine effectiveness plays a critical role in uptake  
- Higher concern about H1N1 is associated with increased vaccination  
- Health workers are more likely to be vaccinated  
- Demographic factors such as age and education also contribute  

These findings highlight the importance of both **healthcare engagement and public perception** in driving vaccination decisions.

---

## Recommendations

Based on the findings, the following recommendations are proposed:

- Encourage healthcare providers to actively recommend vaccines to patients  
- Improve public trust in vaccines through targeted awareness campaigns  
- Increase education on disease risks to influence perception and behavior  
- Focus outreach efforts on non-health workers and underserved populations  
- Tailor campaigns to specific demographic groups for greater effectiveness  

These strategies can help improve vaccination rates and enhance public health outcomes.

---

## Conclusion

This project demonstrates the value of machine learning in understanding and predicting vaccination behavior. While the baseline model provided a strong starting point, the improved model offered better insights by addressing class imbalance and improving recall.

The results show that vaccination decisions are influenced by a combination of medical advice, personal perception, and behavioral factors.

Although limitations exist, the findings provide a strong foundation for designing more targeted and effective public health interventions.

---

## Repository Structure
`data` - Hold the datasets used in this project

`h1n1_vaccine_prediction.ipynb` - The project notebook

`presentation.pdf` - Non-Technical Presentation

`README.md`
