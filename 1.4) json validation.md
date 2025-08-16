
# MongoDB Data Validation with `createCollection`

When working with MongoDB, it's important to validate data types to ensure we store **perfect and consistent data**.  
MongoDB allows schema validation using **`createCollection`** with `$jsonSchema`. 

---

## Syntax
```javascript
db.createCollection("students", {
  validator: {
    $jsonSchema: {
      required: ["name", "age"],
      title: "Student Object Validation",
      properties: {
        name: {
          bsonType: "string",
          description: "Name must be a string and is required"
        },
        age: {
          bsonType: "int",
          minimum: 5,
          maximum: 20,
          description: "Age must be between 5 to 20"
        },
        course: {
          bsonType: "string",
          enum: ["BCA", "BTech", "BSc"],
          description: "Course must be one of the specified values"
        }
      }
    }
  }
})
```

---

## Notes on BSON Types

Available `bsonType` values:
- `"string"`
- `"bool"`
- `"int"`
- `"double"`
- `"array"`
- `"object"`
- `"date"`

### Additional Rules
- **String**: Can use `enum` to restrict values.
- **Double / Int**: Can use `minimum` and `maximum` (optional, can use either).
- **Array**: Can define `bsonType` for each item in the array.
- **Object**: Can define nested objects.

---

## Example: Object Inside an Object
```javascript
db.createCollection("students", {
  validator: {
    $jsonSchema: {
      title: "Student Object Validation",
      required: ["name", "age", "course", "address"],
      properties: {
        name: {
          bsonType: "string",
          description: "Name must be string and is required"
        },
        age: {
          bsonType: "int",
          minimum: 5,
          maximum: 20,
          description: "Age must be between 5 and 20"
        },
        course: {
          bsonType: "string",
          enum: ["BCA", "BTech", "BSc"],
          description: "Course must be one of BCA, BTech, or BSc"
        },
        address: {
          bsonType: "object",
          required: ["street", "city", "zipCode"],
          properties: {
            street: {
              bsonType: "string",
              description: "Street must be a string and is required"
            },
            city: {
              bsonType: "string",
              description: "City must be a string and is required"
            },
            zipCode: {
              bsonType: "string",
              description: "ZipCode must be a string and is required"
            }
          }
        }
      }
    }
  }
})
```

---

## Testing the Validation
```javascript
db.students.insertOne({ name: "YahooBaba", age: 25, course: "BTech" })
// This will fail because age > 20
```

---

### Summary
- `title` is optional.
- `enum` is used to restrict values.
- Nested objects can also have validation rules.
- MongoDB validation ensures **clean, predictable, and safe** data.
## Mongo DB runCommand()


   In MongoDB, db.runCommand() is used to execute database commands directly — even those that don't have a helper method in the mongo shell.
It’s like a “low-level” way to tell MongoDB:

"Hey, execute this exact command and return the raw result."

Syntax
db.runCommand({ <command_name>: <value>, <option1>: <value1>, ... })


<command_name> → Name of the MongoDB command (e.g., ping, collStats, find, aggregate, etc.).

Options depend on the specific command.

Example 1 — Check if MongoDB is running
db.runCommand({ ping: 1 })


Output:

{ "ok" : 1 }


✅ ok: 1 means the database is alive.

Example 2 — Get statistics about a collection
db.runCommand({ collStats: "students" })


Output:

{
  "ns": "school.students",
  "count": 5,
  "size": 256,
  "storageSize": 4096,
  "ok": 1
}


count → Number of documents

size → Total data size

storageSize → Disk storage used

Example 3 — Create a capped collection
db.runCommand({
  create: "logs",
  capped: true,
  size: 10000
})


Output:

{ "ok": 1 }
