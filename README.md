# Gaming-Platform-Loyalty-Analysis-and-Bonus-Allocation

## Project Overview
This project focuses on analyzing user activity data from a gaming platform, including deposits, withdrawals, and gameplay. The primary goal is to calculate player loyalty points based on their engagement and transactional behavior, and then to devise a strategy for allocating bonuses to top-performing players.

## Features
- **Data Loading and Database Integration**: Reads deposit, withdrawal, and gameplay data from CSV files and loads it into a MySQL database.
- **Data Preprocessing**: Cleans and transforms raw data, including date/time parsing and creating time slots (S1/S2).
- **Loyalty Point Calculation**: Implements a custom formula to calculate loyalty points based on total deposits, withdrawals, deposit/withdrawal frequency, and games played.
- **Player Ranking**: Ranks players based on their loyalty points, with a tie-breaking mechanism using games played.
- **Date and Slot-Specific Analysis**: Calculates loyalty points for specific dates and time slots to identify activity patterns.
- **Key Performance Indicators (KPIs)**: Calculates average deposit amounts and average games played per user.
- **Bonus Allocation Strategies**: Explores and demonstrates two methods for distributing a bonus pool to top players: Proportional Distribution and Bracket Method.

## Technologies Used
- **Python**: Core programming language for data manipulation and analysis.
- **Pandas**: For data loading, cleaning, and transformation.
- **MySQL Connector/Python**: To connect and interact with the MySQL database.
- **MySQL**: Relational database for storing and querying user data.

## Setup and Installation
To run this project, you'll need the following:

1.  **MySQL Database**: Ensure a MySQL server is running and accessible. Create a database named `gaming`.
2.  **MySQL Connector/Python**: Install the Python package:
    ```bash
    pip install mysql-connector-python pandas
    ```
3.  **CSV Data Files**: Place the following CSV files in the specified path (or update the paths in the notebook):
    - `Deposit Data.csv`
    - `Withdrawal_Data.csv`
    - `User Gameplay data.csv`

4.  **Database Credentials**: Update the `mysql.connector.connect` details in the first code cell (host, user, password, database) to match your MySQL setup.

## How to Run
1.  **Open the Jupyter Notebook**: Open `loyalty_analysis.ipynb` in a Jupyter environment (e.g., Google Colab, Jupyter Lab).
2.  **Execute Cells Sequentially**: Run all code cells in the notebook in their sequential order. The notebook is structured to guide you through the data loading, processing, analysis, and bonus allocation steps.

## Key Findings
- **Top Loyalty Players**: Identified the top 50 players based on a weighted loyalty points formula, with player `634` consistently ranking highest.
- **Average Deposits**: The average deposit amount across all transactions is `5492.19 Rs`.
- **Average Deposit Per User (Monthly)**: The average total deposit per user in a month is `104669.65 Rs`.
- **Average Games Played**: Users play an average of `355.27` games.
- **Bonus Allocation**: Proportional distribution was recommended as a fair method to allocate bonuses based on loyalty points.

## Conclusion
This project provides a robust framework for understanding player loyalty and implementing data-driven bonus allocation strategies on a gaming platform. The loyalty point formula can be further refined by incorporating more features or dynamic weighting based on business objectives.
