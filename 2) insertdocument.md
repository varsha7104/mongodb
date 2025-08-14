# Insert Document
If we store things in collections is called document
There are 2 types of insert to use in database
1) insertOne()
2) insertMany()
   #  InsertOne():
   When we want to insert only single data file
## Syntax :
```
db.collections_name.insertOne({field1:"Value1",field2:Value2})
```
# insertMany():
When we want to insert multiple data then we can use insertMany() when we want do it at once
## Syntax:
```
db.collections_name.insertMany([
{field1:"Value",field2:value2},
{field1:"Value", field2:value}])
```

# findAll():
It is used to output all the details

## Syntax:
```
db.collections_name.find()
```

## Examples:
```javascript
db.students.insertOne({name:"Akshay Kumar",age:25,class:"BCA"})
```
Output:
````
[{
_id:ObjectID('674743904020430990b01d'),
name:'Akshay Kumar',
age:'25'
class:'BCA'
}]

````


```javascript
db.students.insertOne({name:"Sunil Shetty",age:23,class:"BTech"})
```
Output:
````
[{
_id:ObjectID('674743904020430990b01d'),
name:'Akshay Kumar',
age:'25'
class:'BCA'
},
_id:ObjectID('234743904020430990b01d'),
name:'Sunil Shetty',
age:'23'
class:'BTech'
}]

````
## insertMany():
```javascript
db.students.insertMany([{name:"varsha",age:35,class="Mtech"},{name:"hima" ,age:56,class="Btech"}])
```
Output:
````
[{
_id:ObjectID('674743904020430990b01d'),
name:'Akshay Kumar',
age:'25'
class:'BCA'
},{
_id:ObjectID('234743904020430990b01d'),
name:'Sunil Shetty',
age:'23'
class:'BTech'
},
{
_id:ObjectID('147439040204h30990b01d'),
name:"varsha",
age:35,
class="Mtech"
},
{
_id:ObjectID('743904020430990fhfb01d'),
name:"hima" ,
age:56,
class="Btech"
}]

````
