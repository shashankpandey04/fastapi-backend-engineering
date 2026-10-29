# FastAPI Backend Engineering
### A Project-Based Backend Development Program

## Program Overview

**Objective:** Train developers to design, build, secure, and maintain backend applications using Python, FastAPI, MongoDB, and PostgreSQL.

The program emphasizes practical engineering over memorizing framework syntax. Trainees will gradually progress from basic APIs to complete backend applications with authentication, authorization, database integrations, external services, and production-oriented features.

### Core Technology Stack

- **Language:** Python
- **Framework:** FastAPI
- **Document database:** MongoDB
- **Relational database:** PostgreSQL
- **MongoDB integration:** PyMongo
- **PostgreSQL integration:** Psycopg
- **Authentication:** JWT and password hashing
- **API security:** Authorization, rate limiting, validation, and secure configuration
- **Integrations:** External APIs, webhooks, email services
- **Version control:** Git and GitHub

### Learning Methodology

Every topic follows a practical engineering workflow:

1. Understand the problem.
2. Discuss possible solutions and trade-offs.
3. Design the implementation.
4. Build the feature.
5. Explore edge cases and failure scenarios.
6. Review the code and improve the design.
7. Document important decisions.

The number of sessions per week remains flexible. Each session is approximately one hour, with additional sessions added whenever the subject or practical implementation requires them.

---

# Phase 1 — Backend Foundations

## Week 1: Backend Engineering Fundamentals

### Topics
- How the internet and client-server architecture work
- Frontend versus backend responsibilities
- HTTP request-response lifecycle
- DNS, TCP, TLS, and HTTP fundamentals
- Servers, ports, APIs, and JSON
- REST API fundamentals
- Monolithic and microservice architectures
- Functional and non-functional requirements
- Latency, throughput, scalability, and availability
- Breaking a project into backend components

### Practical Work
Design the backend architecture of an event management platform.

Identify:
- Application components
- Users and their roles
- Main features
- Required API endpoints
- Data entities and relationships
- External dependencies

**Milestone:** A basic system design document and architecture diagram.

## Week 2: Python for Backend Development

### Topics
- Functions, modules, packages, and imports
- Object-oriented programming
- Type hints and Python typing
- Lists, dictionaries, sets, and comprehensions
- Exception handling
- Context managers
- Environment variables and configuration
- Virtual environments and dependency management
- JSON serialization and data transformations
- Synchronous versus asynchronous programming fundamentals
- Writing reusable, maintainable functions

### Practical Work
Build Python modules for:
- User registration validation
- Event creation
- Registration eligibility
- Event capacity calculations
- Consistent error handling

**Milestone:** A small, modular Python application implementing event management logic.

## Week 3: HTTP and REST API Design

### Topics
- HTTP methods and status codes
- Request headers and bodies
- Path and query parameters
- Cookies and authorization headers
- JSON serialization
- Request validation
- REST resource modeling
- Naming endpoints consistently
- Pagination, filtering, and sorting
- Standardized error responses
- API versioning fundamentals
- CORS and preflight requests
- Idempotency and retry considerations
- OpenAPI documentation

### Practical Work
Design the API contract for the event management platform before implementing it.

Example endpoints:
- `POST /users`
- `POST /auth/login`
- `GET /events`
- `POST /events`
- `GET /events/{event_id}`
- `POST /events/{event_id}/registrations`

**Milestone:** A documented API specification with request schemas, response structures, and error cases.

---

# Phase 2 — FastAPI Development

## Week 4: FastAPI Fundamentals

### Topics
- Creating a FastAPI application
- Path and query parameters
- Request bodies
- Pydantic models
- Request validation
- Response models
- Status codes
- Error handling
- Automatic API documentation
- Dependency injection using `Depends`
- Reusable dependencies
- Application configuration
- Routers and modular endpoints
- Middleware fundamentals

### Practical Work
Build the first version of the event management API.

Implement:
- Event creation
- Event listing
- Event details
- Event updates
- Event deletion
- Request validation
- Consistent error responses

**Milestone:** A modular FastAPI application with documented CRUD endpoints.

---

# Phase 3 — Database Engineering

## Week 5: MongoDB Fundamentals and Integration

### Topics
- Document-oriented database concepts
- Databases, collections, and documents
- BSON and JSON
- ObjectId
- CRUD operations
- Query filters and projections
- Sorting and pagination
- Embedded documents versus references
- Schema design
- Unique indexes and constraints
- Connecting MongoDB to FastAPI using PyMongo
- Database connection management
- ObjectId serialization
- Handling database errors

