MongoDB Bookstore CRUD Operations
Setup and Installation
Prerequisites
MongoDB Community Server installed (version 4.4+ recommended)

MongoDB Shell (mongosh) installed

Node.js (optional, only needed if using the provided insert_books.js script)

1. Database Setup
Option A: Using the provided script (recommended)
Clone this repository

Navigate to the project directory

Run the data insertion script:

bash
node insert_books.js
Option B: Manual Setup
Start MongoDB server:

bash
mongod --dbpath "C:\data\db"
(Create the directory first if it doesn't exist: mkdir C:\data\db)

Connect to MongoDB shell:

bash
mongosh
Create and switch to the database:

javascript
use plp_bookstore
Create the books collection and insert sample data:

javascript
db.books.insertMany([
  {
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    published_year: 1960,
    price: 12.99,
    in_stock: true,
    pages: 336,
    publisher: "J. B. Lippincott & Co."
  },
  // Add other books as needed
])
2. Running the Queries
Ensure MongoDB is running (as shown above)

Connect to the MongoDB shell:

bash
mongosh
Switch to your database:

javascript
use plp_bookstore
Execute any of the queries from the sections below

Task 2: Basic CRUD Operations
[Previous CRUD operations content remains the same...]

Task 3: Advanced Queries
[Previous advanced queries content remains the same...]

Task 4: Aggregation Pipeline
[Previous aggregation content remains the same...]

Task 5: Indexing
[Previous indexing content remains the same...]

Troubleshooting
Common Issues
Connection refused errors:

Ensure MongoDB service is running (net start MongoDB on Windows)

Verify the port 27017 isn't blocked

Data directory issues:

bash
mkdir -p /data/db  # Linux/Mac
mkdir C:\data\db   # Windows
Authentication problems:

If you enabled auth, connect with credentials:

bash
mongosh -u username -p password --authenticationDatabase admin
License
This project is open source and available under the MIT License.