## Todo List App

This is a simple To-Do List application built with JavaScript using Express.js, Body-parser, and PostgreSQL for the database.

# Demo

https://github.com/AthanasiosOikonomou/to-do-list/assets/87909481/671f6e61-410f-4739-8eb8-02b39e444e71

# Project Structure

The project consists of four main files:

1) Public Folder:

Contains assets, including two SVG files.
Styles folder with CSS.

2) Views Folder:

Partials folder with footer.ejs and header.ejs.

3) index.ejs.

4) index.js:
   
Main server file that sets up the Express app.
Handles routes and interacts with the PostgreSQL database.

# Setup

Before running the application, make sure to install the required dependencies:

npm install

# Database Configuration

Edit the database connection details in index.js:

const db = new pg.Client({
  user: "postgres",
  host: "localhost",
  database: "permalist",
  password: "Your Password",
  port: 5432,
});
db.connect();

# Running the App
To start the server, run the following command:

nodemon index.js

The application will be accessible at http://localhost:3000/.

# Routes

1) GET /:
Renders the main page with the to-do list items.

2) POST /add:
Adds a new item to the to-do list.

3) POST /edit:
Edits an existing item on the to-do list.

4) POST /delete:
Deletes an item from the to-do list.

# Usage

Visit http://localhost:3000/ in your web browser.
Add, edit, or delete items as needed.

# Notes

The application uses PostgreSQL as the database. Ensure you have a PostgreSQL server running and update the connection details in index.js.
Make sure to handle sensitive information, such as passwords, securely in a production environment.

# Thanks

I would like to thank Dr. Angela Yu for her helpful courses.
