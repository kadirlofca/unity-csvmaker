# unity-csvmaker
Attach this component to your Unity Engine objects to easily manipulate a table of strings and export as a .csv file.

# How to initialize a table.
Once you attach the CSVMaker component to your gameobject, you will have to enter some parameters through the inspector.
- File Name : name of the file that will be created. If you enter "myfile", the result will look like "yyyy.mm.dd_hh.mm.ss_myfile.csv".
- Local Path: the path of the folder you want your .csv to be created. If you enter "myfolder/subfolder", the path will look like "MyProject/Assets/myfolder/subfolder/".
- Attributes: this array of strings will contain the names of the columns. Attributes can be empty strings. You must have at least 1 attribute. Unlike rows, you can not create attributes on runtime.

# How to write on a cell.
Use the SetCell(int \_row, int \_col, string \_value) function to write any string value inside a cell at location (\_col, \_row). You can write on any row, however, you can not write on cells outside the bounds of the attributes (number of columns can not be changed once initialized). The function will return without executing, and log a message on the console instead.
