# GitHub Copilot Advanced Lab – Using /create-agent, Hooks, Skills & Custom Instructions in .NET

## Lab Title

**Building an Intelligent .NET API using GitHub Copilot Agents, Hooks, Skills, and Custom Instructions**

## Duration

60–90 minutes

## Target Audience

Developers, DevOps Engineers, SDETs, Tech Leads

---

## Lab Objectives

By the end of this lab, you will:

* Create a .NET Web API project
* Configure **Copilot Custom Instructions**
* Create and use **/create-agent**
* Implement **/hooks** for lifecycle automation
* Create reusable **/skills**
* Understand differences between Instructions, Agents, and Skills

---

## 🔍 Conceptual Understanding (IMPORTANT)

Before starting, understand how these components differ:

### 1. Copilot Instructions

**What it is:**
Project-level guidance for Copilot.

**Scope:**

* Global (applies to entire repo)

**Purpose:**

* Define coding standards
* Control style and architecture

**Example:**

```markdown
Use clean architecture
Use dependency injection
Return IActionResult
```

**Key Point:**
👉 Instructions guide *how code should be written*

---

### 2. Custom Agent (/create-agent)

**What it is:**
An intelligent AI persona that performs tasks.

**Scope:**

* Task execution
* Multi-step reasoning

**Purpose:**

* Generate APIs
* Refactor code
* Add features

**Example:**

```bash
/create-agent .NET API Developer Agent
```

**Key Point:**
👉 Agent decides *what to do and executes tasks*

---

### 3. Skills

**What it is:**
Reusable capabilities that agents can invoke.

**Scope:**

* Specific functionality

**Purpose:**

* Generate API boilerplate
* Add middleware
* Apply patterns

**Example:**

```bash
/skills api-generator create API
```

**Key Point:**
👉 Skills define *how a specific task is performed*

---

### 🔁 Relationship Summary

| Component    | Role  | Scope         | Analogy                   |
| ------------ | ----- | ------------- | ------------------------- |
| Instructions | Rules | Global        | Coding standards document |
| Agent        | Brain | Task-level    | Developer                 |
| Skills       | Tools | Specific task | Libraries / utilities     |

---

## Prerequisites

* .NET 8 SDK installed
* VS Code or Visual Studio with GitHub Copilot enabled
* GitHub account with Copilot access

---

## Step 1: Create .NET Web API Project

```bash
dotnet new webapi -n CopilotAdvancedLab
cd CopilotAdvancedLab
code .
```

---

## Step 2: Add Copilot Custom Instructions

Create file:

```bash
.github/copilot-instructions.md
```

### Add Content

```markdown
# Copilot Instructions for This Project

## Project Overview
This is a .NET 8 Web API for managing training sessions.

## Coding Guidelines
- Use clean architecture principles
- Use dependency injection
- Follow RESTful API standards
- Use async/await

## Logging & Validation
- Add structured logging
- Validate inputs

## Testing
- Use xUnit and Moq
```

---

## Step 3: Create an Agent

```bash
/create-agent .NET API Developer Agent that:
- Generates Models, Services, Controllers
- Follows project instructions
- Adds logging, validation
- Suggests unit tests
```

---

## Step 4: Generate API using Agent

```bash
@.NET API Developer Agent create Training API with CRUD operations
```

---

## Step 5: Create a Skill

```bash
.copilot/skills/api-generator.md
```

```markdown
# Skill: API Generator

## Description
Generates REST API components.

## Inputs
- Entity
- Fields

## Output
- Model
- Service
- Controller
```

---

## Step 6: Use Skill via Agent

```bash
@.NET API Developer Agent use api-generator to create Course API
```

---

## Step 7: Add Hooks

### Pre Tool Use

```bash
.copilot/hooks/preToolUse.md
```

```markdown
Prevent modification of critical files like Program.cs
```

---

### Post Tool Use

```bash
.copilot/hooks/postToolUse.md
```

```markdown
Suggest logging and unit tests after code generation
```

---

## Step 8: Enhance Code

```bash
@.NET API Developer Agent enhance TrainingService with logging and validation
```

---

## Step 9: Generate Unit Tests

```bash
@.NET API Developer Agent generate unit tests using xUnit and Moq
```

---

## Step 10: Run Application

```bash
dotnet run
```

---

## Reflection Questions

* When should you use Instructions vs Agent?
* Why are Skills reusable across projects?
* How do hooks improve governance?

---

## Summary

| Feature       | Purpose                       |
| ------------- | ----------------------------- |
| Instructions  | Define coding standards       |
| /create-agent | Execute intelligent workflows |
| Skills        | Reusable capabilities         |
| Hooks         | Governance & automation       |

---

## Final Takeaway

👉 Instructions = Rules
👉 Agent = Brain
👉 Skills = Tools
👉 Hooks = Guardrails

---

**End of Lab**
