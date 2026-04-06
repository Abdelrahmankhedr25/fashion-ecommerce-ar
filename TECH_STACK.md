# Technology Stack Documentation

## Frontend Stack

### Core
- **React.js 18+** (via Vite)
- **Tailwind CSS 3.x**
- **React Router v6**

### State & Forms
- **Context API** (initial)
- **React Hook Form + Yup**

### AR Technology
- **AR.js** (MVP) or **8th Wall** (premium)

### Tools
- **Axios** (HTTP client)
- **Vite** (build tool)

---

## Backend Stack

### Runtime
- **Node.js 18+ LTS**
- **Express.js 4.x**

### Database
- **MongoDB 6+** (Atlas)
- **Mongoose 7.x** (ODM)

### Authentication
- **JWT** (access + refresh tokens)
- **bcrypt** (password hashing)

### Services
- **Cloudinary** (image storage)
- **SendGrid** (email)
- **Paymob** (payments)

---

## DevOps & Hosting

### Platforms
- **GitHub** (version control + CI/CD)
- **Vercel** (frontend)
- **Railway** (backend)
- **MongoDB Atlas** (database)

### Monitoring
- **Google Analytics 4**
- **Sentry** (errors)

---

## Security

- **Helmet.js** (HTTP headers)
- **CORS** configuration
- **express-rate-limit**
- **express-validator**
- **HTTPS only**

---

## Database Schemas

### Users
```
email, password (hashed), name, addresses, role
```

### Products
```
name, slug, price, category, sizes, colors, images, stock
```

### Orders
```
orderNumber, user, items, totalAmount, paymentStatus, orderStatus
```

---

**Last Updated**: April 6, 2026
