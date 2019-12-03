# Module 3: Power BI Data

- [Module 3: Power BI Data](#module-3-power-bi-data)
    - [Lab: Importing Data into Power BI Desktop](#Lab-Importing-Data-into-Power-BI-Desktop)
        - [Exercise 1: Importing Data into Power BI](#Exercise-1-Importing-Data-into-Power-BI)
            - [Task 1: Importing Data from SQL Server](#Task-1-Importing-Data-from-SQL-Server)
            - [Task 2: Import Data from Excel](#Task-2-Import-Data-from-Excel)
            - [Task 3: Import Data from the Web](#Task-3-Import-Data-from-the-Web)
            

*The exercises for Modules 3 to 6 have been designed by DDLS staff.*
*They replace the exercises published by Microsoft Learning.*

### Lab: Importing Data into Power BI Desktop

Scenario

To begin the process of analyzing the Adventure Works data, all the
appropriate data will be imported from various sources. The
AdventureWorksDW SQL Server database has all the company’s sales data,
the excel file has data on competitor’s sales, and the website has
information about the estimated number of bikes owned in each country.

### Exercise 1: Importing Data into Power BI

#### Task 1: Importing Data from SQL Server

1.  From the taskbar launch **Power BI Desktop**.

2.  When the Get Data screen shows, click **Get Data**.

7. In the **Get Data** dialog box, in the left pane click **Azure**, in the right pane click **Azure SQL database** and then click **Connect**.

8. In the **SQL Server database** dialog box, in the **Server** box, type **demoazuresqldb.database.windows.net**.

9. In the **Database (optional)** box, type **AdventureWorksDW**, and then click **OK**.

6.  If the **Access a SQL Server Database** dialog box appears, change
    it from **Windows** to **Database**, and enter the User name of **Student**
    and Password of **Pa$$w0rd**, and then click **Connect**. 
    If these credentials are incorrect, your instructor will provide alternatives.

7.  If the **Encryption Support** dialog box appears, click **OK**.

8.  In the **Navigator** dialog box, select the **FactInternetSales**
    check box, click **Select Related Tables**.

9.  Deselect **DimCurrency, DimPromotion, and FactInternetSalesReason**.

10. Select **DimGeography, DimProductSubcategory and DimProductCategory**.

11. Click **Load** and then wait until the load is completed (*there are just under 2 million rows in the fact table*)

12. On the **File** menu, click **Save** As.

15. In the **Save As** dialog box, browse to the **D:\\Student** folder, and in the **File name** box, type **Adventure Works Sales**, and then click **Save**.

14. Leave Power BI Desktop open for the next task.

#### Task 2: Import Data from Excel

1.  Launch Excel and open the file **D:\\Student\\Competitors.xlsx**

2.  If a dialog box appears saying **Your subscription has expired**, click on the **Sign in** button, click **Accept and start Excel** then click **Sign in**.  Enter the email address you are using for the Office 365 trial provided by Sue on the piece of paper then click **Next**.  Type the password for that account and click **Sign in**.

3.  If There is a pink banner near the top of the screen that says the Subscription has expired, close Excel and launch it again.  If needed, click **Accept and start Excel**.

2.  Note the workbook has two worksheets, each containing a matrix of
    sales information for several competitors to AdventureWorks cycles.
    We will just import the data at this stage, but we will reformat the
    data into something usable later on.

3.  In **Power BI Desktop** click **Get Data** and select **Excel**

4.  Browse to **D:\\Student** and open **Competitors.xlsx**

5.  In the Navigator window select **Page1** and **Page2**, and click **Load**.

6.  On the **File** menu, click **Save**.

7.  Leave Power BI Desktop open for the next task.

#### Task 3: Import Data from the Web

1.  Launch a web browser and go to
    [www.worldometers.info/bicycles/](http://www.worldometers.info/bicycles/).

2.  Note the page has information about global bicycle production and
    quantity. We will be importing the data from the table under “How
    many bicycles are there in the world?”

3.  In **Power BI Desktop** click **Get Data** and select **Other**, and then **Web** and click **Connect**.

4.  In the **From Web** dialogue box enter the URL below and click **OK**
    [www.worldometers.info/bicycles/](http://www.worldometers.info/bicycles/)

5.  In the Navigator window select **Table 0** and click **Load**.

6.  On the **File** menu, click **Save**.

7.  Leave **Power BI Desktop** open for the next Lab.
