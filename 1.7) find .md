# Find Document 
It is used to display the values
There are 2 types of find :
1) findOne()
2) findMany()

##   findOne(): 
It is used when we want to reterive only one record at a time.

 ### Syntax:
 ```
db.collection_name.findOne({field:"value1"})
```
## find():
It is used to reterive all the records which satisify the condition
###  Syntax:
 ```
db.collection_name.find({field:"value"})
```
## Note: when we want to reterive all the values present in the document .We can use this command

###  Syntax:
```
db.collection_name.find()
```
##  Using find with projection:
### Projection:
Projection simply means which record should be reterived .
#### syntax:
```
db.collection_name.find({field:"value"},{field1:1,field2:1,field3:0})
```
Here 1 means which should be displayed . 0 means which should be avoided.
----
Another way of writing is :

```
db.collection_name.find().projection({field1:1,field2:1,field3:0})
```
## Mongodb find() with count():
It is used to count the no of records that satisify the given condition.
### Syntax:
```
db.collection_name.find().count()
```
## find() using sort()
It sorts the values either in ascending order or descending order .
Ascending order: 1
Descending order :-1
### Syntax:
```
db.collection_name.find().sort(1)
```
## find() using limit:
 Limit is used to find required no of  records
 ### Syntax:
```
db.collection_name.find().limit(3)
```

## find() using limit and skip :
 Limit is used to find required no of  records.Skip will allow you to skip upto required value then allows limit to reterive those many values
 ### Syntax:
```
db.collection_name.find().limit(3).skip(3)
```
After 3 records it will take next 3 records as the output.

