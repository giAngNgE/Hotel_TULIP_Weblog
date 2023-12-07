# Hotel_TULIP_Weblog

Hotel TULIP (a hypothetical organisation) is a five star hotel that locates in Australia. It is a very special hotel with an equally special purpose: Not only does it embody all the creative energy and spirit of TULIP-Lab, it’s a “learning environment” on which the tourism and hospitality students are trained for future hoteliers.

In the past two decades, the Web server of Hotel TULIP has logged all the web traffic to the hotel website, and stored large amount of data related to the use of various web pages. 

The hotel’s CIO, Dr Bear Guts (not Bill Gates!), believes that those log files are great resources to help their Information Technology Division improve their potential customers’ online experience, and help their Market Promotion Division to identify potential customers and their behaviour patterns. 

Hence, Hotel TULIP would like to outsource the web usage mining task to analyse web log files and discover user accessing patterns of different web pages.

The Web server is using Microsoft Internet Information Service (IIS), and the Web log format
can be found at: https://msdn.microsoft.com/en-us/library/ms525807(v=vs.90).aspx

# Data Manipulation
1. Data Loading 

Load (may need unzip first) the Hotel TULIP Web log data HTWebLog_p1.zip into dataframe df_ht,
and check how many files are loaded. Then check data statistics and general information by printing
its top 5 rows.

2. Data Cleaning 

• Check which columns have NAs

• For each of those columns, display how many records with NA values

• Remove all records with any NAs.

3. Descriptive Statistics

3.1 Traffic Analysis

• Discover on the traffics by analysing hourly requests.

• Plot into Bar Chart.

• Filter the hourly requests by removing any below 490,000 and above 400,000. (hourly_request_amount >= 400000 & hourly_request_amount <= 490000) 

3.2 Server Analysis - Discover on the server status using ‘sc-status’ from DataFrame

• How many types of status reported?

• Figure ‘Server Status’ in Pie Chart.

• Figure ‘Server Status’ in Donut Chart.

3.3 Geographic Analysis
 
• Select all requests at 01 Jan 2007 from 20:00:00 pm to 20:59:59 pm.

• Discover the geographic information by analysing requests from country and city level.

• Plot countries and cities of all requests in two pie charts.

• List top 3 of both with the request numbers.

# Data Anlytics - Weblog Data

1. Data ETL

1.1 Load Data

• Remove missing values. For the columns, if the column is with 15% NAs, you need to remove
that column. Then, for the rows, if there are any NAs in that row, you need to remove that row
(requests)

• Randomly select 30% of the total data into a new dataframe weblog_df.

1.2 Feature Selection

Select ’cs_method’, ’cs_ip’, ’cs_uri_stem’, ’cs(Referer)’ as features and ’sc_status’ as the class
label into a new dataframe ml_df for following Machine Learning.

• Data Description of ml_df.

• Show the top 5 rows of ml_df.

2. Unsupervised learning

• Perform unsupervised learning on ml_df with K Means.

3. Supervised learning 


 Logistic Regression

• Perform supervised learning on ml_df with Logistic Regression.

• Evaluate the classification performance using confusion matrix including TP, TN, FP, FN;

• Evaluate the classification performance using Precision, Recall and F1 score.

 K-fold Cross-Validation

• Implement K-fold cross validation for three (any three) classification models

4. Association Rule Mining

• Analyze the dataset using association rule mining;

• Choose suitable threshold for confidence, support and/or other parameters. 


## Author
- [@Eden Nguyen](https://github.com/giAngNgE)
