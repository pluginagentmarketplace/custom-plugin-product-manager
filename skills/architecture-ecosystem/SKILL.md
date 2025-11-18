---
name: architecture-ecosystem
description: Master system design, software architecture, design patterns, and API design. Use when designing large systems, reviewing architecture decisions, optimizing performance, or solving complex technical problems.
---

# Architecture & Design Patterns Ecosystem Skill

## Quick Start

Design robust, scalable systems using proven architectural patterns and design principles.

### Essential Architecture Concepts

```python
# Clean Architecture with Dependency Injection
from abc import ABC, abstractmethod
from dataclasses import dataclass
from typing import List

# Domain Layer
@dataclass
class User:
    id: int
    name: str
    email: str

# Repository Interface (Abstraction)
class UserRepository(ABC):
    @abstractmethod
    def get_user(self, user_id: int) -> User:
        pass

    @abstractmethod
    def save_user(self, user: User) -> None:
        pass

# Use Case / Service Layer
class GetUserUseCase:
    def __init__(self, repository: UserRepository):
        self.repository = repository

    def execute(self, user_id: int) -> User:
        return self.repository.get_user(user_id)

# Presentation / API Layer
class UserController:
    def __init__(self, use_case: GetUserUseCase):
        self.use_case = use_case

    def get_user_handler(self, user_id: int):
        user = self.use_case.execute(user_id)
        return {
            "id": user.id,
            "name": user.name,
            "email": user.email
        }

# Infrastructure Layer
class PostgreSQLUserRepository(UserRepository):
    def get_user(self, user_id: int) -> User:
        # Query database
        pass

    def save_user(self, user: User) -> None:
        # Save to database
        pass
```

## Learning Domains

### 🏛️ **System Design**

**Distributed Systems Fundamentals**
- Network communication models
- Consistency models (Strong, Eventual)
- Consensus algorithms (Raft, Paxos)
- CAP theorem and trade-offs
- Byzantine fault tolerance

**Scalability Patterns**
- Horizontal vs vertical scaling
- Load balancing (round-robin, consistent hashing)
- Database replication and sharding
- Caching strategies (cache-aside, write-through)
- Read replicas and write primaries

**Data Design**
- Database selection criteria
- Normalization vs denormalization
- Sharding strategies (range, hash-based, directory)
- Replication topologies
- Backup and recovery strategies

**High Availability**
- Redundancy and failover
- Multi-region deployment
- Circuit breakers
- Bulkheads and timeouts
- Graceful degradation

### 🏗️ **Software Architecture**

**Architectural Patterns**
- **Monolithic** - Single deployable unit, simpler initially
- **Microservices** - Independent services, scaling flexibility
- **Serverless** - Event-driven, function-based
- **Event-Driven** - Pub-sub, event sourcing, CQRS
- **Layered** - Presentation, business, data layers
- **Hexagonal** - Ports and adapters, boundary separation

**Design Principles**
- **SOLID** - Single Responsibility, Open/Closed, Liskov, Interface Segregation, Dependency Inversion
- **DRY** - Don't Repeat Yourself
- **KISS** - Keep It Simple, Stupid
- **YAGNI** - You Aren't Gonna Need It

**Domain-Driven Design (DDD)**
- Bounded contexts
- Aggregates and roots
- Value objects and entities
- Repositories
- Ubiquitous language
- Event sourcing

**Clean Architecture**
- Dependency rule (point inward)
- Entity and use case layers
- Interface adapter layer
- Framework and driver layer
- Testability focus

### 🔌 **API Design**

**REST Principles**
- Resources and representations
- HTTP verbs (GET, POST, PUT, DELETE, PATCH)
- Status codes (2xx, 3xx, 4xx, 5xx)
- Headers and content negotiation
- Versioning strategies

**GraphQL**
- Query language and schema design
- Resolvers and data loaders
- Subscriptions for real-time
- Query complexity analysis
- Caching strategies

**gRPC**
- Protocol buffers
- Service definitions
- Streaming (unary, server, client, bidirectional)
- Load balancing
- Compression and performance

**API Versioning**
- URL versioning (/v1/resource)
- Header-based versioning
- Query parameter versioning
- Graceful deprecation
- Backward compatibility

### 🎯 **Design Patterns**

**Creational Patterns**
- Singleton (controlled instance)
- Factory (object creation abstraction)
- Builder (complex object construction)
- Prototype (object cloning)

**Structural Patterns**
- Adapter (interface conversion)
- Decorator (behavior addition)
- Facade (simplified interface)
- Bridge (abstraction from implementation)
- Proxy (access control)

**Behavioral Patterns**
- Observer (event notification)
- Strategy (algorithm encapsulation)
- Command (request encapsulation)
- State (state machine)
- Chain of Responsibility (request chaining)
- Mediator (object communication)

