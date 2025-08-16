# Find Document 
It is used to display the values
There are 2 types of find :
1) findOne()
2) findMany()

##   findOne(): 
It is used when we want to reterive only one record at a time.

 ### Syntax:
 ```
db.findOne({field:"value1"})
```
## find():
It is used to reterive all the records which satisify the condition
###  Syntax:
 ```
db.find({field:"value"})
```
## Note: when we want to reterive all the values present in the document .We can use this command

###  Syntax:
```
db.find()
```
