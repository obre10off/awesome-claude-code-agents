# API First - Design-First API Development

Design, implement, test, and document production-ready APIs using OpenAPI specification and coordinated agents.

## Usage

```bash
api-first "user management API"           # Create from description
api-first @openapi.yaml                  # Implement from OpenAPI spec
api-first @requirements.md --rest        # RESTful API from requirements
api-first "payment API" --graphql       # GraphQL API
```

## Workflow

### Phase 1: API Design
1. **documentation-writer** - Creates OpenAPI specification
2. **code-reviewer** - Reviews API design for RESTful principles

### Phase 2: Implementation
3. **typescript-expert** / **python-expert** - Implements endpoints
4. **test-generator** - Creates API tests with coverage

### Phase 3: Enhancement
5. **refactoring-expert** - Optimizes performance
6. **code-reviewer** - Security and best practices review

### Phase 4: Documentation
7. **documentation-writer** - Generates complete API docs

## What Gets Generated

### OpenAPI Specification
```yaml
openapi: 3.0.0
info:
  title: User Management API
  version: 1.0.0
paths:
  /users:
    get:
      summary: List users
      parameters:
        - name: page
          in: query
          schema:
            type: integer
      responses:
        200:
          description: User list
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/User'
```

### Implementation
```typescript
// Express.js implementation
router.get('/users', 
  authenticate,
  validateQuery(UserListSchema),
  rateLimit({ window: '1m', max: 100 }),
  async (req, res) => {
    const { page = 1, limit = 20 } = req.query;
    
    const users = await userService.list({
      page: Number(page),
      limit: Number(limit)
    });
    
    res.json({
      data: users,
      meta: {
        page: Number(page),
        limit: Number(limit),
        total: users.total
      }
    });
  }
);
```

### Tests
```typescript
describe('GET /users', () => {
  it('returns paginated users', async () => {
    const response = await request(app)
      .get('/users?page=1&limit=10')
      .set('Authorization', `Bearer ${token}`)
      .expect(200);
      
    expect(response.body.data).toHaveLength(10);
    expect(response.body.meta.page).toBe(1);
  });
  
  it('requires authentication', async () => {
    await request(app)
      .get('/users')
      .expect(401);
  });
});
```

## Features

### RESTful API Patterns
- CRUD operations with proper HTTP verbs
- Pagination, filtering, and sorting
- HATEOAS links
- Versioning strategies
- Content negotiation

### GraphQL Support
```bash
api-first "e-commerce API" --graphql
```
Generates:
- GraphQL schema
- Resolvers with DataLoader
- Subscriptions
- Schema documentation

### Authentication & Security
- JWT/OAuth2 implementation
- API key management
- Rate limiting
- CORS configuration
- Input validation
- SQL injection prevention

### API Gateway Features
```bash
api-first @api-spec.yaml --gateway
```
Includes:
- Request/response transformation
- API composition
- Circuit breakers
- Caching strategies

## Output Example

```
🎯 API First Development: User Management API

📋 Design Phase:
✅ OpenAPI 3.0 specification
✅ 12 endpoints defined
✅ Request/response schemas
✅ Authentication flows

🔧 Implementation:
✅ POST   /api/users          - Create user
✅ GET    /api/users          - List users
✅ GET    /api/users/:id      - Get user
✅ PUT    /api/users/:id      - Update user
✅ DELETE /api/users/:id      - Delete user
✅ POST   /api/users/:id/avatar - Upload avatar

🧪 Test Suite:
✅ 45 integration tests
✅ Contract testing
✅ Load testing setup
✅ 98% code coverage

📚 Documentation:
✅ Interactive API explorer
✅ Code examples (curl, JS, Python)
✅ Postman collection
✅ Authentication guide

🚀 Deployment Ready:
✅ Docker configuration
✅ Health check endpoint
✅ Monitoring integration
✅ CI/CD pipeline
```

## Advanced Options

### Microservices
```bash
api-first "order service" --microservice --async
```
Generates service with:
- Event sourcing
- CQRS pattern
- Message queue integration
- Service mesh configuration

### API Versioning
```bash
api-first @api-v2.yaml --version 2 --migrate @api-v1.yaml
```
Creates:
- Version migration guide
- Backward compatibility layer
- Deprecation warnings
- Client migration tools

### Mock Server
```bash
api-first @spec.yaml --mock
```
Generates mock server for frontend development

### Client SDKs
```bash
api-first @api.yaml --sdk typescript,python,go
```
Generates type-safe client libraries

## Best Practices Enforced

1. **RESTful Principles**
   - Proper HTTP methods
   - Status codes
   - Resource naming
   - Statelessness

2. **Security**
   - Authentication required
   - Input validation
   - Rate limiting
   - HTTPS only

3. **Performance**
   - Pagination
   - Caching headers
   - Compression
   - Query optimization

4. **Documentation**
   - Every endpoint documented
   - Request/response examples
   - Error scenarios
   - Authentication flows

## When to Use

- New API development
- API modernization
- Microservices design
- Third-party integrations
- API-first products