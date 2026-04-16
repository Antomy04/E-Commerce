# E-Commerce Project Startup Guide

## Project Overview
This is a full-stack MERN (MongoDB, Express, React, Node.js) e-commerce application with the following features:
- User authentication and authorization
- Product catalog with categories and search
- Shopping cart and wishlist
- Order management
- Admin dashboard
- Payment integration (Razorpay)
- Cloud image storage (Cloudinary)

## Prerequisites
- Node.js (v16 or higher)
- MongoDB (running locally or cloud instance)
- Git (for cloning if needed)

## Project Structure
```
E-Commerce/
├── backend/          # Express.js API server
├── frontend/         # React.js client application
├── server.js         # Main server entry point
├── package.json      # Backend dependencies and scripts
└── startup.md        # This file
```

## Environment Setup
1. Ensure MongoDB is running on `mongodb://localhost:27017` (default)
2. Copy `.env` file to backend folder with required variables:
   ```
   MONGODB_URI=mongodb://localhost:27017/ecommerce
   JWT_SECRET=your_jwt_secret_here
   JWT_EXPIRE=30d
   BCRYPT_SALT_ROUNDS=10
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   FRONTEND_URL=http://localhost:5173
   RAZORPAY_KEY_ID=your_razorpay_key
   RAZORPAY_KEY_SECRET=your_razorpay_secret
   ```

## Installation & Startup Commands

### Backend Setup
```bash
# Navigate to project root
cd "c:\Users\kk\college\E-Commerce"

# Install dependencies
npm install

# Start development server
npm run dev
```
- Backend URL: http://localhost:5000
- API Health Check: http://localhost:5000/api/health

### Frontend Setup
```bash
# Navigate to frontend directory
cd "c:\Users\kk\college\E-Commerce\frontend"

# Install dependencies
npm install

# Start development server
npm run dev
```
- Frontend URL: http://localhost:5173

## Quick Start (Both Services)
Open two terminals:

**Terminal 1 (Backend):**
```bash
cd "c:\Users\kk\college\E-Commerce"
npm run dev
```

**Terminal 2 (Frontend):**
```bash
cd "c:\Users\kk\college\E-Commerce\frontend"
npm run dev
```

## Available Scripts

### Backend Scripts
- `npm start` - Production server
- `npm run dev` - Development server with nodemon

### Frontend Scripts
- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## Troubleshooting
- If MongoDB connection fails, ensure MongoDB is running
- If ports 5000/5173 are in use, kill processes or change ports
- Clear browser cache if frontend doesn't update

## Development Notes
- Backend uses Express.js with middleware for auth, uploads, and error handling
- Frontend uses React with Redux Toolkit for state management
- Database models include User, Product, Cart, Order, Review, etc.
- CORS is configured for development and production origins