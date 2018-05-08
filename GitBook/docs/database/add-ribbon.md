# Add Custom Ribbon to your Microsoft Access Databse

1. Go to Navigation Options

    ![](./img/navigation-options.png)

2. Check `Show System Objects` and press OK

    ![](./img/show-objects.png)

3. Under Options -> Client Settings, check `Show add-in user interface errors`

    ![](./img/show-error.png)

4. Create a table called USysRibbons

    > Hide table by checking `hidden` under table properties

5. Create new form to allow us to input XML for ribbon configuration

    > Also hide the form under form properties

    ![](./img/form-design.png)

    **Connect form to ribbons table**

    ![](./img/connect-form.png)

6. Add appropriate fields in form

    ![](./img/fields.png)

### Add your ribbon XML

![](./img/ribbon-xml.png)

- You can create multiple entries for various users (e.g. Developer, User)

- You can select which custon ribbon xml to use in settings

![](./img/ribbon-select.png)


