# Class Management System

## Overview

A web application for managing academic operations, including student and teacher records, courses, departments, assignments, examinations, and results. The repository contains a React client and an Express API backed by MongoDB.

## Features

Repository routes and data models cover:

- Student, teacher, department, course, and class records
- Department-head records
- Assignment records and uploaded files
- Exams, questions, student answers, and results
- Protected requests using JWT authentication middleware
- Exam answer events through Socket.IO

## Technology Stack

- **Frontend:** React 19, Vite, React Router, Socket.IO Client
- **Backend:** Node.js, Express 5, Socket.IO
- **Database:** MongoDB with Mongoose
- **Other libraries:** JWT, bcryptjs, Multer, csv-parser

## Architecture

The React application provides the interface and calls the Express API for data operations. The backend organizes endpoints and Mongoose models by academic domain. The Express server also hosts Socket.IO for real-time exam activity.

## Authentication

The backend includes JWT authentication middleware for protected requests. The README does not publish tokens or credentials; provide local secret values through the backend environment.

## Real-Time Functionality

The backend uses Socket.IO events for student and teacher connections and exam answer submission. The server processes submitted answers and calculates student exam scores.

## Project Structure

- `class/frontend/` — React application, pages, API helper, and UI components
- `class/backend/` — Express server, Mongoose models, middleware, and upload handling
- `class/backend/routes/` — API route modules grouped by domain

## Setup

Requirements: Node.js, npm, and a MongoDB instance.

1. Configure `class/backend/.env` with the backend's `MONGO_URI`, `JWT_SECRET`, and `PORT` values. Keep real credentials local and do not commit them.
2. Install and start the backend:

   ```bash
   cd class/backend
   npm install
   npm run dev
   ```

3. In a second terminal, install and start the frontend:

   ```bash
   cd class/frontend
   npm install
   npm run dev
   ```

The frontend API helper currently targets `http://localhost:5000`; use compatible local server settings.

## Engineering Highlights

- Domain-oriented Express routes and Mongoose models
- JWT authentication middleware
- CRUD-style academic workflows
- File upload handling and CSV parsing dependencies
- Socket.IO exam events and server-side score calculation

## Developer

**Shalom Solomon**  
Full Stack Developer | Mobile App Developer

[Portfolio](https://portfolio-zeta-teal-99.vercel.app) · [GitHub](https://github.com/shalomrich693-code)
