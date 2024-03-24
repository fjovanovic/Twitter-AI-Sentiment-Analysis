# Twitter (X) AI Sentiment Analysis

The project was developed during the third year of studies for the Data Mining 1 course, under the guidance of PhD Nenad Mitic, with support from teaching associate Marija Eric.  

Author: `Filip Jovanovic`  
Professor: `PhD Nenad Mitic`  
Teaching associate: `Marija Eric`

## Project info  
Employing Natural Language Processing (`NLP`) techniques, the project endeavors to construct a system for detecting hate speech in tweets. 
Hate speech is defined herein as tweets containing racist or sexist sentiments.  
The primary goal is to classify tweets as either containing hate speech (label '1') or non-hate speech (label '0').  
For further exploration of the project and detailed insights into the dataset, interested individuals are encouraged to visit the project repository 
hosted on [kaggle](https://www.kaggle.com/datasets/arkhoshghalb/twitter-sentiment-analysis-hatred-speech).  
There, you can access additional documentation, code implementations, and the dataset itself, facilitating a deeper understanding of the project's methodologies and findings.

## Environment
- [![python](https://img.shields.io/badge/Python-3.7-blue.svg)](https://www.python.org/downloads/release/python-370/)
- [![python](https://img.shields.io/badge/Python-3.8-blue.svg)](https://www.python.org/downloads/release/python-380/)
- [Virtual Environment](https://docs.python.org/3/library/venv.html) (Optional but recommended): Set up a virtual environment to manage project dependencies.
This ensures project isolation and prevents conflicts with other Python projects.
- [Google Colab](https://colab.research.google.com/): Consider utilizing Google Colab for running notebooks and experimenting with machine learning models.
Google Colab provides free access to powerful hardware resources, including GPUs and TPUs, which can significantly accelerate model training.

## Install dependencies 
To install project dependencies, simply run the following command in your terminal:
```bash
pip install -r requirements.txt
```
This command will automatically install all the required packages listed in the `requirements.txt` file, ensuring that your environment is properly configured to run the project.

## Project structure 
:warning: Even though test data exists it is not used in the project since doesn't contain **label** column that is labeling tweets
  as hatred / non-hatred. In the models  (not saved assoc, clustering, classification)  
:warning: Datasets for association rules, classification, and clustering were not added due to their large size.  
:warning: The best model for hierarchical clustering was not saved since the results were not good enough

- `dataset` - Contains **train** and **test** data. 
- `images` - Contains images for data visualization ([wordcloud](https://github.com/amueller/word_cloud) library)
- `models`
  - `association_rules` - **Apriori** algorithm made in [SPSS](https://www.ibm.com/spss)
    - `apriori.str`
  - `classification` - Classification algorithms **Naive Bayes**, **Decision Tree** and **Random Forest**
    - `decision_tree.ipynb`
    - `decision_tree.joblib` (Best *RandomForestClassifier* trained model)
    - `naive_bayes.ipynb`
    - `naive_bayes.joblib` (Best *MultinomialNB* trained model)
  - `clustering` - Clustering algorithms **Hieararchical** and **KMeans**
    - `hierarchical.ipynb`
    - `k_means.ipynb`
    - `k_means.joblib` (Best *KMeans* trained model)
- `preprocessing.ipynb` - Data preprocessing for the needs of algorithms
- `requirements.txt` - Required libraries for the project

## Literature
- `Research`
  - [Research gate](https://www.researchgate.net/profile/Satish-Alaria-2/publication/361728073_An_Approach_for_Cloud_Security_Using_TPA-_and_Role-Based_Hybrid_Concept/links/6369e4c754eb5f547cb0d64e/An-Approach-for-Cloud-Security-Using-TPA-and-Role-Based-Hybrid-Concept.pdf#page=654)
- `Kaggle examples`
  - [All codes](https://www.kaggle.com/datasets/arkhoshghalb/twitter-sentiment-analysis-hatred-speech/code)
  - [Votes #1](https://www.kaggle.com/code/pavansanagapati/knowledge-graph-nlp-tutorial-bert-spacy-nltk)
  - [Votes #2](https://www.kaggle.com/code/prashant111/a-beginners-guide-to-dealing-with-text-data)
  - [Votes #3](https://www.kaggle.com/code/eisgandar/twitter-sentiment-analysis-hatred-speech)
- `Naive Bayes`
  - [IBM](https://www.ibm.com/topics/naive-bayes)
  - [Javatpoint](https://www.javatpoint.com/machine-learning-naive-bayes-classifier)
  - [scikit-learn](https://scikit-learn.org/stable/modules/naive_bayes.html)
  - [Turing](https://www.turing.com/kb/an-introduction-to-naive-bayes-algorithm-for-beginners)
  - [Towardsdatascience](https://towardsdatascience.com/naive-bayes-classifier-81d512f50a7c)
  - [YouTube | StatQuest with Josh Starmer](https://www.youtube.com/watch?v=O2L2Uv9pdDA&t=418s&ab_channel=StatQuestwithJoshStarmer)
- `Decision Tree`
  - [IBM](https://www.ibm.com/topics/decision-trees)
  - [Javatpoint](https://www.javatpoint.com/machine-learning-decision-tree-classification-algorithm)
  - [scikit-learn](https://scikit-learn.org/stable/modules/tree.html)
  - [Harvard Business Review](https://hbr.org/1964/07/decision-trees-for-decision-making)
  - [YouTube | StatQuest with Josh Starmer](https://www.youtube.com/watch?v=_L39rN6gz7Y&ab_channel=StatQuestwithJoshStarmer)
  - [YouTube | Normalized Nerd](https://www.youtube.com/watch?v=ZVR2Way4nwQ&t=526s&pp=ygUhZGVjaXNpb24gdHJlZSBhbGdvcml0aG0gZXhwbGFpbmVk)
- `Random Forest`
  - [IMB](https://www.ibm.com/topics/random-forest)
  - [Javatpoint](https://www.javatpoint.com/machine-learning-random-forest-algorithm)
  - [scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
  - [YouTube | StatQuest with Josh Starmer](https://www.youtube.com/watch?v=J4Wdy0Wc_xQ&pp=ygUNcmFuZG9tIGZvcmVzdA%3D%3D)
  - [YouTube | Normalized Nerd](https://www.youtube.com/watch?v=v6VJ2RO66Ag&t=205s&ab_channel=NormalizedNerd)
- `K-means`
  - [Javatpoint](https://www.javatpoint.com/k-means-clustering-algorithm-in-machine-learning)
  - [scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
  - [YouTube | StatQuest with Josh Starmer](https://www.youtube.com/watch?v=4b5d3muPQmA&t=257s&pp=ygUHayBtZWFucw%3D%3D)
- `Hierarchical`
  - [Learndatasci](https://www.learndatasci.com/glossary/hierarchical-clustering/)
  - [Javatpoint](https://www.javatpoint.com/hierarchical-clustering-in-machine-learning)
  - [YouTube | StatQuest with Josh Starmer](https://www.youtube.com/watch?v=7xHsRkOdVwo&ab_channel=StatQuestwithJoshStarmer)
- `Apriori`
  - [Javatpoint](https://www.javatpoint.com/apriori-algorithm)
  - [Towardsdatascience](https://towardsdatascience.com/apriori-association-rule-mining-explanation-and-python-implementation-290b42afdfc6)
