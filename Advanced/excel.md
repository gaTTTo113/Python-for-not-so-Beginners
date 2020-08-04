
# read/write Excel files

Python don't have a standard library for working with Excel files. I suggest to use `openpyxl`
`openpyxl` is a Python library to read/write Excel files.
You need to download and install it first using pip:
```
pip install openpyxl
```
Next be sure to import the module:
```
import openpyxl
```
To work with Excel workbooks, create a `Workbook` object:
```
wb = Workbook
```
Or load some file from your machine:
```
wb = openpyxl.load_workbook('some_excel.xlsx')
```
Next you can select some sheet to work with:
```
sheet = wb['Sheet1']
```
Now you can select cells and update values inside them:
```
sheet['a1'] = 'some_text'
cell = sheet.cell(1, 1)
print(cell.value())
```
> some_text

```
digit = 1
for row in range(1, 4)
	sheet.cell(row, 1) = digit
	digit += 1
	print(sheet.cell(row, 1).value())
wb.save()
``` 
> 1 \
> 2 \
> 3

You can find more useful functions and scenarios of `openpyxl` [here](https://openpyxl.readthedocs.io/en/stable/).
