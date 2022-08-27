## Reinforcement Learning based Recommendation System

This Project serves as capstone project for Udacity Data Scientist Nanodegree.<br>

This is purely a research project in Reinforcement Learning domain for recommendation systems and <b>not to be confused with business projects where data visualization for stakeholder management is key to success. Model validation and results are appropriately visualized.<br>
Written analysis done on the data can be found in project report
</b><br>

To formulate the recommendation system as Markov Decision Process, we consider the Recommendation System as an Agent. The user interacts with the agent via environment, and obtains a reward and the new state.<br>
Our objective of the project is to learn an Optimal Policy function using Deep Deterministic Policy Gradient Method which can maximize cumulative rewards.<br>

Original Dataset is found [here](https://nijianmo.github.io/amazon/index.html) <br>
Note that due to size of dataset, it is not feasible to upload on github.

Data Sampling and Preprocessing can be found in .py scripts<br>
Custom Gym Environment creation and Actor Critic Networks are written in jupyter notebook .ipynb file.<br>
Images Training Q-vals, Mean rewards and Loss plots can be found in outputs folder <br>
Detailed project writeup/report can be found at [Project Report](https://github.com/thakur-ro/udacity-datascientist/blob/main/Capstone%20Project/Project%20Report.pdf) <br>


### How to run
The .py scripts for data preparation are needed to be run before moving to actor critic modeling in notebook
```
python data_preprocessing.py --file_path data/sample_df.csv --target_dir data/ --min_state_hist 10 --min_actions 1 --states_ratio 0.7 --samples_per_user 10
```
```
python data_sampling.py --file_path data/Electronics.csv --metadata_path data/metadata_df.csv --target_dir data/ --num_items 15000 --min_history 19
```
```
python embeddings_gen.py --file_path data/sample_df.csv --meta_path data/metadata_df.csv --glove_path data/glove.6B.50d.txt --target_dir data/
```


### [Medium Article Link](https://medium.com/@rthakur4298/modeling-recommendation-systems-as-reinforcement-learning-problem-a250e0727ea3)

Resources used in project are appropriately cited at the end of project report.
<br>
Thank you!

  
