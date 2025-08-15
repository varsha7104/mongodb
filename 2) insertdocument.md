# 📌 MongoDB Guide

This README covers MongoDB **Data Types** and **Document Insertion Methods**.

---

## 📖 Table of Contents

1. [Insert Document](#-insert-document)

---



## 📝 Insert Document

In MongoDB, data is stored inside **collections** as **documents**.

There are **two main methods** for inserting data into a collection:
1. `insertOne()` → Insert a single document.
2. `insertMany()` → Insert multiple documents at once.

---

<details>
<summary>1️⃣ insertOne()</summary>

**Purpose:** Used to insert a **single** document into a collection.

### **Syntax:**
```javascript
db.collection_name.insertOne({field1: "Value1", field2: Value2})
```

### **Example:**
```javascript
db.students.insertOne({name: "Akshay Kumar", age: 25, class: "BCA"})
```

**Output:**
```
[{
  _id: ObjectID('674743904020430990b01d'),
  name: 'Akshay Kumar',
  age: 25,
  class: 'BCA'
}]
```

Another example:
```javascript
db.students.insertOne({name: "Sunil Shetty", age: 23, class: "BTech"})
```

**Output:**
```
[{
  _id: ObjectID('674743904020430990b01d'),
  name: 'Akshay Kumar',
  age: 25,
  class: 'BCA'
},
{
  _id: ObjectID('234743904020430990b01d'),
  name: 'Sunil Shetty',
  age: 23,
  class: 'BTech'
}]
```

</details>

---

<details>
<summary>2️⃣ insertMany()</summary>

**Purpose:** Used to insert **multiple** documents at once.

### **Syntax:**
```javascript
db.collection_name.insertMany([
  {field1: "Value", field2: value2},
  {field1: "Value", field2: value}
])
```

### **Example:**
```javascript
db.students.insertMany([
  {name: "varsha", age: 35, class: "MTech"},
  {name: "hima", age: 56, class: "BTech"}
])
```

**Output:**
```
[{
  _id: ObjectID('674743904020430990b01d'),
  name: 'Akshay Kumar',
  age: 25,
  class: 'BCA'
},
{
  _id: ObjectID('234743904020430990b01d'),
  name: 'Sunil Shetty',
  age: 23,
  class: 'BTech'
},
{
  _id: ObjectID('147439040204h30990b01d'),
  name: 'varsha',
  age: 35,
  class: 'MTech'
},
{
  _id: ObjectID('743904020430990fhfb01d'),
  name: 'hima',
  age: 56,
  class: 'BTech'
}]
```

</details>

---

<details>
<summary>3️⃣ find()</summary>

**Purpose:** Retrieve all documents from a collection.

### **Syntax:**
```javascript
db.collection_name.find()
```

</details>
