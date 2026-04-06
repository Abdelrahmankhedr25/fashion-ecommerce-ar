# Development Environment Setup

## Prerequisites

- Node.js 18+
- npm 9+ or yarn
- Git
- MongoDB (local or Atlas)
- VS Code (recommended)

---

## Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/Abdelrahmankhedr25/fashion-ecommerce-ar.git
cd fashion-ecommerce-ar
```

### 2. Frontend Setup
```bash
cd frontend
npm install
cp .env.example .env
# Edit .env with your config
npm run dev
# Runs on http://localhost:5173
```

### 3. Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your config
npm run dev
# Runs on http://localhost:5000
```

---

## Environment Variables

### Frontend (.env)
```
VITE_API_BASE_URL=http://localhost:5000/api/v1
VITE_PAYMOB_PUBLIC_KEY=your_key
```

### Backend (.env)
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/fashion-ecommerce
JWT_SECRET=your_secret_min_32_chars
CLOUDINARY_CLOUD_NAME=your_cloud
PAYMOB_API_KEY=your_key
SENDGRID_API_KEY=your_key
FRONTEND_URL=http://localhost:5173
```

---

## Recommended VS Code Extensions

1. ESLint
2. Prettier
3. Tailwind CSS IntelliSense
4. ES7+ React/Redux snippets
5. MongoDB for VS Code

---

## Development Workflow

1. Create feature branch: `git checkout -b feature/name`
2. Make changes
3. Test locally
4. Lint: `npm run lint`
5. Commit: `git commit -m "feat: description"`
6. Push & create PR

---

**Last Updated**: April 6, 2026
