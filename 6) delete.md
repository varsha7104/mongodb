# DELETE Document
there are 2 types of delete statement They are :
1) deleteOne()
2) deleteMany()
----
## deleteOne():
It deletes the specified condition row 

### Syntax: 
```
db.collection_name.deleteOne({field:"value1"})
```

We need to specify the condition which document should be deleted 

## deleteMany():
It deletes the document in collection that satisifes the above condition

### Syntax:
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
----
## Practical
```
school> use school

school> show collections
```
Output:
````
go
personal
students
````

```

school> db.student.find()
```
Output:
````
[
  {
    _id: ObjectId('68a0123209c2dafb53eec4aa'),
    name: 'Akshay Kumar',
    age: 25,
    class: 'BCA'
  },
  {
    _id: ObjectId('68a0124609c2dafb53eec4ab'),
    name: 'Sunil  Shetty',
    age: 25,
    class: 'BTech'
  },
  {
    _id: ObjectId('68a0125b09c2dafb53eec4ac'),
    name: 'Varsha',
    age: 23,
    class: 'Mtech'
  },
  {
    _id: ObjectId('68a0126709c2dafb53eec4ad'),
    name: 'Hima',
    age: 34,
    class: 'Mtech'
  }
]
````

Delete using name 
-----
```
school> db.student.deleteOne({name:"Varsha"})
```
Output:
````
{ acknowledged: true, deletedCount: 1 }
````
```
school> db.student.find()
```
Output:
````
[
  {
    _id: ObjectId('68a0123209c2dafb53eec4aa'),
    name: 'Akshay Kumar',
    age: 25,
    class: 'BCA'
  },
  {
    _id: ObjectId('68a0124609c2dafb53eec4ab'),
    name: 'Sunil  Shetty',
    age: 25,
    class: 'BTech'
  },
  {
    _id: ObjectId('68a0126709c2dafb53eec4ad'),
    name: 'Hima',
    age: 34,
    class: 'Mtech'
  }
]
````

```
school> db.student.insertOne({name:"Varsha",age:23,class:"Mtech"})
```
Output:
````
{
  acknowledged: true,
  insertedId: ObjectId('68a012d709c2dafb53eec4ae')
}
````
When multiple values are there for single value how deleteOne() behaves
```
school> db.student.deleteOne({class:"Mtech"})
```
Output:
````
{ acknowledged: true, deletedCount: 1 }
````
Showing the Output:

```
school> db.student.find()
```
Output:

````
[
  {
    _id: ObjectId('68a0123209c2dafb53eec4aa'),
    name: 'Akshay Kumar',
    age: 25,
    class: 'BCA'
  },
  {
    _id: ObjectId('68a0124609c2dafb53eec4ab'),
    name: 'Sunil  Shetty',
    age: 25,
    class: 'BTech'
  },
  {
    _id: ObjectId('68a012d709c2dafb53eec4ae'),
    name: 'Varsha',
    age: 23,
    class: 'Mtech'
  }
]
````
To showcase how deleteMany() works we are inserting the value again

```
school> db.student.insertOne({name:"Hima",age:34,class:"Mtech"})
```
Output:
````
{
  acknowledged: true,
  insertedId: ObjectId('68a0131009c2dafb53eec4af')
}
school> db.student.deleteMany({class:"Mtech"})
{ acknowledged: true, deletedCount: 2 }
school> db.student.find()
[
  {
    _id: ObjectId('68a0123209c2dafb53eec4aa'),
    name: 'Akshay Kumar',
    age: 25,
    class: 'BCA'
  },
  {
    _id: ObjectId('68a0124609c2dafb53eec4ab'),
    name: 'Sunil  Shetty',
    age: 25,
    class: 'BTech'
  }
]
````
Deleting all the rows at once:
```
school> db.student.deleteMany({})
{ acknowledged: true, deletedCount: 2 }
```
Showing that we have deleted everything at once 
```
school> db.student.find()
```
Output:
````
````

