---
name: backend-ecosystem
description: Master backend development with Node.js, Python, Go, Java, databases, and API design. Use when building scalable server applications, designing databases, creating APIs, or implementing complex business logic.
---

# Backend Ecosystem Skill

## Quick Start

Build production-grade backend systems with scalable architecture, robust databases, and well-designed APIs.

### Essential Backend Stack

```python
# Python FastAPI example
from fastapi import FastAPI, HTTPException
from sqlalchemy import create_engine
from sqlalchemy.orm import Session
from pydantic import BaseModel

app = FastAPI()
DATABASE_URL = "postgresql://user:password@localhost/dbname"
engine = create_engine(DATABASE_URL)

class UserCreate(BaseModel):
    username: str
    email: str

@app.post("/users/")
async def create_user(user: UserCreate, db: Session):
    # Create user with validation
    db_user = User(username=user.username, email=user.email)
    db.add(db_user)
    db.commit()
    return db_user

@app.get("/users/{user_id}")
async def get_user(user_id: int, db: Session):
    user = db.query(User).filter(User.id == user_id).first()
    if not user:
        raise HTTPException(status_code=404, detail="User not found")
    return user
```

## Learning Domains

### 🗣️ **Programming Languages**

**Node.js/JavaScript**
- Async patterns and event loop
- npm ecosystem and dependencies
- TypeScript for Node.js
- Worker threads and clustering

**Python**
- Flask, Django, FastAPI frameworks
- Async with asyncio
- Type hints and Pydantic
- Virtual environments and dependencies

**Go**
- Goroutines and channels
- Interfaces and composition
- Testing and benchmarking
- Building CLIs and services

**Java**
- Spring Boot framework
- Dependency injection
- ORM with Hibernate/JPA
- Testing with JUnit and Mockito

**Other Languages**
- Rust for systems programming
- PHP/Laravel for web development
- C# and ASP.NET Core

### 🗄️ **Database Design & Optimization**

**SQL Databases**
- Normalization and schema design
- Indexing strategies
- Query optimization
- Transaction management and ACID
- PostgreSQL advanced features

**NoSQL Solutions**
- Document databases (MongoDB)
- Key-value stores (Redis)
- Time-series databases
- When to use NoSQL vs SQL

**Data Modeling**
- Entity-relationship diagrams
- Denormalization strategies
- Partitioning and sharding
- Backup and recovery strategies

### 🔌 **API Design & Implementation**

**REST APIs**
- Resource-oriented design
- HTTP methods and status codes
- Error handling and standardization
- Pagination and filtering
- Versioning strategies

**GraphQL**
- Schema definition language
- Resolvers and data loaders
- Query optimization
- Subscriptions for real-time

**Authentication & Security**
- JWT and OAuth2 implementation
- Password hashing and salt
- Rate limiting and throttling
- CORS and security headers

### 🏗️ **Architecture Patterns**

**Design Patterns**
- Repository pattern
- Factory pattern
- Middleware pattern
- Observer pattern

**Architectural Styles**
- Monolithic architecture
- Microservices patterns
- Service discovery
- API gateways

**Concurrency Patterns**
- Thread pools
- Async/await
- Message queues
- Worker processes

### 📊 **Data Processing**

**Caching Strategies**
- In-memory caching (Redis)
- Cache invalidation patterns
- Cache-aside and write-through
- Distributed caching

**Message Queues**
- RabbitMQ, Kafka, SQS
- Pub-sub patterns
- Message ordering and delivery
- Dead letter queues

**Background Jobs**
- Job queues and workers
- Scheduled tasks (Cron)
- Batch processing
- Error handling and retries

### 🔐 **Security & Reliability**

**Security**
- Input validation
- SQL injection prevention
- XSS and CSRF protection
- Secure configuration management

**Error Handling**
- Exception handling strategies
- Logging and monitoring
- Health checks and metrics
- Circuit breakers

### 🧪 **Testing Strategies**

**Test Types**
- Unit tests
- Integration tests
- Contract testing
- Load testing

## Skill Development Checklist

- [ ] Design database schema for complex domain
- [ ] Build REST API with 20+ endpoints
- [ ] Implement GraphQL API
- [ ] Create comprehensive test suite (80%+ coverage)
- [ ] Setup CI/CD pipeline
- [ ] Implement authentication and authorization
- [ ] Optimize database queries (10x improvement)
- [ ] Handle concurrent requests efficiently

## Real-World Scenarios

**E-Commerce API**
```go
// Go Echo framework example
package main

import (
    "github.com/labstack/echo/v4"
    "github.com/labstack/echo/v4/middleware"
)

type Product struct {
    ID    int     `json:"id"`
    Name  string  `json:"name"`
    Price float64 `json:"price"`
}

func main() {
    e := echo.New()

    // Middleware
    e.Use(middleware.Logger())
    e.Use(middleware.Recover())

    // Routes
    e.GET("/products", getProducts)
    e.POST("/products", createProduct)
    e.GET("/products/:id", getProduct)

    e.Logger.Fatal(e.Start(":1323"))
}

func getProducts(c echo.Context) error {
    // Fetch from DB with pagination
    products := fetchProductsWithPagination(
        c.QueryParam("page"),
        c.QueryParam("limit"),
    )
    return c.JSON(200, products)
}
```

## Practice Projects

1. **User Management System**
   - User registration and authentication
   - Role-based access control
   - User profile management

2. **Blog Platform**
   - Post CRUD operations
   - Comment system with nesting
   - Search functionality

3. **E-Commerce Backend**
   - Product catalog
   - Shopping cart and orders
   - Payment integration
   - Inventory management

4. **Real-Time Chat API**
   - User authentication
   - Message storage
   - Real-time notifications
   - Group conversations

## Resources

- **12+ Backend Roadmaps** - Node.js, Python, Go, Java, PHP, Rust
- **145+ Content Modules** - From basics to advanced patterns
- **Database Guides** - SQL optimization, schema design
- **API Design** - REST, GraphQL, gRPC patterns
- **Framework Tutorials** - Express, Django, Spring Boot, Laravel
- **Testing Guides** - Unit, integration, and load testing

## Assessment Criteria

You've mastered this skill when you can:

✓ Design scalable database schemas
✓ Build secure, production-grade APIs
✓ Implement complex business logic
✓ Optimize database queries significantly
✓ Create comprehensive test coverage
✓ Handle authentication and authorization properly
✓ Monitor and debug production systems
✓ Design for reliability and fault tolerance
