# Step 1: Project Design Prompts

Initial project planning and design decision prompts to help define requirements, choose technologies, and establish project foundations before development begins.

## Table of Contents
- [Requirements Analysis](#requirements-analysis)
- [Technology Selection](#technology-selection)
- [Project Planning](#project-planning)

---

## Requirements Analysis

### Comprehensive Requirements Gathering
**Use Case**: Extract and organize comprehensive requirements from high-level project descriptions or stakeholder input.

**Copy-Pastable Prompt**:
```
Help me analyze and structure requirements for a new software project. Please break down the following project description into detailed requirements:

PROJECT DESCRIPTION:
[Paste your project description here]

Please organize the analysis into:

FUNCTIONAL REQUIREMENTS:
- Core features and capabilities
- User workflows and interactions
- Data processing and business logic
- Integration requirements

NON-FUNCTIONAL REQUIREMENTS:
- Performance expectations (response time, throughput)
- Scalability needs (concurrent users, data volume)
- Security requirements (authentication, authorization, compliance)
- Availability and reliability expectations
- Usability and accessibility standards

TECHNICAL CONSTRAINTS:
- Technology preferences or restrictions
- Platform requirements (web, mobile, desktop)
- Integration with existing systems
- Budget and timeline constraints

ASSUMPTIONS & RISKS:
- Technical assumptions being made
- Potential risks and mitigation strategies
- Dependencies on external systems or teams

Please also suggest any missing requirements that should be considered and ask clarifying questions for ambiguous areas.
```

### User Story Generation and Refinement
**Use Case**: Convert requirements into well-structured user stories with acceptance criteria for agile development.

**Copy-Pastable Prompt**:
```
Help me create detailed user stories from the following requirements or feature descriptions:

FEATURE/REQUIREMENT:
[Describe the feature or requirement]

Please generate user stories in this format:

**As a** [user type]
**I want** [functionality]
**So that** [benefit/value]

**Acceptance Criteria:**
- Given [context]
- When [action]
- Then [expected outcome]

For each user story, also provide:

STORY DETAILS:
- Priority level (High/Medium/Low)
- Estimated complexity (Small/Medium/Large)
- Dependencies on other stories
- Technical considerations

EDGE CASES:
- Error scenarios to handle
- Boundary conditions
- Integration points

DEFINITION OF DONE:
- Code implementation complete
- Unit tests written and passing
- Integration tests covered
- Documentation updated
- Code review completed

Please create 3-5 user stories that thoroughly cover the requirement and ask if any scenarios are missing.
```

### MVP (Minimum Viable Product) Definition
**Use Case**: Define the core features for an MVP version of your product, distinguishing between must-have and nice-to-have features.

**Copy-Pastable Prompt**:
```
Help me define an MVP (Minimum Viable Product) for my project. I need to identify the absolute core features that deliver value while keeping scope manageable.

PROJECT CONCEPT:
[Describe your full project vision]

TARGET USERS:
[Describe your primary user base]

KEY VALUE PROPOSITION:
[What core problem does this solve?]

Please help me create:

MVP CORE FEATURES (Must-Have):
- List the 3-5 features absolutely essential for user value
- Justify why each feature is critical for MVP
- Estimate relative complexity of each feature

PHASE 2 FEATURES (Should-Have):
- Features important but not critical for initial launch
- Can be added after MVP validation

FUTURE FEATURES (Could-Have):
- Nice-to-have features for later versions
- Advanced functionality that enhances but doesn't define core value

MVP SUCCESS CRITERIA:
- How will you measure if the MVP is successful?
- What user behaviors indicate product-market fit?
- Technical metrics to track

DEVELOPMENT TIMELINE:
- Suggested order of feature implementation
- Potential risks and dependencies
- Milestone checkpoints

Please challenge any feature I might be including that isn't truly essential for the MVP.
```

---

## Technology Selection

### Technology Stack Recommendation
**Use Case**: Get recommendations for optimal technology stack based on project requirements, team skills, and constraints.

**Copy-Pastable Prompt**:
```
Help me select the optimal technology stack for my project based on requirements and constraints:

PROJECT DETAILS:
- Type: [Web app/Mobile app/Desktop/API/etc.]
- Expected scale: [Users, data volume, geographic distribution]
- Performance requirements: [Response time, throughput needs]
- Team size and timeline: [Development team details]

REQUIREMENTS:
- Core functionality: [Key features needed]
- Integration needs: [External services, APIs, databases]
- Security requirements: [Compliance, data sensitivity]
- Platform targets: [Web browsers, mobile platforms, etc.]

CONSTRAINTS:
- Team expertise: [Current skills in team]
- Budget considerations: [Hosting, licensing costs]
- Deployment environment: [Cloud providers, on-premise]
- Legacy system integration: [Existing systems to connect with]

Please recommend:

FRONTEND STACK:
- Framework/library choice with reasoning
- UI component libraries
- State management approach
- Build tools and bundlers

BACKEND STACK:
- Programming language and framework
- Database selection (primary and caching)
- API architecture (REST/GraphQL/etc.)
- Authentication and authorization approach

INFRASTRUCTURE:
- Hosting and deployment strategy
- CI/CD pipeline recommendations
- Monitoring and logging tools
- Scaling considerations

ALTERNATIVE OPTIONS:
- Provide 2-3 different stack options with trade-offs
- Explain scenarios where each option excels
- Consider learning curve and maintenance overhead

Include pros/cons for each recommendation and explain the reasoning behind choices.
```

### Database Design and Selection
**Use Case**: Choose appropriate database solutions and design the data architecture for your project requirements.

**Copy-Pastable Prompt**:
```
Help me design the database architecture for my project. I need guidance on database selection and schema design.

PROJECT DATA REQUIREMENTS:
[Describe your data: types, relationships, volume, access patterns]

SPECIFIC NEEDS:
- Data volume: [Current and projected]
- Read/write patterns: [More reads vs writes, query types]
- Consistency requirements: [ACID vs eventual consistency]
- Performance needs: [Response time, concurrent users]
- Geographic distribution: [Single region vs global]

CONSTRAINTS:
- Budget limitations: [Cloud costs, licensing]
- Team expertise: [Database experience level]
- Integration requirements: [Existing systems, APIs]
- Compliance needs: [GDPR, HIPAA, etc.]

Please provide:

DATABASE SELECTION:
- Primary database recommendation with reasoning
- Alternative options and when to consider them
- Caching strategy (Redis, Memcached, CDN)
- Search solutions if needed (Elasticsearch, etc.)

SCHEMA DESIGN:
- Entity relationships and data model
- Indexing strategy for performance
- Data partitioning/sharding considerations
- Backup and disaster recovery approach

SCALING STRATEGY:
- Read replica configuration
- Horizontal vs vertical scaling approach
- Data archiving and lifecycle management
- Performance monitoring recommendations

MIGRATION PLAN:
- Development to production data migration
- Schema versioning and evolution strategy
- Data seeding and testing approaches

Please also identify potential bottlenecks and suggest optimization strategies.
```

### API Design and Architecture
**Use Case**: Design RESTful APIs, GraphQL schemas, or other API architectures that meet your project's integration and scalability needs.

**Copy-Pastable Prompt**:
```
Help me design a robust API architecture for my project. I need guidance on API structure, endpoints, and best practices.

PROJECT CONTEXT:
- Application type: [Web/Mobile/B2B integration/etc.]
- Expected API consumers: [Frontend apps, mobile apps, third parties]
- Data complexity: [Simple CRUD vs complex business logic]
- Scale requirements: [Requests per second, concurrent users]

FUNCTIONAL REQUIREMENTS:
[List the main data operations and business logic the API needs to support]

TECHNICAL REQUIREMENTS:
- Authentication needs: [Public, user auth, API keys, OAuth]
- Response time requirements: [Real-time vs standard]
- Data format preferences: [JSON, XML, binary]
- Versioning strategy needs: [Breaking changes, backwards compatibility]

Please provide:

API ARCHITECTURE:
- REST vs GraphQL vs gRPC recommendation with reasoning
- Overall API structure and organization
- Naming conventions and URL patterns
- HTTP methods and status code usage

ENDPOINT DESIGN:
- Core endpoints with request/response examples
- Resource relationships and nested endpoints
- Pagination and filtering strategies
- Bulk operations design

SECURITY & PERFORMANCE:
- Authentication and authorization approach
- Rate limiting and throttling strategy
- Caching headers and strategies
- Input validation and sanitization

DOCUMENTATION & TESTING:
- API documentation approach (OpenAPI/Swagger)
- Testing strategy (unit, integration, contract testing)
- Error handling and response formats
- Monitoring and logging recommendations

API EVOLUTION:
- Versioning strategy and implementation
- Deprecation timeline and communication
- Backwards compatibility considerations

Please include specific examples and identify potential design pitfalls to avoid.
```

---

## Project Planning

### Development Timeline and Milestones
**Use Case**: Create realistic development timelines with clear milestones and deliverables for project planning and stakeholder communication.

**Copy-Pastable Prompt**:
```
Help me create a realistic development timeline and milestone plan for my software project.

PROJECT SCOPE:
[Describe the full project scope and key features]

TEAM COMPOSITION:
- Team size: [Number of developers]
- Experience level: [Junior/Mid/Senior distribution]
- Roles: [Frontend/Backend/Full-stack/DevOps/etc.]
- Availability: [Full-time/part-time, hours per week]

CONSTRAINTS:
- Total timeline: [Desired or hard deadline]
- Budget limitations: [If applicable]
- External dependencies: [Third-party integrations, approvals]
- Technical constraints: [Legacy systems, compliance requirements]

Please create:

PROJECT PHASES:
- Phase breakdown with clear objectives
- Dependencies between phases
- Deliverables for each phase
- Success criteria and acceptance requirements

DETAILED TIMELINE:
- Week-by-week breakdown for first 2-3 months
- Monthly milestones for remainder of project
- Buffer time for unexpected issues (suggest 20-30%)
- Key decision points and review gates

RISK MANAGEMENT:
- Identify high-risk areas and timeline impacts
- Contingency plans for common delays
- Early warning indicators for timeline slippage
- Mitigation strategies for identified risks

RESOURCE ALLOCATION:
- Task assignment strategy
- Skill development time if needed
- Code review and testing time allocation
- Documentation and deployment time

STAKEHOLDER COMMUNICATION:
- Demo schedule and milestone reviews
- Progress reporting frequency and format
- Key decision points requiring stakeholder input
- Launch preparation and go-live planning

Please also suggest ways to validate timeline assumptions and adjust the plan as the project progresses.
```

### Team Structure and Collaboration Setup
**Use Case**: Organize team roles, responsibilities, and collaboration workflows for effective development team coordination.

**Copy-Pastable Prompt**:
```
Help me design an effective team structure and collaboration workflow for my development project.

PROJECT DETAILS:
- Project size and complexity: [Scope description]
- Timeline: [Duration and key deadlines]
- Technology stack: [Languages, frameworks, tools]

TEAM COMPOSITION:
- Total team size: [Number of people]
- Skill levels: [Distribution of experience]
- Roles needed: [Frontend, backend, DevOps, QA, etc.]
- Remote vs in-person: [Work arrangement]

CURRENT CHALLENGES:
[Any known team coordination issues or constraints]

Please recommend:

TEAM STRUCTURE:
- Optimal role definitions and responsibilities
- Team lead/technical lead assignment
- Code ownership and area responsibilities
- Cross-training and knowledge sharing plan

COLLABORATION WORKFLOW:
- Daily/weekly meeting structure
- Code review process and requirements
- Branch strategy and merge workflow
- Testing and deployment responsibilities

COMMUNICATION TOOLS:
- Primary communication channels
- Documentation and knowledge management
- Progress tracking and project management tools
- Code collaboration and version control setup

DEVELOPMENT PROCESS:
- Sprint/iteration length and structure
- Definition of done and quality gates
- Bug triage and resolution process
- Feature planning and prioritization workflow

ONBOARDING PROCESS:
- New team member integration plan
- Documentation and setup requirements
- Mentoring and pair programming approach
- Skills assessment and development planning

QUALITY ASSURANCE:
- Code review standards and checklist
- Testing strategy and responsibilities
- Performance and security review process
- Technical debt management approach

Please also suggest metrics to track team effectiveness and collaboration quality.
```

### Risk Assessment and Mitigation Planning
**Use Case**: Identify potential project risks early and develop comprehensive mitigation strategies to avoid common development pitfalls.

**Copy-Pastable Prompt**:
```
Help me conduct a comprehensive risk assessment for my software development project and create mitigation strategies.

PROJECT OVERVIEW:
[Describe project scope, timeline, and key requirements]

TEAM & RESOURCES:
- Team size and experience: [Team details]
- Budget and timeline constraints: [Resource limitations]
- Key dependencies: [External teams, vendors, approvals]

TECHNICAL COMPLEXITY:
- New technologies being used: [Learning curve risks]
- Integration requirements: [External systems, APIs]
- Performance and scalability needs: [Technical challenges]

Please identify and analyze:

TECHNICAL RISKS:
- Technology choice and adoption risks
- Integration and dependency risks
- Performance and scalability challenges
- Security and compliance vulnerabilities
- Data migration and compatibility issues

PROJECT MANAGEMENT RISKS:
- Timeline and scope creep risks
- Resource availability and skill gaps
- Communication and coordination challenges
- Quality assurance and testing gaps
- Deployment and go-live risks

BUSINESS RISKS:
- Changing requirements and priorities
- Market and competitive pressures
- User adoption and feedback risks
- Budget and funding uncertainties
- Regulatory and compliance changes

For each identified risk, provide:

RISK ASSESSMENT:
- Probability (High/Medium/Low)
- Impact severity (High/Medium/Low)
- Risk priority (Critical/Important/Monitor)
- Early warning indicators

MITIGATION STRATEGIES:
- Preventive measures to reduce probability
- Contingency plans if risk materializes
- Resource requirements for mitigation
- Timeline impact of mitigation actions

MONITORING PLAN:
- Key metrics to track risk indicators
- Review frequency and responsibility
- Escalation triggers and procedures
- Communication plan for risk updates

Please prioritize risks and suggest a risk review schedule for the project duration.
```

---

*These project design prompts help establish a solid foundation before development begins. Customize them based on your specific project type and organizational needs.*
