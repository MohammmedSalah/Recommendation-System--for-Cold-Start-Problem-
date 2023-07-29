
# Recommendation System​ for Cold Start Problem ​
This project aims to offer recommendations for new users
or things when there is little or no information about their preferences, and this is known as the cold-start problem.

## Dataset
We used the [Tenrec dataset](https://static.qblv.qq.com/qblv/h5/algo-frontend/tenrec_dataset.html) which offers data on item and user overlap, which can be used to solve the cold-start issue.

## Project architecture
We used the four cold-start files of [Tenrec dataset](https://static.qblv.qq.com/qblv/h5/algo-frontend/tenrec_dataset.html):
- cold_data.csv
- cold_data_1.csv
- cold_data_0.3.csv
- cold_data_0.7.csv

For every version of the cold-start CSV file, we used multiple algorithms and tried to find the most algorithm that fits the specific cold-start version.
We did a **five implementations** and organized our work as for every cold-start version we did a folder contains 
- The analysis part of the data and the insights of the cold start file.
- The **five implementations** of algorithms.

The algorithms we used in this project are:
- [Bert4Rec model](#algorithm-1-bert4rec-model)
- [Peter4ColdStart model](#algorithm-2-peter4coldstart)
- [GRURec model](#algorithm-3-grurec-model)
- [Bert4ColdStart model for specific gender (2)](#algorithm-4-bert4coldstart-model-for-specific-gender)
- [Hybrid recommender model](#algorithm-5-hybrid-recommender-model)

More information on each algorithm can be found in the descriptions below.

### Algorithm 1: Bert4Rec model
| |Description |
|:-----------|:----------|
|Evaluation matricis| We used this model in all cold-start CSV files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ : ​0.001 <br /> Recall @5 : 0.003
|Results for cold_data_1.csv|Recall@20​ : ​0.0054 <br /> Recall @5 : 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ : ​0.0017 <br /> Recall @5 : 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ : ​0.0013 <br /> Recall @5 : 0.0003|
|sbr_data_1M contribution |We used the data of the SBR file but selected a sample from the file sbr_data_1M.csv as it's too large to be computed|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn, random, time, joblib, pickle, scipy, tqdm|
|The used environment and running |In this model we used [Queen’s Computing server](https://lobot.caslab.queensu.ca) and implemented for every version of cold start CSV files, to run any implementation of them you just need to load the cold start file with the model version plus the SBR CSV file then run the jupyter notebook normally |
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 2: Peter4ColdStart
| |Description |
|:-----------|:----------|
|Evaluation matricis| We used this model in all cold-start CSV files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ : ​0.0005 <br /> Recall @5 : 0.0016
|Results for cold_data_1.csv|Recall@20​ : ​0.0025 <br /> Recall @5 : 0.00007|
|Results for cold_data_0.3.csv|Recall@20​ : ​0.0241 <br /> Recall @5 : 0.0|
|Results for cold_data_0.7.csv|Recall@20​ : ​0.0140 <br /> Recall @5 : 0.0003|
|sbr_data_1M contribution |We used the data of the SBR file but selected a sample from the file sbr_data_1M.csv as it's too large to be computed|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn, random, time, joblib, pickle, scipy, tqdm|
|The used environment and running |In this model we used [Queen’s Computing server](https://lobot.caslab.queensu.ca) and implemented for every version of cold start CSV files, to run any implementation of them you just need to load the cold start file with the model version plus the sampled SBR CSV file then run the jupyter notebook normally |
||[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/peter4coldstart.py |

### Algorithm 3: GRURec model
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start CSV files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ : ​0.7633 <br /> Recall @5 : 0.7062
|Results for cold_data_1.csv|Recall@20​ : ​0.7707 <br /> Recall @5 : 0.7101|
|Results for cold_data_0.3.csv|Recall@20​ : ​0.7424 <br /> Recall @5 : 0.6777|
|Results for cold_data_0.7.csv|Recall@20​ : ​0.7500 <br /> Recall @5 : 0.6875|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn, random, time, joblib, pickle, scipy, tqdm|
|The used environment and running |In this model we used [Google Colap](https://colab.research.google.com/?utm_source=scs-index) and implemented for every version of cold start CSV files, to run any implementation of them you just need to load the cold start file with the model version then run the jupyter notebook normally |
|Resources|https://arxiv.org/pdf/2107.06427.pdf|

### Algorithm 4: Bert4ColdStart model for specific gender
| |Description |
|:-----------|:----------|
|Evaluation matricis| We used this model in all cold-start CSV files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |batch_size and learning_rate​|
|Results for cold_data.csv with gender=2|Recall@20​ : ​0.0022 <br /> Recall @5 : 0.0008
|Results for cold_data_1.csv with gender=2|Recall@20​ : ​0.0028 <br /> Recall @5 : 0.0010|
|Results for cold_data_0.3.csv with gender=2|Recall@20​ : ​0.0022 <br /> Recall @5 : 0.0009|
|Results for cold_data_0.7.csv with gender=2|Recall@20​ : ​0.0028 <br /> Recall @5 : 0.0006|
|sbr_data_1M contribution |We used the data of the SBR file but selected a sample from the file sbr_data_1M.csv as it's too large to be computed|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn, random, time, joblib, pickle, scipy, tqdm|
|The used environment and running |In this model we used [Queen’s Computing server](https://lobot.caslab.queensu.ca) and implemented for every version of cold start CSV files, to run any implementation of them you just need to load the cold start file with the model version plus the SBR CSV file then run the jupyter notebook normally|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 5: Hybrid recommender model
| |Description |
|:-----------|:----------|
|Evaluation matricis| We used this model in all cold-start CSV files and used Accuracy & Precision & Recall for the evaluation|
|Parameters for tuning |num_epochs and learning_rate​|
|Results for cold_data_1.csv|Accuracy​ : ​0.1461 <br /> Precision : 0.9999 <br /> Recall : 0.1461|
|Results for cold_data_0.3.csv|Accuracy​ : ​0.3029 <br /> Precision : 0.9960 <br /> Recall : 0.3029|
|Results for cold_data_0.7.csv|Accuracy​ : ​0.2818 <br /> Precision : 0.9938 <br /> Recall : 0.2818|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn, random, time, joblib, pickle, scipy, tqdm|
|The used environment and running |In this model we used [Kaggle Kernel](https://www.kaggle.com/) and implemented for every version of cold start CSV files, to run any implementation of them you just need to load the cold start file with the model version then run the jupyter notebook normally|
|Resources|https://www.researchgate.net/publication/364357987_HYBRID_RECOMMENDATION_SYSTEM_TO_SOLVE_COLD_START_PROBLEM |

