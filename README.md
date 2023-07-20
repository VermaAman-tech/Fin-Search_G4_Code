# Roadmap2 Solution - Code.py

## Introduction

This repository contains the solution for Roadmap2 by G4 FinSearch. The team members and their respective roll numbers are listed below:

- Aman Verma (Roll No. 22B3929)
- Hardik Khariwal (Roll No. 22B3954)
- Shruti Ghoniya (Roll No. 22B1288)
- Sachin Yadav (Roll No. 22B1842)

## Description

The `Code.py` file is the main Python script that implements the solution for Roadmap2. It consists of the following components:

1. **Data Preprocessing**: The code starts by loading historical stock data from the file `^NSEI.csv` and preprocesses it to handle any missing data using forward-fill.

2. **Feature Engineering**: Additional features such as 50-day and 200-day moving averages are calculated to enhance the state representation for the stock trading environment.

3. **Action Space**: The action space is defined as a continuous range with granularity specified as 5% of the portfolio value. The bounds for buying and selling actions are set to 20% of the portfolio value and 20% of the current holding, respectively.

4. **Action Mapping**: The code provides a mapping function to interpret the continuous action values as 'BUY', 'SELL', or 'HOLD' actions.

5. **Stock Trading Environment**: The `StockTradingEnvironment` class is defined as a custom Gym environment, which represents the stock trading scenario. It defines the observation space, action space, and methods for resetting and stepping through the environment.

6. **Training with PPO**: The Proximal Policy Optimization (PPO) algorithm from the Stable Baselines3 library is used to train the RL agent on the stock trading environment using historical data.

7. **Evaluation**: After training, the agent's performance is evaluated on a separate testing dataset ('^NSEI_test.csv') to measure the total reward achieved during testing.

## How to Use

1. Clone the repository and navigate to the project directory.

2. Ensure you have the required libraries installed. If not, install them using:

```
pip install pandas numpy gym stable-baselines3
```

3. Place the historical stock data in a file named `^NSEI.csv` in the same directory as `Code.py`.

4. Execute the `Code.py` script to run the solution.

5. The trained agent's performance on the testing dataset will be displayed, showing the total reward achieved during testing.

## Credits

The solution was developed by G4 FinSearch for Roadmap2. The team members and their respective roll numbers are mentioned above.

For any inquiries or questions, feel free to contact the team members.

---
G4 FinSearch | Contact: team@g4finsearch.com | Last Updated: [Date]
