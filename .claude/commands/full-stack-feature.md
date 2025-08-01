# Full Stack Feature - End-to-End Feature Implementation

Implement complete full-stack features with backend, frontend, tests, and documentation using coordinated agents.

## Usage

```bash
full-stack-feature "user authentication"      # Implement auth system
full-stack-feature "payment processing"       # Payment feature
full-stack-feature "real-time chat"          # WebSocket chat
full-stack-feature @requirements.md          # From requirements doc
```

## Workflow

This command orchestrates a complete feature development cycle:

### Phase 1: Architecture & Design
1. **code-reviewer** + **refactoring-expert** - Analyze existing architecture
2. **typescript-expert** / **python-expert** - Design API contracts and types

### Phase 2: Backend Implementation  
3. **python-expert** or **typescript-expert** - Implement API endpoints
4. **test-generator** - Create API tests
5. **documentation-writer** - Generate API documentation

### Phase 3: Frontend Implementation
6. **visual-design-extractor** - Extract any UI designs (if provided)
7. **typescript-expert** - Build React/Vue/Angular components
8. **test-generator** - Create component and integration tests

### Phase 4: Integration & Polish
9. **debugger** - Resolve any integration issues
10. **code-reviewer** - Security and quality validation
11. **documentation-writer** - Complete feature documentation

## Example: User Authentication

```bash
full-stack-feature "JWT authentication with email/password"
```

### Generated Structure:
```
backend/
├── api/
│   ├── auth/
│   │   ├── login.ts         # Login endpoint
│   │   ├── register.ts      # Registration endpoint
│   │   ├── refresh.ts       # Token refresh
│   │   └── logout.ts        # Logout endpoint
│   ├── middleware/
│   │   └── auth.ts          # JWT verification
│   └── models/
│       └── user.ts          # User model with bcrypt
│
frontend/
├── components/
│   ├── LoginForm.tsx        # Login component
│   ├── RegisterForm.tsx     # Registration component
│   └── ProtectedRoute.tsx   # Auth wrapper
├── hooks/
│   └── useAuth.ts          # Auth hook with context
├── services/
│   └── authService.ts      # API client
│
tests/
├── backend/
│   ├── auth.test.ts        # API tests
│   └── middleware.test.ts   # Middleware tests
├── frontend/
│   ├── LoginForm.test.tsx   # Component tests
│   └── auth.e2e.ts         # E2E tests
│
docs/
├── API.md                   # API documentation
├── AUTH_FLOW.md            # Authentication flow
└── SETUP.md                # Setup instructions
```

## Options

- `--backend [node|python|go]` - Backend language
- `--frontend [react|vue|angular]` - Frontend framework
- `--database [postgres|mongo|mysql]` - Database choice
- `--auth [jwt|session|oauth]` - Auth strategy
- `--realtime` - Include WebSocket support
- `--mobile` - Include React Native components

## Feature Templates

### E-commerce Features
```bash
full-stack-feature "shopping cart with checkout"
full-stack-feature "product catalog with search"
full-stack-feature "order management system"
```

### Social Features
```bash
full-stack-feature "user profiles with followers"
full-stack-feature "comment system with threads"
full-stack-feature "real-time notifications"
```

### Admin Features
```bash
full-stack-feature "admin dashboard with analytics"
full-stack-feature "content management system"
full-stack-feature "user role management"
```

## Output Example

```
🚀 Full Stack Feature: User Authentication

📋 Architecture Planning...
✅ JWT with refresh tokens
✅ Bcrypt password hashing  
✅ Rate limiting on auth endpoints

🔧 Backend Implementation...
✅ POST /api/auth/register
✅ POST /api/auth/login
✅ POST /api/auth/refresh
✅ Auth middleware created

🎨 Frontend Implementation...
✅ Login/Register forms
✅ useAuth hook
✅ Protected routes
✅ Token management

🧪 Testing Suite...
✅ 15 backend tests (100% coverage)
✅ 12 frontend tests (95% coverage)
✅ 5 E2E test scenarios

📚 Documentation...
✅ API reference with examples
✅ Authentication flow diagram
✅ Frontend integration guide

✨ Feature Complete!
- Secure authentication system
- Full test coverage
- Production ready
```

## Advanced Usage

### From Requirements
```bash
full-stack-feature @requirements/payment-system.md
```

### With Design Mockups
```bash
full-stack-feature "user dashboard" @designs/dashboard.png
```

### Microservice Mode
```bash
full-stack-feature "notification service" --microservice
```

## When to Use

- New feature development
- MVP implementation
- Hackathon projects
- Learning full-stack development
- Rapid prototyping