# 📌 Data Types Overview

This README explains common data types, their memory usage, ranges, and examples.

---

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
```javascript
db.personal.insertOne({name:"Yahoo Baba",//String
age:25,//Integer
married:false,//booolean
dob:ISODate("2000-10-15T08:00:00Z")//UTC Format
weight:75.6,
kids:null,
hobbies:["Sports","chess"]//array
address:{music:"samayama",
lyriclength:34,}//Objects

})
```

