# Now we are preparing a Financial report for Atliq Hardware 
for the financial report, we need the cost of a company:
fact_sales_monthly_with_cost: https://drive.google.com/drive/u/0/folders/1kODw9JqK2IaG44-yST7vS3hab7a-M-Tu

## To make our report we reuse previous data of ```Sales analysis```

## Steps to make a financial report:-
1. Firstly, we need to add our new data to our previous data model to that we have to go to the 'Data' tab --> get data--> From file--> From Text/CSV.
2. Afterward we select 'Transform Data' to do cleaning stuff in `Power Query`. In our previous sales data we have *fact_sales_montly* which has the same columns as in *fact_sales_monthly_with_cost* which has additional columns.
3. So we need to join the two tables to make it simple first we rename the table *fact_sales_monthly_with_cost* to *finance_ref* and make a  group by selecting the tables and arrange them in groups:

![Screenshot (7)](https://github.com/hamant-jagwan/Excel_analysis/assets/117731315/6a017354-8b6e-4e2f-b009-0dbc4bf3e562)
4. With the help of `power pivot` we connect our tables.
5. And play with `PivotTable`and add 'new measures' to add data in PivotTable 

