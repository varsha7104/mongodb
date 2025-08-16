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
##  Using find with projection:
### Projection:
Projection simply means which record should be reterived .
#### syntax:
```
db.find({field:"value"},{field1:1,field2:1,field3:0})
```
Here 1 means which should be displayed . 0 means which should be avoided.
----
Another way of writing is :

```
db.collection_name.find().projection({field1:1,field2:1,field3:0})
```
