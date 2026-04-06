# Technology Stack Details

## Frontend Stack

### Core
- **React 18.2+** - UI library
- **Vite** - Build tool (faster than CRA)
- **TypeScript** - Type safety (optional, recommended)

### Styling
- **Tailwind CSS 3.x** - Utility-first CSS
- **Headless UI** - Accessible components
- **React Icons** - Icon library

### State Management
- **React Context API** - Global state (auth, cart)
- **React Query (TanStack Query)** - Server state management
- **Zustand** - Alternative lightweight state (optional)

### Routing & Navigation
- **React Router v6** - Client-side routing

### Forms & Validation
- **React Hook Form** - Form state management
- **Zod** - Schema validation

### HTTP Client
- **Axios** - API requests with interceptors

### Image Handling
- **React Image Gallery** - Product image carousels
- **React Lazy Load Image** - Performance optimization

## Backend Stack

### Core
- **Node.js 18 LTS** - Runtime
- **Express.js 4.x** - Web framework
- **TypeScript** - Type safety (optional)

### Database
- **MongoDB 6+** - NoSQL database
- **Mongoose** - ODM for MongoDB

### Authentication
- **jsonwebtoken (JWT)** - Token-based auth
- **bcryptjs** - Password hashing
- **express-validator** - Input validation

### File Upload
- **Multer** - File upload middleware
- **Cloudinary SDK** - Image CDN

### Payment Gateway
- **Paymob Node.js SDK** - Payment integration

### Email
- **Nodemailer** - Email sending
- **Gmail SMTP** or **SendGrid** - Email service

### Security
- **helmet** - Security headers
- **cors** - CORS middleware
- **express-rate-limit** - Rate limiting
- **express-mongo-sanitize** - NoSQL injection prevention

### Logging
- **winston** - Logging library
- **morgan** - HTTP request logger

## Development Tools

### Code Quality
- **ESLint** - Linting
- **Prettier** - Code formatting
- **Husky** - Git hooks
- **lint-staged** - Pre-commit checks

### Testing
- **Jest** - Unit testing
- **Supertest** - API testing
- **React Testing Library** - Component testing
- **Cypress** - E2E testing

### API Development
- **Postman** - API testing
- **Swagger / OpenAPI** - API documentation

## Infrastructure & DevOps

### Hosting
- **Vercel** - Frontend deployment
- **Railway** or **Render** - Backend deployment
- **MongoDB Atlas** - Database hosting

### CDN & Storage
- **Cloudinary** - Image storage & optimization

### CI/CD
- **GitHub Actions** - Automated testing & deployment

### Monitoring
- **Sentry** - Error tracking
- **Google Analytics** - User analytics
- **LogRocket** - Session replay (optional)

### Performance
- **Lighthouse** - Performance audits
- **GTmetrix** - Speed testing

## AR Module (Future Phase)

### WebAR Options
- **AR.js** - Free, lightweight (basic AR)
- **8th Wall** - Premium, robust (advanced AR)
- **Three.js** - 3D rendering engine

### AI/ML (for body detection)
- **TensorFlow.js** - Body pose detection
- **MediaPipe** - Google's ML solutions

## Package Management
- **npm** or **pnpm** - Dependency management

## Version Control
- **Git** - Source control
- **GitHub** - Repository hosting

## Recommended VSCode Extensions
- ESLint
- Prettier
- Tailwind CSS IntelliSense
- ES7+ React/Redux/React-Native snippets
- MongoDB for VS Code