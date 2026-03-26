# GitHub Copilot Lab – Pull Request Summary & Code Review

## Lab Title

**Using GitHub Copilot for Pull Request (PR) Summary and Code Review**



## Prerequisites

* Azure repository with at least one open Pull Request
* GitHub Copilot enabled (IDE or GitHub UI with Copilot Chat)
* Basic understanding of Azure Pull Request workflow

---

## Learning Objectives

By the end of this lab, participants will be able to:

* Use GitHub Copilot to generate **clear PR summaries**
* Perform **AI-assisted code reviews**
* Identify code quality, security, and performance risks
* Provide actionable review comments
* Improve review speed without compromising quality

---

## Why Use GitHub Copilot for PR Reviews?

Traditional PR reviews are often:

* Time-consuming
* Inconsistent across reviewers
* Focused on syntax instead of intent

GitHub Copilot helps by:

* Summarizing changes quickly
* Highlighting potential risks
* Enforcing coding standards
* Acting as a "second reviewer"

---

# LAB 1: PR Summary Generation

## Objective

Generate a concise and meaningful Pull Request summary using Copilot.

---

## Step 1: Open the Pull Request

* Navigate to an open PR in Azure Repo
* Open **GitHub Copilot Chat** (or IDE Copilot Chat)

---

## Step 2: Generate PR Summary

### Prompt

```
Summarize the changes in this pull request
```

### Expected Output

* High-level description of changes
* Files/modules impacted
* Purpose of the PR

---

## Step 3: Improve the Summary

### Prompt (More Structured)

```
Create a PR summary including:
- What was changed
- Why the change was needed
- Impacted modules
- Any risks or assumptions
```

### Expected Outcome

* Ready-to-use PR description
* Clear context for reviewers

---

# LAB 2: Functional Code Review

## Objective

Use Copilot to validate correctness and logic.

---

### Prompt

```
Review this pull request for functional correctness
```

### Follow-up Prompts

```
Are there any logical bugs or edge cases?
```

```
Does this code handle nulls, errors, and invalid inputs?
```

### Expected Outcome

* Identification of logical gaps
* Suggestions for safer handling

---

# LAB 3: Code Quality & Maintainability Review

## Objective

Ensure code is clean, readable, and maintainable.

---

### Prompt

```
Review this PR for code quality and maintainability issues
```

### Follow-up Prompts

```
Are there any violations of clean code or SOLID principles?
```

```
Suggest refactoring opportunities to reduce complexity
```

### Expected Outcome

* Naming improvements
* Reduced complexity suggestions
* Modularization recommendations

---

# LAB 4: Security Review

## Objective

Identify potential security vulnerabilities early.

---

### Prompt

```
Review this pull request for security vulnerabilities
```

### Follow-up Prompts

```
Are there any OWASP Top 10 concerns?
```

```
Is any sensitive data exposed in logs or responses?
```

### Expected Outcome

* Input validation gaps
* Data exposure risks
* Authentication/authorization concerns

---

# LAB 5: Performance Review

## Objective

Detect performance bottlenecks before merge.

---

### Prompt

```
Review this PR for potential performance issues
```

### Follow-up Prompts

```
Are there unnecessary loops, API calls, or database queries?
```

```
Suggest optimizations for scalability
```

### Expected Outcome

* Performance improvement suggestions
* Scalability considerations

---

# LAB 6: Test Coverage Review

## Objective

Validate testing completeness.

---

### Prompt

```
Review this PR for test coverage gaps
```

### Follow-up Prompts

```
Are critical business rules covered by tests?
```

```
Suggest additional unit or integration tests
```

### Expected Outcome

* Missing test scenarios identified
* Better test completeness

---

# LAB 7: Reviewer Comment Generation

## Objective

Generate professional, actionable PR comments.

---

### Prompt

```
Generate concise and constructive review comments for this PR
```

### Alternative Prompt (Strict Review)

```
Generate strict review comments highlighting must-fix issues only
```

### Expected Outcome

* Clear, respectful feedback
* Actionable comments ready to post

---

# LAB 8: Approval Recommendation

## Objective

Decide merge readiness.

---

### Prompt

```
Based on the review, should this PR be approved, needs changes, or blocked? Explain why.
```

### Expected Outcome

* Merge recommendation
* Justification for decision

---

# Best Practices

* Use Copilot as an **assistant**, not the sole reviewer
* Combine AI review with human judgment
* Ask focused follow-up questions
* Use Copilot consistently to standardize reviews

---

# Lab Completion Checklist

* [ ] PR summary generated
* [ ] Functional review completed
* [ ] Code quality reviewed
* [ ] Security review performed
* [ ] Performance considerations checked
* [ ] Test gaps identified
* [ ] Review comments generated

---

## Key Takeaways

* Copilot accelerates PR understanding
* Improves review consistency
* Helps catch issues early
* Enhances reviewer productivity

---

**End of Lab**
