# Make Your Ribbons Do Something

### Open Specific Form

XML Code:

    ```
    <button id="btn1" label="Contacts" imageMso="BlogHomePage"
        size="large" supertip="Open Contacts Form"
        tag="frmContacts" onAction="ribOpenForm"
        />
    ```

> `onAction` decides which function will be run

VBA Sub:

    ```
    Option Compare Database
    Option Explicit


    'open the form that is specified in the ribbon tag property

    Public Sub ribOpenForm(Control As IRibbonControl)
        DoCmd.OpenForm (Control.Tag)
        
    End Sub
    ```

> Add the vba code under a new module
 