

# UNICORN Companies Analysis 

### Data Gathering

1. The data is in CSV format.

2. Load the data in PowerBI using 'Get Data'.

### Data Cleaning

3. Go to power query editor and use first row as header.

4. In 'city' column, replace blank cell by 'unknown'.

5. In 'company' column, remove duplicates.

6. Add Index column after selecting company column.

### Data Preparation

7. Duplicate the main table and named as 'Investors'.

8. In new table, remove all columns except 'Company' , 'Index', 'Investment' and move the 'Investor' column at the end.

9. Split 'Investors' column.

10. Select all 'Investor' column and then unpivot columns.

11. Delete the 'Attribute' column from there and rename the 'value' column as 'investors.

12. Remove empty cells from 'Investors' column.

13. Remove 'company' column as it is already present in main table.

14. Go to main table, split the 'Date joined' column.

15. Add a new column'Years' using formula [Date joined.2-Year founded]

16. Merge Date joined.1 and Date joined.2

17. Duplicate the main table and named as 'Funding'.

18. Keep only 'funding' and 'index' columns.

19. Split funding and remove funding.1.

20. split funding.2.

21. Add conditional column using formula:
        if funding2.2 equals B then 1000
        elseif funding2.2 equals M then 1
        Else -1
        (-1 represents unknown funding)

22. Change datatype of 'Valuation' column (number).

23. Remove 'funding' column from main table.

24. Make a new column 'year declared' using 'date joined' column.

25. Click on 'manage relationships' and check the relationships between 3 tables.
