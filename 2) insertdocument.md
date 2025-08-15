# 📌 MongoDB Guide

This README covers MongoDB **Data Types** and **Document Insertion Methods**.

---

## 📖 Table of Contents
1. [Data Types](#-data-types)
2. [Insert Document](#-insert-document)

---

## 📦 Data Types

<details>
<summary>1️⃣ String</summary>

**Definition:** Text enclosed in quotes.  

```javascript
name: "Yahoo Baba"
```

</details>

---

<details>
<summary>2️⃣ Double (Floating Point)</summary>

**Definition:** A number with decimal values.  

```javascript
price: 72.50
```

</details>

---

<details>
<summary>3️⃣ 32-bit Integer</summary>

- **Size:** 4 bytes (32 bits)  
- **Range:** `-2,147,483,648` to `2,147,483,647`  

```javascript
age: 25
```

</details>

---

<details>
<summary>4️⃣ 64-bit Integer</summary>

- **Size:** 8 bytes (64 bits)  
- **Range:** `-9,223,372,036,854,775,808` to `9,223,372,036,854,775,807`  

```javascript
bigNumber: 9223372036854775807
```

</details>

---

<details>
<summary>5️⃣ Boolean</summary>

**Definition:** Holds `true` or `false`.  

```javascript
isActive: true
```

</details>

---

<details>
<summary>6️⃣ Array</summary>

**Definition:** Stores multiple values of the same type.  

```javascript
hobbies: ["music", "sports"]
```

</details>

---

<details>
<summary>7️⃣ Object</summary>

**Definition:** Stores different types of data together.  

```javascript
address: {
    street: "123 Main Street",
    city: "New York"
}
```

</details>

---

<details>
<summary>8️⃣ Null</summary>

**Definition:** Represents an intentional empty value.  

```javascript
middleName: null
```

</details>

---

<details>
<summary>9️⃣ Regular Expression</summary>

**Definition:** Specifies pattern-matching conditions.  

```javascript
pattern: /^[A-Za-z0-9]+$/
```

</details>

---

<details>
<summary>🔟 Timestamp</summary>

**Definition:** A numeric value representing date/time (unreadable by humans).  

```javascript
createdAt: 1697591400
```

</details>

---

<details>
<summary>1️⃣1️⃣ Date</summary>

**Definition:** Stores date and time.  

```javascript
// Coordinated Universal Time (UTC)
dob: ISODate("2024-10-18T18:30:00Z")

// Central European Time (+02:00)
dob: ISODate("2024-10-18T18:30:00+02:00")

// Eastern Standard Time (-05:00)
dob: ISODate("2024-10-18T18:30:00-05:00")

// Local Time
dob: ISODate("2024-10-18T18:30")
```

**JavaScript Date Object Examples:**
```javascript
dob = new Date("2024-10-18T18:20:00Z");
dob = new Date(); // Current date and time
```

</details>

---

<details>
<summary>1️⃣2️⃣ Object ID</summary>

**Definition:** Unique identifier generated when creating a document in a database collection.  

```javascript
_id: ObjectId("50f34345fsd08986")
```

</details>

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
