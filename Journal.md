# Project Journal

## Part 1/17 - Initial Server Setup & Database Foundation

### Commit Message
```
Initial setup: Install dependencies and create Express server with Posts table

- Install core dependencies: cors, express, mysql2, nodemon, sequelize, sequelize-cli
- Initialize Express server on port 3001
- Create Posts database model/table using Sequelize ORM
- Configure Sequelize to sync with database on server startup
```

### What Was Done

#### Dependencies Installed
- **cors** (^2.8.5) - Cross-Origin Resource Sharing middleware for Express
- **express** (^5.2.1) - Web framework for Node.js
- **mysql2** (^3.16.0) - MySQL database driver
- **nodemon** (^3.1.11) - Development tool for auto-restarting server on file changes
- **sequelize** (^6.37.7) - ORM (Object-Relational Mapping) for database operations
- **sequelize-cli** (^6.6.3) - CLI tool for Sequelize migrations and seeders

#### Server Implementation
- Created main server file: `server/index.js`
- Configured Express app with `require('express')`
- Set up database synchronization with `db.sequelize.sync()`
- Server listens on port 3001

#### Database Model
- Created Posts table model: `server/models/Posts.js`
- Defined using Sequelize ORM for structured data management

### Files Created/Modified
- `server/index.js` - Main server entry point
- `server/package.json` - Project dependencies and scripts
- `server/models/Posts.js` - Posts table model
- `server/models/index.js` - Database initialization

### Notes: Database tooling on Linux

- Attempted to install MySQL Workbench and MySQL server engine, but encountered compatibility issues on my Linux antiX system.
- Installed **MariaDB** as an alternative server engine and used the **Beekeeper Studio AppImage** as a GUI client.
- Successfully created a database in MariaDB and connected the `Posts` table to that database via the GUI.
- This workaround enabled local development and verification of the Sequelize `Posts` model.

---

**Status**: Part 1 Complete  
**Date Started**: December 22, 2025

## Part 2/17 - Express Router for Posts with GET and POST Endpoints

### Commit Message
```
Add Express router for Posts with GET and POST endpoints

- Create Posts router with RESTful endpoints
- Implement GET endpoint to retrieve posts
- Implement POST endpoint to create new posts
- Integrate router with main Express application
```

### What Was Done

#### Router Implementation
- Created Posts router: `server/routes/Posts.js`
- Implemented GET endpoint for retrieving posts
- Implemented POST endpoint for creating new posts
- Integrated router with main server file using `app.use('/posts', postRouter)`

#### API Testing Tool Selection
- Evaluated three API testing tools: **Bruno**, **Insomnia**, and **Postman**
- Selected **Bruno** for the following reasons:
  - Easier installation process
  - Distributed as a lightweight app image (AppImage format)
  - Lower resource consumption
  - Better performance on slower systems (important for my laptop setup)

### Files Created/Modified
- `server/routes/Posts.js` - Posts router with GET and POST endpoints
- `server/index.js` - Added post router integration

### Tools Added
- **Bruno** - API testing and development tool for testing REST endpoints

### Notes: API Testing Tool Choice
- Bruno was selected over alternatives due to installation simplicity and lightweight nature
- The app image format provides better compatibility and portability on antiX Linux
- Superior performance on resource-constrained systems like my current laptop

---

**Status**: Part 2 Complete  
**Date Completed**: December 22, 2025
