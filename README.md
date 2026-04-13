# English Exam Bank Management System

[![React](https://img.shields.io/badge/React-18.3.1-blue)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.7+-green)](https://www.mongodb.com/)

---

## 📋 Project Overview

**English Exam Bank Management System** is a comprehensive web application for managing English language exams, built using the MERN stack (MongoDB, Express.js, React.js, Node.js). The system supports three user roles: Head of Department, Teachers, and Students, providing specialized functionalities for each role.

## 🚀 Installation & Setup

### Step 1: Download Source Code
Download the source code to your local machine.

### Step 2: Set Up MongoDB Database
1. **Basic Setup**: Add `User` and `Exam` collections in the 'database' folder and import JSON data to view basic system features.
2. **Full System Setup**: Use the following MongoDB URI in the server's `.env` file for complete functionality:
   ```
   mongodb+srv://Cluster59773:bankexamenglish@cluster59773.dghmqtd.mongodb.net/EnglishExamBankDB
   ```

### Step 3: Install Dependencies
Using terminal, navigate to the EEB source code folder and execute:

```bash
# Install client dependencies
cd client
npm install

# Install server dependencies
cd ../server
npm install
```

### Step 4: Start the Application
```bash
# Start client (React)
cd client
npm start

# Start server (Node.js/Express)
cd ../server
npm start
```

### Step 5: Access the Application
- **Student Login**: Navigate to `http://localhost:3000/`
- **Teacher/Head Login**: Navigate to `http://localhost:3000/teacher/login`

## 👥 Login Credentials

### Head of Department
- **Username**: H20240001
- **Password**: admin

### Teacher
- **Username**: T20240001
- **Password**: admin

### Student
- **Username**: 120240001
- **Password**: admin

## 🏗️ Project Structure

```
/Source
├── client/                          # React Frontend
│   ├── public/                      # Static assets
│   │   ├── index.html              # Main HTML file
│   │   └── manifest.json           # PWA configuration
│   ├── src/                        # React source code
│   │   ├── components/             # UI Components
│   │   │   ├── Avata/             # Avatar components
│   │   │   ├── DarkMode/          # Dark mode toggle
│   │   │   ├── Head/              # Head/Admin components
│   │   │   ├── Language/          # Language selection
│   │   │   ├── Layout/            # Layout components
│   │   │   ├── Locations/         # Location display
│   │   │   ├── Message/           # Message components
│   │   │   ├── Profile/           # Profile management
│   │   │   ├── Sidebar/           # Sidebar navigation
│   │   │   ├── Student/           # Student components
│   │   │   ├── Teacher/           # Teacher components
│   │   │   └── Toast/             # Toast notifications
│   │   ├── pages/                  # Application pages
│   │   │   ├── Auth/              # Authentication pages
│   │   │   ├── Head/              # Head/Admin pages
│   │   │   ├── Student/           # Student pages
│   │   │   └── Teacher/           # Teacher pages
│   │   ├── Redux/                  # State management
│   │   │   ├── Auth/              # Auth slice & selectors
│   │   │   ├── Language/          # Language slice
│   │   │   └── store.js           # Redux store configuration
│   │   ├── assets/                 # Static resources
│   │   ├── actions/                # Redux action creators
│   │   ├── routes/                 # Application routing
│   │   │   ├── HeadRoutes.jsx     # Head/Admin routes
│   │   │   ├── ProtectedRoute.jsx # Protected routes
│   │   │   ├── StudentRoutes.jsx  # Student routes
│   │   │   └── TeacherRoutes.jsx  # Teacher routes
│   │   └── services/               # API services
│   └── tailwind.config.js          # Tailwind CSS configuration
└── server/                         # Node.js Backend
    ├── config/                     # Server configurations
    │   ├── cors.js                # CORS configuration
    │   ├── database.js            # Database configuration
    │   ├── mail.js               # Email configuration
    │   └── socket.js             # WebSocket configuration
    └── src/                       # Server source code
        ├── controllers/           # Request controllers
        │   ├── authController.js  # Authentication logic
        │   ├── headControllers.js # Head/Admin operations
        │   ├── studentControllers.js # Student operations
        │   └── teacherControllers.js # Teacher operations
        ├── middlewares/           # HTTP middleware
        │   ├── authMiddleware.js  # Authentication middleware
        │   └── getCurrentSemester.js # Semester middleware
        ├── models/                # Database models
        │   ├── ApprovedExam.js    # Approved exam model
        │   ├── Chapters.js        # Chapter model
        │   ├── Chat.js           # Chat model
        │   ├── Class.js          # Class model
        │   ├── Exam.js           # Exam model
        │   ├── ExamSubmission.js # Exam submission model
        │   ├── QuestionRandom.js # Random question model
        │   ├── Questions.js      # Question model
        │   ├── SchoolYear.js     # School year model
        │   ├── Score.js          # Score model
        │   ├── Semester.js       # Semester model
        │   └── User.js           # User model
        ├── routes/                # API routes
        │   ├── authRoutes.js     # Authentication routes
        │   ├── headRoutes.js     # Head/Admin routes
        │   ├── studentRoutes.js  # Student routes
        │   └── teacherRoutes.js  # Teacher routes
        └── server.js             # Main server entry point
```

## 🎯 Main Objectives

### Efficient Exam Management
- Provide tools for teachers to create, store, and manage exams easily and flexibly
- Support multiple exam creation methods (manual, file-based, random) to meet teacher preferences

### Enhanced Learning Environment
- Allow students to access practice exams and official tests
- Provide detailed exam information and statistical reports for progress tracking

### Human Resource Management
- Ensure proper assignment of teachers and students to classes and exams
- Provide department heads with tools to manage academic years, semesters, classes, and exams

### Optimized Information Management
- Manage user accounts including information updates, status management, and security
- Provide reporting and statistical functions for effective monitoring

### Comprehensive User Support
- Support login/logout, password changes, and personal information updates
- Ensure user-friendly experience with theme and language switching

### Security and Reliability
- Implement authentication and security features including OTP email verification

## 🔧 System Features

### Common Features (All Users)
- Login/Logout
- Password change
- Email addition to account (with OTP verification)
- Password recovery (for accounts with registered email)
- Personal information updates (address, phone, gender display)
- Real-time chat communication
- Dark/Light mode switching
- English/Vietnamese language switching

### Head of Department Features
- **Academic Year Management**: Add/delete academic years
- **Semester Management**: Add semesters, modify dates, change status
- **Class Management**: View, add, delete, and rename classes
- **Class Details Management**: Add teachers and students, remove students
- **Exam Management**: View, add, and configure exams; manage submitted exams
- **Statistics Reporting**: View student distribution and class scores
- **User Account Management**: View all users, search, modify information, generate passwords

### Teacher Features
- **Class Management**: View assigned classes, grade students, modify scores
- **Exam Creation**: Three methods (manual, file-based, random generation)
- **Exam Repository**: Search, share, view, download, edit, and delete exams
- **Exam Submission**: Submit exams for department approval
- **Statistics**: View student scores and performance charts

### Student Features
- **Practice Exams**: Search and attempt publicly shared practice exams
- **Exam Attempts**: Detailed feedback on correct/incorrect answers
- **Upcoming Exams**: View details of scheduled exams
- **Official Exams**: Password-protected exam attempts with auto-saving
- **Statistics**: View personal scores and performance charts

## 🛠️ Technologies Used

### MERN Stack Components
- **MongoDB**: NoSQL database
- **Express.js**: Backend web framework
- **React.js**: Frontend library
- **Node.js**: JavaScript runtime

### Frontend Dependencies
- **Core**: React, React DOM, React Router
- **State Management**: Redux Toolkit, React Redux
- **UI/UX**: Tailwind CSS, Framer Motion, React Icons
- **Charts**: Chart.js, React ChartJS 2
- **Forms**: React Hook Form
- **File Handling**: DOCX, ExcelJS, jsPDF, html2canvas
- **Communication**: Socket.io-client, Axios
- **Utilities**: Moment, Date-fns, JWT-decode

### Backend Dependencies
- **Core**: Express, Mongoose, MongoDB
- **Authentication**: Bcrypt, JSON Web Token
- **Validation**: Express Validator
- **Communication**: Socket.io, Nodemailer
- **Utilities**: Dotenv, Crypto, Body-parser

## 👥 Development Team
- **51900167 - Nguyễn Tiến Phát**
- **51900178 - Phạm Ngọc Phụng**

## ⚠️ Important Notes
- Install `node_modules` for both client and server before running
- Add at minimum the `User` collection to MongoDB
- Ensure all environment variables are properly configured

## 🔗 Project Links
- **Main Drive Link**: [https://drive.google.com/file/d/1Z5iYJcgLOLgLqK6w_xt6ymcC1HtT_Il8/view](https://drive.google.com/file/d/1Z5iYJcgLOLgLqK6w_xt6ymcC1HtT_Il8/view)
- **Backup Link**: [https://drive.google.com/drive/folders/1Ew7mpjcEuo43073BChZoJIPqmG5_-t29](https://drive.google.com/drive/folders/1Ew7mpjcEuo43073BChZoJIPqmG5_-t29)

---

**Happy Learning and Teaching! 📚✨**