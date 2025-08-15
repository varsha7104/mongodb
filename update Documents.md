# Update Document:
There are 2 commands for updating in mongodb:
update One(),updateMany()
Update contains 2 values like filter ,update (set )
Only First Value which is matched with this is updated
### Syntax for InsertOne():
```
db.collection_name.updateOne({field:value},{$set:{update_field:"new_value"})
```
## Syntax of Insert Many():
```
db.collection_name.updateMany(field:value},{$set:{update_field:"new_value"})
```