**Concurrency Patterns**
- Thread pool (reusable threads)
- Connection pool (reusable connections)
- Lock striping (fine-grained locking)
- Producer-consumer (queue-based processing)
- Monitor object (thread-safe objects)

**Integration Patterns**
- Message Queue (asynchronous processing)
- Saga Pattern (distributed transactions)
- Webhook (push notifications)
- Polling (pull notifications)
- Service discovery (dynamic location)

### 📊 **Performance Architecture**

**Caching Strategies**
- Cache-aside (load-through)
- Write-through (synchronous)
- Write-behind (asynchronous)
- Cache invalidation patterns
- Distributed caching (Redis, Memcached)

**Database Optimization**
- Indexing strategies
- Query optimization (EXPLAIN ANALYZE)
- Denormalization for read performance
- Partitioning and sharding
- Connection pooling

**Code Optimization**
- Algorithmic improvements (Big O analysis)
- Memory optimization
- Lazy loading and initialization
- Memoization and caching
- Profiling and benchmarking

**Network Optimization**
- Connection reuse (HTTP keep-alive)
- Compression (gzip, brotli)
- CDN and edge caching
- Batching and bundling
- Async loading and non-blocking

### 🔐 **Security Architecture**

**Threat Modeling**
- STRIDE methodology
- Attack surface analysis
- Risk assessment and mitigation
- Security requirements
- Secure design patterns

**Cryptography**
- Symmetric vs asymmetric encryption
- Hashing and salting
- Key management and rotation
- Digital signatures
- TLS/SSL implementation

**Authentication & Authorization**
- OAuth2 and OpenID Connect
- SAML for enterprise
- JWT tokens
- Multi-factor authentication
- Role-based access control (RBAC)
- Attribute-based access control (ABAC)

**API Security**
- Input validation and sanitization
- Rate limiting and throttling
- CORS configuration
- CSRF protection
- SQL injection prevention
- XSS prevention

**Data Protection**
- PII (Personally Identifiable Information) handling
- Data encryption at rest
- Encryption in transit
- Secure deletion
- Privacy by design

### 👀 **Code Review & Quality**

**Code Review Practices**
- Standards and guidelines
- Security review checklist
- Performance considerations
- Testing requirements
- Documentation expectations

**Code Quality Metrics**
- Cyclomatic complexity
- Test coverage (unit, integration, E2E)
- Code duplication
- Maintainability index
- Technical debt quantification

**Refactoring Techniques**
- Safe refactoring with tests
- Large-scale refactoring
- Incremental migration
- Feature flags for safe rollout

## Skill Development Checklist

- [ ] Design system for 1M+ users
- [ ] Create architectural decision records (ADRs)
- [ ] Design resilient API
- [ ] Implement circuit breaker pattern
- [ ] Optimize database queries (10x improvement)
- [ ] Design caching strategy
- [ ] Create threat model
- [ ] Conduct architecture review
- [ ] Design disaster recovery

## Real-World Scenarios

**Designing a Scalable Social Network**
```
1. Data Model
   - Users (id, name, email, created_at)
   - Posts (id, user_id, content, created_at)
   - Likes (user_id, post_id)
   - Follows (follower_id, followee_id)

2. Sharding Strategy
   - Shard by user_id (geographic or hash-based)
   - Keep user's posts in same shard
   - Cross-shard queries for feeds

3. Caching
   - Cache recent posts per user
   - Cache follower lists
   - Cache user profiles

4. Load Balancing
   - Geographic load balancing
   - API gateway for routing
   - Database replicas for read scaling

5. Real-time Features
   - WebSocket connections per user
   - Message queue for notifications
   - Event streaming for analytics
```

## Practice Projects

1. **Microservices Architecture**
   - Service decomposition
   - Inter-service communication
   - Distributed transactions

2. **High-Traffic System Design**
   - Handle 100K+ requests per second
   - Multi-region deployment
   - Data consistency at scale

3. **Real-Time Collaboration**
   - Conflict resolution
   - Operational transformation
   - Eventual consistency

## Resources

- **7+ Architecture & Design Roadmaps**
- **95+ Content Modules** - Patterns, principles, case studies
- **System Design Interview** - Preparation guides
- **Architecture Decision Records** - Decision framework
- **Performance Profiling** - Tools and techniques
- **Security Architecture** - Threat modeling and design

## Assessment Criteria

You've mastered this skill when you can:

✓ Design systems handling millions of users
✓ Make informed architecture trade-off decisions
✓ Design secure, resilient systems
✓ Optimize system performance
✓ Create clean, maintainable code
✓ Identify and address technical debt
✓ Mentor others on architecture
✓ Review architecture decisions critically