### Practical Work
Build a MongoDB-backed API for users, profiles, and events.

Focus on choosing appropriate document structures and implementing database operations cleanly.

**Milestone:** A working FastAPI application backed by MongoDB.

## Week 6: PostgreSQL Fundamentals and Integration

### Topics
- Relational database concepts
- Tables, rows, and columns
- Primary and foreign keys
- Relationships and normalization
- SQL queries
- JOINs and aggregation
- Constraints and indexes
- Parameterized queries
- Connecting PostgreSQL through Psycopg
- Connection management
- Transactions
- Data integrity
- SQL injection prevention
- Mapping database records to API responses

### Practical Work
Implement the event registration system using PostgreSQL.

Features:
- User and event relationships
- Event registrations
- Registration capacity
- Duplicate-registration prevention
- Transactional database operations

**Milestone:** A PostgreSQL-backed API with relational integrity and transactional business logic.

## Week 7: Database Design and Real-World Data Operations

### Topics
- MongoDB versus PostgreSQL
- Choosing databases based on access patterns
- Relational versus document modeling
- Data consistency
- Database constraints versus application validation
- Indexing fundamentals
- Pagination for large datasets
- Transaction boundaries
- Concurrent requests and race conditions
- Preventing duplicate operations
- Query performance fundamentals
- Separating database access from API routes

### Practical Work
Extend the event management platform.

Trainees must justify:
- Which data belongs in MongoDB
- Which data belongs in PostgreSQL
- How relationships are represented
- Which constraints belong in the database
- How concurrent registrations are handled

**Milestone:** A database-backed application with documented design decisions and reliable business operations.

---

# Phase 4 — Authentication and Security

## Week 8: Authentication with JWT

### Topics
- Authentication versus authorization
- User registration and login
- Password hashing
- Secure password verification
- JWT structure
- Token signing and verification
- Access tokens
- Token expiration
- JWT claims and validation
- Protecting FastAPI endpoints
- Authentication dependencies
- Handling invalid and expired tokens

### Practical Work
Implement:
- User registration
- Login
- Password verification
- JWT issuance
- Protected endpoints
- Current-user dependency

**Milestone:** A working JWT-based authentication system.

## Week 9: Refresh Tokens, Roles, and Authorization

### Topics
- Access-token and refresh-token lifecycles
- Refresh-token rotation and revocation strategies
- Logout behavior
- Role-based access control
- User roles and permissions
- Resource ownership
- Admin-only operations
- Preventing unauthorized resource access
- Authentication versus authorization errors
- Testing permission boundaries manually

### Practical Work
Implement roles such as:
- User
- Event organizer
- Administrator

Ensure that users can only access or modify resources they are authorized to use.

**Milestone:** A complete authentication and authorization flow with resource-level permissions.

## Week 10: API Security and Rate Limiting

### Topics
- Common API security vulnerabilities
- SQL injection and unsafe queries
- Broken object-level authorization
- Brute-force attacks
- Input validation
- Sensitive data exposure
- CORS configuration
- Secure secret management
- Rate-limiting algorithms
- Fixed-window and sliding-window approaches
- Token-bucket concepts
- Per-IP and per-user limits
- Endpoint-specific limits
- HTTP 429 responses
- Trusted proxy and client-IP considerations

### Practical Work
Secure the authentication and event APIs.

Implement:
- Login rate limits
- Public endpoint limits
- Authenticated-user limits
- Consistent rate-limit responses
- Authorization checks
- Protection against common input and access-control vulnerabilities

**Milestone:** A secured API with appropriate authorization and rate-limiting controls.

---

# Phase 5 — Intermediate Backend Engineering

## Week 11: Application Architecture and Maintainable Code

### Topics
- Organizing a FastAPI project
- Routes, services, and database access
- Separating HTTP handling from business logic
- Dependency injection
- Reusable components
- Application configuration
- Exception handling
- Modular monolith architecture
- Separation of concerns
- Avoiding circular imports
- Avoiding unnecessary abstractions
- Architecture decision records

### Practical Work
Refactor the existing application into clear modules.

A possible structure:

```text
app/
├── main.py
├── core/
│   ├── config.py
│   └── security.py
├── api/
│   └── routes/
├── schemas/
├── services/
├── repositories/
├── database/
└── models/
```

The exact structure should follow project complexity rather than being treated as a universal rule.

**Milestone:** A maintainable application with clearly defined responsibilities.

