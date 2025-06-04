# Step 3: Project WBS Prompts

Work Breakdown Structure (WBS) prompts for organizing project tasks, estimating effort, and creating detailed implementation plans. These prompts help translate architectural designs into actionable development tasks.

## Table of Contents
- [Task Decomposition](#task-decomposition)
- [Estimation and Planning](#estimation-and-planning)
- [Sprint and Iteration Planning](#sprint-and-iteration-planning)

---

## Task Decomposition

### Feature-Based Work Breakdown
**Use Case**: Break down large features into manageable development tasks with clear dependencies and deliverables.

**Copy-Pastable Prompt**:
```
Help me create a detailed work breakdown structure for implementing a specific feature. I need tasks organized by component, with effort estimates and dependencies.

FEATURE DESCRIPTION:
[Describe the feature you want to implement]

TECHNICAL CONTEXT:
- Architecture: [Microservices, monolith, etc.]
- Technology stack: [Languages, frameworks, databases]
- Team composition: [Frontend, backend, full-stack developers]
- Integration requirements: [APIs, third-party services, databases]

ACCEPTANCE CRITERIA:
[List the specific acceptance criteria for this feature]

Please create:

TASK BREAKDOWN:
- Frontend tasks (UI components, state management, API integration)
- Backend tasks (API endpoints, business logic, data models)
- Database tasks (schema changes, migrations, indexing)
- Integration tasks (third-party services, external APIs)
- Testing tasks (unit tests, integration tests, E2E tests)
- DevOps tasks (deployment, configuration, monitoring)

For each task, provide:

TASK DETAILS:
- Task title and clear description
- Effort estimate (story points or hours)
- Required skills and assignee suggestions
- Dependencies on other tasks
- Definition of done criteria

TECHNICAL SPECIFICATIONS:
- Implementation approach and key considerations
- Potential challenges and risk factors
- Testing strategy and requirements
- Documentation and code review needs

SEQUENCING:
- Task dependency graph and critical path
- Parallel execution opportunities
- Integration points and testing milestones
- Risk mitigation for blocked dependencies

DELIVERABLES:
- Code components and artifacts
- Tests and documentation
- Configuration and deployment scripts
- Review and approval checkpoints

Please also identify tasks that could be started early and those that require specific expertise or additional research.
```

### Epic to Story Decomposition
**Use Case**: Break down large epics into manageable user stories with proper sizing and clear acceptance criteria.

**Copy-Pastable Prompt**:
```
Help me decompose a large epic into well-sized user stories that can be completed within a single sprint. I need stories that are independent, testable, and valuable.

EPIC DESCRIPTION:
[Describe the epic or large feature]

TARGET USERS:
[Define the primary users who will benefit from this epic]

BUSINESS VALUE:
[Explain the business value and success metrics]

TECHNICAL CONSTRAINTS:
- Timeline: [Sprint length and number of sprints available]
- Team capacity: [Team size and velocity]
- Technical dependencies: [External systems, APIs, infrastructure]
- Quality requirements: [Performance, security, accessibility]

Please create:

USER STORY BREAKDOWN:
Stories should follow the format:
"As a [user type], I want [functionality] so that [benefit]"

For each story, include:

STORY DETAILS:
- User story title and description
- Acceptance criteria (Given/When/Then format)
- Story points or effort estimate
- Priority level (Must have, Should have, Could have)

TECHNICAL TASKS:
- Frontend implementation tasks
- Backend/API development tasks
- Database schema or data migration tasks
- Testing requirements (unit, integration, E2E)
- Documentation and deployment tasks

DEPENDENCIES AND SEQUENCING:
- Dependencies between stories
- Recommended implementation order
- Stories that can be developed in parallel
- Integration points and testing dependencies

VALUE DELIVERY:
- Business value of each story
- User impact and feedback opportunities
- Incremental delivery and demo possibilities
- Risk reduction and learning opportunities

STORY VALIDATION:
- How to validate each story meets requirements
- User testing and feedback mechanisms
- Performance and quality metrics
- Success criteria and measurement approach

EDGE CASES AND CONSIDERATIONS:
- Error scenarios and exception handling
- Edge cases that need specific attention
- Non-functional requirements per story
- Technical debt considerations

Please ensure stories follow INVEST criteria (Independent, Negotiable, Valuable, Estimable, Small, Testable) and can realistically be completed in one sprint.
```

### Technical Debt Assessment and Planning
**Use Case**: Identify, prioritize, and plan technical debt reduction work alongside feature development.

**Copy-Pastable Prompt**:
```
Help me assess and create a work plan for addressing technical debt in my project. I need to balance debt reduction with feature delivery while improving code quality and maintainability.

CURRENT CODEBASE:
- Project age and size: [Years old, lines of code, team size]
- Technology stack: [Languages, frameworks, major dependencies]
- Known problem areas: [Performance issues, maintenance challenges]
- Code quality metrics: [Test coverage, complexity scores, if available]

DEVELOPMENT CHALLENGES:
[Describe current pain points in development, deployment, or maintenance]

BUSINESS CONSTRAINTS:
- Feature delivery pressure: [Timeline and priority constraints]
- Team availability: [Percentage of time available for debt work]
- Risk tolerance: [Conservative vs aggressive refactoring approach]
- Budget for debt work: [Dedicated time or integrated with features]

Please provide:

TECHNICAL DEBT INVENTORY:
- Code quality issues (complexity, duplication, coupling)
- Architecture problems (design patterns, layer violations)
- Performance bottlenecks and scalability issues
- Security vulnerabilities and compliance gaps
- Documentation and knowledge gaps
- Testing gaps and quality assurance issues

DEBT PRIORITIZATION:
For each debt item, assess:
- Impact on development velocity
- Risk to system stability and security
- Effort required to address
- Business impact of leaving unaddressed
- Dependencies on other debt items

REDUCTION STRATEGY:
- Quick wins that provide immediate value
- Large refactoring projects that need dedicated time
- Gradual improvement that can be done alongside features
- Boy Scout Rule opportunities (leave code better than found)

IMPLEMENTATION PLANNING:
- Sprint-by-sprint debt reduction plan
- Integration with feature development work
- Dedicated refactoring sprints vs continuous improvement
- Risk mitigation for large refactoring efforts

MEASUREMENT AND TRACKING:
- Metrics to track debt reduction progress
- Code quality improvements over time
- Developer productivity and satisfaction metrics
- System performance and reliability improvements

TEAM ALIGNMENT:
- Communication strategy for debt work value
- Developer skill building and knowledge sharing
- Code review standards and quality gates
- Technical decision documentation and standards

RISK MANAGEMENT:
- Rollback plans for major refactoring efforts
- Testing strategies for debt reduction work
- Impact assessment for system changes
- Communication plan for stakeholders

Please provide specific recommendations for my technology stack and prioritize debt items based on impact and effort.
```

---

## Estimation and Planning

### Agile Estimation Techniques
**Use Case**: Apply story points, t-shirt sizing, and other agile estimation techniques for accurate project planning and sprint commitment.

**Copy-Pastable Prompt**:
```
Help me estimate the effort for development tasks using agile estimation techniques. I need guidance on story pointing, velocity calculation, and capacity planning.

PROJECT CONTEXT:
[Describe the project scope and technical complexity]

TEAM DETAILS:
- Team size: [Number of developers and their roles]
- Experience level: [Junior, mid, senior distribution]
- Domain expertise: [Familiarity with technology stack and business domain]
- Sprint length: [1, 2, or 3 weeks]

HISTORICAL DATA (if available):
- Previous sprint velocities: [Story points completed per sprint]
- Team capacity: [Available hours per sprint per person]
- Typical story complexity distribution: [Small, medium, large story ratios]

ESTIMATION TARGETS:
[List the features, user stories, or tasks you need to estimate]

Please provide:

ESTIMATION FRAMEWORK:
- Story point scale recommendation (Fibonacci, T-shirt sizes, etc.)
- Reference stories for each point value with examples
- Complexity factors to consider (technical, domain, integration)
- Team calibration exercises and baseline establishment

EFFORT ESTIMATION:
For each item to estimate:
- Story point assignment with reasoning
- Complexity breakdown (frontend, backend, testing, etc.)
- Risk factors and uncertainty considerations
- Comparison to similar completed work

PLANNING POKER GUIDANCE:
- Structured estimation session format
- Questions to ask during estimation discussions
- Handling disagreements and outlier estimates
- Re-estimation triggers and criteria

VELOCITY PLANNING:
- Historical velocity analysis and trends
- Capacity adjustments for holidays, vacations, meetings
- Sprint commitment recommendations
- Buffer for unplanned work and bug fixes

ESTIMATION REFINEMENT:
- Regular estimation accuracy review process
- Learning from estimation vs actual effort variances
- Team estimation skill improvement strategies
- Calibration with other teams (if applicable)

UNCERTAINTY HANDLING:
- Techniques for estimating unknowns and research tasks
- Spike estimation and time-boxing
- Three-point estimation for high-uncertainty items
- Risk assessment and contingency planning

PLANNING CONSIDERATIONS:
- Sprint planning recommendations based on estimates
- Feature slicing strategies for large estimates
- Technical debt estimation and planning
- Cross-team dependency coordination

Please include specific examples relevant to my technology stack and project type.
```

### Resource Allocation and Capacity Planning
**Use Case**: Plan resource allocation across multiple features, projects, or teams while optimizing for skill utilization and delivery timeline.

**Copy-Pastable Prompt**:
```
Help me create a comprehensive resource allocation and capacity planning strategy for my development project. I need to optimize team utilization while meeting delivery commitments.

TEAM COMPOSITION:
[List team members with their roles, skill levels, and availability]

PROJECT PORTFOLIO:
[Describe multiple projects, features, or workstreams that need resources]

CONSTRAINTS:
- Timeline requirements: [Hard deadlines, business milestones]
- Skill requirements: [Specialized skills needed for different work]
- Team preferences: [Developer interests, growth opportunities]
- Budget limitations: [If hiring or contracting is possible]

CURRENT COMMITMENTS:
- Ongoing maintenance work: [Percentage of capacity]
- Bug fixes and support: [Estimated capacity needed]
- Technical debt work: [Planned improvement efforts]
- Training and development: [Skill building time]

Please provide:

CAPACITY ANALYSIS:
- Available capacity per team member per sprint
- Skill matrix and capability assessment
- Workload distribution and utilization targets
- Peak and low-demand period identification

ALLOCATION STRATEGY:
- Primary and secondary assignments for each team member
- Cross-training opportunities and skill development
- Load balancing across team members
- Backup coverage for critical skills

WORKSTREAM PLANNING:
- Priority ordering of projects and features
- Parallel vs sequential execution strategies
- Critical path identification and resource needs
- Risk mitigation for resource constraints

SKILL OPTIMIZATION:
- Matching tasks to individual strengths and interests
- Stretch assignments for professional development
- Pair programming and knowledge sharing opportunities
- Specialist vs generalist utilization strategies

FLEXIBILITY PLANNING:
- Resource reallocation triggers and procedures
- Response strategies for changing priorities
- Buffer capacity for unplanned work
- Escalation procedures for resource conflicts

PERFORMANCE TRACKING:
- Utilization metrics and target ranges
- Delivery velocity and quality indicators
- Team satisfaction and engagement measures
- Skill development progress tracking

SCENARIO PLANNING:
- Resource plans for different priority scenarios
- Impact analysis of team member unavailability
- Scaling strategies (hiring, contracting, overtime)
- Descoping options if capacity is insufficient

COMMUNICATION PLAN:
- Resource allocation transparency and updates
- Stakeholder expectation management
- Team workload visibility and feedback
- Regular planning review and adjustment cycles

Include specific recommendations for my team size and project complexity.
```

### Risk-Based Planning and Contingencies
**Use Case**: Incorporate risk assessment into project planning with specific contingency plans and mitigation strategies.

**Copy-Pastable Prompt**:
```
Help me create a risk-based project plan that identifies potential issues and includes specific contingency strategies. I need to plan for uncertainty while maintaining delivery commitments.

PROJECT OVERVIEW:
[Describe the project scope, timeline, and key deliverables]

KNOWN RISKS:
[List any risks you're already aware of]

PROJECT CONSTRAINTS:
- Hard deadlines: [Non-negotiable dates and milestones]
- Resource limitations: [Team size, budget, skill constraints]
- Technical constraints: [Legacy systems, compliance requirements]
- External dependencies: [Third-party services, vendor deliveries]

RISK TOLERANCE:
[Describe your organization's risk tolerance and preference for contingency planning]

Please provide:

RISK IDENTIFICATION:
- Technical risks (complexity, new technology, integration challenges)
- Resource risks (availability, skill gaps, turnover)
- External risks (vendor delays, requirement changes, market factors)
- Operational risks (infrastructure, security, compliance)

RISK ASSESSMENT:
For each identified risk:
- Probability of occurrence (High/Medium/Low)
- Impact severity on timeline, quality, and budget
- Risk score and priority ranking
- Early warning indicators and detection methods

MITIGATION STRATEGIES:
- Preventive measures to reduce risk probability
- Specific actions and responsible parties
- Timeline for implementing mitigation measures
- Resource requirements for risk mitigation

CONTINGENCY PLANNING:
- Specific response plans for high-priority risks
- Alternative approaches and workarounds
- Resource reallocation strategies
- Scope adjustment options (descoping, phasing)

BUFFER PLANNING:
- Time buffers for high-risk activities
- Resource buffers for critical path items
- Budget contingencies for risk responses
- Quality trade-off options under pressure

MONITORING AND RESPONSE:
- Risk monitoring schedule and responsibilities
- Trigger points for activating contingency plans
- Escalation procedures for emerging risks
- Communication protocols for risk events

SCENARIO PLANNING:
- Best case, worst case, and most likely scenarios
- Impact on delivery timeline and scope
- Resource needs for different scenarios
- Stakeholder communication for various outcomes

LEARNING AND ADAPTATION:
- Regular risk reassessment schedule
- Lessons learned capture and application
- Plan adjustment triggers and procedures
- Team knowledge sharing about risk management

STAKEHOLDER COMMUNICATION:
- Risk transparency and reporting approach
- Expectation setting for potential impacts
- Decision-making authority for risk responses
- Regular updates on risk status and mitigation progress

Provide specific risk mitigation tactics relevant to my technology stack and project type.
```

---

## Sprint and Iteration Planning

### Sprint Planning Optimization
**Use Case**: Structure effective sprint planning sessions that result in realistic commitments and clear execution plans.

**Copy-Pastable Prompt**:
```
Help me optimize our sprint planning process to create realistic sprint commitments with clear execution plans. I need a structured approach that engages the team and produces actionable sprint goals.

TEAM CONTEXT:
- Sprint length: [1, 2, or 3 weeks]
- Team size and composition: [Developers, testers, etc.]
- Historical velocity: [Average story points per sprint]
- Team experience: [How long team has been working together]

CURRENT CHALLENGES:
[Describe any issues with current sprint planning - overcommitment, unclear goals, etc.]

SPRINT PLANNING INPUTS:
- Product backlog state: [How well-groomed and estimated]
- Sprint goal priorities: [Business objectives for upcoming sprint]
- Team capacity: [Availability, holidays, other commitments]
- Technical constraints: [Dependencies, technical debt, infrastructure needs]

Please provide:

SPRINT PLANNING STRUCTURE:
- Pre-planning preparation and backlog refinement
- Sprint planning meeting agenda and timing
- Participant roles and responsibilities
- Decision-making process and authority

CAPACITY PLANNING:
- Team capacity calculation methodology
- Adjustments for meetings, code reviews, and overhead
- Buffer allocation for unplanned work and bugs
- Skill-based capacity considerations

STORY SELECTION:
- Prioritization criteria and decision framework
- Story dependency analysis and sequencing
- Technical feasibility assessment
- Value delivery optimization

SPRINT GOAL DEFINITION:
- SMART sprint goal creation process
- Goal alignment with business objectives
- Success criteria and measurement approach
- Stakeholder communication and buy-in

TASK BREAKDOWN:
- User story to task decomposition approach
- Task estimation and ownership assignment
- Dependency identification and management
- Integration and testing task planning

COMMITMENT PROCESS:
- Team consensus building for sprint commitment
- Risk assessment and mitigation planning
- Contingency planning for scope adjustments
- Communication of commitments to stakeholders

EXECUTION PLANNING:
- Daily standup structure and cadence
- Progress tracking and visibility methods
- Impediment identification and resolution process
- Sprint burndown and velocity tracking

QUALITY PLANNING:
- Definition of done verification process
- Code review and testing integration
- Technical debt and refactoring allocation
- Documentation and knowledge sharing plans

Please include specific techniques for common sprint planning challenges and meeting facilitation tips.
```

### Release Planning and Roadmapping
**Use Case**: Create multi-sprint release plans that align with business objectives and manage feature dependencies across iterations.

**Copy-Pastable Prompt**:
```
Help me create a comprehensive release plan and roadmap that coordinates multiple sprints and features toward business objectives. I need to manage dependencies and communicate realistic timelines.

RELEASE SCOPE:
[Describe the features and objectives for the upcoming release]

BUSINESS CONTEXT:
- Release timeline: [Target release date and business drivers]
- Key stakeholders: [Product owners, business sponsors, users]
- Success criteria: [How will release success be measured]
- Market or competitive pressures: [External factors influencing timeline]

TECHNICAL CONTEXT:
- Current system state: [Starting point for the release]
- Architecture changes: [Major technical initiatives]
- Dependencies: [External services, infrastructure, other teams]
- Technical debt: [Known issues that need addressing]

TEAM CAPACITY:
- Team composition: [Size and skills available]
- Sprint capacity: [Historical velocity and availability]
- Skill constraints: [Specialized expertise needed]
- External dependencies: [Other teams, vendors, approvals]

Please provide:

FEATURE PRIORITIZATION:
- Feature value scoring and ranking methodology
- Dependency analysis and sequencing constraints
- Risk assessment for each major feature
- Minimum viable release scope definition

SPRINT ALLOCATION:
- Feature-to-sprint mapping and timeline
- Sprint themes and objectives
- Cross-sprint dependency management
- Integration and testing sprint planning

ROADMAP VISUALIZATION:
- Timeline view with features and milestones
- Dependency visualization and critical path
- Risk indicators and mitigation plans
- Progress tracking and reporting approach

SCOPE MANAGEMENT:
- Core vs optional feature classification
- Scope adjustment triggers and criteria
- Feature slicing and phased delivery options
- Quality vs scope trade-off framework

RISK AND MITIGATION:
- Timeline risks and probability assessment
- Technical risks and complexity factors
- Resource risks and mitigation strategies
- External dependency risks and alternatives

STAKEHOLDER COMMUNICATION:
- Release progress reporting cadence and format
- Milestone review and approval processes
- Scope change request and approval workflow
- Market readiness and launch preparation

QUALITY ASSURANCE:
- Release testing strategy and timeline
- Performance and security testing integration
- User acceptance testing coordination
- Release readiness criteria and checklist

DEPLOYMENT PLANNING:
- Release deployment strategy and rollback plans
- Environment progression and testing stages
- Feature flag and gradual rollout planning
- Post-release monitoring and support preparation

CONTINUOUS IMPROVEMENT:
- Release retrospective and lessons learned
- Process improvement identification
- Metric collection and analysis plan
- Next release planning preparation

Include specific templates and tools recommendations for my project scale and complexity.
```

### Cross-Team Coordination and Dependencies
**Use Case**: Manage work coordination between multiple teams with shared dependencies and integration points.

**Copy-Pastable Prompt**:
```
Help me create a coordination plan for managing dependencies and integration between multiple development teams. I need processes that ensure alignment while maintaining team autonomy.

TEAM STRUCTURE:
[Describe the teams involved, their responsibilities, and current coordination challenges]

SHARED COMPONENTS:
- Shared services or APIs: [Common infrastructure or services]
- Data dependencies: [Shared databases, data flows]
- Integration points: [Where teams need to coordinate]
- Technical standards: [Common frameworks, patterns, tools]

COORDINATION CHALLENGES:
[Describe current issues with cross-team coordination]

PROJECT TIMELINE:
- Sprint cadence: [Sprint lengths and alignment across teams]
- Release timeline: [Shared milestones and deadlines]
- Integration points: [When teams need deliverables from each other]

Please provide:

DEPENDENCY MANAGEMENT:
- Dependency identification and mapping process
- Cross-team dependency tracking and visibility
- Blocking dependency escalation procedures
- Alternative approach planning for blocked dependencies

COORDINATION MECHANISMS:
- Regular sync meetings and cadence (daily, weekly, sprint)
- Cross-team representative roles and responsibilities
- Shared planning sessions and joint sprint planning
- Integration testing and validation processes

COMMUNICATION PROTOCOLS:
- Information sharing standards and channels
- Decision-making authority and escalation paths
- Change notification and impact assessment process
- Conflict resolution procedures and authority

SHARED DELIVERABLES:
- API contract definition and versioning process
- Shared component development and ownership
- Documentation standards and maintenance
- Testing strategy for integrated components

INTEGRATION PLANNING:
- Integration timeline and milestone coordination
- Shared environment management and access
- End-to-end testing coordination and ownership
- Deployment coordination and release management

RISK MANAGEMENT:
- Cross-team risk identification and assessment
- Impact analysis for team delays or changes
- Contingency planning for dependency failures
- Risk communication and stakeholder management

QUALITY ASSURANCE:
- Cross-team code review and standards enforcement
- Integration testing strategy and responsibility
- Performance testing for integrated systems
- Security and compliance coordination

TOOLS AND INFRASTRUCTURE:
- Shared tooling and development environment setup
- Version control and branching strategy coordination
- CI/CD pipeline integration and shared infrastructure
- Monitoring and alerting for shared components

GOVERNANCE AND STANDARDS:
- Technical decision-making process across teams
- Architecture review board and approval processes
- Standards enforcement and compliance monitoring
- Knowledge sharing and best practice dissemination

METRICS AND REPORTING:
- Cross-team progress visibility and reporting
- Integration success metrics and dashboards
- Team performance and collaboration indicators
- Continuous improvement feedback and action planning

Provide specific coordination patterns and tools appropriate for my team size and organizational structure.
```

---

*These WBS prompts help transform high-level plans into actionable development tasks. Customize them based on your team's agile maturity and project complexity.*
