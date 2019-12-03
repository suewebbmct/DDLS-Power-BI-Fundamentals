# Module 4: Shaping and Combining Data

- [Module 4: Shaping and Combining Data](#Module-4-Shaping-and-Combining-Data)
    - [Lab: Editing Queries in Power BI Desktop](#Lab-Editing-Queries-in-Power-BI-Desktop)
        - [Exercise 1: Shaping the data into Power BI](#Exercise-1-Shaping-the-data-into-Power-BI)
            - [Task 1: Editing Data Queries from SQL Server](#Task-1-Editing-Data-Queries-from-SQL-Server)
            - [Task 2: Editing Data Queries from Excel](#Task-2-Editing-Data-Queries-from-Excel)
            - [Task 3: Editing Data Queries from the Web](#Task-3-Editing-Data-Queries-from-the-Web)

*The exercises for Modules 3 to 6 have been designed by DDLS staff.*
*They replace the exercises published by Microsoft Learning.*

## Module 4

### Lab: Editing Queries in Power BI Desktop

Scenario

Now that the data has been imported it is apparent that some
modifications to the queries are required. There are many unnecessary
columns, the names of many of the tables and columns are not intuitive,
even the format of some the data will make it hard to analyze.

### Exercise 1: Shaping the data into Power BI

#### Task 1: Editing Data Queries from SQL Server

1.  In **Power BI Desktop**, in the **Home** ribbon, click **Edit Queries**.

2.  In the Query editor window, in the **Queries** pane (on the left),
    select **FactInternetSales**.

3.  In the **Query Settings** pane (on the right), change the **Name** to
    **Internet Sales**.

4.  In the middle pane, Ctrl-Select the columns **PromotionKey, RevisionNumber,**
    **UnitPriceDiscountPct, DiscountAmount, CarrierTrackingNumber,**
    **CustomerPONumber**, and then in the ribbon click **Remove Columns**.
    
9.  **Rename** the following columns:
    - "SalesOrderNumber" to "Sales Order Number"
    - "SalesOrderLineNumber" to "Sales Order Line Number"
    - "OrderQuantity" to "Order Quantity"
    - "UnitPrice" to, "Unit Price"
    - "ExtendedAmount" to "Extended Amount"
    - "ProductStandardCost" to "Product Standard Cost"
    - "TotalProductCost" to "Total Product Cost"
    - "SalesAmount" to "Sales Amount"
    - "TaxAmt" to "Tax Amount"
    - "OrderDate" to "Order Date"
    - "DueDate" to "Due Date"
    - "ShipDate" to "Ship Date"

5.  In the Queries pane select **DimCustomer** and rename this to Customer.

6.  Remove the columns **Title, NameStyle, Suffix, SpanishEducation,**
    **FrenchEducation, SpanishOccupation, and FrenchOccupation.**

9.  **Rename** the following columns:
    - "MaritalStatus" to "Marital Status"
    - "EmailAddress" to "Email Address"
    - "YearlyIncome" to "Yearly Income"
    - "TotalChildren" to "Total Children"
    - "NumberChildrenAtHome" to "Number Children At Home"
    - "EnglishEducation" to "Education"
    - "EnglishOccupation" to "Occupation"
    - "HouseOwnerFlag" to "House Owner Flag"
    - "NumberCarsOwned" to "Number Cars Owned"
    - "DateFirstPurchase" to "Date First Purchase"
    - "CommuteDistance" to "Commute Distance"


10. Select the **Gender** column, and in the ribbon click **Replace Values** (or you can right-click the column heading and choose **Replace Values** from the shortcut menu).

11. In the **Value To Find** box type **M.**

12. In the **Replace With** box type **Male**, then click **OK**.

13. Repeat the process to replace the value **F** with **Female**.

15. repeat the process to replace the values in the **MaritalStatus** column so the **S** becomes
    **Single** and **M** becomes **Married**.

16. In the Queries pane select **DimDate**.

17. Rename it to Date.

18. Remove the Spanish and French columns.

22. Right-click the column **DayNumberOfWeek** and select Remove.

23. In the Applied Steps pane, click the X next to the last step
    (Removed Columns1) to undo it.
    
24. **Rename** the following Columns:
    - "DayNumberOfWeek" to "Day Number Of Week"
    - "EnglishDayNameOfWeek" to "Day Name Of Week"
    - "DayNumberOfMonth" to "Day Number Of Month"
    - "DayNumberOfYear" to "Day Number Of Year"
    - "WeekNumberOfYear" to "Week Number Of Year"
    - "EnglishMonthName" to "Month Name"
    - "MonthNumberOfYear" to "Month Number Of Year"
    - "CalendarQuarter' to "Calendar Quarter"
    - "CalendarYear" to "Calendar Year"
    - "CalendarSemester" to "Calendar Semester"
    - "FiscalQuarter" to "Fiscal Quarter"
    - "FiscalYear" to"Fiscal Year"
    - "FiscalSemester" to "Fiscal Semester"

24. **Rename** all queries that begin with “Dim” by removing the prefix
    “Dim” and putting spaces into multi-word names (i.e. Sales Territory, Product Category etc.).

25. From the queries now named **Geography, Product, Product Subcategory**,
    and **Product Category** also remove the Spanish and French columns, and
    remove the word English from any remaining columns and put spaces into the names of any non-key non-table columns.

26. In the Queries pane select **Product**.

27. Remove the **Description** columns and the **LargePhoto** column.

28. On the **File** menu, click **Save**. When prompted, click **Apply**.

29. Leave Power BI Desktop and Power Query Editor open for the next
    task.

#### Task 2: Editing Data Queries from Excel

1.  In the Queries pane select **Page1**.

2.  In the Applied Steps pane, delete the rows **Changed Type** and **Promoted Headers**

3.  In the ribbon select the **Transform** tab, and then click **Transpose**.

4.  Click **Use First Row As Headers**.

5.  On the column header **2010**, click the down arrow and select **Remove
    Empty**.

6.  Rename **Column1** to **Competitor**.

7.  Rename **Column2** to **Category**.

8.  Select the columns **2007, 2008, 2009, and 2010**, and then in the
    ribbon click **Unpivot Columns**.

9.  Rename the **Attribute** column to **Year**, and the **Value** column to
    **Sales Amount**.

10. Right-click the **Competitor** column and select **Fill** and then **Down**.

11. In the Queries pane select **Page2** and repeat steps 2 to 9 for this
    query
    *Alternatively, you can copy and paste the "M" Power Query Language using the the Advanced Editor window.  Use caution if attempting to edit the "M" using the Advanced Editor.  Copy and paste the code from "Page1" to Notepad then cancel out of the Advanced Editor.  Open the Advanced Editor for "Page2", copy and paste the current "M" below the code from "Page1" in Notepad, this way if the edited code doesn't work you can revert to the previous code.  To reuse the "M" from "Page1" for "Page2" you will need to edit any references to "Page1" so they read "Page2"*

28. On the **File** menu, click **Save**. When prompted, click **Apply Later**.

12. In the ribbon, select the **Home** tab, and then click the down arrow next to **Append Queries** and choose **Append Queries As
    New**.

13. In the **Append** dialog box, set the **Primary table** to be **Page1**, and the
    **Table to append…** to be **Page2** then click on **OK**

14. In the Queries pane, rename the query **Append1** to **Competitor Sales**.

15. In the Queries pane select **Page1**.

16. In the ribbon click **Properties**.

17. In the Query Properties window, deselect **Enable load to report** and
    click **OK**.

18. Repeat above steps for the query **Page2**.

19. On the **File** menu, click **Save**. When prompted, click **Apply**.

20. Leave **Power BI Desktop** open for the next task.

#### Task 3: Editing Data Queries from the Web

1.  In the Queries pane select **Table 0**.

2.  On the **Country** column click the down arrow.

3.  Only select the countries **Australia, Canada, France, Germany, UK**,
    and **USA**.

4.  Replace the values **UK** and **US**A with **United Kingdom** and **United States**
    respectively.

5.  Remove the **Year** column.

6.  Rename the query to **Bike Numbers by Country**.

7.  In the ribbon click **Close & Apply** to close the Query Editor window.

8.  On the File menu click **Save**.

9.  Leave **Power BI Desktop** open for the next Lab.
