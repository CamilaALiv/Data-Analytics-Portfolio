# Stock Market Data Analysis

This is a project done in the course "Microsoft Power BI for Business Intelligence and Data Science" at the Data Science Academy. This dashboard was created with real data from the stock market of IBM, Microsoft, Oracle, Tesla and Walmart, between March 2022 and March 2023. The data used was extracted from the Nasdaq portal and is publicly available on the website: https://www.nasdaq.com 

### **Our dashboard should answer these business questions:**

1 - What is the total trading volume of shares over time for the 5 companies being analyzed? Allow this analysis to be done for a single company or combination of companies.

2 - What is the average opening (Open), highest (High), lowest (Low) and closing (Close) value of shares of all companies for all months of the analyzed data period?

3 - What is the change in the average closing value (close) of the shares of all companies over time, month by month? Allow this analysis to be done for a single company or combination of companies.

4 - Use the Smart narrative to explain the main characteristics and trends in the data.

# Dataset:
The first step was to extract the data from the selected companies directly from the Nasdaq website. The data for each company was downloaded in cvc format. We added a field with the name of each company and concatenated the data into a single spreadsheet in xlxs format. This dataset contains 6 columns with the following informations: Company, Date, Close, Volume, Open, High, Low.

# Data Analysis

### 1 - What is the total trading volume of shares over time for the 5 companies being analyzed? Allow this analysis to be done for a single company or combination of companies.

For a better visualization of the trading volume of stocks over the period of one year, we use the ‘Area Chart’. This chart is often used to find trends in data over time and allows you to view a timeline, with padding below the lines to show the magnitude of trends. When we hover the mouse over the chart line, we see the values traded each day. So that this analysis could be done for each company, for a combination of companies or for all companies, 'Slicer' per company was added.

![Chart1](https://user-images.githubusercontent.com/123582788/229661161-cb7b865e-7af5-4ba2-866a-4ed858fbe1c2.png) 
![segmentation](https://user-images.githubusercontent.com/123582788/229662281-b0aba2a0-e44f-4497-97b2-792db9d24bf6.png)

### 2 - What is the average opening (Open), highest (High), lowest (Low) and closing (Close) value of shares of all companies for all months of the analyzed data period?

To show this data in a clean and organized way, the 'Table' format was chosen. In the hierarchy of dates, we selected the options year and month, since the period starts in 2022 and ends in 2023. To display the average values of Open, High, Low and Close, it was necessary to replace the 'Sum' option that comes as default in the data view to the 'Average' option. The same Slicer created in the previous section allows this analysis to be performed for a single company or a combination of companies.

![table](https://user-images.githubusercontent.com/123582788/229662620-96e7fd8e-0d24-4558-b854-43dd6c9d944b.png)

### 3 - What is the change in the average closing value (close) of the shares of all companies over time, month by month? Allow this analysis to be done for a single company or combination of companies.

The visualization chosen was a 'Steacked Area Chart', where each color symbolizes one of the companies. The stock price is a time series (event that occurs over time), and can be calculated with a ‘Quick Measure’. A Quick measure runs a set of Data Analysis Expressions (DAX) commands behind the scenes, then presents the results for you to use in your report.
In Quick Measure, choosing the option Time Intelligence – month-over-month change. The fields required to create this measure were filled in with the following metrics:
- Base value = average of close
- Date = the entire date hierarchy
- Number of periods = 1 (means that the calculation will be shown month by month).
The same Slicer created in the previous section allows this analysis to be performed for a single company or a combination of companies.

![chart2](https://user-images.githubusercontent.com/123582788/229662731-a262b679-4427-480b-b0ea-4ea6c0a55eda.png)

### 4 - Use the Smart narrative to explain the main characteristics and trends in the data.

Smart narrative visualization helps to quickly summarize visuals and reports, providing relevant insights that can be customized. They can be added to the report to address key findings, point out trends, and other insights. It is automatically generated when selected in visualizations – smart narrative.

![smart_narrative](https://user-images.githubusercontent.com/123582788/229662878-d8dd801f-3977-431d-8622-15a962c781d9.png)

To complement the visualization, another Slicer was added, this time with the variable date, per months, allowing the end user to interact with the dashboard and also facilitating the segmented view by date.
Below the final result of the dashboard:


![dashboard_stock_market](https://user-images.githubusercontent.com/123582788/229662942-11390716-3564-4c24-a460-321b4df98957.png)



# Bibliographic References:

https://learn.microsoft.com/en-us/power-bi/

https://www.datascienceacademy.com.br/course/microsoft-power-bi-para-business-intelligence-e-data-science

https://www.nasdaq.com 
