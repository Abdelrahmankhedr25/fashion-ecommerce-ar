# Development Environment Setup Guide

## Prerequisites
- **Node.js 18+** (LTS recommended)
- **npm 9+** or **pnpm 8+**
- **MongoDB 6+** (local) or **MongoDB Atlas** account
- **Git**
- **Code Editor** (VSCode recommended)

## Initial Setup

### 1. Clone Repository
```bash
git clone https://github.com/Abdelrahmankhedr25/fashion-ecommerce-ar.git
cd fashion-ecommerce-ar
```

### 2. Frontend Setup

```bash
cd frontend
npm install

# Create .env.local
cat > .env.local << EOF
VITE_API_URL=http://localhost:5000/api
VITE_PAYMOB_PUBLIC_KEY=your_paymob_key
VITE_CLOUDINARY_CLOUD_NAME=your_cloud_name
EOF

# Start development server
npm run dev
```

Frontend runs on: **http://localhost:5173**

### 3. Backend Setup

```bash
cd backend
npm install

# Create .env
cat > .env << EOF
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/fashion-ecommerce
JWT_SECRET=your-super-secret-jwt-key-change-in-production
JWT_EXPIRE=7d
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
PAYMOB_API_KEY=your_paymob_api_key
PAYMOB_INTEGRATION_ID=your_integration_id
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
FRONTEND_URL=http://localhost:5173
EOF

# Start development server
npm run dev
```

Backend runs on: **http://localhost:5000**

## Database Setup

### Option 1: Local MongoDB
```bash
# Install MongoDB (macOS)
brew tap mongodb/brew
brew install mongodb-community

# Start MongoDB service
brew services start mongodb-community

# Verify connection
mongosh
```

### Option 2: MongoDB Atlas (Cloud)
1. Create account at [mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Create a free cluster
3. Whitelist your IP (0.0.0.0/0 for development)
4. Get connection string
5. Update `MONGODB_URI` in backend `.env`

## Third-Party Services Setup

### Cloudinary (Image CDN)
1. Create account at [cloudinary.com](https://cloudinary.com)
2. Get Cloud Name, API Key, API Secret from dashboard
3. Add to both frontend and backend `.env` files

### Paymob (Payment Gateway)
1. Create account at [paymob.com](https://paymob.com)
2. Get API Key and Integration ID
3. Add to frontend and backend `.env` files
4. Test with sandbox mode first

### Email (Gmail SMTP)
1. Enable 2-Step Verification in Gmail
2. Generate App Password: [myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)
3. Use App Password in `EMAIL_PASS`

## Project Structure

```
fashion-ecommerce-ar/
│
├── frontend/
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── context/        # Context providers
│   │   ├── services/       # API services
│   │   ├── utils/          # Utility functions
│   │   ├── assets/         # Images, fonts, etc.
│   │   └── App.jsx         # Root component
│   ├── public/             # Static files
│   ├── package.json
│   └── vite.config.js
│
├── backend/
│   ├── src/
│   │   ├── controllers/    # Route controllers
│   │   ├── models/         # Mongoose models
│   │   ├── routes/         # API routes
│   │   ├── middleware/     # Custom middleware
│   │   ├── utils/          # Helpers
│   │   ├── config/         # Configuration
│   │   └── server.js       # Entry point
│   ├── package.json
│   └── .env
│
├── docs/                   # Documentation
└── design/                 # UI/UX assets
```

## Development Workflow

### Frontend Commands
```bash
npm run dev          # Start dev server
npm run build        # Production build
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run test         # Run tests
```

### Backend Commands
```bash
npm run dev          # Start with nodemon (auto-reload)
npm start            # Start production server
npm run test         # Run tests
npm run seed         # Seed database (if available)
```

## Testing Setup

### Frontend Testing
```bash
cd frontend
npm install -D @testing-library/react @testing-library/jest-dom vitest
```

### Backend Testing
```bash
cd backend
npm install -D jest supertest
```

## Common Issues & Solutions

### Port Already in Use
```bash
# Kill process on port 5000
lsof -ti:5000 | xargs kill -9

# Or change PORT in backend .env
```

### MongoDB Connection Failed
- Ensure MongoDB service is running
- Check connection string format
- Verify IP whitelist (Atlas)

### CORS Errors
- Ensure `FRONTEND_URL` in backend .env matches frontend URL
- Check CORS middleware configuration

### Module Not Found
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

## Recommended VSCode Settings

Create `.vscode/settings.json`:
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "tailwindCSS.experimental.classRegex": [
    ["cn\\(([^)]*)\\)", "(?:'|\"|`)([^']*)(?:'|\"|`)"]
  ]
}
```

## Next Steps
1. ✅ Environment setup complete
2. 📝 Start with database schema creation
3. 🎨 Begin frontend component development
4. 🔌 Implement API endpoints
5. 🧪 Write tests
6. 🚀 Deploy to staging