## Week 12: External API Integrations

### Topics
- Calling external APIs from Python
- HTTP clients
- API keys and external-service authentication
- Request timeouts
- Response validation
- Handling non-success status codes
- Retry strategies and exponential backoff
- External-service failures
- Webhooks
- Webhook signature verification
- Duplicate webhook delivery
- Idempotent processing
- Integration-specific error handling

### Practical Work
Integrate an external service into the event platform.

Possible integrations:
- Email delivery
- Payment gateway sandbox
- Third-party user or organization data
- External notification service

**Milestone:** A backend integration that handles timeouts, failures, and duplicate requests appropriately.

## Week 13: Async Python and Background Processing

### Topics
- `async` and `await`
- Event-loop fundamentals
- Synchronous versus asynchronous functions
- I/O-bound versus CPU-bound workloads
- Blocking calls inside asynchronous endpoints
- Async HTTP clients
- Database driver compatibility
- FastAPI background tasks
- Long-running operations
- Email and notification processing
- Background workers and task queues
- Retry and failure-handling strategies

### Practical Work
Add background notification processing to the project.

Discuss when FastAPI background tasks are sufficient and when a separate worker or task queue is more appropriate.

**Milestone:** An application that handles I/O and background work without unnecessarily blocking requests.

---

# Phase 6 — Testing, Debugging, and Reliability

## Week 14: API Testing and Debugging

### Topics
- Why backend applications need tests
- Unit, integration, and API testing concepts
- Testing endpoints with an API client
- Valid and invalid request scenarios
- Authentication and authorization checks
- Database behavior
- Debugging tracebacks
- Reproducing bugs
- Logging useful diagnostic information
- Testing edge cases
- Investigating transaction failures
- Regression testing fundamentals

### Practical Work
Create a manual API verification collection and a documented set of test scenarios.

Cover:
- Successful requests
- Invalid input
- Missing authentication
- Insufficient permissions
- Duplicate registration
- Database failures
- Rate-limit violations
- External-service failures

**Milestone:** A repeatable API verification process with documented expected results.

## Week 15: Performance and Production Readiness

### Topics
- Latency and throughput
- Database indexes
- Query performance
- Connection management
- Pagination and large responses
- Caching fundamentals
- Redis use cases
- Rate-limit state across application instances
- Request timeouts
- Graceful error handling
- Structured logging
- Health endpoints
- Environment-specific configuration
- Performance measurement before optimization

### Practical Work
Identify and improve a performance bottleneck in the existing application.

Document:
- The original problem
- How it was measured
- The change made
- The measured result
- Remaining limitations

**Milestone:** A backend with documented performance improvements and basic operational visibility.

---

# Phase 7 — Capstone Project

## Week 16: Independent Project and Architecture Review

### Project Requirements

Each trainee or team builds a backend application that demonstrates the concepts covered throughout the program.

Possible projects:
- E-commerce backend
- Recruitment management system
- Learning management system
- Appointment booking platform
- Inventory management system
- Expense management SaaS
- Notification platform
- AI inference API
- URL shortener

### Required Features

Every capstone should include:
- Clear requirements
- Documented architecture
- FastAPI endpoints
- MongoDB or PostgreSQL, selected according to the project's requirements
- Appropriate data modeling
- Authentication
- Authorization
- Input validation
- Consistent error handling
- Rate limiting where appropriate
- At least one meaningful external integration or equivalent advanced feature
- API documentation
- A repeatable verification process
- Setup and deployment instructions

### Final Review

Trainees must:
1. Explain their architecture.
2. Demonstrate the application.
3. Explain their database decisions.
4. Walk through authentication and authorization.
5. Demonstrate how errors and edge cases are handled.
6. Explain important trade-offs.
7. Identify limitations and future improvements.

**Final milestone:** A complete backend project that the trainee can explain, operate, and extend independently.

---

# Assessment Framework

| Category | Weight |
|---|---:|
| System design and requirements | 10% |
| API design and FastAPI implementation | 15% |
| Database design and integration | 15% |
| Authentication and security | 20% |
| Application architecture and code quality | 10% |
| External integrations and backend logic | 10% |
| API verification and debugging | 10% |
| Capstone demonstration and technical explanation | 10% |
| **Total** | **100%** |

## Definition of Success

By the end of the program, a trainee should be able to take a backend requirement from initial design to a working API, select an appropriate database, implement authentication and authorization, integrate external services, diagnose common failures, and explain their engineering decisions.
