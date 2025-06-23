# 🏈 Predict the Winning Team

The purpose of this project is to build a machine learning model that can predict the team that is more likely to win. 

Historical matchup data was imported and used from [**`nfl_data_py`**](https://pypi.org/project/nfl-data-py) to train, test, and validate results. The [**XGBoost**](https://xgboost.readthedocs.io/en/stable/index.html) classifier model yielded results close to **60% accuracy** in predicting the correct  team.

## Sports Data and Challenges

The NFL api contains information on teams, players, game results/schedules, and more. However, modeling sports data can be tricky and overcomplicated. There's too many variables to select from with limited information for predictive usage.  

For example, earlier in this project, I built a model taking the moving average of both teams quarterback statistics and determining the "better" quarterback to predict the winning team. That model faced issues and was not ideal for the main objective I was looking to achieve.

As many machine learning experts say, *garbage in, garbage out*. Before modeling data, make sure to define the objective, analyze relevant features, and avoid overcomplication.

## Project Summary

###  Information
Please refer to `notebook/project.ipynb` to find the code used for data preprocessing, categorical encoding, feature engineering, data modeling, and results.

### Results
- The model has better chances of predicting home winning teams.
- There was significant edge for predicting in the 2024 season (with over **62% accuracy**).
- The last season win record for a team improved results.


### Drawbacks
- **Matchup** - There is not enough matchup data between two teams. Leading to false predictions.
-  **Limited data** - The model is limited to regular season games, last season win percentage, and historical matchup between two teams.
- **Team changes** - The model does not have information on the team changes each season.

## Next Steps
1. Build an interactive web app
2. Fine-tune the model
3. Test other features