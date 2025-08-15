## Datatypes:
Types of datatypes:
1) string: Text which is "Quoted" ex: name:"Yahoo Baba"
2) double:floatvalue ex:72.50
3) 32-bit integer:
   It differs by size .Numeric range -2147483648 to 2147483647 Uses 32 bit (4 bytes ) of memory to store the integer value
5) 64- bit integer:Minimum Value: -9,223,372,036,854,775,808 uses 64 bit (8 bytes) of memory to store the integer value 
Maximum Value: 9,223,372,036,854,775,807
6) boolean:It contain either true or false
7) array:It store same types of data
   ex:hobbies :["music","sports"]
8) object:We can store different types in datatypes  ex:address:{"street":"123 Main Street","city":"New York"}
9) null
10) regular expression :Which can specify conditions
12) timestamp:lengthy numerical value just like date which is unreadable data 
13) date:It stores date ex:dob:ISODate("2024-10-18T18:30:00Z) Starts with yearfollowed by month ,followed date T(menas time ) at last Z means coordinate universal time  .If we add at last 2hours before z it becomes central european time
```javascript
     dob:ISODate("2024-10-18T18:30:00Z") Coordinate Universal Time
    dob:ISODate("2024-10-18T18:30:00+02:00")Central Eureopean time
    dob:ISODate("2024-10-18T18:30:00-05:00") Eastern Standard Time
    dob:ISODate("2024-10-18T18:30")Local Time 
    ```
```javascript
dob=new Date("2024-1018T18:20:00Z")
dob =new Date()
```
15) object id: Unique id is generated when we create a document in the collection
    ex:_id:ObjectId("50f34345fsd08986")
