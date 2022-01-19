# Asset Managers Risk and Return Analysis

This project analyzes one data sets ```whale_navs.csv``` which includes the net asset value of four different funds/asset managers (Soros Fund Management, Paulson & Co, Tiger Global Management, and Berkshire Hathaway) and the S&P 500 index ranging from October 2014 to September 11th, 2020. The project consists of obtaining and analyzing different risk/return parameters to evaluate which investment has the best performance, this includes creating plots and obtaining summary statistics (such as the mean) as well as useful information such as Standard Deviation, Variance, Covariance, Beta and Sharpe Ratio.

The dataset includes the following:
* Timestamp (data set includes the following information for each day in our time range )
* Net Asset Values (NAVS)

---

## Technologies

The following technologies were used to build and deploy this application:

* Python - Version 3.9.7
* Anaconda (Which includes Jupyter Lab and Pandas)
* Path (from pathlib)
* matplotlib

---

## Installation and Usage Guide

### 1. Install Python 3.9.7

For installing Python 3.9.7 you can find the Installation Files for both Windows/Mac OS in the following link
 * [Anaconda Installation Files](https://www.anaconda.com/products/individual "Anaconda Installation Files")

If you require assistance installing it, you can follow the following videos for guidance
* [Youtube Video Python Installation Guide - Windows](https://www.youtube.com/watch?v=uSVl7gRXP80 "Python Installation Video - Windows") 
* [Youtube Video Python Installation Guide - Mac](https://www.youtube.com/watch?v=r6bBaj797t8 "Python Installation Video - Mac") 
 
### 2. Install Anaconda

For installing Python 3.9.7 you can find the Installation Files for both Windows/Mac OS in the following link
 * [Python Installation Guide](https://www.python.org/downloads/release/python-397/ "Python Installation Guide")

If you require assistance installing it, you can follow the following videos for guidance
* [Youtube Video Anaconda Installation Guide - Windows](https://www.youtube.com/watch?v=g6ln1dAt-RI "Anaconda Installation Video - Windows") 
* [Youtube Video Anaconda Installation Guide - Mac](https://www.youtube.com/watch?v=oWVTO_69U4c "Anaconda Installation Video - Mac")

### 3. Downloading the Asset Managers Risk and Return Analysis Repository

Navigate to your desired location where you would like to save the documents for this application. You can do this by using the ```cd``` command followed by a space and the file path inside quotations ```" file path "```. In my example I have gone to Desktop.

Note that in this example we are downloading a different repository, however the process is still the same.
![image](https://user-images.githubusercontent.com/94983278/149385012-181d1769-0af6-487e-8e04-823a28f2c3ed.png)

Clone this project's repository from GitHub using the following command 

``` git clone https://github.com/epocaterrasus/Asset-Managers-Risk-and-Return-Analysis.git```

### 4. Opening the file on Jupyter Notebook

Being in the folder created when you downloaded the repository type ```jupyter lab```, this should open a window in your predetermined browser with Jupyter Lab. In the left corner you can see the files inside the repository, open the ```risk_return_analysis.ipynb``` which contains all steps and notes followed to analyze this dataset pair.

---

## Explanation of the Processes Followed

### 1. Data Import & Conversion

Before being able to properly analyze the data to draw conclusions we must first import the data, the following bullett gives a summary of what was done:

* Importing both the dataset using the pandas ```read_csv``` function and setting parameters to set index column to "Timestamp", making it parse dates and infer date/time format
* Calculating daily returns using the ```pct_change``` function in conjunction with the ```dropna```
* Aggregating daily return values to have cumulative data using the ```cumprod```

### 2. Plotting

It is always useful to get visualizations that allow us to see the "bigger picture" of our data, in this case we did the following graphs using the ```plot```

* Daily returns line plot for all four asset managers and the S&P 500
* Cumulative daily returns line plot for all four asset managers and the S&P 500
* Box plots of all four asset managers and the S&P 500 to analyze volatility and spread of the returns
* Plotting 21 day Moving Standard Deviation of all four asset managers and the S&P 500
* Plotting Sharpe Ratios to compare the Risk/Return of the funds vs. the S&P 500
* Plotting 60 day Moving Beta's for two selected Asset Managers (Berkshire and Tiger)

### 2. Analytics Performed

* Standard Deviation using the ```std``` function
* Variance using the ```var``` function
* Covariance using the ```covar``` function
* Sharpe Ratios by dividing the average annual returns by the annualized standard deviation
* Beta calculations by dividing the covariance of a portfolio/asset manager by the variance of the S&P 500
* Descriptive statistics such as the mean for the standard deviation, variance, covariance and beta


---

## Conclusions drawn from our analysis

From our analysis we can conclude that over the long run the best investment is Berkshire Hathaway, followed by Tiger Global Management. The main factor that we used in making this determination was the Sharpe Ratio, which gives us an idea on how much risk to expect for a certain degree of returns. In addition we also drew the conclusion that Berkshire Hathaway is more sensitive to movements in the market (higher Beta) in comparison to Tiger Global Management. This can easily be attributed to the fact that many of the companies that Buffet holds are major components of the index.

Sharpe Ratio of the Asset Managers and the SP&500
![image](https://user-images.githubusercontent.com/94983278/150148934-4081dd8c-e1d3-4a4c-b0b4-1f0ee8475b4e.png)

Plot of 21 Day Moving Standard Deviation for Funds/Asset Managers and the SP500
![image](https://user-images.githubusercontent.com/94983278/150149258-1c3eb5d2-613a-4745-905f-595156496025.png)


---

## Contributors

Edgar Pocaterra - epocaterra@protonmail.ch / +1 806 283 5455

---

## License

MIT License

Copyright (c) 2022 epocaterrasus

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.