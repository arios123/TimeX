<div align="center">

# TimeX

**A time-based service marketplace platform connecting community needs with service providers**

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.1.6-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Ionic](https://img.shields.io/badge/Ionic-8.0.0-3880FF?logo=ionic&logoColor=white)](https://ionicframework.com/)
[![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-3.11.4-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Vite](https://img.shields.io/badge/Vite-5.2.0-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)

</div>

## Tech Stack

### Frontend
- **React 18** - Modern UI library with **hooks** and **component-based architecture**
- **TypeScript** - Type-safe development with **static typing**
- **Ionic React** - Cross-platform mobile framework with **responsive design**
- **Vite** - Fast build tool and **development server**
- **React Router** - **Client-side routing** and navigation
- **Axios** - **HTTP client** for API communication

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - **RESTful API** framework
- **MySQL** - **Relational database** management system
- **bcrypt** - **Password hashing** and security
- **CORS** - Cross-origin resource sharing

## Overview

TimeX is an innovative **time-based service marketplace** that revolutionizes how communities connect and exchange services. Instead of traditional currency, users trade time as the primary medium of exchange, creating a **peer-to-peer economy** where community members can post service requests and offer their skills.

The platform features a **full-stack web application** with a **responsive mobile-first design**, enabling users to seamlessly browse, post, and manage service opportunities. Built with modern **web development** practices, TimeX implements **user authentication**, **real-time messaging**, and a comprehensive **job management system**.

## Key Features

- **User Authentication & Authorization** - Secure **signup/login** system with **password encryption** using bcrypt
- **Job Posting & Management** - Create, browse, and manage service listings with detailed descriptions
- **Search & Discovery** - Advanced search functionality to find relevant service opportunities
- **Real-time Messaging** - **Private messaging system** for communication between users
- **Social Features** - Friend management and user profiles
- **Job Acceptance & Finalization** - Complete workflow from job posting to completion
- **Admin Dashboard** - Administrative interface for platform management
- **Cross-platform Support** - **Progressive Web App** capabilities with Capacitor for native mobile deployment
- **Comprehensive Testing** - **E2E testing** with Cypress and **unit tests** with Vitest

## Getting Started

### Prerequisites

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MySQL** database server
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd TimeX
   ```

2. **Set up the database**
   - Create a MySQL database named `timex`
   - Import the SQL schemas:
     ```bash
     mysql -u root -p timex < backend/usuarios.sql
     mysql -u root -p timex < backend/posts.sql
     ```

3. **Configure the backend database connection**
   - Edit `backend/database.js` with your MySQL credentials:
     ```javascript
     host: 'localhost',
     user: 'your_username',
     password: 'your_password',
     database: 'timex'
     ```

4. **Install frontend dependencies**
   ```bash
   npm install
   ```

5. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   cd ..
   ```

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   node server.js
   ```
   The backend will run on `http://localhost:3000` (or your configured port)

2. **Start the frontend development server** (in a new terminal)
   ```bash
   npm run dev
   ```
   The frontend will be available at `http://localhost:5173` (or the port shown in terminal)

3. **Open your browser**
   - Navigate to the frontend URL shown in the terminal
   - The application will redirect to the login page

### Building for Production

```bash
# Build the frontend
npm run build

# Preview the production build
npm run preview
```

### Running Tests

```bash
# Run end-to-end tests
npm run test.e2e

# Run unit tests
npm run test.unit
```

## Project Structure

```
TimeX/
├── backend/              # Express.js backend server
│   ├── database.js      # MySQL connection configuration
│   ├── server.js        # Express server and API routes
│   ├── usuarios.sql     # User table schema
│   └── posts.sql        # Posts/jobs table schema
├── src/                 # React frontend source code
│   ├── components/      # Reusable React components
│   ├── pages/           # Application pages/routes
│   │   ├── Home.tsx
│   │   ├── Search.tsx
│   │   ├── Jobs.tsx
│   │   ├── Messages.tsx
│   │   ├── Account.tsx
│   │   └── ...
│   ├── theme/           # Ionic theme variables
│   └── App.tsx          # Main application component
├── cypress/             # E2E test suite
├── public/              # Static assets
└── package.json         # Frontend dependencies
```

## API Endpoints

The backend provides **RESTful API** endpoints for:

- `POST /usuarios/signup` - User registration with **password hashing**
- `POST /usuarios/login` - User authentication
- `POST /posts/add` - Create new job posting
- `GET /posts` - Retrieve job listings
- Additional endpoints for messaging, job management, and user operations

## Technical Highlights

- **Component-based architecture** with React functional components and hooks
- **Type-safe development** with TypeScript throughout the codebase
- **RESTful API design** following industry best practices
- **Secure authentication** with bcrypt password hashing
- **Responsive UI/UX** with Ionic's mobile-first components
- **Modern build tooling** with Vite for fast development and optimized production builds
- **Cross-platform deployment** ready with Capacitor integration
- **Test-driven development** with comprehensive E2E and unit test coverage

<div align="center">

**Built with modern web technologies**

</div>
