# Module 5: Modeling Data

   - [Module 5: Modeling Data](#Module-5-Modeling-Data)
      - [Lab: Modelling Data in Power BI Desktop](#Lab-Modelling-Data-in-Power-BI-Desktop)
         - [Exercise 1: Modelling Data in Power BI](#Exercise-1-Modelling-Data-in-Power-BI)
            - [Task 1: Modifying Field Properties in Power BI](#Task-1-Modifying-Field-Properties-in-Power-BI)
            - [Task 2: Adding Hierarchies](#Task-2-Adding-Hierarchies)
            - [Task 3: Adding Calculated Columns](#Task-3-Adding-Calculated-Columns)
            - [Task 4: Adding Measures](#Task-4-Adding-Measures)
            - [Task 5: Creating and Modifying Relationships](#Task-5-Creating-and-Modifying-Relationships)
            - [Task 6: Adding a Calculated Table](#Task-6-Adding-a-Calculated-Table)

*The exercises for Modules 3 to 6 have been designed by DDLS staff.*
*They replace the exercises published by Microsoft Learning.*

## Module 5

### Lab: Modelling Data in Power BI Desktop

Scenario

Now that the data has been imported, some relationships need to be added
to allow the analysis to occur across all the different sources. Some of
the fields need to be modified so that Power BI can display them
correctly on reports. Creating some hierarchies will be useful later
when visualizations are added to the reports. Additionally, some missing
values required will need to be calculated from the data that has been
imported.

### Exercise 1: Modelling Data in Power BI

#### Task 1: Modifying Field Properties in Power BI

1.  In **Power BI Desktop** click on the **Data** icon on the left hand side.

2.  In the Fields pane on the right hand side, expand the
    **Bike Numbers by Country** table.

3.  Click on the **Quantity** column.

4.  In the ribbon click on the **Modeling** tab.

5.  If the **Quantity** column has a Data Type of **Decimal Number** change
    it to **Whole Number**.

6.  If the **Format** is **General** change it to **Whole Number**.

7.  Make sure the **Default Summarization** is **Sum**. In the Fields pane note
    that a Sigma symbol appears next to the Quantity field.

8.  Click on the **Country** column.

9.  In the ribbon, change the **Data Category** from **Uncategorized** to
    **Country/Region**. In the Fields pane note that a Globe symbol appears
    next to the Country field.

10. In the Fields pane expand **Geography**.

11. Change the Data Category appropriately for the following fields:
    **City, State Province Name, Country Region Name, Postal Code**.

12. On the **File** menu, click **Save**.

13. Leave **Power BI Desktop** open for the next Task.

#### Task 2: Adding Hierarchies

1.  In the Fields pane, in the **Geography** table, select the
    **Country Region Name** column.

2.  Either right-click this column, or click the … , and then select **New hierarchy**.

3.  Drag the **State Province Name** column and drop it on **Country Region Name Hierarchy**.

4.  Drag the **City** column and drop it on **Country Region Name Hierarchy**.

5.  Right click **Country Region Name Hierarchy** and select **Rename**. Change
    its name to **Location**.

6.  Repeat the above steps to create two hierarchies in the **Date** table,
    one for **Calendar Year, Calendar Quarter** and **Month Name**, and one for
    **Fiscal Year, Fiscal Quarter** and **Month Name**. Name them **Calendar Dates** and
    **Fiscal Dates**.

#### Task 3: Adding Calculated Columns

1.  In the Fields pane expand **Customer**.

2.  In the ribbon, on the Modeling tab, click **New Column**.

3.  In the formula bar, highlight **Column =**, type the following code,
    and then press Enter:

> Income Status = IF (Customer\[Yearly Income\] &lt; 25000, "Lower
> Income",
>
> IF (AND(Customer\[Yearly Income\] &gt;= 25000, Customer\[Yearly Income\]
> &lt; 60000), "Middle Income",
>
> IF (AND(Customer\[Yearly Income\] &gt;= 60000, Customer\[Yearly Income\]
> &lt; 100000), "Higher Income",
>
> IF (Customer\[Yearly Income\] &gt;= 100000, "Very High Income",
> "Other"))))

1.  In the ribbon, on the Modeling tab, click **New Column**.

2.  In the formula bar, highlight Column =, type the following code, and
    then press Enter:

> Days Since First Purchase = DATEDIFF(Customer\[Date First Purchase\],TODAY(), DAY)

1.  Click **New Column**.

2.  In the formula bar, highlight **Column =**, type the following code,
    and then press Enter:

> FullName = \[FirstName\] & " " & \[LastName\]

1.  In the Fields pane expand **Internet Sales**.

2.  Click **New Column**.

3.  In the formula bar, highlight **Column =**, type the following code,
    and then press Enter:

> Sales Profit = CURRENCY('Internet Sales'[Sales Amount] - 'Internet Sales'[Total Product Cost])

1.  On the **File** menu click **Save**.

2.  Leave **Power BI Desktop** open for the next task.

#### Task 4: Adding Measures

1.  In the fields expand **Internet Sales**.

2.  In the ribbon on the Modeling tab, click **New Measure**.

3.  In the formula bar, highlight **Measure =**, type the following
    code, and then press Enter:

> Internet Revenue = SUM('Internet Sales'\[Sales Amount\])

1.  In the Fields pane select **Internet Revenue**. In the **Modeling** tab
    change the **Format** to **Currency**  **$ English (United States)**.

2.  In the ribbon on the Modeling tab, click **New Measure**.

3.  In the formula bar, highlight **Measure =**, type the following
    code, and then press Enter:

> Internet Profit = sum('Internet Sales'[Sales Profit])

1.  In the Fields pane select **Internet Profit**. In the **Modeling** tab change
    the **Format** to **Currency**  **$ English (United States)**.

2.  In the ribbon on the Modeling tab, click **New Measure**.

3.  In the formula bar, highlight **Measure =**, type the following
    code, and then press Enter:

> Internet Margin = \[Internet Profit\] / \[Internet Revenue\]

1.  In the Fields pane select **Internet Margin**. In the **Modeling** tab change
    the **Format** to **Percentage**.

2.  In the ribbon on the Modeling tab, click **New Measure**.

3.  In the formula bar, highlight **Measure =**, type the following
    code, and then press Enter:

> Internet Target Margin = (sum('Product'[List Price])-sum('Product'[Standard Cost]))/sum('Product'[List Price])

1.  In the Fields pane select **Internet Target Margin**. In the **Modeling** tab
    change the **Format** to **Percentage**.

2.  On the **File** menu click **Save**.

3.  Leave **Power BI Desktop** open for the next task.

#### Task 5: Creating and Modifying Relationships

1.  In Power BI Desktop click on the **Model** icon on the left hand
    side.

2.  Create a relationship to the **Bike Numbers By Country** table by dragging
    the **Country** column and dropping it on the **Country Region Name** column
    in the **Geography** table. (You might have to scroll across to the
    right to see the table).

3.  Create a relationship to the **Competitor Sales** table by dragging the
    **Category** column and dropping it on the **Product Category Name** column in
    the **Product Category** table.

4.  Then drag the **Year** column and drop it on the **Calendar Year** column of
    the Date table. Note the warning that appears about the **Many-to-Many** relationship because neither column
    has unique values.  Click on **Cancel**

5.  On the **File** menu click **Save**.

6.  Leave **Power BI Desktop** open for the next task.

#### Task 6: Adding a Calculated Table

1.  Click on the **Data** icon on the left hand side.

2.  In the ribbon, on the Modeling tab, click **New Table**.

3.  In the formula bar, highlight **Table =**, type the following code,
    > and then press Enter:

> Years = DISTINCT('Date'\[Calendar Year\])

1.  Click on the **Model** icon.

2.  Drag the **Years** column from the **Competitor Sales** table to the
    **Calendar Year** column of the **Years** table.

3.  Drag the **Calendar Year** column from the **Date** table to the **Calendar Year**
    column of the **Years** table.

4.  On the **File** menu click **Save**.

5.  Leave **Power BI Desktop** open for the next Lab.
