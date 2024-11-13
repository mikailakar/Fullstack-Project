# Angular Frontend for Backend Project

This is the **Angular frontend** for the [Backend Project](https://github.com/mikailakar/Backend-Project). The frontend connects with the ASP.NET Core backend to provide a full-stack application that handles user management, authentication, JWT token decoding, and more.

## Table of Contents
- [Demo](#demo)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)

---

## Demo
Check out the live demo of the frontend hosted on **Vercel**:
- [Live Demo URL](https://fullstack-project-mauve.vercel.app)

## Features
- User authentication using JWT tokens
- View, add, update, and delete users
- Decode JWT tokens to get user information
- Search users by ID
- Filter users by roles and dates
- Responsive UI with Bootstrap integration

## Technologies Used
- **Angular 18.2.0**
- **TypeScript**
- **Bootstrap 5**
- **ASP.NET Core 8** (for backend)
- **Entity Framework Core** (for database management)
- **Vercel** (for frontend deployment)

## Prerequisites
Make sure you have the following installed on your machine:
- [Node.js](https://nodejs.org/) (v16 or later)
- [Angular CLI](https://angular.io/cli)
- [Git](https://git-scm.com/)

## Getting Started

### Installation
1. **Clone the Repository**
   ```bash
   git clone https://github.com/mikailakar/Fullstack-Project.git
   cd Fullstack-Project
   ```

3. **Install Dependencies**
   ```bash
   npm install
   ```

4. **Environment Configuration**
   - Configure `environment.ts` and `environment.prod.ts` files inside the `src/environments` folder.
   - Add your API URL to connect with the backend:

   ```typescript
   export const environment = {  
     production: false,  
     apiUrls: {  
       ApiUrl: 'https://your-backend-url.com/'  
     }  
   };
   ```

### Running the Application
- **Development Server**
   ```bash
  ng serve
   ```

  Navigate to [http://localhost:4200](http://localhost:4200). The app will automatically reload if you change any of the source files.

- **Build for Production**
   ```bash
  ng build --prod
   ```

## API Endpoints
Here's a list of the key endpoints used in this project:

- **GET** `/api/Users` - Get all users
- **GET** `/api/Users/{id}` - Get user by ID
- **POST** `/api/Users` - Add a new user
- **PUT** `/api/Users/{id}` - Update user details
- **DELETE** `/api/Users/{id}` - Soft delete user by ID
- **POST** `/api/Users/login` - User login and get JWT token
- **GET** `/api/Users/DecodeJwtToken?token={token}` - Decode JWT token
- **GET** `/api/Users/GetUsersWithRoles` - Get users with roles
- **GET** `/api/Users/GetUserWithRoleById?id={id}` - Get user with role by ID
- **GET** `/api/Users/GetAllUsersOrderByDate` - Get users by date

## Screenshots
### 1. Main Page
![Main Page](https://)

### 2. Users List
![Users List](https://)

### 3. JWT Token Decoding
![Decode JWT](https://)
