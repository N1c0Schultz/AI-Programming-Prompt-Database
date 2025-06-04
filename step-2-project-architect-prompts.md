# Step 2: Project Architect Prompts

System architecture and technical design prompts for creating scalable, maintainable, and robust software architectures. These prompts help design system components, define interfaces, and establish technical patterns.

## Table of Contents
- [System Architecture Design](#system-architecture-design)
- [Component Design](#component-design)
- [Integration Architecture](#integration-architecture)

---

## System Architecture Design

### Microservices Architecture Planning
**Use Case**: Design a microservices architecture with proper service boundaries, communication patterns, and data management strategies.

**Copy-Pastable Prompt**:
```
Help me design a microservices architecture for my application. I need guidance on service decomposition, communication patterns, and infrastructure design.

APPLICATION OVERVIEW:
[Describe your application's core functionality and business domain]

CURRENT REQUIREMENTS:
- Expected scale: [User base, transaction volume, data size]
- Performance needs: [Response times, throughput requirements]
- Team structure: [Number of teams, their expertise areas]
- Deployment preferences: [Cloud providers, container orchestration]

BUSINESS DOMAINS:
[List the main business areas/domains in your application]

Please provide:

SERVICE DECOMPOSITION:
- Recommended microservice boundaries based on business domains
- Service responsibilities and ownership
- Data ownership and database-per-service strategy
- Service size guidelines (team ownership, complexity)

COMMUNICATION DESIGN:
- Synchronous vs asynchronous communication patterns
- API gateway and service mesh recommendations
- Event-driven architecture design
- Message broker selection and event schema design

DATA ARCHITECTURE:
- Database selection per service
- Data consistency strategies (SAGA pattern, eventual consistency)
- Data sharing and integration approaches
- CQRS and Event Sourcing considerations

INFRASTRUCTURE PATTERNS:
- Service discovery and configuration management
- Load balancing and circuit breaker patterns
- Monitoring, logging, and distributed tracing
- Security and authentication across services

DEPLOYMENT STRATEGY:
- Container orchestration approach (Kubernetes, Docker Swarm)
- CI/CD pipeline design for multiple services
- Environment management and configuration
- Rolling deployment and blue-green deployment strategies

EVOLUTION STRATEGY:
- Migration path from monolith (if applicable)
- Service versioning and backward compatibility
- Technical debt management across services
- Team autonomy and governance balance

Include specific technology recommendations and highlight potential challenges with mitigation strategies.
```

### Monolithic to Microservices Migration
**Use Case**: Plan the decomposition of an existing monolithic application into microservices with minimal disruption and risk.

**Copy-Pastable Prompt**:
```
Help me plan a migration from a monolithic architecture to microservices. I need a strategic approach that minimizes risk and business disruption.

CURRENT MONOLITH:
- Technology stack: [Language, framework, database]
- Application size: [Lines of code, team size, age]
- Business domains: [Major functional areas]
- Known pain points: [Performance, scaling, maintenance issues]

MIGRATION DRIVERS:
- Primary reasons for migration: [Scale, team autonomy, technology modernization]
- Success criteria: [How will you measure success?]
- Timeline constraints: [Hard deadlines, business cycles]
- Risk tolerance: [Conservative vs aggressive approach]

CONSTRAINTS:
- Team availability and skills: [Current expertise, training needs]
- Budget limitations: [Infrastructure, tooling, training costs]
- Business continuity requirements: [Downtime tolerance, feature delivery]

Please provide:

MIGRATION STRATEGY:
- Recommended decomposition approach (Strangler Fig, Database decomposition, etc.)
- Service extraction priority and sequencing
- Parallel run vs phased cutover strategy
- Rollback plans and safety measures

TECHNICAL APPROACH:
- Data migration and synchronization strategies
- API extraction and versioning approach
- Shared library and common code handling
- Testing strategy during migration phases

INFRASTRUCTURE EVOLUTION:
- Gradual infrastructure modernization plan
- Monitoring and observability improvements
- Deployment pipeline evolution
- Configuration and secret management updates

ORGANIZATIONAL CHANGES:
- Team restructuring recommendations
- Skill development and training plan
- Communication and coordination adjustments
- Service ownership and responsibility models

RISK MITIGATION:
- Technical risks and contingency plans
- Business continuity protection measures
- Performance and reliability safeguards
- Quality assurance during transition

PHASE-BY-PHASE PLAN:
- Detailed breakdown of first 3-6 months
- Milestone definitions and success criteria
- Decision points and go/no-go gates
- Resource allocation and timeline estimates

Provide specific recommendations for my domain and highlight common pitfalls to avoid.
```

### Event-Driven Architecture Design
**Use Case**: Design event-driven systems with proper event modeling, messaging patterns, and consistency guarantees.

**Copy-Pastable Prompt**:
```
Help me design an event-driven architecture for my system. I need guidance on event modeling, messaging infrastructure, and consistency patterns.

SYSTEM CONTEXT:
[Describe your system's purpose and main business processes]

BUSINESS PROCESSES:
[List key business workflows that generate or consume events]

SCALABILITY REQUIREMENTS:
- Event volume: [Events per second/minute/hour]
- Processing latency: [Real-time vs near real-time vs batch]
- Geographic distribution: [Single region vs multi-region]
- Durability requirements: [Event retention, replay capabilities]

Please design:

EVENT MODELING:
- Core business events and their structure
- Event taxonomy and naming conventions
- Event schema evolution and versioning strategy
- Event metadata and correlation patterns

MESSAGING INFRASTRUCTURE:
- Message broker selection (Kafka, RabbitMQ, AWS SQS/SNS, etc.)
- Topic/queue design and partitioning strategy
- Message ordering and delivery guarantees
- Dead letter queue and error handling patterns

PROCESSING PATTERNS:
- Event sourcing implementation approach
- CQRS (Command Query Responsibility Segregation) design
- Saga pattern for distributed transactions
- Event replay and reprocessing capabilities

CONSISTENCY AND RELIABILITY:
- Eventual consistency handling strategies
- Idempotency and duplicate event handling
- At-least-once vs exactly-once delivery tradeoffs
- Cross-service transaction coordination

CONSUMER DESIGN:
- Event handler patterns and implementation
- Consumer scaling and load balancing
- Event filtering and routing strategies
- Error handling and retry mechanisms

MONITORING AND OBSERVABILITY:
- Event flow tracking and tracing
- Performance metrics and alerting
- Event audit trails and debugging tools
- Schema registry and governance

OPERATIONAL CONCERNS:
- Event stream backup and disaster recovery
- Performance tuning and optimization
- Security and access control for events
- Testing strategies for event-driven systems

Include specific technology recommendations, implementation patterns, and common architectural pitfalls to avoid.
```

---

## Component Design

### Domain-Driven Design (DDD) Implementation
**Use Case**: Apply Domain-Driven Design principles to create well-bounded contexts, aggregates, and domain models that reflect business reality.

**Copy-Pastable Prompt**:
```
Help me apply Domain-Driven Design (DDD) principles to my software architecture. I need guidance on domain modeling, bounded contexts, and tactical patterns.

BUSINESS DOMAIN:
[Describe your business domain and core problem you're solving]

KEY BUSINESS PROCESSES:
[List the main business workflows and rules]

STAKEHOLDERS:
[Identify different user types and their roles]

EXISTING SYSTEM CONTEXT:
[Describe current system boundaries and integrations if any]

Please help me design:

STRATEGIC DESIGN:
- Bounded context identification and boundaries
- Context mapping between bounded contexts
- Ubiquitous language definition for each context
- Core domain vs supporting subdomain classification

DOMAIN MODEL:
- Entity and value object identification
- Aggregate design and boundaries
- Domain service responsibilities
- Repository and factory patterns

TACTICAL PATTERNS:
- Aggregate root selection and design
- Domain event modeling and handling
- Specification pattern implementation
- Policy and rule object patterns

LAYERED ARCHITECTURE:
- Application service layer design
- Domain layer isolation and dependencies
- Infrastructure layer abstractions
- Anti-corruption layer design for external integrations

IMPLEMENTATION GUIDANCE:
- Code organization and package structure
- Dependency injection and inversion patterns
- Testing strategies for domain logic
- Persistence ignorance and abstraction

EVOLUTION STRATEGY:
- Domain model refactoring approaches
- Legacy system integration patterns
- Gradual migration to DDD patterns
- Team knowledge sharing and adoption

COMMON PITFALLS:
- Anemic domain model avoidance
- Over-engineering vs under-modeling balance
- Context boundary violation prevention
- Domain logic leakage into other layers

Provide specific code structure examples and implementation patterns for my domain.
```

### API Gateway and Service Mesh Design
**Use Case**: Design API gateway patterns and service mesh architecture for managing microservices communication, security, and observability.

**Copy-Pastable Prompt**:
```
Help me design an API gateway and service mesh architecture for my microservices ecosystem. I need guidance on traffic management, security, and observability.

MICROSERVICES CONTEXT:
- Number of services: [Current and projected]
- Service types: [Public APIs, internal services, legacy integrations]
- Client types: [Web apps, mobile apps, third-party integrations]
- Traffic patterns: [Request volume, geographic distribution]

REQUIREMENTS:
- Security needs: [Authentication, authorization, rate limiting]
- Performance requirements: [Latency, throughput, availability]
- Operational needs: [Monitoring, logging, debugging]
- Compliance requirements: [GDPR, HIPAA, etc.]

Please design:

API GATEWAY ARCHITECTURE:
- Gateway placement and topology (single vs multiple gateways)
- Routing and load balancing strategies
- Request/response transformation patterns
- Rate limiting and throttling policies

SECURITY IMPLEMENTATION:
- Authentication and authorization flows
- JWT token management and validation
- API key management and rotation
- SSL/TLS termination and certificate management

SERVICE MESH DESIGN:
- Sidecar proxy configuration (Istio, Linkerd, Consul Connect)
- Service discovery and load balancing
- Circuit breaker and retry policies
- Traffic splitting and canary deployment support

CROSS-CUTTING CONCERNS:
- Distributed tracing implementation
- Centralized logging and metrics collection
- Error handling and fault tolerance
- Configuration management and feature flags

OPERATIONAL CAPABILITIES:
- Health checking and service monitoring
- Performance metrics and SLA tracking
- Debugging and troubleshooting tools
- Automated scaling and traffic management

TECHNOLOGY SELECTION:
- API gateway product recommendations (Kong, Ambassador, AWS API Gateway)
- Service mesh platform comparison and selection
- Integration with existing infrastructure
- Migration strategy from current setup

DEPLOYMENT AND OPERATIONS:
- High availability and disaster recovery
- Rolling updates and blue-green deployments
- Configuration as code and GitOps workflows
- Security scanning and vulnerability management

Include specific configuration examples and highlight best practices for production deployment.
```

### Database Architecture and Data Modeling
**Use Case**: Design database architecture with proper data modeling, indexing strategies, and scalability patterns for complex applications.

**Copy-Pastable Prompt**:
```
Help me design a comprehensive database architecture and data model for my application. I need guidance on schema design, performance optimization, and scalability strategies.

APPLICATION CONTEXT:
[Describe your application and its data requirements]

DATA CHARACTERISTICS:
- Data volume: [Current size and growth projections]
- Access patterns: [Read-heavy, write-heavy, mixed workloads]
- Consistency requirements: [ACID vs eventual consistency needs]
- Query complexity: [Simple lookups vs complex analytics]
- Geographic distribution: [Single region vs global data access]

BUSINESS ENTITIES:
[List main business entities and their relationships]

Please design:

DATA MODEL DESIGN:
- Entity-relationship design and normalization strategy
- Primary and foreign key relationships
- Data type selection and constraints
- Audit trail and versioning considerations

SCHEMA ARCHITECTURE:
- Database selection rationale (SQL vs NoSQL vs hybrid)
- Schema organization and naming conventions
- Cross-database relationships and data synchronization
- Schema migration and evolution strategy

PERFORMANCE OPTIMIZATION:
- Indexing strategy and index selection
- Query optimization and execution plan analysis
- Partitioning and sharding strategies
- Caching layers and cache invalidation patterns

SCALABILITY PATTERNS:
- Read replica configuration and usage
- Horizontal scaling and data distribution
- Connection pooling and resource management
- Load balancing across database instances

DATA CONSISTENCY:
- Transaction design and isolation levels
- Distributed transaction coordination
- Eventual consistency handling
- Conflict resolution strategies

BACKUP AND RECOVERY:
- Backup strategy and retention policies
- Point-in-time recovery capabilities
- Disaster recovery and business continuity
- Data archiving and lifecycle management

SECURITY AND COMPLIANCE:
- Data encryption at rest and in transit
- Access control and privilege management
- Data masking and anonymization strategies
- Audit logging and compliance reporting

OPERATIONAL CONCERNS:
- Database monitoring and alerting
- Performance tuning and maintenance
- Capacity planning and resource allocation
- Database DevOps and automation

Include specific schema examples, query patterns, and migration strategies for my use case.
```

---

## Integration Architecture

### Third-Party Integration Patterns
**Use Case**: Design robust integration patterns for connecting with external APIs, services, and legacy systems while maintaining system reliability.

**Copy-Pastable Prompt**:
```
Help me design integration architecture for connecting with third-party services and external systems. I need patterns for reliability, error handling, and data consistency.

INTEGRATION REQUIREMENTS:
[List the external systems you need to integrate with]

INTEGRATION TYPES:
- Real-time API calls: [Which services need immediate responses]
- Batch data exchange: [Bulk data import/export requirements]
- Event-based integration: [Webhook/event-driven interactions]
- File-based integration: [File transfer requirements]

RELIABILITY REQUIREMENTS:
- Uptime expectations: [Tolerance for third-party downtime]
- Data consistency needs: [Eventually consistent vs immediate consistency]
- Error recovery requirements: [Manual vs automatic recovery]
- Performance expectations: [Response time, throughput]

Please design:

INTEGRATION PATTERNS:
- API integration patterns (REST, GraphQL, SOAP)
- Message queue integration for asynchronous processing
- Webhook handling and event processing
- File-based integration and ETL processes

RELIABILITY AND RESILIENCE:
- Circuit breaker implementation for failing services
- Retry policies with exponential backoff
- Timeout configuration and dead letter queues
- Fallback mechanisms and graceful degradation

DATA SYNCHRONIZATION:
- Data mapping and transformation strategies
- Conflict resolution for data inconsistencies
- Idempotency handling for duplicate requests
- Data validation and sanitization

ERROR HANDLING:
- Comprehensive error classification and handling
- Error logging, monitoring, and alerting
- Manual intervention workflows for critical failures
- Error recovery and reprocessing mechanisms

SECURITY CONSIDERATIONS:
- API authentication and authorization (OAuth, API keys)
- Data encryption in transit and at rest
- Rate limiting and abuse prevention
- Audit logging for compliance

OPERATIONAL PATTERNS:
- Integration monitoring and health checks
- Performance metrics and SLA tracking
- Configuration management for multiple environments
- Testing strategies for external dependencies

ARCHITECTURE COMPONENTS:
- Integration layer design and abstraction
- Adapter pattern implementation for different APIs
- Anti-corruption layer for legacy system integration
- Event bus design for decoupled integration

VENDOR MANAGEMENT:
- API versioning and change management
- Vendor SLA monitoring and escalation
- Cost optimization and usage tracking
- Migration strategies for vendor changes

Provide specific implementation patterns and highlight common integration pitfalls to avoid.
```

### Message Queue and Event Streaming Architecture
**Use Case**: Design message queuing and event streaming systems for asynchronous processing, system decoupling, and reliable data flow.

**Copy-Pastable Prompt**:
```
Help me design a comprehensive message queue and event streaming architecture for my distributed system. I need guidance on technology selection, topology design, and operational patterns.

SYSTEM REQUIREMENTS:
[Describe your system's messaging and event processing needs]

MESSAGE CHARACTERISTICS:
- Message volume: [Messages per second/minute/hour]
- Message size: [Typical and maximum message sizes]
- Processing latency: [Real-time vs batch processing needs]
- Ordering requirements: [Strict ordering vs best-effort]
- Durability needs: [Message persistence requirements]

USE CASES:
- Asynchronous processing: [Background jobs, batch processing]
- Event notification: [System events, user notifications]
- Data streaming: [Real-time analytics, data pipelines]
- System integration: [Service decoupling, legacy integration]

Please design:

MESSAGING TOPOLOGY:
- Message broker selection (Kafka, RabbitMQ, AWS SQS/SNS, etc.)
- Topic/queue organization and naming strategy
- Partitioning and routing strategies
- Producer and consumer group configuration

EVENT PROCESSING PATTERNS:
- Event sourcing and stream processing design
- Complex event processing (CEP) patterns
- Message transformation and enrichment
- Event aggregation and windowing strategies

RELIABILITY AND DELIVERY:
- Message delivery guarantees (at-least-once, exactly-once)
- Dead letter queue handling and poison message management
- Message retry policies and exponential backoff
- Duplicate detection and idempotency handling

SCALABILITY DESIGN:
- Horizontal scaling of producers and consumers
- Load balancing and partition assignment strategies
- Auto-scaling based on queue depth and processing time
- Cross-region replication and disaster recovery

CONSUMER PATTERNS:
- Consumer group design and load distribution
- Message processing order and parallelization
- Error handling and failure recovery
- Consumer offset management and checkpointing

MONITORING AND OPERATIONS:
- Message flow monitoring and alerting
- Performance metrics (latency, throughput, error rates)
- Queue depth monitoring and capacity planning
- Message tracing and debugging tools

SECURITY AND GOVERNANCE:
- Message encryption and access control
- Schema registry and message validation
- Audit logging and compliance tracking
- Rate limiting and quota management

INTEGRATION PATTERNS:
- Message bus vs event bus design decisions
- Request-response patterns over messaging
- Publish-subscribe patterns and fan-out strategies
- Choreography vs orchestration for workflow management

Include specific configuration examples, operational procedures, and performance tuning recommendations.
```

### Security Architecture and Authentication Design
**Use Case**: Design comprehensive security architecture including authentication, authorization, data protection, and compliance requirements.

**Copy-Pastable Prompt**:
```
Help me design a comprehensive security architecture for my application. I need guidance on authentication, authorization, data protection, and security best practices.

APPLICATION CONTEXT:
[Describe your application type, user base, and data sensitivity]

SECURITY REQUIREMENTS:
- User types: [Internal users, external customers, admin users]
- Data classification: [Public, internal, confidential, restricted]
- Compliance needs: [GDPR, HIPAA, SOC2, PCI-DSS, etc.]
- Threat model: [Key security concerns and attack vectors]

TECHNICAL ENVIRONMENT:
- Architecture: [Monolith, microservices, cloud-native]
- Platforms: [Web, mobile, APIs, third-party integrations]
- Infrastructure: [Cloud providers, on-premise, hybrid]

Please design:

AUTHENTICATION ARCHITECTURE:
- Identity provider selection and integration (OAuth2, SAML, OpenID Connect)
- Multi-factor authentication (MFA) implementation
- Session management and token lifecycle
- Single sign-on (SSO) and federated identity patterns

AUTHORIZATION DESIGN:
- Role-based access control (RBAC) vs attribute-based access control (ABAC)
- Permission model and policy engine design
- API authorization and resource protection
- Fine-grained access control for data and features

DATA PROTECTION:
- Encryption at rest and in transit strategies
- Key management and rotation policies
- Data masking and tokenization for sensitive data
- Secure data storage and backup procedures

APPLICATION SECURITY:
- Secure coding practices and input validation
- API security (rate limiting, input sanitization, CORS)
- Cross-site scripting (XSS) and injection attack prevention
- Dependency scanning and vulnerability management

INFRASTRUCTURE SECURITY:
- Network security and segmentation
- Container and orchestration security
- Cloud security configuration and monitoring
- Secrets management and configuration security

SECURITY MONITORING:
- Security event logging and SIEM integration
- Intrusion detection and response procedures
- Vulnerability scanning and penetration testing
- Security metrics and compliance reporting

INCIDENT RESPONSE:
- Security incident response plan and procedures
- Breach notification and communication protocols
- Forensic capabilities and evidence preservation
- Recovery procedures and business continuity

COMPLIANCE FRAMEWORK:
- Regulatory requirement mapping and controls
- Privacy by design and data minimization
- Audit trail and compliance reporting
- Third-party security assessment requirements

Provide specific implementation guidance, security controls, and highlight common security vulnerabilities to address.
```

---

*These architecture prompts help design robust, scalable, and maintainable systems. Adapt them based on your specific technology stack and architectural constraints.*
