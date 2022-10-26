# Tip-Tricks

## RegEx in T-SQL Query
https://www.sqlshack.com/t-sql-regex-commands-in-sql-server/

## Download File from Kaggle:
```
from IPython.display import FileLink
FileLink(r'./model.h5')
```

## CSV Hacks
1. How to Write data into CSV using `String Builder` and SuperScript the hashstric before data like [LINK](https://stackoverflow.com/questions/23862622/how-to-format-superscript-string-in-c)
```
StringBuilder str = new StringBuilder();
var line = "\xB*InvoiceNo, \xB*Customer, \xB*InvoiceDate, \xB*DueDate, Term, Location, Memo, Item(Product/Service), ItemDescription, " +
                    "ItemQuantity, ItemRate, \xB*ItemAmount, \xB*ItemTextCode, ItemTaxAmount, Currency, ServiceDate";
str.AppendLine(line);
str.AppendLine();

File.WriteAllText("D:\\test.csv", str.ToString());
```
![image](https://user-images.githubusercontent.com/86957308/193277709-f5fb7baf-1612-4609-addc-d6d81078b752.png)


## Visual Studio Code Extensions(Installation Tips):
- prettier
- Material icon theme
- markdown all in one
- one monokai theme
- bracket pair colorization
- auto rename tag
- live server
- Simple React Snippets
- Prettier - Code formatter
- Path intellisense
- ES7+ React/Redux


## ExcelSheet Formulas:
1. Join/Combine every Row of single column with seperated by simething: 
  ``` 
  =TEXTJOIN(";",TRUE,B34:B73)
  ```
2. Transpose all rows into column:
  ```
  =TRANSPOSE(E9:BF9)
  ```
3. Sort every sentence in Lexicography order(Sorting based on a,b,c...) based on word level: Prerequisites - In every sentense every words are seperated by comma
  ```
  =TEXTJOIN(" ",1,SORT(FILTERXML("<x><y>"&SUBSTITUTE(F6,",","</y><y>")&"</y></x>","//y")))
  ```
4. Extract sub-text from string whose sub-text between Bracket "[]" OR "{}" OR"()"
  ```
  =MID(B2,SEARCH("[",B2)+1,SEARCH("]",B2)-SEARCH("[",B2)-1)
  ```
5. General way to extract sub-string from string starts from 'UCM' and also replace brackets as well
  ```
  =SUBSTITUTE(SUBSTITUTE(TRIM(LEFT(SUBSTITUTE(MID(C3,FIND("UCM",C3),LEN(C3))," ",REPT(" ",100)),100)),"[",""),"]","")
  ```
6. Find The Word from String Query
  ```
  =IF(ISNUMBER(FIND("prix",G2,1)),TRUE,FALSE)
  ```
7. Find the Exact Word from String Query
  ```
  =ISNUMBER(SEARCH(" low ", " "&A2&" "))
  ```
8. Find Unique AdInfoScore from Array
  ```
  =UNIQUE(A2:A142)
  ```
9. Find Fiscal Year from Created Date
  ```
  =YEAR(DATE(YEAR(E2),MONTH(E2)+($I$2-1),1))
  ```
  ![image](https://user-images.githubusercontent.com/86957308/189090097-38a6902d-8b43-4c06-b5af-3b1a518218a1.png)
  <br>
10. Find Week Number based on Month in excel
  ```
  =WEEKNUM(E2,2)-WEEKNUM(DATE(YEAR(E2),MONTH(E2),1),2)+1
  ```
  ![image](https://user-images.githubusercontent.com/86957308/197994562-684332c3-3525-415f-bfdd-013c0f94bf2a.png)


## Azure Boards:

1. How to get last week workitem only:
![image](https://user-images.githubusercontent.com/86957308/165046225-e22f3ad5-7db4-4553-8c7e-cc0bcf9bb4e8.png)


## Installing Aether VS Extenstion:

1. Error [Link](https://stackoverflow.com/questions/69218960/cannot-install-an-extension-in-visual-studio-2019-due-to-missing-references/69226397#69226397)
