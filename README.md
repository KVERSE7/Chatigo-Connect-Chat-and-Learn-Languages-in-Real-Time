# 🎥 Camigo - Connect, Chat, Learn Languages

A real-time video chatting application that connects you with people worldwide, helping you learn new languages by talking to native speakers through smooth, high-quality streams.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation & Setup](#-installation--setup)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Environment Variables](#-environment-variables)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- **Real-time Video Chatting** - High-quality video streams powered by Stream.io SDK
- **Global Connection** - Connect with language learners and native speakers from around the world
- **Language Learning** - Learn new languages by practicing with native speakers
- **Smooth Streaming** - Optimized video quality for seamless conversations
- **User Authentication** - Secure login and registration with JWT tokens
- **Messaging** - Real-time chat messaging integrated with Stream Chat API
- **Responsive Design** - Mobile-friendly interface using Tailwind CSS

---

## 🛠️ Tech Stack

### Frontend
- **React 19.1** - UI library for building interactive interfaces
- **Vite 7.0** - Next-generation frontend build tool
- **Stream.io Video SDK** - Real-time video streaming (`@stream-io/video-react-sdk`)
- **Stream Chat React** - Real-time messaging capabilities
- **Tailwind CSS** - Utility-first CSS framework for styling
- **DaisyUI** - Tailwind CSS component library
- **React Router** - Client-side routing
- **Zustand** - State management
- **Axios** - HTTP client
- **React Query** - Server state management
- **Lucide React** - Icon library

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB + Mongoose** - NoSQL database and ODM
- **JWT (jsonwebtoken)** - Authentication
- **bcryptjs** - Password hashing
- **Stream Chat SDK** - Messaging API integration
- **Cookie Parser** - HTTP cookie parsing
- **CORS** - Cross-Origin Resource Sharing
- **Dotenv** - Environment variable management
- **Nodemon** - Development server with auto-reload

### Development Tools
- **ESLint** - Code quality and style linting
- **PostCSS** - CSS transformation
- **Autoprefixer** - CSS vendor prefixing

---

## 📁 Project Structure

```
Camigo/
├── frontend/                      # React frontend application
│   ├── src/
│   │   ├── components/           # Reusable React components
│   │   ├── pages/                # Page components
│   │   ├── hooks/                # Custom React hooks
│   │   ├── store/                # Zustand state management
│   │   ├── api/                  # API integration (axios)
│   │   ├── App.jsx               # Main App component
│   │   └── main.jsx              # Entry point
│   ├── package.json
│   ├── vite.config.js            # Vite configuration
│   ├── tailwind.config.js        # Tailwind CSS configuration
│   └── index.html
│
├── backend/                       # Express.js backend application
│   ├── src/
│   │   ├── models/               # MongoDB schemas
│   │   ├── routes/               # API routes
│   │   ├── controllers/          # Route controllers
│   │   ├── middleware/           # Custom middleware (auth, etc.)
│   │   ├── config/               # Configuration files
│   │   └── server.js             # Server entry point
│   ├── package.json
│   └── .env.example              # Environment variables template
│
└── package.json                   # Root package.json (workspace)
```

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0 or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local or MongoDB Atlas cloud instance)
- **Git** (for cloning the repository)

### Required API Keys/Services
- **Stream.io Account** - For video and chat functionality
  - Video API key and token
  - Chat API key and token
- **MongoDB Connection String** - For database

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Hiitesh-g3/Camigo.git
cd Camigo
```

### 2. Backend Setup

```bash
cd backend

# Install dependencies
npm install

# Create .env file with required variables
cp .env.example .env

# Edit .env with your credentials
# (See Environment Variables section below)
```

### 3. Frontend Setup

```bash
cd ../frontend

# Install dependencies
npm install

# Create .env file with required variables
touch .env.local
```

---

## 🏃 Running the Application

### Development Mode

**Backend:**
```bash
cd backend
npm run dev
# Server runs on http://localhost:5000 (or your configured port)
```

**Frontend (in a new terminal):**
```bash
cd frontend
npm run dev
# Application runs on http://localhost:5173 (Vite default)
```

### Production Build

**Frontend Build:**
```bash
cd frontend
npm run build
# Creates optimized build in dist/ folder
```

**Backend Production:**
```bash
cd backend
npm start
```

---

## 📡 API Documentation

### Authentication Endpoints

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### User Endpoints

- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile
- `GET /api/users/search` - Search for users

### Video/Chat Endpoints

- `GET /api/stream/token` - Get Stream.io video token
- `GET /api/chat/token` - Get Stream Chat token
- `POST /api/calls` - Create video call
- `GET /api/calls/active` - Get active calls

---

## 🔐 Environment Variables

### Backend `.env`

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/camigo

# JWT
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRY=7d

# Stream.io Video
STREAM_VIDEO_API_KEY=your_stream_video_api_key
STREAM_VIDEO_SECRET=your_stream_video_secret

# Stream.io Chat
STREAM_CHAT_API_KEY=your_stream_chat_api_key
STREAM_CHAT_SECRET=your_stream_chat_secret

# CORS
CORS_ORIGIN=http://localhost:5173

# Cookies
COOKIE_SECRET=your_cookie_secret
```

### Frontend `.env.local`

```env
VITE_API_URL=http://localhost:5000
VITE_STREAM_VIDEO_API_KEY=your_stream_video_api_key
VITE_STREAM_CHAT_API_KEY=your_stream_chat_api_key
```

---

## 🤝 Contributing

Contributions are welcome! To contribute to Camigo:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Code Style

- Follow ESLint rules configured in the project
- Use consistent naming conventions
- Write clear commit messages

---

## 📝 License

This project is licensed under the ISC License - see the LICENSE file for details.

---

## 👤 Author

**Hiitesh-g3**  
GitHub: [@Hiitesh-g3](https://github.com/Hiitesh-g3)

---

## 🙋 Support

For support, please open an issue on the GitHub repository or contact the maintainer.

---

## 🌟 Acknowledgments

- Stream.io for providing real-time video and chat SDKs
- React and Vite communities for excellent development tools
- All contributors and users of Camigo

---

**Last Updated:** May 2026  
**Repository:** [Hiitesh-g3/Camigo](https://github.com/Hiitesh-g3/Camigo)
