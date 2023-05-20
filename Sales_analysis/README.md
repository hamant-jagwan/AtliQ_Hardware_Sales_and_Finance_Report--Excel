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

## Building Report 
### Customer Performance Report
1. Changing the Big amount in small number--> value Field settings--> number format -->custom and change the length of amount like 2,456,234 to 2M.
2. some cleaning work with the 'View' tab like page layout, etc
3. Some 'design' tab work to make our report beautiful.
4. Using `Condtional formatting` to highlight numbers.
5. To insert a LOGO use 'Header Footer'
6. And you are ready to apply filters and get whatever you want like I use this AtliQ hardware data to get **INDIA SALES.** 
![India sales](https://github.com/hamant-jagwan/Excel_analysis/assets/117731315/4c7bb4a1-cb93-4061-befa-57d54f51f93a)

### Market Performance VS Target Report
netsales_targets_2021: https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu
1. We copy our previous sheet -->Right click on the sheet option--> Select Move or copy--> Move to end--> Create copy and rename it 'market performance vs target'
2. Changing the fields of data with the help of `PivotTable`
3. Now it is time to add my 'netsales_targets_2021'data into my existing data--> Open the 'Data' tab--> Get Data --> From file--> From text/CSV and import it.
4. Then we click on Transform data--> This option will take us to `Power Query`--> Data looks clean so we close and load in our existing file and choose 'only create connection' and check the box.
5. Now it is time to use `Power Pivot`-->click manage and establish the relation with another column --> click diagram View and connect the fields
6. After connection, we added measures in our table and field to our `PowerPivot`.
7. Then we change our values by clicking in the value field and converting numbers in million like 2,456,234 to 2M.
8. We successfully added our '2021 - Target' column, now we add another column to make our report which is '%' and doing some `Conditional Formatting ` 
9. Finally we go to the 'View' Tab -->  and use the page layout to print this report.


