## Link SQL Server Tables to MS Access using ODBC

> IMPORTANT: Back up your database! (Ctrl + c, Ctrl + v)

- This guide is assuming that you have your SQL Database set up and you've configured an ODBC connection already


1. Delete all your existing tables 

    ![](img/delete-tables.png)

2. Select "ODBC Database" under "External Data" tab in MS Access

    ![](img/odbc-db.png)

3. 

    ![](img/link-tables.png)

4. Select your ODBC Database

    ![](img/select-odbc-db.png)

5. Select tables to link (ones that proceed with dbo)

    ![](img/import-tables.png)

6. Rename the linked tables for your database to recognize (delete "dbo_")

    ![](img/rename-dbo.png)

> IMPORTANT: If you modify the name of the table in the SQL Server, you need to delete the linked table in MS Access and re-import the renamed table. 