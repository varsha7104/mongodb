# 🗄️ MongoDB - Database Basics

A **Database** is a collection of organized data.  
In **MongoDB**:
- Files are called **collections**.
- **Collections** contain **documents** (actual data).

---

<details>
<summary>1️⃣ Creating / Using a Database</summary>

**Command:**  
```javascript
use database_name
```
- Creates a **new database** (if it doesn't exist).
- Switches to an **existing database** (if it exists).

**Example:**
```javascript
use school
```

---

**Creating a New Collection:**
```javascript
db.createCollection("collection_name")
```
**Example:**
```javascript
db.createCollection("school")
```
**Output:**
```
{ ok: 1 }
```

</details>

---

<details>
<summary>2️⃣ Show Databases</summary>

**Command:**
```javascript
show dbs
```
**Output:**
```
admin
config
local
```
- Shows all **existing databases**.

</details>

---

<details>
<summary>3️⃣ Show Collections</summary>

**Command:**
```javascript
show collections
```
**Output:**
```
school
```

</details>

---

<details>
<summary>4️⃣ Rename Collection</summary>

**Command:**
```javascript
db.students.renameCollection("student")
```
**Output:**
```
{ ok: 1 }
```

</details>

---

<details>
<summary>5️⃣ Help Commands</summary>

**To list all database commands:**
```javascript
db.help()
```

**To list all commands for a specific collection:**
```javascript
db.student.help()
```

</details>

---

<details>
<summary>6️⃣ Remove a Collection</summary>

**Command:**
```javascript
db.library.drop()
```
**Output:**
```
true
```
`true` means the collection is removed.

**Example check after deletion:**
```javascript
show collections
```
**Output:**
```
student
```

</details>

---

<details>
<summary>7️⃣ Drop a Database</summary>

**Command:**
```javascript
db.dropDatabase()
```
**Output:**
```
{ ok: 1, dropped: 'school' }
```

</details>
