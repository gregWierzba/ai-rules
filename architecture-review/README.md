# Technical Architecture Review Prompt

## Overview

This prompt enables AI assistants to perform comprehensive technical architecture reviews with a focus on system design, scalability, and architectural patterns. It is designed for evaluating existing system architectures while maintaining a strong emphasis on strategic recommendations and architectural improvements.

# Required Information (all fields must be provided before proceeding with the review)

System Information:

- System Name: Example System
- Current Scale:
  - Daily Active Users: 100,000
  - Peak Concurrent Users: 10,000
  - Data Volume: 500GB/day
- Technology Stack:
  - Frontend: React/TypeScript
  - Backend: Node.js/Express
  - Database: PostgreSQL
  - Cache: Redis
  - Message Queue: RabbitMQ

Available Documentation:

- System Architecture: docs/architecture.md
- Infrastructure Diagrams: docs/infrastructure/
- Performance Requirements: REQUIREMENTS.md
- Current Pain Points: ISSUES.md

````

Expected output will include:

1. System Overview

```markdown
## System Overview

### Current Architecture

- Microservices-based architecture
- REST APIs for service communication
- Event-driven processing for async operations
- Multi-region deployment

### Scale and Performance

- Current bottlenecks in data processing pipeline
- Load balancing strategy assessment
- Resource utilization analysis
````

2. Architecture Assessment

```markdown
## Architecture Assessment

### Design Patterns Evaluation

- Effective use of CQRS in order processing
- Incomplete implementation of Circuit Breaker pattern
- Missing retry mechanisms in critical services

### Scalability Analysis

- Horizontal scaling limitations in database layer
- Efficient caching strategy in place
- Potential issues with session management at scale
```

3. Technical Debt Analysis

```markdown
## Technical Debt Analysis

### Infrastructure Debt

- Legacy load balancer configuration
- Outdated container orchestration
- Manual scaling procedures

### Architecture Debt

- Tight coupling between core services
- Inconsistent API versioning
- Monolithic components in critical path
```

4. Risk Assessment

```markdown
## Risk Assessment

### High-Risk Areas

- Single point of failure in authentication service
- Data consistency issues during peak loads
- Limited disaster recovery capabilities

### Compliance and Security

- Data residency requirements not fully met
- Incomplete audit logging
- Security vulnerabilities in service mesh
```

5. Recommendations

```markdown
## Critical Improvements

1. Implement service mesh for better reliability
2. Migrate to distributed database architecture
3. Automate scaling procedures
4. Enhance monitoring and observability

## Strategic Improvements

1. Adopt event-sourcing for critical workflows
2. Implement blue-green deployment
3. Establish API gateway pattern
4. Enhance data replication strategy
```

The prompt is designed to work as a complete system, with the pre-prompting phase establishing the foundation for a thorough architectural review. The system ensures all necessary information is gathered before beginning the analysis and maintains consistent output organization through dedicated file storage.
