# Error 3622

### Occurs when selecting combo box of Youth Resiliency & Self Sufficiency Assessment

![](img/svip-err-msg.png)

- The error box shows which function the error is occuring in

![](img/err-function.png)

- Go to VBA editor for the database and look for that specific function

![](img/function-search.png)

- When we look inside the function, we see what the error-

    `(You must use the dbSeeChanges option with OpenRecordset when accessing a SQL Server table that has an IDENTITY column)` 

    -above was referencing to:

 ![](img/err-3622-function.png)

- According to Paul, a Microsoft Access MVP on [access-programmers forums](https://access-programmers.co.uk/forums/showthread.php?t=270053), this is the propper syntax for an access database with SQL backend:

    For a recordset:
    ```
    Set rs = db.OpenRecordset(strSQL, dbOpenDynaset, dbSeeChanges)
    ```

- After fixing the code accordingly, the combo box is working again!

![](img/working-combo.png)