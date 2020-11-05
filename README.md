# AI-1 HW3: Cancer Classification from Gene Expressions, Racial bias in ML systems
Homework group members: Akash Reddy, Karthik Balaji.

In this assignment we have two different datasets, one with gene data from a cancer study in Part A and another with the COMPAS data in Part B.

### Part A: Cancer classification from gene expressions:

In this problem, we will build a classification model to distinguish between two related classes of cancer, acute lymphoblastic leukemia (ALL) and acute myeloid leukemia (AML), using gene expression measurements. The dataset is provided in the file `data/cancer_genes.csv`. Each row in this file corresponds to a tumor tissue sample from a patient with one of the two forms of Leukemia. The column `Cancer_type` gives the types of cancer, with **0 indicating the ALL** class and **1 indicating the AML** class. Columns 2-7130 contain expression levels of 7129 genes recorded from each tissue sample. 

### Part B: Racial bias in machine learning systems:

The main dataset is the *compas.csv*. The variables are roughly explained in the `compas_datadict.csv` file, and ProPublica's analysis is publically available here: https://github.com/propublica/compas-analysis.

The dataset was made publically available by **Northpointe**, an American tech-company that works with law establishment across several states in the US to predict future crimes based on past records of criminals. It has been suspected that the software used by Northpointe, `COMPAS`, is biased against the african american criminals, who end up with `high-risk` tags, despite minor criminal record, whereas `Caucasians` regularly received low-scores despite more significant criminal charges.

After pressure from several news agencies and a public investigation by ProPublica, the company released this dataset with a slice of the factors usually considered in order to assign a score to criminals. The dataset also contains a column `two_year_recid` with a binary response, i.e `1` if the released criminal ended up committing another crime within two years and `0` if the criminal did not commit a crime within a period of two years.

(To learn more about this dataset, and the public investigation, you are highly recommended to read ProPublica's article on [Machine Bias](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing))

In this part, we used classification metrics like **confusion matrix, ROC curve, BCA (Bias Corrected Accuracy)**, etc. to analyse the inherent bias present in `COMPAS`, and used data-engineering techniques like **bootstraping, feature selection, one-hot encoding, stratification and SMOTE upsampling**, and also tried using different models other than simple logistic regression, such as **polynomial & interaction terms, regularization parameters, different upsampling techniques, KNN classification**, etc. to try to reduce the bias as much as possible and get the best BCA score for our model.
