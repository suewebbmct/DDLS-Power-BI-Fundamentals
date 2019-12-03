# Module 1: Introduction to Self-Service BI Solutions

- [Module 1: Introduction to Self-Service BI Solutions](#module-1-introduction-to-self-service-bi-solutions)
  - [Lab: Exploring an Enterprise BI Solution](#lab-exploring-an-enterprise-bi-solution)
    - [Exercise 1: Viewing Reports](#exercise-1-viewing-reports)
      - [Task 1: Prepare the Lab Environment](#task-1-prepare-the-lab-environment)
    - [Exercise 2: Creating a Power BI Report](#exercise-2-creating-a-power-bi-report)
      - [Task 1: Import Data into Power BI Desktop](#task-1-import-data-into-power-bi-desktop)
      - [Task 2: Add Visualizations to the Report](#task-2-add-visualizations-to-the-report)
    - [Exercise 3: Creating a Power BI Dashboard](#exercise-3-creating-a-power-bi-dashboard)
      - [Task 1: Create a Power BI Dashboard](#task-1-create-a-power-bi-dashboard)
      - [Task 2: Ask Questions of Your Data](#task-2-ask-questions-of-your-data)


## Lab: Exploring an Enterprise BI Solution

### Exercise 1: Viewing Reports 

*(can't do this, no SharePoint environment)*

#### Task 1: Prepare the Lab Environment

1. Sue will walk everyone through signing in to PowerBI (through Office.com) and Power BI Desktop

---

### Exercise 2: Creating a Power BI Report

#### Task 1: Import Data into Power BI Desktop

1. On the Taskbar, click **Power BI Desktop**.

6. On the **Power BI Desktop** screen appears, click **Get data**.

7. In the **Get Data** dialog box, in the left pane click **Azure**, in the right pane click **Azure SQL database** and then click **Connect**.

8. In the **SQL Server database** dialog box, in the **Server** box, type **demoazuresqldb.database.windows.net**.

9. In the **Database (optional)** box, type **AdventureWorksDW**, and then click **OK**.

10. If the **Access a SQL Server Database** dialog box appears, change
    it from Windows to Database, and enter the User name of **Student**
    and Password of **Pa$$w0rd**, and then click **Connect**. 
    If these credentials are incorrect, your instructor will provide alternatives.

11. If the **Encryption Support** dialog box appears, click **OK**.

12. In the **Navigator** dialog box, select the **FactInternetSales** check box.

13. Click **Select Related Tables**, and then click **Load**.

14. On the **File** menu, click **Save**.

15. In the **Save As** dialog box, browse to the **D:\\Student\\Lab01\\Starter\\Project** folder, and in the **File name** box, type **Adventure Works Sales 1**, and then click **Save**.

#### Task 2: Add Visualizations to the Report

1. In the **FIELDS** pane, expand **FactInternetSales**, and drag the **SalesAmount** field onto the report canvas to create a column chart.

2. Expand **DimDate**, and drag the **EnglishDayNameOfWeek** field to the **Axis** property.

3. Move the chart to the top left-hand corner of the canvas, and expand the chart width so the days of the week display in full.

4. In the **VISUALIZATIONS** pane, click **Format**, and expand **Title**.

5. In the **Title text** box, type **Sales by Day of Week**.

6. Next to **Alignment**, click the **Center** icon.

7. In the **FIELDS** pane, under **FactInternetSales**, drag the **SalesAmount** field onto the report canvas to create a column chart.

8. Under **DimDate**, drag the **CalendarQuarter** field onto the chart. Notice that there is only one column.

9. In the **VISUALIZATIONS** pane, click **Fields**. Drag the **CalendarQuarter** field from **Value** to **Axis**.

10. Click **Format**, and expand **Title**.

11. In the **Title text** box, type **Sales by Calendar Quarter**.

12. Next to **Alignment**, click the **Center** icon.

13. Expand **Data colors**, change **Show all** to **On**, and for **1**, select **red**, for **2**, select **blue**, and for **3**, select **yellow**.

14. Move the chart to the right of the **Sales by Day of Week** chart, and expand it so both charts are the same height.

15. In the **FIELDS** pane, expand **DimSalesTerritory**, and drag the **SalesTerritoryCountry** column onto the report canvas under the **Sales by Day of Week** chart.

16. Under **FactInternetSales**, drag the **SalesAmount** field onto the map.

17. Expand the map to show all the values.

18. In the **Title text** box, type **Sales by Country**.

19. Next to **Alignment**, click the **Center** icon.

20. In the **FIELDS** pane, expand **DimCustomer**, and drag the **CommuteDistance** field onto the report canvas under the **Sales by Calendar Quarter** chart.

21. Under **FactInternetSales**, drag the **SalesAmount** field onto the chart.

22. In the **VISUALIZATIONS** pane, click **Donut chart**.

23. In the **Title text** box, type **Sales by Commute Distance**.

24. Next to **Alignment**, click the **Center** icon.

25. On the **File** menu, click **Save**.

---

### Exercise 3: Creating a Power BI Dashboard

#### Task 1: Create a Power BI Dashboard

1. In Power BI Desktop, on the **Home** tab, click **Publish**.

2. In the **Publish to Power BI** dialog box, click **My workspace**, and then click **Select**.

3. The report will then be published to the Power BI portal. When the window displays **Success**, close the dialog box.  *Note that we don't want to click the link from here because it will open the report in Internet Explorer, and we want to open it in Chrome.* 

4. From the taskbar, launch **Google Chrome**.  The Power BI Portal should still be open, if not, in the address by type **powerbi.com** and then sign in using the credentials supplied to you at the start of the course.

4. In the black navigation pane down the left side of the screen, click on **My Workspace** and then on **Reports**.  Click on the **Adventure Works Sales 1** report name to open it

5. On the **Sales by Day of Week** column chart, click the pushpin to **Pin visual**.

6. In the **Pin to dashboard** dialog box, click **New dashboard**, type **Adventure Works Sales 1**, and then click **Pin**.

7. On the **Sales by Calendar Quarter** column chart, click **Pin visual**.

8. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

9. On the **Sales by Country** map chart, click **Pin visual**.

10. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

11. On the **Sales by Commute Distance** donut chart, click **Pin visual**.

12. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

13. In the left pane, expand **My Workspace**.

14. Under **DASHBOARDS**, click **Adventure Works Sales 1**.

#### Task 2: Ask Questions of Your Data

1. In the **Adventure Works Sales 1** dashboard, click in the **Ask a question about your data** box.

2. In the **Ask a question about your data** box, type **dim customers**.

3. Power BI shows you a table of the data in the **DimCustomers** table.

4. In the **Ask a question about your data** box, type **how many customer**, and the count of **18484** shows in the results.

5. Click **Pin visual**.

6. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

7. In the **Ask a question about your data** box, type **who is the oldest customer**, and the results show the oldest customer.

8. In the **Ask a question about your data** box, type **how many products are red**, and the result is displayed.

9. In the **Ask a question about your data** box, type **which country has the most male customers**, and a bar chart shows the results. *Note that unless you shaped the data properly, this will likely show an erroneous result as it will be counting the wrong attribute starting with M.  Mine was counting MiddleName.  To check, click on the yellow underlined word "male" and it will show you a list. If you click on the Gender option, it should correct itself to the correct values *

10. Click **Pin visual**.

11. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

12. In the left pane, under **My Workspace**, under **DASHBOARDS**, click **Adventure Works Sales 1**. Scroll down and notice the two additional tiles now appear.

13. Leaving the browser open for the next lab, click on the Power BI Desktop icon in the taskbar to return to that application.

14. If the **Publishing to Power BI** dialog box is still open, click **Got it**.

15. Close Power BI Desktop.
