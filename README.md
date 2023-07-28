
# Recommendation System​ for Cold Start Problem ​
This project aims to offer recommendations for new users
or things when there is little or no information about their preferences, and this is known as the cold-start problem.

## Dataset
We used the [Tenrec dataset](https://static.qblv.qq.com/qblv/h5/algo-frontend/tenrec_dataset.html) which offers data on item and user overlap, which can be used to solve the cold-start issue.

## Project architecture
We used the four cold-start files of [Tenrec dataset](https://static.qblv.qq.com/qblv/h5/algo-frontend/tenrec_dataset.html);
- cold_data.csv
- cold_data_1.csv
- cold_data_0.3.csv
- cold_data_0.7.csv

For every version of the cold-start CSV file, we used multiple algorithms and tried to find the most algorithm that fit the specific cold-start version.
We did a **five implementations** and organized our work as for every cold-start version we did a folder contains 
- The analysis part of the data and the insights.
- The **five implementations** of algorithms.

The algorithms we used in this project are;
- [Bert4ColdStart model](#Algorithm-1:-Bert4ColdStart)
- [Peter4ColdStart model](#Algorithm-2:-Bert4ColdStart)
- [GRURec model](#Algorithm-3:-Bert4ColdStart)
- [Hybrid recommender model](#Algorithm-4:-Bert4ColdStart)
- [Bert4ColdStart model for specific gender](#Algorithm-5:-Bert4ColdStart)

More information on each algorithm can be found in the descriptions below.

### Algorithm 1: Bert4ColdStart model
todo check if need to handle all the ev matrics or not
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start csv files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ ; ​0.001 <br /> Recall @5 ; 0.003
|Results for cold_data_1.csv|Recall@20​ ; ​0.0054 <br /> Recall @5 ; 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ ; ​0.0017 <br /> Recall @5 ; 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ ; ​0.0013 <br /> Recall @5 ; 0.0003|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn|
|The used environment|[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 2: Peter4ColdStart
todo check if need to handle all the ev matrics or not
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start csv files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ ; ​0.001 <br /> Recall @5 ; 0.003
|Results for cold_data_1.csv|Recall@20​ ; ​0.0054 <br /> Recall @5 ; 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ ; ​0.0017 <br /> Recall @5 ; 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ ; ​0.0013 <br /> Recall @5 ; 0.0003|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn|
|The used environment|[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 3: GRURec model
todo check if need to handle all the ev matrics or not
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start csv files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ ; ​0.001 <br /> Recall @5 ; 0.003
|Results for cold_data_1.csv|Recall@20​ ; ​0.0054 <br /> Recall @5 ; 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ ; ​0.0017 <br /> Recall @5 ; 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ ; ​0.0013 <br /> Recall @5 ; 0.0003|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn|
|The used environment|[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 4: Hybrid recommender model
todo check if need to handle all the ev matrics or not
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start csv files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ ; ​0.001 <br /> Recall @5 ; 0.003
|Results for cold_data_1.csv|Recall@20​ ; ​0.0054 <br /> Recall @5 ; 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ ; ​0.0017 <br /> Recall @5 ; 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ ; ​0.0013 <br /> Recall @5 ; 0.0003|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn|
|The used environment|[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |

### Algorithm 5: Bert4ColdStart model for specific gender
todo check if need to handle all the ev matrics or not
| |Description |
|:-----------|:----------|
|Evaluation matricis|we used this model in all cold-start csv files and used Recall@20 & Recall@5​ for the evaluation|
|Parameters for tuning |num_epochs, batch_size and learning_rate​|
|Results for cold_data.csv|Recall@20​ ; ​0.001 <br /> Recall @5 ; 0.003
|Results for cold_data_1.csv|Recall@20​ ; ​0.0054 <br /> Recall @5 ; 0.0001|
|Results for cold_data_0.3.csv|Recall@20​ ; ​0.0017 <br /> Recall @5 ; 0.0005|
|Results for cold_data_0.7.csv|Recall@20​ ; ​0.0013 <br /> Recall @5 ; 0.0003|
|Requirements|Python 3.9+, Pytorch, Jupyter Lab, numpy, pandas, matplotlib, seaborn, scikit-learn|
|The used environment|[Queen’s Computing server](https://lobot.caslab.queensu.ca)|
|Resources|https://github.com/yuangh-x/2022-NIPS-Tenrec/blob/master/model/coldstart/bert4coldstart.py |



## Resources

todo github code and libs
