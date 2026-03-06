# Find-It 🔍

Find-It is a comprehensive Lost and Found application designed for educational institutions, allowing students and faculty to seamlessly report, browse, and claim lost or found items on campus. 

## 🚀 Features
- **Role-Based Authentication**: Secure login and registration tailored for both Students (using Roll Number) and Faculty (using Faculty Code).
- **Report Lost Items**: Users can report items they have lost with detailed descriptions and images.
- **Report Found Items**: Users can report items they have found, fostering a helpful community.
- **Browse Items**: Dedicated sections to view all currently reported lost and found items.
- **Item Claims**: Users can intelligently claim items they have lost or found.
- **Manage Claims**: A straightforward interface to view and delete your claims.
- **Secure & Fast**: JWT-based authentication, password hashing with bcrypt, and a responsive React frontend via Vite.

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 19 (with Vite for incredibly fast builds)
- **Styling**: Tailwind CSS v4 for a beautiful and highly responsive UI
- **Routing**: React Router DOM (v7)
- **Icons**: Lucide React
- **Notifications**: React Toastify
- **State/Auth**: JWT Decode & LocalStorage

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MySQL (using `mysql2` driver)
- **Authentication**: JsonWebToken (JWT) & Bcryptjs
- **File Uploads**: Multer (for handling item images)
- **Middleware**: CORS, Dotenv for environment management

## 📁 Project Structure

```text
Find-It/
├── backend/               # Express & MySQL backend
│   ├── config/            # Database configurations
│   ├── middleware/        # JWT Authentication middlewares
│   ├── routes/            # API routes (auth, lostItems, foundItems, claims)
│   ├── uploads/           # Directory where image uploads are stored
│   ├── package.json       # Backend dependencies
│   └── server.js          # Entry point for the Express server
├── src/                   # React frontend
│   ├── components/        # React components (Dashboard, Navbar..., Login, Signup)
│   ├── App.jsx            # Main React application and Router configuration
│   ├── main.jsx           # React DOM rendering
│   └── index.css          # Global Tailwind CSS styles
├── package.json           # Frontend dependencies
├── vite.config.js         # Vite configuration
└── README.md              # Project documentation
```

## ⚙️ Installation & Setup

### Prerequisites
- Node.js installed on your machine
- MySQL Server running locally or remotely

### 1. Clone the repository
```bash
git clone <repository_url>
cd Find-It
```

### 2. Backend Setup
```bash
cd backend
npm install
```
- Ensure you have a MySQL database running. Create a database named `findit` (default configuration in `server.js`).
- Set up your database tables (e.g., `users`, `students`, `faculty`, `lost_items`, `found_items`, `claims`) as expected by the backend routes.
- Update database credentials in `backend/server.js` or through environment variables if applicable.
- Start the Express server:
```bash
node server.js
# Or with nodemon if installed globally:
nodemon server.js
```

### 3. Frontend Setup
```bash
# Open a new terminal from the root directory of the project
npm install
```
- Start the Vite development server:
```bash
npm run dev
```

## 🔒 Authentication & Roles
- **Student**: Requires Name, Email, Password, and Roll Number to register.
- **Faculty**: Requires Name, Email, Password, Faculty Code, and optionally Department to register.
- **JWT**: Tokens are issued upon login and stored in the frontend's local storage to persist the session and protect routes.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome!

---
*Built with ❤️ to simplify the lost and found process on campus.*
