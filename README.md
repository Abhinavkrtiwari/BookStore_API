Bookstore Server
Test Questions
Bookstore Sales System
Technologies Used:
Express.js

Express Generator

Sequelize (ORM for database management)

MySQL (Database)

Data Design
ERD (Entity-Relationship Diagram)

API Planning

API Documentation

Installation Guide
Installing Express Generator
sh
Copy
Edit
npm install -g express-generator
This command installs Express Generator globally.

Check Express Generator Settings
sh
Copy
Edit
express -h
This command displays available settings and options in Express Generator.

Create an Express Project Automatically
sh
Copy
Edit
express --no-view bookstore-server
This generates an Express project with default configurations.

Install All Dependencies
sh
Copy
Edit
npm install
This installs all dependencies listed in the package.json file.

Install Nodemon for Auto-Restart
sh
Copy
Edit
npm install -g nodemon
This installs Nodemon globally, enabling automatic restarts when changes are made.

Install Sequelize and MySQL
sh
Copy
Edit
npm install --save sequelize mysql2
This installs Sequelize ORM and MySQL database driver.

Install Sequelize CLI for Development
sh
Copy
Edit
npm install --save-dev sequelize-cli
This installs Sequelize CLI as a development dependency for database migrations and model management.

Install Bcrypt.js for Password Encryption
sh
Copy
Edit
npm install bcryptjs
This package is used to hash passwords for security.

Install JSON Web Token for Authentication
sh
Copy
Edit
npm install jsonwebtoken
This package is used to generate and verify authentication tokens (JWT).

Install Multer for File Uploads
sh
Copy
Edit
npm install multer
This package handles image uploads in the project.

Install PostgreSQL Dependencies for Production
sh
Copy
Edit
npm install --save pg pg-hstore
These packages allow the project to use PostgreSQL as a production database (e.g., for deployment on Heroku).

Sequelize Commands for Database Management
Initialize Sequelize in the Project
sh
Copy
Edit
npx sequelize-cli init
This command generates the following directories:

config/

models/

migrations/

seeders/

Create a Database
sh
Copy
Edit
npx sequelize-cli db:create
This creates a database based on the configuration in config.json.

Drop (Delete) a Database
sh
Copy
Edit
npx sequelize-cli db:drop
This removes the database as specified in config.json.

Sequelize Commands for Table Creation
Generate a User Model and Migration
sh
Copy
Edit
npx sequelize-cli model:generate --name User --attributes name:string,email:string,password:string,role:enum
Creates a Users table with specified attributes.

Generate a Category Model and Migration
sh
Copy
Edit
npx sequelize-cli model:generate --name Category --attributes name:string,user:integer
Creates a Categories table.

Generate a Book Model and Migration
sh
Copy
Edit
npx sequelize-cli model:generate --name Book --attributes title:string,user:integer,category:integer,author:string,image:text,published:date,price:integer,stock:integer
Creates a Books table.

Generate a Transaction Model and Migration
sh
Copy
Edit
npx sequelize-cli model:generate --name Transaction --attributes invoice:string,user:integer,date:date
Creates a Transactions table.

Generate a DetailTransaction Model and Migration
sh
Copy
Edit
npx sequelize-cli model:generate --name DetailTransaction --attributes transaction:integer,user:integer,book:integer,titleBook:string,imageBook:string,priceBook:integer,quantity:integer
Creates a DetailTransactions table.

Run Migrations to Create Tables
sh
Copy
Edit
npx sequelize-cli db:migrate
Executes all pending migrations to create tables in the database.

Undo All Migrations (Delete All Tables)
sh
Copy
Edit
npx sequelize-cli db:migrate:undo:all
Removes all tables from the database.

Sequelize Commands for Seeders
Generate a Seeder for Users
sh
Copy
Edit
npx sequelize-cli seed:generate --name seeder-user
Creates a seeder file for users.

Generate a Seeder for Categories
sh
Copy
Edit
npx sequelize-cli seed:generate --name seeder-category
Creates a seeder file for categories.

Generate a Seeder for Books
sh
Copy
Edit
npx sequelize-cli seed:generate --name seeder-book
Creates a seeder file for books.

Run Seeders to Populate Tables with Sample Data
sh
Copy
Edit
npx sequelize-cli db:seed:all
Executes all seeders and populates the database.

Undo All Seeders (Delete Seeded Data)
sh
Copy
Edit
npx sequelize-cli db:seed:undo:all
Removes all seeded data.

Reset Auto-Increment IDs
sh
Copy
Edit
npx sequelize-cli db:drop
Resets the ID count in tables.

Sequelize Documentation Command
sh
Copy
Edit
npx sequelize-cli -h
Displays all available Sequelize commands.

Running the Express Server
sh
Copy
Edit
npm run start
This starts the Express server.

Sequelize Migration Terms
UP
Used to create tables or insert data.

DOWN
Used to delete tables or remove data.

SequelizeMeta Table
Stores all executed migrations for tracking.
