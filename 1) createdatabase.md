Database is data stored in it 
It is organised in files 
Mangodb files are called collections
collections contain actual data
Collections contain document
# How to create a database ?
use database_name
It is used to create a new database and we can use existing database
```javascript
db.createCollection("collection_name")
```
## Show DBs
```javascript
show dbs
```
```` Output
Output:
admin
config
local
````
It is used to know the previous existing  database 
## Use Database
```javascript
use school
```
It creates a new database and switches to existing database if it exists
## Creating the new collections
we use createCollection to create a new collection
```javascript
db.createCollection("school")
```
Output:
````
{ok:1}
````
## Showing the collections:
To show the existing collections 
```javascript
show collections
```
Output:
````
school
````
## Rename the collections
We  can rename the collections by using rename collections
```javascript
db.students.renameCollections("student")
```
Output:
````
{ok:1}
````
## To know all the commands
We can use db.help() which is used to know all the commands which can be used with the commands
```javascript
db.help()
```
Output:
````
all the commands
````
We can also use the db.[collection_name].help()

```javascript
db.student.help()
```
Output will contain all the commands related to collections
## To remove the collections from the database 
```javascript
db.library.drop()
```
Output:
````
true
````
True means it is removed
```javascript
db.showcollections
```
Output:
````
student

````
## To drop the database
```javascript
db.dropDatabase()
```
Output:
````
{ok:1 ,dropped:'school'}
````
