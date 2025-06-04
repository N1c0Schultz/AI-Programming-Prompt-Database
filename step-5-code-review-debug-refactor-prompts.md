# Step 5: Code Review, Debug & Refactor Prompts

Quality assurance and optimization prompts for reviewing code, debugging issues, and refactoring for improved maintainability. These prompts help ensure code quality and system reliability.

## Table of Contents
- [Code Review and Quality](#code-review-and-quality)
- [Debugging and Troubleshooting](#debugging-and-troubleshooting)
- [Refactoring and Optimization](#refactoring-and-optimization)

---

## Code Review and Quality

### Comprehensive Code Review Checklist
**Use Case**: Conduct thorough code reviews that ensure quality, security, maintainability, and adherence to coding standards.

**Copy-Pastable Prompt**:
```
Please conduct a comprehensive code review of the following code. Focus on quality, security, performance, and maintainability aspects using industry best practices.

CODE TO REVIEW:
[Paste the code you want reviewed here]

PROJECT CONTEXT:
- Programming language: [Language and version]
- Framework/libraries: [Relevant frameworks being used]
- Application type: [Web app, API, library, etc.]
- Performance requirements: [Any specific performance constraints]
- Security requirements: [Data sensitivity, compliance needs]

Please review for:

CODE QUALITY:
- Readability and clarity of code structure
- Naming conventions and consistency
- Function/method length and complexity
- Code organization and modularity
- Comments and documentation quality

LOGIC AND FUNCTIONALITY:
- Correctness of business logic implementation
- Edge case handling and boundary conditions
- Error handling and exception management
- Input validation and sanitization
- Return value handling and type safety

PERFORMANCE CONSIDERATIONS:
- Algorithm efficiency and optimization opportunities
- Memory usage and potential leaks
- Database query optimization (if applicable)
- Caching opportunities and strategies
- Resource management and cleanup

SECURITY REVIEW:
- Input validation and SQL injection prevention
- Authentication and authorization checks
- Sensitive data handling and exposure
- Cross-site scripting (XSS) prevention
- Secure coding practices compliance

MAINTAINABILITY:
- SOLID principles adherence
- Design pattern usage and appropriateness
- Code duplication and DRY principle
- Dependency management and coupling
- Testability and mock-ability

TESTING COVERAGE:
- Unit test completeness and quality
- Test case coverage for edge cases
- Integration test requirements
- Mocking strategy appropriateness
- Test readability and maintainability

STANDARDS COMPLIANCE:
- Coding standard adherence
- Framework best practices following
- Documentation requirements fulfillment
- Accessibility compliance (if applicable)
- Browser compatibility (if web-based)

SUGGESTIONS FOR IMPROVEMENT:
- Specific refactoring recommendations
- Performance optimization opportunities
- Security enhancement suggestions
- Code structure improvements
- Additional test case recommendations

Please provide specific examples and explanations for each issue identified, along with suggested fixes and improvements.
```

### Security-Focused Code Analysis
**Use Case**: Perform in-depth security analysis of code to identify vulnerabilities, security anti-patterns, and compliance issues.

**Copy-Pastable Prompt**:
```
Conduct a comprehensive security analysis of the following code. Identify potential vulnerabilities, security anti-patterns, and compliance issues with specific remediation recommendations.

CODE FOR SECURITY ANALYSIS:
[Paste the code for security review here]

SECURITY CONTEXT:
- Application type: [Web app, API, mobile backend, etc.]
- Data handled: [Personal data, financial, healthcare, etc.]
- Threat model: [Known threats or attack vectors of concern]
- Compliance requirements: [GDPR, HIPAA, PCI-DSS, SOC2, etc.]
- Deployment environment: [Cloud, on-premise, hybrid]

Please analyze for:

INPUT VALIDATION SECURITY:
- SQL injection vulnerability assessment
- Cross-site scripting (XSS) prevention
- Command injection and code execution risks
- Path traversal and file inclusion vulnerabilities
- Input sanitization and validation completeness

AUTHENTICATION AND AUTHORIZATION:
- Authentication mechanism security
- Session management and token handling
- Password storage and hashing practices
- Access control implementation
- Privilege escalation prevention

DATA PROTECTION:
- Sensitive data exposure risks
- Encryption implementation (at rest and in transit)
- Data masking and tokenization usage
- Logging of sensitive information
- Data retention and deletion practices

CRYPTOGRAPHIC SECURITY:
- Cryptographic algorithm selection and implementation
- Key management and storage practices
- Random number generation security
- Certificate validation and pinning
- Hashing and digital signature usage

API AND COMMUNICATION SECURITY:
- API endpoint security and rate limiting
- HTTPS/TLS configuration and enforcement
- Cross-Origin Resource Sharing (CORS) configuration
- Request/response header security
- Third-party API integration security

ERROR HANDLING AND LOGGING:
- Information disclosure through error messages
- Logging security and log injection prevention
- Audit trail completeness and integrity
- Sensitive data in logs and error outputs
- Debug information exposure risks

BUSINESS LOGIC SECURITY:
- Business rule bypass vulnerabilities
- Race condition and timing attack risks
- Transaction integrity and atomicity
- State management security
- Workflow manipulation prevention

DEPENDENCY AND SUPPLY CHAIN:
- Third-party library vulnerability assessment
- Dependency version security analysis
- Supply chain attack prevention
- License compliance and security implications
- Outdated dependency identification

INFRASTRUCTURE SECURITY:
- Configuration security and hardening
- Secret management and exposure
- Container and deployment security
- Cloud service configuration security
- Network security considerations

COMPLIANCE ANALYSIS:
- Regulatory requirement adherence
- Privacy law compliance (GDPR, CCPA)
- Industry standard compliance (PCI-DSS, HIPAA)
- Security control implementation
- Audit readiness and documentation

REMEDIATION RECOMMENDATIONS:
- Specific vulnerability fixes with code examples
- Security control implementation guidance
- Best practice recommendations
- Security testing suggestions
- Monitoring and detection improvements

Please prioritize findings by severity and provide specific code examples for recommended fixes.
```

### Performance and Scalability Review
**Use Case**: Analyze code for performance bottlenecks, scalability issues, and optimization opportunities with specific improvement recommendations.

**Copy-Pastable Prompt**:
```
Analyze the following code for performance bottlenecks, scalability issues, and optimization opportunities. Provide specific recommendations for improvement with measurable impact assessment.

CODE FOR PERFORMANCE ANALYSIS:
[Paste the code for performance review here]

PERFORMANCE CONTEXT:
- Expected load: [Requests per second, concurrent users, data volume]
- Performance requirements: [Response time targets, throughput needs]
- Infrastructure constraints: [Memory, CPU, network limitations]
- Current performance baseline: [Current metrics if available]
- Scalability needs: [Growth projections and scaling requirements]

Please analyze for:

ALGORITHMIC EFFICIENCY:
- Time complexity analysis and optimization opportunities
- Space complexity and memory usage efficiency
- Algorithm selection and data structure optimization
- Loop optimization and iteration efficiency
- Recursive algorithm optimization and stack usage

DATABASE PERFORMANCE:
- Query efficiency and optimization opportunities
- Index usage and performance impact
- N+1 query problem identification
- Database connection and transaction management
- Caching opportunities and strategies

MEMORY MANAGEMENT:
- Memory allocation patterns and optimization
- Garbage collection impact and tuning
- Memory leak identification and prevention
- Object lifecycle and resource cleanup
- Buffer management and memory pooling

CONCURRENCY AND PARALLELISM:
- Thread safety and synchronization efficiency
- Deadlock and race condition identification
- Parallel processing opportunities
- Asynchronous operation optimization
- Resource contention and bottleneck analysis

I/O AND NETWORK OPTIMIZATION:
- File I/O efficiency and buffering strategies
- Network call optimization and batching
- Compression and data transfer optimization
- Connection pooling and resource reuse
- Streaming and lazy loading opportunities

CACHING ANALYSIS:
- Caching strategy effectiveness and opportunities
- Cache invalidation and consistency management
- Memory vs distributed caching trade-offs
- Cache hit ratio optimization
- Cache warming and preloading strategies

SCALABILITY ASSESSMENT:
- Horizontal scaling compatibility
- Vertical scaling limitations and bottlenecks
- Load distribution and balancing considerations
- State management for scalability
- Resource utilization and capacity planning

FRAMEWORK AND LIBRARY USAGE:
- Framework performance best practices adherence
- Library usage efficiency and alternatives
- Configuration optimization opportunities
- Third-party service integration efficiency
- Middleware and plugin performance impact

PROFILING AND MONITORING:
- Performance monitoring integration points
- Metrics collection and analysis recommendations
- Profiling strategy and tool suggestions
- Bottleneck identification methodologies
- Performance regression detection approaches

OPTIMIZATION RECOMMENDATIONS:
- High-impact, low-effort optimizations
- Major refactoring opportunities with ROI analysis
- Technology upgrade or replacement suggestions
- Architecture pattern improvements
- Performance testing and validation strategies

MEASUREMENT AND VALIDATION:
- Performance metrics to track improvement
- Benchmarking and testing methodologies
- A/B testing strategies for optimizations
- Monitoring and alerting setup
- Performance goal setting and validation

Please prioritize recommendations by impact and implementation effort, and provide specific code examples for optimization techniques.
```

---

## Debugging and Troubleshooting

### Systematic Debugging Approach
**Use Case**: Apply systematic debugging methodologies to identify and resolve complex issues in production and development environments.

**Copy-Pastable Prompt**:
```
Help me systematically debug and resolve the following issue using proven debugging methodologies. Provide a structured approach to identify root causes and implement fixes.

PROBLEM DESCRIPTION:
[Describe the issue you're experiencing in detail]

SYSTEM CONTEXT:
- Application: [Type and technology stack]
- Environment: [Development, staging, production]
- Recent changes: [Code deployments, configuration changes, infrastructure updates]
- Error symptoms: [Error messages, unexpected behavior, performance issues]
- Reproduction steps: [How to reproduce the issue, if known]

IMPACT ASSESSMENT:
- User impact: [Number of users affected, severity of impact]
- Business impact: [Revenue loss, SLA violations, reputation damage]
- System impact: [Performance degradation, service availability]
- Urgency level: [Critical, high, medium, low priority]

Please provide:

DEBUGGING STRATEGY:
- Systematic approach to problem isolation
- Hypothesis formation and testing methodology
- Data collection and analysis plan
- Root cause analysis framework
- Fix validation and testing approach

INFORMATION GATHERING:
- Log analysis strategy and key log sources
- Metrics and monitoring data to examine
- System state and configuration verification
- External dependency status checking
- User environment and reproduction context

PROBLEM ISOLATION:
- Component isolation and testing methodology
- Network vs application vs database issue determination
- Environment-specific vs universal issue identification
- Timing and sequence analysis for intermittent issues
- Load and concurrency impact assessment

DEBUGGING TECHNIQUES:
- Logging enhancement and instrumentation
- Debugging tool selection and configuration
- Breakpoint and inspection strategies
- Profiling and performance analysis
- Memory and resource leak detection

ROOT CAUSE ANALYSIS:
- 5 Whys methodology application
- Fishbone diagram for complex issues
- Timeline analysis for sequence-dependent problems
- Change impact analysis and correlation
- System interaction mapping and analysis

HYPOTHESIS TESTING:
- Testable hypothesis formulation
- Controlled testing environment setup
- A/B testing for behavior verification
- Rollback testing and validation
- Performance impact measurement

FIX IMPLEMENTATION:
- Fix design and impact assessment
- Implementation approach and staging
- Testing strategy for fix validation
- Rollback plan and risk mitigation
- Monitoring and validation criteria

VERIFICATION AND VALIDATION:
- Fix effectiveness measurement
- Regression testing and side effect checking
- Performance impact validation
- User acceptance and feedback collection
- Long-term monitoring and stability assessment

PREVENTION MEASURES:
- Similar issue prevention strategies
- Monitoring and alerting improvements
- Code quality and review enhancements
- Testing coverage and automation improvements
- Documentation and knowledge sharing

INCIDENT DOCUMENTATION:
- Issue timeline and impact documentation
- Root cause analysis report
- Fix implementation and validation log
- Lessons learned and improvement recommendations
- Knowledge base update and team communication

Provide specific debugging commands, tools, and techniques relevant to my technology stack and environment.
```

### Log Analysis and Error Investigation
**Use Case**: Analyze application logs and error patterns to identify issues, understand system behavior, and implement monitoring improvements.

**Copy-Pastable Prompt**:
```
Help me analyze application logs and investigate error patterns to identify issues and improve system monitoring. Provide systematic approaches for log analysis and error investigation.

LOG CONTEXT:
[Paste relevant log entries or describe the log sources and error patterns]

SYSTEM INFORMATION:
- Application type: [Web app, API, microservices, etc.]
- Logging framework: [Log4j, Winston, Python logging, etc.]
- Log aggregation system: [ELK Stack, Splunk, CloudWatch, etc.]
- Log volume: [Approximate volume and retention period]
- Error frequency: [How often errors occur]

INVESTIGATION GOALS:
- Error pattern identification and classification
- Root cause analysis for recurring issues
- System performance and behavior analysis
- Monitoring and alerting improvement recommendations

Please provide:

LOG ANALYSIS STRATEGY:
- Systematic log examination methodology
- Error pattern recognition and classification
- Timeline reconstruction and sequence analysis
- Correlation analysis across multiple log sources
- Statistical analysis for trend identification

ERROR CATEGORIZATION:
- Error severity classification and impact assessment
- Error type grouping and pattern identification
- Frequency analysis and trending
- Error source identification (component, service, layer)
- User impact correlation and assessment

LOG PARSING AND FILTERING:
- Effective log search queries and filters
- Regular expression patterns for error extraction
- Log aggregation and grouping strategies
- Noise reduction and signal amplification
- Structured logging analysis techniques

CORRELATION ANALYSIS:
- Cross-service log correlation and tracing
- Time-based correlation and sequence analysis
- User session and request ID tracking
- Infrastructure event correlation
- External service impact analysis

PERFORMANCE ANALYSIS:
- Response time analysis from logs
- Resource utilization pattern identification
- Bottleneck detection through log analysis
- Throughput and concurrency analysis
- Error rate correlation with load patterns

SECURITY ANALYSIS:
- Security event identification in logs
- Attack pattern recognition and analysis
- Authentication and authorization failure analysis
- Suspicious activity detection and investigation
- Compliance and audit trail analysis

ROOT CAUSE INVESTIGATION:
- Error propagation tracing and analysis
- Configuration change impact assessment
- Code deployment correlation analysis
- Infrastructure change impact evaluation
- Third-party service dependency analysis

VISUALIZATION AND REPORTING:
- Log visualization and dashboard creation
- Error trend reporting and analysis
- Key metric identification and tracking
- Executive summary and impact reporting
- Historical analysis and comparison

MONITORING IMPROVEMENTS:
- Enhanced logging strategy recommendations
- Alert threshold optimization and tuning
- Proactive monitoring rule creation
- Log retention and archival strategy
- Real-time monitoring and notification setup

AUTOMATION OPPORTUNITIES:
- Automated log analysis and pattern detection
- Error notification and escalation automation
- Log parsing and enrichment automation
- Report generation and distribution automation
- Incident response automation triggers

PREVENTIVE MEASURES:
- Enhanced logging and instrumentation recommendations
- Error handling improvement suggestions
- Monitoring gap identification and resolution
- Testing strategy improvements based on log analysis
- Documentation and runbook creation

TOOLS AND TECHNIQUES:
- Log analysis tool recommendations and configuration
- Query optimization and performance improvement
- Custom log parsing and analysis scripts
- Integration with incident response tools
- Backup and disaster recovery for log data

Please provide specific log analysis queries, tools, and monitoring configurations relevant to my logging infrastructure.
```

### Performance Troubleshooting and Optimization
**Use Case**: Diagnose performance issues, identify bottlenecks, and implement targeted optimizations to improve system performance.

**Copy-Pastable Prompt**:
```
Help me diagnose and resolve performance issues in my application. Provide systematic approaches for performance troubleshooting and targeted optimization strategies.

PERFORMANCE ISSUE DESCRIPTION:
[Describe the performance problem you're experiencing]

SYSTEM CONTEXT:
- Application architecture: [Monolith, microservices, serverless, etc.]
- Technology stack: [Languages, frameworks, databases, infrastructure]
- Current performance metrics: [Response times, throughput, error rates]
- Performance requirements: [Target response times, capacity needs]
- Environment: [Development, staging, production]

SYMPTOMS AND OBSERVATIONS:
- Performance degradation patterns: [When does it occur, under what conditions]
- Affected components: [Frontend, backend, database, network]
- User impact: [Slow response, timeouts, errors]
- Resource utilization: [CPU, memory, disk, network usage]

Please provide:

PERFORMANCE DIAGNOSIS STRATEGY:
- Systematic performance analysis methodology
- Bottleneck identification and prioritization
- Performance baseline establishment
- Metric collection and analysis plan
- Root cause isolation techniques

PROFILING AND MONITORING:
- Application profiling tools and techniques
- Database performance monitoring and analysis
- Infrastructure monitoring and resource tracking
- Network latency and throughput analysis
- Real-time performance monitoring setup

BOTTLENECK IDENTIFICATION:
- CPU bottleneck identification and analysis
- Memory usage patterns and leak detection
- Database query performance analysis
- Network bandwidth and latency issues
- I/O bottleneck identification and resolution

APPLICATION LAYER ANALYSIS:
- Code-level performance profiling
- Algorithm efficiency analysis and optimization
- Framework configuration and tuning
- Caching effectiveness and optimization
- Asynchronous processing opportunities

DATABASE PERFORMANCE:
- Query execution plan analysis
- Index optimization and missing index identification
- Database configuration tuning
- Connection pooling optimization
- Database scaling and replication strategies

INFRASTRUCTURE OPTIMIZATION:
- Server resource allocation and scaling
- Load balancing configuration and optimization
- Content delivery network (CDN) optimization
- Caching layer implementation and tuning
- Container and orchestration optimization

CONCURRENCY AND SCALING:
- Thread pool configuration and optimization
- Concurrency bottleneck identification
- Race condition and synchronization issues
- Horizontal vs vertical scaling analysis
- Load distribution and balancing optimization

MEMORY AND RESOURCE MANAGEMENT:
- Memory allocation pattern analysis
- Garbage collection tuning and optimization
- Resource leak identification and prevention
- Connection and resource pooling optimization
- Buffer management and sizing

NETWORK AND I/O OPTIMIZATION:
- Network call optimization and batching
- File I/O efficiency improvement
- Compression and data transfer optimization
- Protocol optimization and upgrade opportunities
- External service integration optimization

CACHING STRATEGIES:
- Multi-level caching implementation
- Cache hit ratio optimization
- Cache invalidation strategy improvement
- Distributed caching configuration
- Cache warming and preloading strategies

PERFORMANCE TESTING:
- Load testing strategy and implementation
- Stress testing and capacity planning
- Performance regression testing
- Baseline establishment and comparison
- Continuous performance monitoring

OPTIMIZATION IMPLEMENTATION:
- Incremental optimization approach
- Performance improvement measurement
- A/B testing for optimization validation
- Rollback planning for optimization changes
- Production deployment strategies

MONITORING AND ALERTING:
- Performance metric dashboard creation
- Proactive alerting and threshold setting
- Performance trend analysis and reporting
- Capacity planning and growth prediction
- Incident response for performance issues

LONG-TERM STRATEGY:
- Performance architecture improvements
- Technology upgrade recommendations
- Scalability planning and implementation
- Performance culture and best practices
- Continuous optimization processes

Provide specific tools, commands, and configuration examples relevant to my technology stack and infrastructure.
```

---

## Refactoring and Optimization

### Code Refactoring Strategy and Implementation
**Use Case**: Plan and execute comprehensive code refactoring to improve maintainability, readability, and performance while minimizing risk.

**Copy-Pastable Prompt**:
```
Help me plan and execute a comprehensive refactoring strategy for the following code. Focus on improving maintainability, readability, and performance while minimizing risk and ensuring backward compatibility.

CODE TO REFACTOR:
[Paste the code that needs refactoring here]

REFACTORING CONTEXT:
- Current code problems: [Technical debt, maintainability issues, performance problems]
- Refactoring goals: [Specific improvements desired]
- Risk tolerance: [Conservative vs aggressive refactoring approach]
- Timeline constraints: [Available time for refactoring work]
- Team capacity: [Developer availability and skill levels]

BUSINESS CONSTRAINTS:
- Feature delivery timeline: [Upcoming deadlines and priorities]
- Testing requirements: [Test coverage and validation needs]
- Deployment constraints: [Release cycles and downtime tolerance]
- User impact tolerance: [Acceptable risk for user-facing changes]

Please provide:

REFACTORING ASSESSMENT:
- Code quality analysis and technical debt identification
- Refactoring priority assessment and impact analysis
- Risk evaluation for different refactoring approaches
- Effort estimation and timeline planning
- Success criteria and measurement approach

REFACTORING STRATEGY:
- Incremental vs comprehensive refactoring approach
- Dependency analysis and refactoring sequence
- Backward compatibility maintenance strategy
- Testing strategy throughout refactoring process
- Rollback planning and risk mitigation

CODE STRUCTURE IMPROVEMENTS:
- Class and method decomposition strategies
- Design pattern application and implementation
- SOLID principles adherence improvements
- Separation of concerns and layer clarification
- Dependency injection and inversion improvements

NAMING AND CLARITY:
- Variable, function, and class naming improvements
- Code organization and module structure enhancement
- Comment and documentation improvements
- Magic number and constant extraction
- Code complexity reduction techniques

PERFORMANCE OPTIMIZATIONS:
- Algorithm efficiency improvements
- Data structure optimization
- Memory usage reduction and management
- Database query and access pattern optimization
- Caching and memoization opportunities

DESIGN PATTERN APPLICATION:
- Appropriate design pattern identification
- Pattern implementation and integration
- Anti-pattern elimination and replacement
- Architecture pattern alignment
- Framework pattern utilization

TESTING INTEGRATION:
- Test coverage improvement during refactoring
- Test-driven refactoring approach
- Mock and stub improvement for testability
- Integration test enhancement
- Performance test implementation

REFACTORING EXECUTION PLAN:
- Phase-by-phase refactoring breakdown
- Milestone definition and validation criteria
- Code review and approval process
- Continuous integration and testing approach
- Progress tracking and reporting

QUALITY ASSURANCE:
- Automated testing strategy for refactored code
- Manual testing and validation procedures
- Performance impact measurement and validation
- Security impact assessment and testing
- User acceptance testing coordination

TEAM COORDINATION:
- Knowledge sharing and documentation strategy
- Code review standards and procedures
- Pair programming and collaboration approach
- Training and skill development needs
- Communication and progress reporting

RISK MANAGEMENT:
- Refactoring risk assessment and monitoring
- Rollback procedures and contingency planning
- Performance regression detection and response
- Bug introduction prevention and detection
- Production deployment safety measures

LONG-TERM MAINTENANCE:
- Code standard establishment and enforcement
- Technical debt prevention strategies
- Continuous refactoring culture development
- Architecture evolution planning
- Knowledge documentation and transfer

TOOLING AND AUTOMATION:
- Refactoring tool recommendations and usage
- Automated refactoring script development
- Static analysis tool integration
- Code quality metric tracking
- Continuous improvement automation

Provide specific refactoring techniques, code examples, and implementation steps relevant to my programming language and framework.
```

### Technical Debt Reduction Planning
**Use Case**: Create comprehensive plans for reducing technical debt while balancing feature delivery and maintaining system stability.

**Copy-Pastable Prompt**:
```
Help me create a comprehensive technical debt reduction plan that balances debt paydown with feature delivery while maintaining system stability and team productivity.

CURRENT TECHNICAL DEBT:
[Describe the technical debt issues in your codebase]

SYSTEM CONTEXT:
- Codebase size and age: [Lines of code, years in development]
- Team size and composition: [Number of developers, experience levels]
- Development velocity: [Current sprint velocity, delivery frequency]
- Maintenance burden: [Time spent on bug fixes, support issues]

BUSINESS CONSTRAINTS:
- Feature delivery pressure: [Upcoming deadlines, business priorities]
- Available capacity: [Percentage of time available for debt work]
- Risk tolerance: [Conservative vs aggressive debt reduction]
- Budget constraints: [Financial limitations for debt work]

Please provide:

DEBT ASSESSMENT AND INVENTORY:
- Technical debt categorization and classification
- Impact assessment for each debt category
- Effort estimation for debt reduction work
- Dependency analysis between debt items
- Priority ranking based on impact and effort

DEBT IMPACT ANALYSIS:
- Development velocity impact measurement
- Code quality and maintainability effects
- Security and compliance risk assessment
- Performance and scalability implications
- Team productivity and morale impact

REDUCTION STRATEGY:
- Incremental vs comprehensive debt reduction approach
- Integration with feature development work
- Boy Scout Rule implementation and guidelines
- Dedicated debt reduction sprint planning
- Long-term debt elimination roadmap

PRIORITIZATION FRAMEWORK:
- High-impact, low-effort quick wins identification
- Critical debt that blocks feature development
- Security and compliance debt prioritization
- Performance-critical debt identification
- Team skill development opportunities

IMPLEMENTATION PLANNING:
- Sprint-by-sprint debt reduction allocation
- Feature development integration strategies
- Team capacity planning and allocation
- Risk mitigation for large refactoring efforts
- Progress tracking and measurement approach

TEAM ENGAGEMENT:
- Developer buy-in and motivation strategies
- Skill building and knowledge sharing plans
- Code quality culture development
- Technical decision documentation and standards
- Recognition and incentive programs

MEASUREMENT AND TRACKING:
- Technical debt metrics and KPIs
- Code quality improvement tracking
- Developer productivity metrics
- System performance and reliability metrics
- Business impact measurement

PROCESS IMPROVEMENTS:
- Technical debt prevention strategies
- Code review standards and quality gates
- Automated quality checking and enforcement
- Architecture decision documentation
- Technical debt tracking and reporting

COMMUNICATION STRATEGY:
- Stakeholder education about technical debt impact
- Business value communication for debt work
- Progress reporting and success story sharing
- Resource allocation justification
- Timeline and milestone communication

RISK MANAGEMENT:
- Debt reduction risk assessment and mitigation
- System stability protection during refactoring
- Rollback planning for major changes
- Testing strategy for debt reduction work
- Production deployment safety measures

SUSTAINABLE PRACTICES:
- Technical debt prevention culture
- Continuous improvement processes
- Regular debt assessment and review cycles
- Knowledge documentation and sharing
- Team rotation and cross-training

TOOLS AND AUTOMATION:
- Static analysis tool configuration for debt detection
- Automated code quality measurement
- Technical debt tracking and reporting tools
- Refactoring tool integration and usage
- Continuous integration quality gates

LONG-TERM VISION:
- Target code quality and architecture vision
- Technology modernization roadmap
- Skills development and team growth planning
- Sustainable development velocity goals
- Innovation and experimentation capacity

Provide specific strategies, metrics, and implementation approaches relevant to my technology stack and organizational context.
```

### Legacy Code Modernization
**Use Case**: Plan and execute modernization of legacy codebases with minimal disruption while improving maintainability and performance.

**Copy-Pastable Prompt**:
```
Help me plan and execute a comprehensive legacy code modernization strategy that improves maintainability and performance while minimizing business disruption and technical risk.

LEGACY CODEBASE CONTEXT:
[Describe the legacy system: age, technology, size, critical business functions]

MODERNIZATION DRIVERS:
- Technical challenges: [Maintenance issues, performance problems, security concerns]
- Business requirements: [New feature needs, integration requirements, compliance]
- Technology constraints: [Outdated frameworks, unsupported dependencies, skill gaps]
- Risk factors: [System criticality, user impact, business continuity needs]

MODERNIZATION GOALS:
- Technical objectives: [Code quality, performance, security improvements]
- Business objectives: [Feature delivery, cost reduction, risk mitigation]
- Timeline constraints: [Project deadlines, business cycles]
- Success criteria: [Measurable outcomes and validation approaches]

Please provide:

LEGACY ASSESSMENT:
- Code quality analysis and technical debt evaluation
- Architecture assessment and modernization opportunities
- Dependency analysis and technology stack evaluation
- Risk assessment for modernization approaches
- Business criticality and impact analysis

MODERNIZATION STRATEGY:
- Strangler Fig pattern vs Big Bang vs hybrid approach
- Component-by-component modernization planning
- API-first modernization and service extraction
- Database modernization and migration strategy
- UI/UX modernization and responsive design

RISK MITIGATION:
- Backward compatibility maintenance strategies
- Gradual migration and rollback planning
- Data integrity and consistency protection
- User experience continuity assurance
- Business operation continuity planning

TECHNOLOGY MODERNIZATION:
- Framework and library upgrade planning
- Language version migration strategy
- Database modernization and optimization
- Infrastructure modernization and cloud migration
- Security enhancement and compliance updates

ARCHITECTURE EVOLUTION:
- Monolith to microservices decomposition planning
- Service-oriented architecture implementation
- Event-driven architecture integration
- API gateway and service mesh implementation
- Cloud-native architecture adoption

DATA MIGRATION:
- Database schema modernization and optimization
- Data migration strategy and validation
- Legacy data format conversion and cleanup
- Data synchronization during transition periods
- Backup and recovery planning for data migration

TESTING STRATEGY:
- Legacy system characterization testing
- Regression testing for modernized components
- Integration testing for new and legacy components
- Performance testing and optimization validation
- User acceptance testing coordination

INCREMENTAL DELIVERY:
- Feature flag implementation for gradual rollout
- A/B testing for modernized components
- Canary deployment and blue-green strategies
- User feedback collection and iteration
- Performance monitoring and optimization

TEAM ENABLEMENT:
- Skills assessment and training planning
- Knowledge transfer from legacy to modern systems
- Team structure and responsibility evolution
- Documentation and knowledge management
- Mentoring and pair programming strategies

OPERATIONAL TRANSITION:
- Monitoring and alerting modernization
- Deployment automation and CI/CD implementation
- Support and maintenance process updates
- Incident response and troubleshooting updates
- Performance monitoring and optimization

STAKEHOLDER MANAGEMENT:
- Business stakeholder communication and alignment
- User training and change management
- Timeline and milestone communication
- Risk communication and mitigation updates
- Success metric reporting and celebration

QUALITY ASSURANCE:
- Code quality improvement and standardization
- Security enhancement and vulnerability remediation
- Performance optimization and scalability improvement
- Maintainability enhancement and technical debt reduction
- Documentation improvement and knowledge sharing

SUSTAINABILITY PLANNING:
- Technical debt prevention in modernized code
- Continuous improvement and innovation culture
- Regular technology assessment and updates
- Team skill development and knowledge sharing
- Architecture evolution and future planning

BUDGET AND RESOURCE PLANNING:
- Resource allocation and capacity planning
- Technology licensing and infrastructure costs
- Training and skill development investment
- External consultant and vendor management
- ROI calculation and business case validation

Provide specific migration strategies, tools, and implementation approaches for my legacy technology stack and modernization goals.
```

---

*These review, debug, and refactor prompts help maintain and improve code quality throughout the development lifecycle. Adapt them based on your specific codebase characteristics and quality requirements.*
