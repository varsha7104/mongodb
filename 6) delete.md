# DELETE Document
there are 2 types of delete statement They are :
1) deleteOne()
2) deleteMany()
----
## deleteOne():
It deletes the specified condition row 
Syntax: 
```
db.collection_name.deleteOne({field:"value1"})
```

We need to specify the condition which document should be deleted 
----
## deleteMany():
It deletes the document in collection that satisifes the above condition
Syntax:
```
db.collection_name.deleteMany({field:"value1"})
```
It deletes everything that satisifies the condition

## Note:
If we want to delete all the documents in the collection we can use the deleteMany() Like this
Syntax
```
db.collection_name.deleteMany()
```
