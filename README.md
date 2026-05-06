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

## Databricks Utilities (dbutils)

1) dbutils.fs.ls(path) -> Will list down the files in mentioned data path.
2) dbutils.widgets.text(<parametername>, <Default_value>) -> Create a parameter with name and default value.
3) dbutils.widgets.get(<paramatername>) -> Will fetch the value in the mentioned parameter, usage will be like: a=dbutils.widgets.get(<paramtername>).
4) dbutils.secrets.list(scope="databricks_scope") -> In the databricks settings, we need to attach the keyvalut, so we are calling that thing as a databricks scope.
5) dbutils.secrets.get(scope=<scope_name>,key='keyname') -> will get the value of mentioned key from the keyvalut.


## Data Reading
1) spark.read.format("csv").option("header", True).option("inferSchema", True).load(<path_of_the_data>) -> This is a spark command, where are telling that are reading a CSV file, in that consider first line as header and get to know the schema, then spark will get to know the datatypes of each column. if we didn't mention inferSchema, every column is considered as string.
2) 
