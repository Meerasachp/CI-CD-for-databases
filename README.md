Node.js PostgreSQL Todo Application
A simple Node.js application demonstrating database migrations with PostgreSQL using node-pg-migrate.

Features
PostgreSQL database integration
Database migrations using node-pg-migrate
Environment-based configuration
Simple todo management system

Prerequisites
Node.js (v14 or higher)
PostgreSQL database server
npm (Node Package Manager)
Project Structure
├── migrations/
│   └── 1698765432345_create-todos-table.js
├── .env.example
├── .env
├── index.js
├── package.json
└── README.md

Setup
Clone the repository
Install dependencies:
npm install
Create a .env file based on .env.example:
cp .env.example .env
Update the .env file with your PostgreSQL connection details:
DATABASE_URL=postgres://username:password@localhost:5432/database_name
Database Migrations
This project uses node-pg-migrate for managing database schema changes.

Available Migration Commands
Run all pending migrations:
npm run migrate:up
Revert the last migration:
npm run migrate:down
Current Migrations
1698765432345_create-todos-table.js
Creates the initial todos table with:
id (Primary Key)
title (varchar)
completed (boolean)
created_at (timestamp)
Running the Application
Start the application:

npm start
The application will:

Connect to the PostgreSQL database
Display the current timestamp
List all todos in the database
Environment Variables
Variable	Description	Example
DATABASE_URL	PostgreSQL connection URL	postgres://username:password@localhost:5432/todos
Security Notes
Never commit the .env file to version control
Keep your database credentials secure
The .env.example file should not contain actual credentials
Scripts
npm start - Run the application
npm run migrate - Run database migrations
npm run migrate:up - Apply pending migrations
npm run migrate:down - Revert the last migration
Dependencies
pg - PostgreSQL client for Node.js
node-pg-migrate - Database migration tool
dotenv - Environment variable management
