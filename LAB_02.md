# Module 2: Introducing Power BI

- [Module 2: Introducing Power BI](#module-2-introducing-power-bi)
  - [Lab: Creating a Power BI Dashboard](#lab-creating-a-power-bi-dashboard)
    - [Exercise 1: Connecting to Power BI Data](#exercise-1-connecting-to-power-bi-data)
      - [Task 1: Prepare the Lab Environment](#task-1-prepare-the-lab-environment)
      - [Task 2: Connect to SQL Server from the Power BI Desktop](#task-2-connect-to-sql-server-from-the-power-bi-desktop)
      - [Task 3: Add Charts to the Report](#task-3-add-charts-to-the-report)
      - [Task 4: Publish the Report to the Power BI Portal](#task-4-publish-the-report-to-the-power-bi-portal)
    - [Exercise 2: Create a Power BI Dashboard](#exercise-2-create-a-power-bi-dashboard)
      - [Task 1: Create a New Dashboard](#task-1-create-a-new-dashboard)
      - [Task 2: Add Chart Items to the Dashboard](#task-2-add-chart-items-to-the-dashboard)
      - [Task 3: Customize the Dashboard](#task-3-customize-the-dashboard)
      - [Task 4: Display the Dashboard in Full Screen Mode](#task-4-display-the-dashboard-in-full-screen-mode)


## Lab: Creating a Power BI Dashboard

### Exercise 1: Connecting to Power BI Data

#### Task 1: Prepare the Lab Environment

*(task removed as environment ready)*

#### Task 2: Connect to SQL Server from the Power BI Desktop

1. On the Taskbar, click **Power BI Desktop**.

5. On the **Power BI Desktop** window, in the left-hand pane, click **Get data**.

6. In the **Get Data** dialog box, in the left pane click **Azure**, in the right pane click **Azure SQL database** and then click **Connect**.

7. In the **SQL Server database** dialog box, in the **Server** box, type **demoazuresqldb.database.windows.net**, in the **Database (optional)** box, type **AdventureWorks**, and then click **OK**.

8. If the **Access a SQL Server Database** dialog box appears, change
    it from Windows to Database, and enter the User name of **Student**
    and Password of **Pa$$w0rd**, and then click **Connect**. 
    If these credentials are incorrect, your instructor will provide alternatives.

9. If an **Encryption Support** message is displayed, click **OK**.

10. In the **Navigator** dialog box, select the **Sales.vSalesPerson** check box, and then click **Load**.

11. In the **FIELDS** pane, expand **Sales vSalesPerson** to view all the columns.

12. On the **Home** tab, click **Recent Sources**, and then click **demoazuresqldb.database.windows.net: AdventureWorks**.

13. In the **Navigator** dialog box, select the **Sales.vStoreWithDemographics** check box, and then click **Load**.

14. If the **Connection settings dialog box** appears, ensure **Import** is selected, and then click **OK**.

15. In the **FIELDS** pane, expand **Sales.vStoreWithDemographics** to view all the columns.

16. On the **Home** tab, click the **Get Data** arrow, and then click **SQL Server**.

17. In the **Get Data** dialog box, in the left pane click **Azure**, in the right pane click **Azure SQL database** and then click **Connect**.

18. In the **SQL Server database** dialog box, in the **Server** box, type **demoazuresqldb.database.windows.net**, in the **Database (optional)** box, type **AdventureWorks**, and then expand **Advanced options**, in the **SQL statement (optional, required database)** box, type the following code (or copy and paste from below), and then click **OK**:
    ```
    SELECT TOP 10 P.ProductID, P.Name AS Product, SUM(CAST(LineTotal AS decimal(18,2))) AS LineTotal
    FROM Purchasing.PurchaseOrderDetail AS POD
    INNER JOIN Production.Product AS P
    ON POD.ProductID = P.ProductID
    GROUP BY P.ProductID, P.Name
    ORDER BY LineTotal DESC
    ```

19. If the **Connection settings dialog box** appears, ensure **Import** is selected, and then click **OK**.

20. In the **demoazuresqldb.database.windows.net: AdventureWorks** dialog box, click **Load**.

21. In the **FIELDS** pane, expand **Query1** to view all columns.

22. Right-click **Query1**, click **Rename**, type **Top 10 Selling Products**, and then press Enter.

#### Task 3: Add Charts to the Report

1. In the **VISUALIZATIONS** pane, click **Stacked column chart** to add a control to the report.

2. In the **FIELDS** pane, under **Sales** **vSalesPerson**, drag the **FirstName** field to the **Axis** box in the **VISUALIZATIONS** pane.

3. Drag the **SalesYTD** field to the **Value** box. The chart will populate with the data.

4. On the chart in the report, click and drag the sizer on the right-hand side of the chart to widen the chart and display all the salespeople.

5. Ensure the chart has focus, and then in the **VISUALIZATIONS** pane, click **Format**.

6. Expand **Data colors**, then toggle **Show all** to **On**.

7. Change the color for **Linda**, **Jae**, and **Michael** to red.

8. Click the report canvas then in the **VISUALIZATIONS** pane, click **Pie chart** to add a control to the report. Drag the pie chart to the right of the bar chart, or below if there is not enough space.

9. In the **FIELDS** pane, under **Sales** **vStoreWithDemographics**, drag the **Specialty** field to the **Legend** box in the **VISUALIZATIONS** pane.

10. Drag the **NumberEmployees** field to the **Values** box. The chart will populate with the data and should display three pie sections.

11. Click the report canvas, then in the **VISUALIZATIONS** pane, click **Stacked column chart** to add a control to the report. The chart should be located under the previous charts.

12. In the **FIELDS** pane, expand **Top 10 Selling Products**, drag the **Product** field to the **Axis** box in the **VISUALIZATIONS** pane.

13. Drag the **LineTotal** field to the **Value** box. The chart will populate with the data.

14. Click the **Top 10 Selling Products** chart to give it focus, then in the **VISUALIZATIONS** pane, click **Donut chart**. Note how easy it is to switch to a different chart type.

15. On the chart, grab the sizer on the right-hand side of the donut chart to widen the chart to display all the product names in full.

16. In the **FIELDS** pane, under **Sales vStoreWithDemographics**, click and drag the **AnnualSales** field directly onto the report canvas. See how this automatically creates a column chart.

17. In the **FIELDS** pane, select the **AnnualRevenue** check box, and note that this adds the field to the bar chart.

18. In the **FIELDS** pane, next to the **AnnualRevenue**, click the ellipsis (**...**) , and click **Rename**. Type **Annual Revenue**, and then press Enter.

19. Repeat Step 18 to rename the **AnnualSales** field to **Annual Sales**. Note that the names in the title and legend of the bar chart update accordingly.

20. Click the report canvas, and then in the **VISUALIZATIONS** pane, click **Format**.

21. Expand **Page information**, and in the **Name** box, type **Sales**, and then press Enter. Note the name has changed in the tab at the bottom of the report.

22. On the **File** menu, click **Save**.

23. In the **Save As** dialog box, navigate to **D:\\Student\\Lab02\\Power BI**, in the **File name** box, type **Adventure Works Sales 2**, and then click **Save**.

#### Task 4: Publish the Report to the Power BI Portal

1. In Power BI Desktop, on the **Home** tab, click **Publish**.

2. In the **Publish to Power BI** dialog box, click **My workspace**, and then click **Select**.

3. The report will then be published to the Power BI portal. When the window displays **Success**, close the dialog box.  *Note that we don't want to click the link from here because it will open the report in Internet Explorer, and we want to open it in Chrome.* 

4. From the taskbar, launch **Google Chrome**.  The Power BI Portal should still be open, if not, in the address by type **powerbi.com** and then sign in using the credentials supplied to you at the start of the course.

6. Leave the browser window open for the next lab exercise.

---

### Exercise 2: Create a Power BI Dashboard

#### Task 1: Create a New Dashboard

1. In the Power BI portal, click **My Workspace**.

2. Click **+ Create**, and then click **Dashboard.**

3. In the **Create dashboard** dialog box, in the **Dashboard name** box, type **Adventure Works Sales 2**, and then click **Create**.

4. The blank dashboard canvas will appear in the main window.

#### Task 2: Add Chart Items to the Dashboard

1. Under **My Workspace**, under **REPORTS**, click **Adventure Works Sales 2**. This will open the report in the main window.

2. Position the cursor on the **SalesYTD by FirstName** bar chart, and click **Pin visual**.

3. In the **Pin to dashboard** dialog box, click **Existing dashboard**, and in the list, click **Adventure Works Sales 2**, and then click **Pin**. You will see a notification to say the visual has been pinned.

4. Position the cursor on the **LineTotal by Product** chart, and click **Pin visual**.

5. In the **Pin to dashboard** dialog box, click **Existing dashboard**, and in the list, click **Adventure Works Sales 2**, and then click **Pin**. You will see a notification to say the visual has been pinned.

6. Position the cursor on the **Annual Sales and Annual Revenue** bar chart, and click **Pin visual**.

7. In the **Pin to dashboard** dialog box, click **Existing dashboard**, and in the list, click **Adventure Works Sales 2**, and then click **Pin**. You will see a notification to say the visual has been pinned.

8. Under **My Workspace**, under **DASHBOARDS**, click **Adventure Works Sales 2** to open the dashboard.

#### Task 3: Customize the Dashboard

1. In the **Adventure Works Sales 2** dashboard, position the cursor on the **Annual Sales, Annual Revenue** chart to change the icon to a hand. Then drag the chart to the top left-hand corner of the canvas. It will change places with the **SalesYTD** chart. Notice that the names of the charts have been changed.

2. Position the cursor on the **SalesYTD** chart so the arrow appears in the bottom right-hand corner of the chart. Grab the arrow and widen the chart so it spans the width of the charts above.

3. With the mouse on the **SalesYTD** chart, in the top right-hand corner, click the ellipsis (**...**), and then click **Edit details**.

4. In the **Tile details** pane, in the **Title** box, change the name to **Year to Date** **Sales**.

5. In the **Subtitle** box, type **By Sales Person**, and then click **Apply**.

6. Repeat Steps 3 to 5 for the **LineTotal** chart. Rename the **Title** to **Top 10 Selling Products**. Change the **Subtitle** to **By Sales**.

7. Repeat Steps 3 to 5 for the **Annual Sales, Annual Revenue** chart. Rename the **Title** to **Annual Sales v Annual Revenue**. Change the **Subtitle** to **By Stores**.

#### Task 4: Display the Dashboard in Full Screen Mode

1. On the **Adventure Works Sales 2** dashboard, click **Enter Full Screen Mode** from the menu items on the top right-hand side. Notice that the browser disappears.

2. Notice the floating menu in the bottom right-hand corner of the screen. Click **Fit to Screen** and notice how the screen zooms in to remove as much of the excess background space as possible.

3. Position the cursor on the **Year to Date Sales** tile so the **More options** menu ellipsis appears on the top right-hand corner of the chart. Click the ellipsis, then click **Open in** **focus mode**. The single tile is displayed and fits the screen.

4. On the floating menu, in the bottom right-hand corner of the screen, click **Exit Full Screen Mode**.

5. On the **Year to Date Sales** tile, click **Pin visual**.

6. In the **Pin to dashboard** dialog box, click **New dashboard**, and in the **Dashboard name** box, type **Year to Date Sales**, and then click **Pin**. The **Pinned to dashboard** pop-up displays to confirm the tile has been pinned.

7. In the top left-hand corner of the screen, click **Exit Focus mode** to return to the dashboard.

8. Leaving the browser open for the next lab, click on the Power BI Desktop icon in the taskbar to return to that application.

9. If the **Publishing to Power BI** dialog box is still open, click **Got it**.

10. Close Power BI Desktop.
