# 🎓 Odoo Finals - Placement Management System

A comprehensive placement management system for educational institutions, featuring job posting, application management, testing, and placement tracking with role-based access for Students, Companies, and TPOs (Training & Placement Officers).

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [Environment Variables](#-environment-variables)
- [API Documentation](#-api-documentation)
- [Frontend Components](#-frontend-components)
- [Database Models](#-database-models)
- [Authentication & Authorization](#-authentication--authorization)
- [Usage Examples](#-usage-examples)
- [Contributing](#-contributing)

## ✨ Features

### 🎯 Core Features
- *Multi-Role Authentication*: Students, Companies, and TPOs
- *Job Management*: Post, view, and manage job opportunities
- *Application System*: Complete application lifecycle management
- *Testing Platform*: Create and take aptitude/technical tests
- *Placement Tracking*: Monitor placement statistics and history
- *Upgrade Path System*: Manage offer upgrades and negotiations
- *Real-time Notifications*: Timeline and notification system
- *Analytics Dashboard*: Comprehensive reporting and analytics

### 👨‍🎓 Student Features
- Profile management and resume upload
- Job browsing and application submission
- Test taking interface with timer
- Offer management with upgrade paths
- Placement history tracking
- Practice materials access

### 🏢 Company Features
- Job posting with approval workflow
- Application review and status management
- Company profile management
- Dashboard with application statistics

### 👨‍💼 TPO/Admin Features
- Complete system administration
- Job approval workflow
- Test creation and management
- Analytics and reporting
- Student and company management

## 🛠 Tech Stack

### Backend
- *Node.js* - Runtime environment
- *Express.js* - Web framework
- *MongoDB* - Database
- *Mongoose* - ODM for MongoDB
- *JWT* - Authentication
- *bcrypt* - Password hashing
- *Nodemailer* - Email service
- *Express Rate Limit* - API rate limiting

### Frontend
- *React.js* - UI framework
- *TypeScript* - Type-safe development
- *Vite* - Build tool and development server
- *Shadcn/ui* - Modern component library
- *Axios* - HTTP client
- *React Router* - Navigation
- *React Query* - Data fetching and caching
- *React Hook Form* - Form management
- *React Toastify* - Notifications

## 📁 Project Structure


odoofinals/
├── 📁 Backend
│   ├── app.js                 # Main server file
│   ├── package.json           # Dependencies
│   ├── 📁 config/
│   │   ├── auth.js           # Authentication config
│   │   └── db.js             # Database connection
│   ├── 📁 controllers/
│   │   ├── authController.js
│   │   ├── CompanyController.js
│   │   ├── StudentController.js
│   │   ├── TPOController.js
│   │   ├── testController.js
│   │   ├── questionController.js
│   │   ├── rankingController.js
│   │   ├── timelineController.js
│   │   └── upgradePathController.js
│   ├── 📁 models/
│   │   ├── User.js
│   │   ├── Student.js
│   │   ├── Company.js
│   │   ├── TPO.js
│   │   ├── Jobs.js
│   │   ├── Application.js
│   │   ├── Test.js
│   │   ├── Question.js
│   │   ├── QuestionSet.js
│   │   ├── TestResult.js
│   │   ├── StudentAnswer.js
│   │   ├── Offer.js
│   │   ├── PlacementHistory.js
│   │   └── Notification.js
│   ├── 📁 routes/
│   │   ├── auth.js
│   │   ├── student.js
│   │   ├── company.js
│   │   ├── tpo.js
│   │   ├── tests.js
│   │   ├── questions.js
│   │   ├── ranking.js
│   │   ├── timeline.js
│   │   └── tpoJobApproval.js
│   ├── 📁 middleware/
│   │   └── auth.js           # Authentication middleware
│   ├── 📁 helpers/
│   │   └── helper.js         # Utility functions
│   └── 📁 utils/
│       └── emailService.js   # Email functionality
│
├── 📁 client/
│       ├── 📁 src/
│       │   ├── 📁 components/
│       │   │   └── 📁 ui/                    # Shadcn/ui Components
│       │   │       ├── accordion.tsx
│       │   │       ├── alert-dialog.tsx
│       │   │       ├── alert.tsx
│       │   │       ├── aspect-ratio.tsx
│       │   │       ├── avatar.tsx
│       │   │       ├── badge.tsx
│       │   │       ├── breadcrumb.tsx
│       │   │       ├── button.tsx
│       │   │       ├── calendar.tsx
│       │   │       ├── card.tsx
│       │   │       ├── carousel.tsx
│       │   │       ├── chart.tsx
│       │   │       ├── checkbox.tsx
│       │   │       ├── collapsible.tsx
│       │   │       ├── command.tsx
│       │   │       ├── context-menu.tsx
│       │   │       ├── dialog.tsx
│       │   │       ├── drawer.tsx
│       │   │       ├── dropdown-menu.tsx
│       │   │       ├── form.tsx
│       │   │       ├── hover-card.tsx
│       │   │       ├── input-otp.tsx
│       │   │       ├── input.tsx
│       │   │       ├── label.tsx
│       │   │       ├── loading-spinner.tsx
│       │   │       ├── menubar.tsx
│       │   │       ├── navigation-menu.tsx
│       │   │       ├── pagination.tsx
│       │   │       ├── popover.tsx
│       │   │       ├── progress.tsx
│       │   │       ├── radio-group.tsx
│       │   │       ├── resizable.tsx
│       │   │       ├── scroll-area.tsx
│       │   │       ├── select.tsx
│       │   │       ├── separator.tsx
│       │   │       ├── sheet.tsx
│       │   │       ├── sidebar.tsx
│       │   │       ├── skeleton.tsx
│       │   │       ├── slider.tsx
│       │   │       ├── switch.tsx
│       │   │       ├── table.tsx
│       │   │       ├── tabs.tsx
│       │   │       ├── textarea.tsx
│       │   │       ├── toast.tsx
│       │   │       ├── toaster.tsx
│       │   │       ├── toggle-group.tsx
│       │   │       ├── toggle.tsx
│       │   │       ├── tooltip.tsx
│       │   │       ├── 📁 hooks/
│       │   │       │   ├── use-mobile.tsx
│       │   │       │   └── use-toast.ts
│       │   │       └── 📁 lib/
│       │   │           ├── queryClient.ts
│       │   │           └── utils.ts
│       │   ├── 📁 pages/
│       │   │   ├── App.tsx
│       │   │   ├── index.css
│       │   │   ├── main.tsx
│       │   │   └── index.html
│       │   └── 📁 server/
│       │       ├── index.ts
│       │       ├── routes.ts
│       │       ├── storage.ts
│       │       └── vite.ts
│       └── package.json
│
├── ALL_ROUTES_DOCUMENTATION.md  # Complete API documentation
└── README.md                    # This file


## 🚀 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm or yarn

### Backend Setup

1. *Clone the repository*
   bash
   git clone <repository-url>
   cd odoofinals
   

2. *Install dependencies*
   bash
   npm install
   

3. *Set up environment variables*
   bash
   cp .env.example .env
   # Edit .env with your configuration
   

4. *Start the server*
   bash
   # Development mode
   npm run dev
   
   # Production mode
   npm start
   

### Frontend Setup

1. *Navigate to frontend directory*
   bash
   cd client
   

2. *Install dependencies*
   bash
   npm install
   

3. *Start the development server*
   bash
   npm run dev
   

## 🔧 Environment Variables

Create a .env file in the root directory:

env
# Server Configuration
PORT=5900
NODE_ENV=development

# Database
MONGO_URL=mongodb://localhost:27017/odoofinals

# Authentication
JWT_SECRET=your_super_secret_jwt_key_here
JWT_EXPIRE=30d

# Email Configuration (for notifications)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Rate Limiting
RATE_LIMIT_WINDOW_MS=900000
RATE_LIMIT_MAX_REQUESTS=100


## 📚 API Documentation

### Base URL

http://localhost:5900/api


### Authentication Endpoints
- POST /auth/register - Register new user
- POST /auth/login - User login

### Student Endpoints
- GET /student/dashboard - Student dashboard
- GET /student/home - View available jobs
- POST /student/apply/:jobId - Apply for job
- GET /student/tests - Available tests
- POST /student/test/:testId/start - Start test
- POST /student/test/:testId/submit - Submit test

### Company Endpoints
- GET /company/dashboard - Company dashboard
- POST /company/jobs - Post new job
- GET /company/applications - View applications
- PATCH /company/applications/:id/status - Update application status

### TPO Endpoints
- GET /tpo/dashboard - TPO dashboard
- POST /tpo/jobs - Create job
- GET /tpo/applications - View all applications
- POST /tpo/tests - Create test
- GET /tpo/analytics - System analytics

### Test & Question Endpoints
- POST /tests/start/:questionSetId - Start test session
- POST /tests/:sessionId/answer/:questionId - Submit answer
- POST /tests/:sessionId/submit - Submit test
- GET /tests/results/:sessionId - Get test results

### Ranking & Analytics
- GET /ranking/leaderboard - Campus leaderboard
- GET /ranking/my-ranking - Personal ranking
- GET /ranking/top-performers - Top performers

For complete API documentation, see [ALL_ROUTES_DOCUMENTATION.md](./ALL_ROUTES_DOCUMENTATION.md)

## 🎨 Frontend Components

### Modern UI Component Library
The frontend uses *Shadcn/ui* - a comprehensive component library built on top of Radix UI and Tailwind CSS, providing:

#### Core Components
- *Layout Components*: Card, Sheet, Drawer, Sidebar, Navigation Menu
- *Form Components*: Input, Textarea, Select, Checkbox, Radio Group, Form
- *Interactive Components*: Button, Dialog, Dropdown Menu, Popover, Tooltip
- *Data Display*: Table, Badge, Avatar, Progress, Skeleton
- *Feedback Components*: Alert, Toast, Loading Spinner
- *Advanced Components*: Calendar, Carousel, Chart, Command, Resizable

#### Custom Hooks
- *use-mobile.tsx*: Mobile responsiveness utilities
- *use-toast.ts*: Toast notification management

#### Utility Libraries
- *queryClient.ts*: React Query configuration for data fetching
- *utils.ts*: Common utility functions

### Application Structure
- *App.tsx*: Main application component
- *main.tsx*: Application entry point
- *index.html*: HTML template
- *index.css*: Global styles

### Server Integration
- *index.ts*: Server configuration
- *routes.ts*: API route definitions
- *storage.ts*: Data storage utilities
- *vite.ts*: Vite build configuration

## 🗄 Database Models

### Core Models
- *User*: Base user model with authentication
- *Student*: Student-specific data and profile
- *Company*: Company information and profile
- *TPO*: TPO/admin user data

### Business Logic Models
- *Jobs*: Job postings with approval workflow
- *Application*: Job applications with status tracking
- *Test*: Test definitions and configurations
- *Question*: Individual test questions
- *QuestionSet*: Collections of questions
- *TestResult*: Student test results and analytics
- *Offer*: Job offers with upgrade paths
- *PlacementHistory*: Historical placement data
- *Notification*: System notifications and timeline

## 🔐 Authentication & Authorization

### JWT-based Authentication
- Secure token-based authentication
- Role-based access control (Student, Company, TPO)
- Token expiration and refresh mechanism

### Middleware
- verifyToken: JWT token verification
- authorizeRoles: Role-based authorization
- authorizeStudent: Student-only routes
- authorizeCompany: Company-only routes
- authorizeTPO: TPO/admin-only routes

### Security Features
- Password hashing with bcrypt
- Rate limiting on API endpoints
- CORS configuration
- Input validation and sanitization

## 💰 Salary Display

The application displays all salaries in *Indian Rupees (₹)* as per user preference.

## 📊 Usage Examples

### Student Job Application
javascript
// Apply for a job
const response = await axios.post(
  `/api/student/apply/${jobId}`,
  { resumeId: 'resume123' },
  { headers: { Authorization: `Bearer ${token}` } }
);


### Company Job Posting
javascript
// Post a new job
const jobData = {
  title: "Software Engineer",
  description: "Full-stack development role",
  package: 800000, // ₹8 LPA
  jobTier: "Tier 2",
  requirements: ["React", "Node.js", "MongoDB"]
};

const response = await axios.post(
  '/api/company/jobs',
  jobData,
  { headers: { Authorization: `Bearer ${token}` } }
);


### TPO Test Creation
javascript
// Create a new test
const testData = {
  title: "Technical Assessment",
  category: "Technical Skills",
  duration: 60,
  questions: [
    {
      question: "What is React?",
      options: ["Library", "Framework", "Language", "Database"],
      correctAnswer: 0
    }
  ]
};

const response = await axios.post(
  '/api/tpo/tests',
  testData,
  { headers: { Authorization: `Bearer ${token}` } }
);
