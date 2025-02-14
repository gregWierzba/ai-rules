# Technical Code Review Prompt

## Overview

This prompt enables AI assistants to perform comprehensive technical code reviews with a focus on architecture, code quality, and best practices. It is designed for reviewing existing codebases while maintaining a strong emphasis on actionable recommendations and concrete improvements.

## Complete Usage Example

To use this prompt effectively, provide it in two parts:

1. First, set the AI's role and context (pre-prompting):

```markdown
You are a principal engineer with deep expertise in clean code principles, SOLID design patterns, and clean architecture. Your role is to conduct a comprehensive technical assessment of the provided codebase, focusing on maintainability, scalability, and code quality.
```

2. Then, provide the specific review request with all required information and output file specification:

```markdown
Based on your expertise as a principal engineer, please review the following codebase and store the complete review in code-review.md:

# Required Information (all fields must be provided before proceeding with the review)

Repository Information (choose A or B):

A. Remote Repository:

- URL: https://github.com/company/project
- Target commit ID(s):
  - Single commit review: 8f7e6d5c4b3a2n1m
    OR
  - Multiple commits review:
    Start: 8f7e6d5c4b3a2n1m
    End: 9g8h7i6j5k4l3m2n
- Branch: main

B. Local Git Project:

- Project Path: /path/to/local/project
- Target commit ID(s):
  - Current review: 7d8e9f0a1b2c
- Branch: feature/new-auth
- Git Status: Clean (no uncommitted changes)

Note: The review will focus specifically on the changes introduced in the specified commit(s). For multiple commits, the review will analyze the evolution of the code between the start and end commits.

Primary Language/Framework: TypeScript/React

Available Documentation:

- Architecture guidelines: docs/architecture.md
- Coding standards: None (use industry standards)
- Requirements: REQUIREMENTS.md
```

Expected output will include:

1. Commit Analysis

```markdown
## Commit Analysis

### Single Commit Review

- Detailed analysis of changes in commit 8f7e6d5c4b3a2n1m
- Impact: Added authentication middleware
- Context: Implementation of security requirements

### Multiple Commits Review (if applicable)

- Evolution from 8f7e6d5c4b3a2n1m to 9g8h7i6j5k4l3m2n
- Progressive improvements in auth system
- Consistent pattern of security enhancements
```

2. Technical Assessment

```markdown
## Technical Assessment

### Architecture Evaluation

- Component structure follows React best practices
- Identified circular dependency between auth and user modules
- ...

### Design Pattern Analysis

- Proper implementation of Observer pattern in state management
- Inconsistent use of Factory pattern across services
- ...
```

3. Code Analysis

````markdown
## Code Analysis

### Code Smells

- UserManager.ts: Large class with multiple responsibilities
- AuthService.ts: Excessive coupling with external services
- Example fix:

  ```typescript
  // Before
  class UserManager {
    // 200+ lines of mixed responsibilities
  }

  // After
  class UserManager {
    constructor(
      private authService: AuthService,
      private profileService: ProfileService
    ) {}
    // Focused user management responsibilities
  }
  ```
````

### Security Issues

- Severity: High - Unvalidated user input in API calls
- Severity: Medium - Insecure password hashing algorithm
- ...

````

3. Prioritized Recommendations
```markdown
## Must-Have Improvements
1. Fix authentication input validation (Security)
2. Resolve circular dependencies (Architecture)
3. Implement proper error boundaries (Reliability)

## Should-Have Improvements
1. Refactor UserManager class (Maintainability)
2. Update password hashing algorithm (Security)
...
````

## Prompt Structure and Best Practices

1. **Pre-prompting Phase**

   - Always start with the role definition to set the AI's expertise and context
   - Include the full scope of responsibilities and focus areas
   - This establishes the depth and breadth of the technical review

2. **Review Request Phase**

   - Provide all required repository information
   - Include available documentation references
   - Specify any particular areas of concern (optional)

3. **Best Practices**

   - Keep the role definition and review request separate for clarity
   - Ensure all repository information is precise and verified
   - Include commit IDs for exact version targeting
   - Specify when documentation is missing to trigger fallback to industry standards
   - Be explicit about the primary technology stack
   - Validate all required inputs are provided before starting the review
   - Always specify code-review.md as the output file for consistency

4. **Input Validation and Output**
   - The model will verify all required information is provided before proceeding
   - If any required field is missing, the model will request it before starting the review
   - All review output will be stored in code-review.md for proper documentation
   - The output file will maintain consistent structure and formatting

The prompt is designed to work as a complete system, with the pre-prompting phase setting the foundation for a thorough and professional review. The system ensures all necessary information is gathered before beginning the analysis and maintains consistent output organization through dedicated file storage.
