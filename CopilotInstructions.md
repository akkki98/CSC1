# GitHub Copilot Instructions File – Hands-on Lab

## Lab Title

**Creating and Using GitHub Copilot Instructions File (`.github/copilot-instructions.md`)**

## Target Audience

Backend Developers, Frontend Developers, Full-Stack Engineers, QA/SDETs



---

## Learning Objectives

By the end of this lab, participants will be able to:

* Understand what a **GitHub Copilot Instructions file** is
* Create and structure `.github/copilot-instructions.md`
* Guide Copilot to generate **consistent, secure, and standards-aligned code**
* Apply instructions for **backend** and **frontend** scenarios


---

## What Is a Copilot Instructions File?

A **Copilot Instructions file** allows teams to define **project-wide guidance** for GitHub Copilot.

Copilot uses this file to understand:

* Coding standards
* Architectural patterns
* Security and compliance rules
* Naming conventions
* Testing expectations

📍 Location:

```
.github/copilot-instructions.md
```

---

# LAB 1: Creating the Copilot Instructions File

## Step 1: Create Folder Structure

Inside your repository root:

```
.github/
  copilot-instructions.md
```

---

## Step 2: Basic Instructions Template

Add the following content:

```md
# GitHub Copilot Instructions

## General Guidelines
- Generate clean, readable, production-ready code
- Follow SOLID principles
- Avoid hard-coded values
- Prefer configuration-driven logic

## Code Style
- Use meaningful variable and function names
- Follow language-specific best practices
- Add comments only where business logic exists

## Error Handling
- Handle all edge cases
- Never suppress exceptions silently
- Return meaningful error messages

## Testing
- Always generate unit-testable code
- Prefer pure functions where possible
```

---

# LAB 2: Backend-Specific Instructions

## Add Backend Rules

```md
## Backend Instructions

### API Design
- Use RESTful conventions
- Validate all request inputs
- Return proper HTTP status codes

### Security
- Do not expose sensitive data
- Sanitize user inputs
- Follow OWASP best practices

### Logging
- Log errors and critical business events
- Do not log PII or secrets

### Performance
- Avoid unnecessary database calls
- Prefer pagination for list APIs
```

---

## Backend Hands-on Task

### Task

Create an API to fetch orders by customer ID.

### Prompt (No Extra Context Needed)

```java
Create a GET API to fetch orders by customerId
```

### Expected Outcome

* Input validation
* REST-compliant endpoint
* Secure and clean code
* Error handling included automatically

---

# LAB 3: Frontend-Specific Instructions

## Add Frontend Rules

```md
## Frontend Instructions

### UI Components
- Create reusable components
- Use props for configuration
- Avoid inline styles

### State Management
- Handle loading, success, and error states
- Avoid unnecessary re-renders

### Accessibility
- Follow basic accessibility guidelines (ARIA, labels)
- Ensure keyboard navigation support

### UX
- Display user-friendly error messages
- Disable actions during async operations
```

---

## Frontend Hands-on Task

### Task

Create a form submit button.

### Prompt

```jsx
Create a submit button component
```

### Expected Outcome

* Disabled state during API call
* Accessible markup
* Reusable component design

---

# LAB 4: QA / Testing Instructions

## Add Testing Rules

```md
## Testing Instructions

- Generate unit tests alongside production code
- Prefer deterministic, data-driven tests
- Avoid hard-coded assertions
- Use descriptive test names

## Test Coverage
- Cover happy paths and edge cases
- Validate business rules, not static values
```

---

## Testing Hands-on Task

### Task

Generate unit tests for fee calculation logic.

### Prompt

```python
Generate unit tests for fee calculation logic
```

### Expected Outcome

* Formula-based assertions
* Edge case coverage
* Readable test structure

---

# LAB 5: Advanced Instructions (Enterprise Use)

## Add Enterprise Constraints

```md
## Enterprise Constraints

- Follow internal coding standards
- Ensure compliance with data protection regulations
- Do not generate mock credentials or secrets
- Prefer dependency injection
```

---

## Scenario: Regulated Environment

### Task

Generate code in a compliance-heavy environment.

### Prompt

```text
Implement user profile update API
```


---

## Key Takeaways

* Copilot Instructions act as **persistent context**
* Reduces repetitive prompting
* Improves consistency, security, and quality
* Essential for enterprise and team-scale adoption

---

**End of Lab**
