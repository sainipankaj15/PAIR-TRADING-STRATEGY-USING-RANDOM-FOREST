# Main Goal of the Project 
Prepare a Model that beat the NIFTY50 and NIFTY500 yearly returns in long term and also Make a trading strategy that can be automated.


# About project 

- In this model, the Model will give the names of the stocks for the Long(First buy then sell) and Short(First sell then buy) for every upcoming trading day of the upcoming whole year. 
- Example : Let's say our model trained in 2010, 2011, and 2012 then our model will tell the names of the stocks for long and short for every trading day in 2013.
- Our main goal is to find the best stocks just by changing the features, parameters, and maximize the yearly returns by changing the number of stocks that we are selecting.
- All codes run on two datasets NIFTY50 and NIFTY500

# Repositry structure 

- There are mainly 2 folders named dataset NIFTY50 and dataset NIFTY500 
- In every folder, You will find files like (Parameter)-RF-K(Stocknumber).ipynb
  - Here "Parameter" value can be {1,2,3,4}
  - "StockNumber" value can be {1,2,3,....10}

- Let's say one code file name is 3-RF_K5. It means in this particular code I used three parameters and pick 5 stocks for long and 5 stocks for short. Find more in Code Notations section
- For every code, you have one result folder where you will find the long and short stocks name of testing year and their returns.

# Code Notations
```
Intraday_1_RF_K_5 means One parameter which is "Today open and Today close" with five stocks

Nextday_1_RF_K_5 means One parameter which is "Today close and Tomorrow close" with five stocks

IntraDay_2_RF_A_K_3 means Two parameters which are "Today close and Tomorrow close" & "Today close and Tomorrow open" with three stocks

IntraDay_2_RF_B_K_3 means Two parameters which are "Today open and Today close" & "Today close and Tomorrow open" with three stocks

IntraDay_2_RF_C_K_5 means Two parameters which are "Today open and Today close" & "Today close and Tomorrow close" with five stocks

Intraday_3_RF_K_6 means Three parameters which are "Today close and Tomorrow close" & "Today close and Tomorrow open" & "Today open and Today close" with six stocks

Intraday_4_RF_K_7 means Four parameters which are "Today close and Tomorrow close" & "Today close and Tomorrow open" & "Today open and Today close" & "Today open and Tomorrow open" with seven stocks
```

# Results 

## When dataset is NIFTY50
### All Models in one frame 
<img src="charts\Nifty50ALL.png">
<img src ="charts\nifty50+all+normal+graph.png">

As we can see when all models comes in single chart it becomes noisy so taking best models and ploting them again.
### Best Models in one frame for NIFTY50
<img src="charts\Nifty50_main.png">
<img src="charts\NIFTY50_main_nomral_graph.png">

## When dataset is NIFTY500
<img src="charts\NIFTY500_ALL_Bar+graph.png">
<img src="charts\NIFTY500_ALL_normal+graph.png">
As we can see when all models comes in single chart it becomes noisy so taking best models and ploting them again.

### Best Models in one frame for NIFTY500
<img src="charts\Nifty500_main_bar_graph.png">
<img src="charts\Nifty500+main+normal+chart.png">

## NIFTY50 Best Models vs NIFTY500 Best Models
<img src="charts\VS.png">

## Best Model VS Real Index Returns (Both NIFTY50 and NIFTY500)
<img src = "charts\realreturnvsnifty50vsnifty500.png">

# Conclusion
- As we can see, we don’t get negative results for any year in our model, but index returns give negative returns for two study periods. In the total of seven study periods, we beat five times index returns, and index returns beat two times our model returns.


- Developed a model using Random Forest algorithm to get
prediction of user defined number of stocks to go long & short in
all trading sessions of upcoming year.
- Achieved 14.04% CAGR with 100% profitability in all seven years of backtested data.
- The model outperformed the index in 5 years out of the total 7
years of testing.

# Technologies used
Pandas, Numpy, Matplotlib, Sklearn Ensemble Model, RandomForestClassifier