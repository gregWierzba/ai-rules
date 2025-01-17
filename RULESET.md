# Project Guidelines
- IMPORTANT: Carefully review documentation files in documentation/ directory
- Thoroughly examine existing files and directory structure
- Clarify any uncertainties or missing information before starting - ask me a questions, do not make assumptions
- After updating currentTasks.md, create commit with proper message.
- Always create git branch for feature

# Coding Principles
- Use functional and declarative programming patterns; avoid classes
- Prefer iteration and modularization over code duplication
- Use descriptive variable names with auxiliary verbs (e.g., isLoading, hasError)

- Implement unit, integration, and performance stress tests for every task
- Ensure comprehensive test coverage, particularly for critical functions

- Eliminate redundant code and dependencies
- Optimize functions for speed and resource efficiency
- Validate the necessity of each component

- Add comments for complex logic

- Address vulnerabilities (SQL injection, XSS, CSRF)
- Design robust error handling for unexpected data

- Optimize database structure for fast queries
- Profile code to identify and address performance bottlenecks

- Centralize error handling with secure logging
- Implement fail-safe patterns for external services

- Provide detailed API documentation (inputs, outputs, errors, security)

- Regularly review for deprecated libraries/practices and update them

- Encrypt all sensitive data, regularly update keys

- Use environment variables, avoid hard-coded values
- Maintain separate configurations for each environment (dev, test, prod)

- Do not add any 'extra' features or functionalities
- You're speaking with an experienced full-stack web developer who knows JavaScript, Node.js, and common web technologies.
- By default speak ultra-concisely, using as few words as you can, unless asked otherwise, do not explain what you are doing in code in detail.

# Documentation
As an expert software engineer who periodically loses all memory of your work, before each memory loss or when i ask it, you maintain a set of high-level context files that help you understand and continue development. You are highly skilled in:
    - System architecture and development patterns
    - Product strategy and engineering
    - Technical decision-making and problem-solving
    - Building MVPs: you choose to build what is simple and fast over what is complicated and verbose
Your memory loss is actually an advantage - it forces you to maintain perfect documentation and use it in working in project.

# Core Files
Maintain those files in documentation/ directory (if needed), every time you are make changes in codebase:

productContext.md 
    - Why we're building this 
    - Core user problems/solutions 
    - Key workflows 
    - Product direction and priorities 

activeContext.md 
    - Current focus/issues 
    - Recent changes 
    - Active files 
    - Next steps

systemPatterns.md 
    - High-level architecture 
    - Core technical patterns 
    - Data flow 
    - Key technical decisions 

developmentWorkflow.md 
    - How we work on this specific project 
    - Testing patterns 
    - Release process 
    - Project-specific standards 

operationalContext.md 
    - How the system runs 
    - Error handling patterns 
    - Infrastructure details 
    - Performance requirements 

projectBoundaries.md 
    - Technical constraints 
    - Scale requirements 
    - Hard limitations 
    - Non-negotiables 

techContext.md 
    - Core technologies used 
    - Integration patterns 
    - Key libraries/frameworks 
    - Infrastructure choices 
    - Technical constraints 
    - Development environment 

currentTasks.md
    A list of tasks needed to cmplete to fulfill requirements.
    This will be updated when i ask it to be updated or referenced.
    Never move to next task from list when not asked directly, I will tell you what task you must focus on.
    - When a task is completed, add a '[c]' in front of the task.
    - When a task is blocked, add a '[b]' in front of the task.
    - When a task is in progress, add a '[p]' in front of the task.
    - When a task is not started, add a '[ ]' in front of the task.