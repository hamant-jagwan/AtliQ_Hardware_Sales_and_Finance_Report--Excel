# *These are raw CSV(comma-separated values) files:*
* Dim_customer CSV--https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu
* Dim_market CSV--https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu
* Dim_product CSV--https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu
* Fact_sales_monthly--https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu

# *With the help of these raw files we analyze Excel with the help of the following functions and tools:*


## *Steps of Load and Data Transformation*
1. Loading data from DATA Tab--> Get data--> From folder
2. We first do some Transformation through `Power Query`
3. we use the *reference option* in our raw data and create separate Table names as dim_customer, dim_market, dim_product, and Fact_sales_mountly. There is a mistake in auto-detection in the column header, so we use the table option 'use the first row as headers'.
4. *Data cleaning in `Power Query`*
* dim_customer--> customer name misspelled so we use the 'replace values' option and replace it.
* dim_market--> 'nan' stands for 'North America(NA)'
* fact_sales_montly--> 'Qty' has a negative value which is wrong so we need to make it positive--> Open the 'Transform' tab-->select 'Qty' and go to scientific and select Absolute value.
so we complete our data cleaning checklists which are -
* Ensure there are no missing values
* Ensure all dimensional columns contain a unique column
* Ensure there is no error/#na in the column
* Check spelling randomly
5. so we are ready to use 'close and load'--> select 'only create connection'

## building report 
1. Changing the Big amount in small number--> value Field settings--> number format -->custom and change the length of amount like 2,456,234 to 2M.
2. some cleaning work with 'View' tab like page layout, etc
3. Some 'design' tab work to make our report beautiful.
4. Using `Condtional formatting` to highlight numbers.
5. To insert a LOGO use 'Header Footer'
6. And you are ready to apply filters and get what ever you want like I use this AtliQ hardware data to get **INDIA SALES.** 
![India sales](https://github.com/hamant-jagwan/Excel_analysis/assets/117731315/4c7bb4a1-cb93-4061-befa-57d54f51f93a)


