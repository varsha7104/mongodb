# MongoDB Update Document Guide

In MongoDB, documents can be updated using the following commands:

## Update Methods

1. **updateOne()** – Updates the first document that matches the filter.
2. **updateMany()** – Updates all documents that match the filter.

---

### Syntax for `updateOne()`:
```javascript
db.collection_name.updateOne(
  { field: value },
  { $set: { update_field: "new_value" } }
)

## Syntax of Insert Many():
```
db.collection_name.updateMany(field:value},{$set:{update_field:"new_value"})
```
## Update Operators
a) $set – Sets the value of a field to the specified value.
db.students.updateOne({ name: "Akshay Kumar" }, { $set: { age: 30 } })

b) $unset – Removes a field from a document.
db.students.updateOne({ name: "Sunil Shetty" }, { $unset: { class: "" } })

c) $inc – Increments a field by a specified value (can be negative).
db.students.updateOne({ name: "varsha" }, { $inc: { age: 2 } })

d) $mul – Multiplies the value of a field by a specified number.
db.students.updateOne({ name: "hima" }, { $mul: { age: 2 } })

e) $rename – Renames a field.
db.students.updateOne({}, { $rename: { class: "course" } })

f) $currentDate – Sets a field to the current date or timestamp.
db.students.updateOne({ name: "Akshay Kumar" }, { $currentDate: { lastModified: true } })

g) $min – Updates the field only if the specified value is less than the current value.
db.students.updateOne({ name: "varsha" }, { $min: { age: 30 } })

h) $push – Appends a value to an array.
db.students.updateOne({ name: "Akshay Kumar" }, { $push: { hobbies: "cricket" } })

i) $pop – Removes the first (-1) or last (1) element from an array.
db.students.updateOne({ name: "Akshay Kumar" }, { $pop: { hobbies: 1 } })

j) $pull – Removes all array elements that match a condition.
db.students.updateOne({ name: "Akshay Kumar" }, { $pull: { hobbies: "cricket" } })

k) $addToSet – Adds a value to an array only if it doesn’t already exist.
db.students.updateOne({ name: "Akshay Kumar" }, { $addToSet: { hobbies: "reading" } })
## Replace
db.collection_name.replaceOne({field:"Value",{$set:{"new field":value}})
