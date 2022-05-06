# Tip-Tricks

## Download File from Kaggle:
```
from IPython.display import FileLink
FileLink(r'./model.h5')
```

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


## Azure Boards:

1. How to get last week workitem only:
![image](https://user-images.githubusercontent.com/86957308/165046225-e22f3ad5-7db4-4553-8c7e-cc0bcf9bb4e8.png)
