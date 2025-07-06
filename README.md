# MongoDB Exercises

This repository contains a collection of practical exercises to learn and practice MongoDB — a NoSQL document-oriented database. Perfect for beginners who want to understand the core concepts and essential commands of the tool.

---

## Table of Contents

- [What is MongoDB?](#what-is-mongodb)
- [Installation](#installation)
  - [Install on Linux (Ubuntu)](#install-on-linux-ubuntu)
  - [Install on macOS (via Homebrew)](#install-on-macos-via-homebrew)
  - [Check if it's working](#check-if-its-working)
- [Core Concepts](#core-concepts)
  - [JSON](#json-javascript-object-notation)
  - [Collection](#collection)
  - [Document](#document)
- [Basic Methods and Commands](#basic-methods-and-commands)
  - [Insert documents](#insert-documents)
  - [Find documents](#find-documents)
  - [Update documents](#update-documents)
  - [Delete documents](#delete-documents)
- [Repository Structure](#repository-structure)
- [Get Started](#get-started)
- [Contributions](#contributions)
- [References](#references)

---

## What is MongoDB?

MongoDB is a NoSQL database that stores data in BSON documents (a binary extension of JSON). It is highly scalable, flexible, and ideal for applications that handle large volumes of unstructured data. Case sensitive

- Does not use tables like relational databases  
- Stores data in JSON-like documents  
- Supports powerful and flexible queries  
- Enables horizontal scalability  

---

## Installation

### Install on Linux (Ubuntu)

```bash
sudo apt update && \
sudo apt install -y mongodb && \
sudo systemctl start mongodb && \
sudo systemctl enable mongodb
```

### Install on macOS (via Homebrew)

```bash
brew tap mongodb/brew && \
brew install mongodb-community && \
brew services start mongodb/brew/mongodb-community
```

### Check if it's working

```bash
mongosh
```

---

## Core Concepts

### JSON (JavaScript Object Notation)

A lightweight data-interchange format used to represent documents in MongoDB. Example:

```json
{
  "name": "Maria",
  "age": 30,
  "profession": "Developer"
}
```

### Collection

A collection is a group of MongoDB documents, similar to a table in relational databases.

### Document

A document is a JSON-like data structure that contains key-value pairs. Each document is stored in a collection.

---

## Basic Methods and Commands

### Insert documents

```js
db.users.insertOne({ name: "John", age: 25 })

db.users.insertMany([
  { name: "Anna", age: 28 },
  { name: "Carlos", age: 32 }
])
```

### Find documents

```js
db.users.find()

db.users.find({ age: { $gt: 30 } })
```

### Update documents

```js
db.users.updateOne(
  { name: "John" },
  { $set: { age: 26 } }
)
```

### Delete documents

```js
db.users.deleteOne({ name: "Carlos" })
```

---

## Repository Structure

```
mongodb-exercises/
├── README.md
├── exercises/
│   ├── 01-insert.js
│   ├── 02-find.js
│   ├── 03-update.js
│   └── 04-delete.js
```

---

## Get Started

```bash
git clone https://github.com/your-username/mongodb-exercises.git && \
cd mongodb-exercises && \
mongosh
```

Then, run the commands from the exercise files to practice.

---

## Contributions

Contributions are welcome! Feel free to open issues or submit pull requests with new exercises or improvements.

---

## References

- https://www.mongodb.com/docs/
- https://university.mongodb.com/

---

Made for those who want to master modern databases.
