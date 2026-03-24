
## Lab Title

**Improving Code Readability, Maintainability, and Modularity with GitHub Copilot Chat**

## Repository

Clone URL: [https://github.com/akkki98/ImproveCodeQualiy.git](https://github.com/akkki98/ImproveCodeQualiy.git)

---

## Target Audience

Developers, Junior–Senior Engineers, QA/SDETs, Tech Leads


## Learning Objectives

By completing this challenge, participants will be able to:

* Use **GitHub Copilot Chat** to analyze existing code
* Improve **readability** by clarifying intent and structure
* Improve **maintainability** by reducing complexity and duplication
* Improve **modularity** by refactoring code into logical units
* Ask the *right prompts* to guide Copilot effectively

---

## Step 1: Clone the Repository

```bash
git clone https://github.com/akkki98/ImproveCodeQualiy.git
cd ImproveCodeQualiy
```

Open the project in **VS Code**.

---

## Step 2: Understand the Existing Code

1. Browse through the source files
2. Identify code smells such as:

   * Long methods
   * Poor naming
   * Nested conditionals
   * Duplicated logic
   * Mixed responsibilities

> ⚠️ Do **not** refactor manually yet. Use Copilot Chat first.

---

# LAB 1: Improving Code Readability

## Objective

Make the code easier to read and understand without changing behavior.

---

## Instructions

1. Select a block of code (method or class)
2. Open **GitHub Copilot Chat**
3. Use the following prompt

### Prompt

```text
@workspace /explain How can I improve the readability of the selected code?
```

### What Copilot Will Suggest

* Better variable and method names
* Simplified conditional logic
* Improved formatting
* Inline comments for complex logic

### Apply

* Apply suggestions incrementally
* Re-run the prompt if needed

---

# LAB 2: Improving Code Maintainability

## Objective

Ensure the code is easy to modify and extend in the future.

---

## Instructions

1. Select the same or another code block
2. Open Copilot Chat

### Prompt

```text
@workspace /explain #selection How can I improve the maintainability of the selected code?
```

### What Copilot Will Suggest

* Reducing duplication
* Extracting constants
* Applying single-responsibility principle
* Improving error handling

### Apply

* Refactor one suggestion at a time
* Validate logic remains unchanged

---

# LAB 3: Improving Code Modularity (Analysis)

## Objective

Understand how to break code into smaller, reusable units.

---

## Instructions

1. Select a large function or class
2. Open Copilot Chat

### Prompt

```text
@workspace /explain How can I improve the modularity of the selected code?
```

### What Copilot Will Suggest

* Extracting helper methods
* Splitting classes by responsibility
* Creating reusable utilities

---

# LAB 4: Refactoring for Modularity (Action)

## Objective

Actively refactor code based on modularity suggestions.

---

## Instructions

1. Select the same code block
2. Use the following prompt

### Prompt

```text
#selection How can I refactor the selected code to improve modularity?
```

### Expected Changes

* Smaller, focused functions
* Clear separation of concerns
* Reusable components or services

---

# LAB 5: Simplifying Complex Code

## Objective

Reduce unnecessary complexity while preserving functionality.

---

## Instructions

1. Select complex or deeply nested code
2. Open Copilot Chat

### Prompt

```text
@workspace /explain What are some options for simplifying the selected code?
```

### What Copilot Will Suggest

* Guard clauses
* Flattened conditionals
* Early returns
* Removal of redundant logic

---

# Suggested Prompt Variations (Optional)

```text
Explain this code in simple terms
```

```text
Refactor this code to follow clean code principles
```

```text
Identify code smells in the selected code
```

```text
Suggest a cleaner design without changing behavior
```


---

## Key Takeaways

* Copilot Chat is powerful for **code understanding + refactoring guidance**
* High-quality prompts lead to high-quality refactoring
* Use Copilot iteratively, not in one large step
* Always validate logic after refactoring

---


