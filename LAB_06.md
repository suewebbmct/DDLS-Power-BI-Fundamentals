# Module 6: Interactive Data Visualizations](#Module 6: Interactive Data Visualizations)
    

- [Module 6: Interactive Data Visualizations](#Module-6-Interactive-Data-Visualizations)
    - [Lab: Visualizations in Power BI Desktop](#Lab-Visualizations-in-Power-BI-Desktop)
        - [Exercise 1: Using Visualizations in Power BI](#Exercise-1-Using-Visualizations-in-Power-BI)
            - [Task 1: Using the Column visualization in Power BI](#Task-1-Using-the-Column-visualization-in-Power-BI)
            - [Task 2: Using Drill Down functionality in Power BI](#Task-2-Using-Drill-Down-functionality-in-Power-BI)
            - [Task 3: Using the Map visualization in Power BI](#Task-3-Using-the-Map-visualization-in-Power-BI)
            - [Task 4: Using the Treemap visualization in Power BI](#Task-4-Using-the-Treemap-visualization-in-Power-BI)
            - [Task 5: Using the Scatter visualization in Power BI](#Task-5-Using-the-Scatter-visualization-in-Power-BI)
            - [Task 6: Using the Gauge visualization in Power BI](#Task-6-Using-the-Gauge-visualization-in-Power-BI)
            - [Task 7: Using the KPI visualization in Power BI](#Task-7-Using-the-KPI-visualization-in-Power-BI)
            - [Task 8: Creating a New Report Page in Power BI](#Task-8-Creating-a-New-Report-Page-in-Power-BI)
        - [Exercise 2: Importing Custom Visualizations in Power BI](#Exercise-2-Importing-Custom-Visualizations-in-Power-BI)
            - [Task 1: Downloading custom visualizations](#Task-1-Downloading-custom-visualizations)
            - [Task 2: Importing custom visualizations](#Task-2-Importing-custom-visualizations)
        - [Exercise 3: Publishing to the Power BI Service](#Exercise-3-Publishing-to-the-Power-BI-Service)
            - [Task 1: Publishing to the Power BI Service](#Task-1-Publishing-to-the-Power-BI-Service)
            - [Task 2: Exploring the Power BI Service](#Task-2-Exploring-the-Power-BI-Service)
            - [Task 3: Editing an existing report in the Power BI Service](#Task-3-Editing-an-existing-report-in-the-Power-BI-Service)
            - [Task 4: Editing a dashboard tile in the Power BI Service](#Task-4-Editing-a-dashboard-tile-in-the-Power-BI-Service)
            - [Task 5: Using Q and A in the Power BI Service to create a report](#Task-5-Using-Q-and-A-in-the-Power-BI-Service-to-create-a-report)


*The exercises for Modules 3 to 6 have been designed by DDLS staff.*
*They replace the exercises published by Microsoft Learning.*

## Module 6

### Lab: Visualizations in Power BI Desktop

Scenario

Now that the data has been imported, shaped and modelled, it’s time to
do some analysis by adding visualizations to a report. Report pages need
to be added for Internet Sales and Reseller Sales. Some custom
visualizations will also be added to provide additional functionality.

### Exercise 1: Using Visualizations in Power BI

#### Task 1: Using the Column visualization in Power BI

1.  In **Power BI Desktop** click on the **Report** icon on the left hand side.

2.  In the Fields pane on the right hand side, expand **Internet Sales**.

3.  Select the checkbox next to **Sales Amount**. This will add a new Clustered Column Chart visualization
    to the report page.

4.  In the Fields pane expand **Date**, and select the **Fiscal Dates** hierarchy. This will add more columns to the chart.

5.  Resize the chart so that all the Year names are visible.

6.  With the chart still selected, in the **Visualizations** pane select **Clustered bar chart**.

7.  Change it back to **Clustered column chart**.

8.  Resize the chart so that it fills the top left quarter of the design surface of the report.

9.  In the Visualizations pane, click the **Format** icon (looks like a paint roller).

10. Expand **Title** and change the **Title Text** to **Internet Sales by Date**.  *Note:  Once you have changed the Title Text to a static value, it will no longer be dynamic.  If you have well named and properly shaped data, you shouldn't need to override the default title text with a static value.  

11. Change the **Alignment** of the Title to center alignment,  the font color to black and the size 10.

12. On the **File** menu, click **Save**.

13. Leave **Power BI Desktop** open for the next task.

#### Task 2: Using Drill Down functionality in Power BI

1.  With the column chart still selected, click the double down arrow
    symbol to drill down to the **Fiscal Quarter** level.

2.  Click the up arrow to go back up to the **Fiscal Year** level.

3.  Click the **expand all** button (looks like an upside down U).

4.  Click the **up arrow** to go back to the **Fiscal Year** level.

5.  Click on the column for **2011**. This just highlights the column.

6.  In the chart, click on the **single down arrow** symbol to turn on **Drill
    Down**.

7.  Click on the column for **2008**. This now drills down to show the data
    for that year only.

8.  Click on the **up arrow** to go back to the **Fiscal Year level**.

9.  Click on the **single down arrow** symbol to turn off **Drill Down**.

10. On the **File** menu click **Save**.

11. Leave **Power BI Desktop** open for the next task.

#### Task 3: Using the Map visualization in Power BI

1.  In the report page click on a blank part of the design surface.

2.  In the Fields pane select the **Location** hierarchy from the **Geography**
    table, and **Sales Amount** from the **Internet Sales** table.

3.  Move and resize the Map chart so the fills the top right quarter of the
    report.

4.  Drag the **Fiscal Year** column from the **Date** table to the Legend field
    in the Visualization pane.

5.  In the column chart, click on a year column. Click on the
    year column again.

6.  Click on the Map visualization.

7.  Remove **FiscalYear** from the Legend field.

8.  Hover the cursor over one of the bubbles and view the pop-up.

9.  Drag the **Order Quantity** column from the **Internet Sales** table to the
    **Tooltips** field in the Visualizations pane.

10. Hover the cursor over one of the bubbles and view the pop-up again.

11. Change the chart title to **Internet Sales by Geography**, center
    aligned, black, size 10.

12. At the bottom of the screen, right click **Page 1** and select **Rename Page**. Name the page **Internet Sales**.

13. On the **File** menu click **Save**.

14. Leave **Power BI Desktop** open for the next task.

#### Task 4: Using the Treemap visualization in Power BI

1.  In the report page click a blank area.

2.  In the Fields pane select **Product Category Name** from the
    **Product Category** table, and **Internet Profit** from the **Internet Sales**
    table.

3.  In the Visualizations pane select **Treemap**.

4.  Resize the Treemap chart to fill the bottom left quarter of the
    report.

5.  Drag the **Fiscal Year** column from the **Date** table to the Group field in
    the Visualization pane.

6.  In the treemap chart experiment with the Drill Down settings used in
    Task 2.

7.  In the Visualizations pane drag **Product Category Name** from the Group
    field to the Details field.

8.  On the **File** menu click **Save**.

9.  Leave **Power BI Desktop** open for the next task.

#### Task 5: Using the Scatter visualization in Power BI

1.  In the report page click a blank area.

2.  In the Fields pane select **Sales Amount** from the **Internet Sales** table.

3.  In the Visualizations pane select **Scatter** chart.

4.  Resize the Scatter chart to fill the bottom right corner of the
    report.

5.  Drag the **Order Quantity** column from the **Internet Sales** table to the Y
    Axis field in the Visualizations pane.

6.  Drag the **Location** hierarchy from the **Geography** table to the Details
    field.

7.  If you get an error, in the Vizualization pane, click the down arrow
    next to **Order Quantity** and select “Sum”.

8.  Drag the **Fiscal Year** column from the **Date** table to the Legend field.

9.  Hover the cursor over one the circles in the scatter chart.

10. In the column chart, click on a year column. Click on the year
    column again.

11. Click on the scatter chart.

12. Drag the **Internet Margin** column from the **Internet Sales** table to the
    Size field.

13. Hover the cursor over one the circles in the scatter chart.

14. In the scatter chart experiment with the **Drill Down** settings.

15. Drag **Fiscal Year** from the **Legend** field to the **Play Axis** field.

16. In the scatter chart, click on the **Play** button.

17. Click on the Play button again and this time pause when the pointer
    gets to 2008.

18. While paused, click on one of the circles in the chart.

19. Click the Play button to let the animation complete.

20. Drag **Fiscal Year** back to the **Legend** field from the **Play Axis** field.

21. On the **File** menu click **Save**.

22. Leave **Power BI Desktop** open for the next task.

#### Task 6: Using the Gauge visualization in Power BI

1.  On the Report page, resize the Treemap and Scatter charts to make
    some room to the right then click on a blank part of the report.

2.  In the Fields pane select **Internet Margin** from the **Internet Sales**
    table.

3.  In the Visualizations pane, select **Gauge**.

4.  In the Fields pane, drag **Internet Target Margin** to the Target value
    field.

5.  In the Visualization pane click on the **Format** icon (paint roller).

6.  Expand **Gauge axis**, and make **Min** equal 0 and **Max** equal 0.45.

7.  Test the Gauge by clicking on the other charts.

8.  On the **File** menu click **Save**.

9.  Leave **Power BI Desktop** open for the next task.

**Task 7: Using the KPI visualization in Power BI.**

1.  On the Report page, resize the Column and Map charts to make some
    room to the right.

2.  Click on a blank area of the report.

3.  In the Fields pane select **Internet Margin** from the **Internet Sales**
    table.

4.  In the Visualizations pane, select KPI.

5.  In the Fields pane, drag **Internet Target Margin** to the Target goals
    field.

6.  In the Fields pane, drag **Fiscal Year** from the **Date** table to the Trend
    axis field.

7.  In the Visualization pane click on the Format icon (paint roller).

8.  Turn the **Trend Axis** off.

9.  If the KPI shows **(Blank)**, in the Filters section change the **Fiscal Year** visual level filter type to **Basic filtering** then select the years 2006 to 2009

9.  Test the KPI by clicking on the other charts.

10. On the **File** menu click **Save**.

11. Leave **Power BI Desktop** open for the next task.

#### Task 8: Creating a New Report Page in Power BI

1.  At the bottom of the **Internet Sales** page, click on the **+** symbol to
    create a new page.

2.  Rename the page as **2009 Sales**.

3.  Go back to the **Internet Sales** page, select all the visualizations
    (Ctrl-A) and copy them to the clipboard (Ctrl-C).

4.  Paste them on to the new page.

5.  Drag **Fiscal Year** from the **Date** table to the “Page level filters”
    area.

6.  Change the filter type to **Basic filtering**  Only select the year 2009.

7.  On the **File** menu click **Save**.

8.  Leave **Power BI Desktop** open for the next Exercise.

### Exercise 2: Importing Custom Visualizations in Power BI

#### Task 1: Downloading custom visualizations

1. On the **Home** Tab of **Power BI Desktop**, in the section titled **Custom Visuals** click **From Marketplace**

2.  A **Power BI Visuals** dialogue box will open.  

3. If **Histogram Chart** is visible in the **Suggested for you** section, click on the **Add** button, otherwise search for **Histogram** and then click on the **Add** button in the search results.

4.  A dialogue box should appear confirming that the visual was successfully imported.  Click on **OK**

#### Task 2: Importing custom visualizations

2.  On the Report page, at the bottom click on the **+** sign to add another
    page to the report.

3.  Rename to page to **Customer Yearly Incomes**.

4.  In the Visualization pane, click on the **Histogram x.x.x** chart to add it to the report page.

8.  From the Fields pane, drag **Yearly Income** from the **Customer** table to
    the **Values** field.

9.  Then drag **CustomerKey** from the **Customer** table to the Frequency
    field.

10. In the **Visualization** pane, click on **Format**.

11. Expand **General**, and change the Bins value to 17.

12. In the ribbon on the **Data / Drill** tab, click **See Data**.

13. Click **See Data** again to return to the report.

14. Click on the elipses (…) in the top right corner of the Histogram chart, and
    select **Export data**.

15. Save the CSV file to the D:\\**Student** folder.

16. Navigate to the file and open it to view the results.

17. Add another Histogram chart that shows **Average of Sales Amount by
    Yearly Income** (copy and paste the Histogram chart and change the
    Frequency field to **Sales Amount** from the **Internet Sales** table then change the aggregation function to **Average**).

7.  On the **File** menu click **Save**.

18. Add another page to the report.

19. Rename the page to **Sales by Time**.

20. Create a stacked column chart that shows **Sales Amount** by
    **Country Region Name**.

21. Resize the column chart so that it takes up the lower half of the
    page.

22. Click a blank area of the page and add a **Slicer** visualization.

23. Drag **FullDateAlternateKey** from the **Date** table to the Field area.

24. Resize the Slicer so that it occupies the upper half of the report.

25. Use the Slicer to adjust which date period is included in this
    report page.

7.  On the **File** menu click **Save**.

26. Add another page to the report.

27. Rename the page to **Sharks**.

1. On the **Home** Tab of **Power BI Desktop**, in the section titled **Custom Visuals** click **From Marketplace**

2.  A **Power BI Visuals** dialogue box will open.  
29. In the Power BI Visuals page, in the Search box, type **Aquarium**.

30. Next to **Enlighten Aquarium** click the **Add** button.

31. Click on **OK** when it has imported the visual.

32. Add the **Aquarium** visual to the report.

33. Drag **Sales Amount** from the **Internet Sales** table to the visual.

34. Drag **Country Region Name** from the **Geography** table to the Fish field.

35. Resize the visual so it takes up most of the page.

36. Click on the **Format** icon (paint roller).

37. Under Series, change **Series 1** to **Sharks**.

38. Change the Title to **Sharks**.

39. On the **File** menu click **Save**.

40. Leave **Power BI Desktop** open for the next Exercise.

### Exercise 3: Publishing to the Power BI Service

#### Task 1: Publishing to the Power BI Service

1.  If Power BI Desktop is not signed in to your Office 365 trial account, in **Power BI Desktop**, in the top right corner click Sign In.  When prompted provide your login name and password.

3.  In the ribbon on the Home tab, click **Publish**.

4.  In the Publish to Power BI window, choose **My workspace** as the
    destination, and click the **Select** button.

5.  When it has successfully published the data, click **Got It**.

6.  Launch Chrome or Firefox and go to the address <http://powerbi.com>

7.  Sign in to the Power BI Service using your credentials.

8.  In the Navigator pane on the left hand side, expand **My Workspace**.

9.  Under **Reports**, click on **Adventure Works Sales**.

10. At the bottom of the report click on each of the pages.

#### Task 2: Exploring the Power BI Service

1.  On the **Internet Sales** page, click on the Gauge chart and pin it to a
    new dashboard called **Sales**.

2.  Under **Dashboards**, click on **Sales**.

3.  Click on the Gauge chart.  Clicking on the chart should navigate you back to the report.

4.  Go the **Sales by Time** page.

5.  In the menu bar across the top, click **Pin Live Page**, and select the
    existing **Sales** dashboard.

6.  Go to the **Sales** dashboard.

7.  Change the Dates selected in the Slicer.

#### Task 3: Editing an existing report in the Power BI Service

1.  Go back to the report and to the **Internet Sales** page.

2.  In the menu bar across the top click **Edit Report**.

3.  Click on the gauge and change the title to **Internet Sales Margin and Target**.

4.  Make the title black, centered and size 10.

5.  In the menu bar click **Save**.

6.  Go the **Sales by Time** page.

7.  Change the title of the Slicer to be **Fiscal Dates**.

8.  Make the title black, centered, and size 10.

9. Turn the **Slicer header** Off.

9.  In the menu bar click **Save**.

10. Go the **Sales** dashboard.

11. Notice the title has changed for the Slicer but not the Gauge.

#### Task 4: Editing a dashboard tile in the Power BI Service

1.  Hover over the Gauge chart and click on the …

2.  Click on the Edit Details icon (looks like a pen).

3.  In the Tile details page change the title to **Internet Sales Margin and Target**, and then click **Apply**.

4.  Hover over the **Sales by Time** tile and click on the …

5.  Click on **Delete tile**  to remove this from the dashboard.

#### Task 5: Using Q and A in the Power BI Service to create a report

1.  On the **Sales** dashboard, click at the top where it says **Ask a question about your data**.

2.  On the Q&A screen type **show margin by product category as column chart**

5.  The words **margin, product category** and **column chart** should have yellow lines underneath indicating that Power BI recognised them.

6.  click on **column chart** to see the other visuals available.  Note that this is not all of them.  Replace **column chart** with **tree**

6.  Change the visual again to **a pie chart**

7.  On the far right, expand Visualizations and explore the settings.

8.  Change the title to **Margin by Product Category**

9.  Make the title black, centered, and size 10.

10. In the top right hand corner click the icon to pin this to the **Sales** dashboard.

11. Go to the **Sales** dashboard and move the **Margin by Product Category** tile so it is below to the Gauge tile added earlier.

12. Play.
