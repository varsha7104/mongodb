# Mangodb comparsion operator
We will be searching the data in case for find(),updateMany(),deleteMany()
## Comparsion Operator:
1) $eq: eq values are equal ``` {"age":{$eq:20}}```
2)  $ne : Values are not equal  ``` {"age":{$ne:20}}```
3) $gt: Value is greater than the value : ``` {"age":{$gt:20}}```
4) $gte:Value is greater than  or equal to the value : ``` {"age":{$gte:20}}```
5) $lt: Value is less than the value : ``` {"age":{$lt:20}}```
6) $lte:Value is less  than or equal to  the value : ``` {"age":{$lte:20}}```
7) $in: Value is matched in array : ``` {"age":{$in:[20,24,28]}}```
8) $nin: Value that is not  matched in array : ``` {"age":{$nin:[20,24,28]}}```
