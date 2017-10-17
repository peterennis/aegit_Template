## aegit_Template is a playground to test & learn to use aegit
You can find the aegit repostory here: https://github.com/peterennis/aegit

## Quickstart

This is assuming you have already setup a GitHub account.

Minimum requirement is Microsoft Access 2010.

1. Fork this repo https://github.com/peterennis/aegit_Template
2. Clone it to your local workspace
3. In the project folder rename the file **aegit_Template.accd** to **aegit_Template.accdb** and run the file **aegit_Template.accdb**
	1. The file **.gitignore** is set to ignore **accdb** files so this work around allows the template file to be available.
4. Open aegit_Template.accdb and open the module **aebasTEST_aegit_template_expClass** in the VBA editor
5. Run the command **aegit_Template_EXPORT** in the Immediate Window
7. Run Compact and Repair
> *IMPORTANT* - Make a backup copy of the database beforehand (Ctr-C, Ctrl-V ***OR*** File -> Save as -> Advanced -> Back Up Database)
8. Review the output in **.\src** and **.\src\xml**
9. Commit and push the changes to GitHub
10. Edit, Export, Compact (Backup), Commit, Rinse & Repeat

## Using aegit with your own database

1. Fork aegit repo to your local workspace: https://github.com/peterennis/aegit
1. Import adaept revision control.accdb to your database and import module **aebasChangeLog_aegit_expClass**, **aebasTEST_aegit_expClass**, and also the class module **aegit_expClass**. 
2. Adjust the public constants that define the path to your project as appropriate. The default values will export data in the project folder that was selected when cloning.

**NOTE:** The class is configured to EXCLUDE the aegit files from export.
  
**NOTE:** Your initial commit of changes will look similar to this
[Second Commit](https://github.com/peterennis/aegit_Template/commit/dd71ff55a71372abcbeadec7ce250f09ff4ad6bd)

If you look at **src/frm_Dummy.frm.txt** there is binary encoding for ImageData
and that is a result of the "Name AutoCorrect Option" setting of Access. So get
rid of it, *then may you live long and prosper!*

*File* -> *Options* -> *Current Database* -> *Name AutoCorrect Options*

>Uncheck: Track name AutoCorrect info

>Uncheck: Perform name AutoCorrect
