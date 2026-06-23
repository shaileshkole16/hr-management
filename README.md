# HR Management System

A full-stack Human Resource Management System built with modern web technologies for efficient employee management, attendance tracking, and departmental organization.

## 🚀 Features

- **Dashboard**: Real-time statistics showing total employees, departments, and department-wise employee counts
- **Employee Management**: Complete CRUD operations - view, create, update, and delete employee records
- **Attendance Tracking**: Daily attendance management with present/absent/not set status
- **Department Organization**: View employees categorized by departments with detailed information
- **Authentication**: Secure login/signup with Firebase Authentication (Email/Password & Google Sign-In)
- **Search Functionality**: Quick employee search by name or email
- **Responsive Design**: Mobile-friendly UI built with Tailwind CSS

## 🛠️ Tech Stack

### Frontend
- **React 18** - UI library
- **Tailwind CSS** - Styling
- **React Router** - Navigation
- **TanStack Query** - Data fetching and caching
- **SweetAlert2** - Beautiful alerts
- **Firebase** - Authentication

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MySQL** - Database
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variables

## 📁 Project Structure

```
hr-management/
├── backend/
│   ├── index.js          # Main server file with all API endpoints
│   ├── package.json      # Backend dependencies
│   └── .env             # Database configuration
├── client/
│   ├── src/
│   │   ├── Components/   # Reusable UI components
│   │   ├── Pages/        # Page components
│   │   ├── hooks/        # Custom React hooks
│   │   ├── Layout/       # Layout components
│   │   ├── Router/       # Route configuration
│   │   └── Provider/     # Context providers
│   ├── public/           # Static assets
│   └── package.json     # Frontend dependencies
└── hr_management_db/     # SQL database schemas
```

## 🗄️ Database Schema

The system uses MySQL with the following tables:
- **employees** - Employee information
- **departments** - Department details
- **jobs** - Job titles and salary ranges
- **attendance** - Daily attendance records
- **leaves** - Leave management
- **performance_reviews** - Performance evaluation records
- **salaries** - Salary history
- **users** - User authentication data

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or later)
- MySQL Server
- Firebase project (for authentication)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/shaileshkole16/hr-management.git
   cd hr-management
   ```

2. **Install frontend dependencies**
   ```bash
   cd client
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd ../backend
   npm install
   ```

4. **Setup MySQL Database**
   - Create a new MySQL database named `hr_management`
   - Import all SQL files from `hr_management_db/` directory

5. **Configure environment variables**
   
   **Backend (.env):**
   ```env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_password
   DB_NAME=hr_management
   PORT=5000
   ```
   
   **Client (.env):**
   ```env
   VITE_apiKey=your_firebase_api_key
   VITE_authDomain=your_firebase_auth_domain
   VITE_projectId=your_firebase_project_id
   VITE_storageBucket=your_firebase_storage_bucket
   VITE_messagingSenderId=your_firebase_messaging_sender_id
   VITE_appId=your_firebase_app_id
   ```

6. **Run the application**
   
   **Start backend:**
   ```bash
   cd backend
   npm start
   ```
   
   **Start frontend:**
   ```bash
   cd client
   npm run dev
   ```

7. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5000

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Health check |
| GET | `/employees` | Get all employees |
| GET | `/employees/:id` | Get employee by ID |
| POST | `/employees` | Create new employee |
| PATCH | `/employees/:id` | Update employee |
| DELETE | `/employees/:id` | Delete employee |
| GET | `/attendance` | Get all attendance |
| GET | `/attendance/employees/:date` | Get attendance by date |
| PUT | `/attendance/employees/:date` | Update attendance |
| GET | `/departments/employees` | Get department-wise employees |
| GET | `/statistics` | Get dashboard statistics |
| GET | `/users` | Get all users |
| POST | `/users` | Create new user |

## 🎯 Key Functionalities

### Employee Management
- Add new employees with job and department assignment
- Update employee information
- Delete employees with cascade deletion of related records
- Search employees by name or email
- View detailed employee information

### Attendance System
- Daily attendance tracking
- Status options: Present, Absent, Not Set
- Date-wise attendance viewing
- Bulk attendance updates

### Dashboard
- Total employee count
- Total department count
- Total job positions
- Department-wise employee distribution

## 🔐 Authentication

The application uses Firebase Authentication for:
- Email/Password login
- Google Sign-In
- Protected routes using PrivateRouter
- User context management

## 📝 Future Enhancements

- [ ] Leave management system
- [ ] Performance review module
- [ ] Salary management
- [ ] Advanced reporting and analytics
- [ ] Export data to PDF/Excel
- [ ] Role-based access control

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Shailesh Kole**
- GitHub: [@shaileshkole16](https://github.com/shaileshkole16)

---

⭐ If you find this project helpful, please consider giving it a star!

