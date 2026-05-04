# databricksnotes


## Magic Commands
These commands will change the language of the cell to the metioned  

1) %python
2) %sql
3) %r
4) %md

**Create Dataframe**

mydata = [(1,"aa",30),(2,"bb",40),(3, "cc",90)]  
myschema="id INT, name STRING, marks INT"  

df=spar.CreateDataFrame(mydata, schema=myschema)  

**Display Dataframe**

df.display()
