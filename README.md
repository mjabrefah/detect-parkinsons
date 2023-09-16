# detect-parkinsons
The aim of this project was to build a model to accurately detect the presence of Parkinson's Disease in an individual using speech data with XGBoost.

---

## What is Parkinson's Disease?
**Parkinson's disease (PD)** is a chronic degenerative disorder of the central nervous system that affects both the motor system and non-motor systems. The symptoms usually emerge slowly, and as the disease worsens, non-motor symptoms become more common. Early symptoms are tremor, rigidity, slowness of movement, and difficulty with walking. Problems may also arise with cognition, behaviour, sleep, and sensory systems.

As the disease advances, disability is more related to motor symptoms that are uncontrollable by medication, such as swallowing and speech difficulties, and gait and balance problems; and to levodopa-induced complications, which appear in up to 50% of individuals after five years of levodopa usage [Poewe(2006)](https://pubmed.ncbi.nlm.nih.gov/17131223/)



## Dataset Information
According to [Little _et al._, 2009](https://ieeexplore.ieee.org/document/4636708/authors#authors), the authors provide an evaluation of the real-world utility of established conventional and unconventional metrics for distinguished individuals without PD from those with PD through identification of dysphonia (hoarse voice).
They introduce a novel dysphonia metric known as pitch period entropy (PPE) which demontrates resilience in the face of various uncrontrollabble factors, such as background noise in acoustic environments and typical, natural fluctuations in voice pitch among healthy individuals.

This dataset is composed of a range of biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD). Each column in the table is a particular voice measure, and each row corresponds one of 195 voice recording from these individuals ("name" column). The main aim of the data is to discriminate healthy people from those with PD, according to "status" column which is set to 0 for healthy and 1 for PD. 

The data is in ASCII CSV format. The rows of the CSV file contain an instance corresponding to one voice recording. There are around six recordings per patient, the name of the patient is identified in the first column.

## What is XGBoost?
XGBoost is a new Machine Learning algorithm designed with speed and performance in mind. XGBoost stands for eXtreme Gradient Boosting and is based on decision trees. The XGBClassifier is primarily used for classification tasks, where the goal is to predict a categorical target variable. In this project, I import the XGBClassifier from the xgboost library; this is an implementation of the scikit-learn API for XGBoost classification.

In this project, the data is loaded and the features and labels are obtained. The features are scaled and the dataset split. Using **scikit-learn**, **pandas**, and **xgboost**, a model is built with an XGBClassifier and the accuracy is calculated.
