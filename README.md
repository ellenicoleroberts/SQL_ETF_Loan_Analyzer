<img src= "Images/sanfran.png" width="930" height="300">

# Challenge_7_Passive_Investing

This application offers clients an online investment solution for their retirement portfolios through the use of algorithms that choose from various investment styles and options.

The goal is to determine the fund with the most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios, and betas.

---
## Technologies

This application leverages python 3.7 with the following packages:

* pandas: an open-source library that offers easy-to-use data analysis tools for Python.
* pathlib: for creation of file paths allowing the application to interact with a computer's filesystem.
* hvplot.pandas: a visualization library included in the PyViz package that can produce advanced charts    
  and interactive visualizations. 
* sqlalchemy: a library that facilitates the communication between a Python program and a 
  database created from a Jupyter notebook.  

---
## Installation Guide

To run PyViz and its dependencies, it is best to first create a new environment in your terminal and install the PyViz pacakges within this environment by completing the following steps:

STEP 1: In your terminal, enter:

`conda create -n PyViz python=3.7 anaconda`

STEP 2: Activate the environment you created in Step 1 (PyViz) by inputting the following command in your terminal:

`conda activate PyViz`

STEP 3: Within this environment, install the PyViz packages by using the conda install command as follows:

`conda install -c pyviz hvplot geoviews`

STEP 4: Clone the GitHub repo (the one this file is contained in) into your Terminal. 

STEP 5: To install the remaining packages, while in this same repo in your Terminal, enter `pip install -r requirements.txt`.

Finally, to run the code, in your IDE open the "san_francisco_housing.ipynb" notebook file and run it.

---

## Usage

To begin with, the code imports and reads data from the whale_navs.csv file included in this repo. This file contains NAV prices of four major funds plus S&P 500 Index data. Once the data is imported, it is converted into a Pandas DataFrame including only daily return values for each of the funds and the S&P 500 Index. 

These daily returns are plotted on an overlay line plot for visual comparison. Next, each of the funds' and the S&P 500 Index's cumulative returns are calculated for the time period and then plotted on the same plot, again overlayed for visual comparison, as shown here:

![Cumulative returns plot.](images/geomap.png)

Volatility of each of the four fund portfolios and of the S&P 500 Index is then visually analyzed with box plots. Standard deviations are next determined, as well as the annualized standard deviation and rolling standard deviations for a 21-day window. These rolling standard deviations are plotted on an overlay line plot.

Risk-return metrics are next analyzed. Sharpe ratios are calculated and visualized via a bar plot for comparison.

To evaluate how the portfolios react relative to the broader market, covariance using a 60-day rolling window is determined for each of the best two performing funds (selected on a risk-return basis) compared to the S&P 500 Index. Beta values, likewise using a 60-day rolling window, are then determined and plotted.

---

## Contributors

Nicole Roberts,
elle.nicole.roberts@gmail.com

---

## License

[BSD 3](https://choosealicense.com/licenses/bsd-3-clause-clear/): BSD 3-clause is a permissive licence, allowing nearly unlimited freedom with the software as long as BSD copyright and license notice is included.
