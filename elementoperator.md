# Element  Query operator:
There are 2 types in element query operator:
1)$exists
2) $type
## $exists:
Matches document that have specified value
### Syntax:
```
{field:{$exists:<boolean>}}
```
It can be either true or false
If we specify the true it means we reterive records which satisify the condition

## $type:
Selects the documents if a field is of specified type.
### Syntax:
````
{field:{$type:<type>}}
````
We can pass all of the types which are supported in the mongodb
