# **GitHub Copilot Lab — Inline Suggestions, Chat & Comments-to-Code for .NET**

## **Objective**

This lab helps you understand and practice GitHub Copilot features in a .NET (ASP.NET Core) environment:

* Inline Suggestions
* Copilot Chat
* Inline Chat
* Comments-to-Code

You will build a simple Web API while leveraging AI-assisted development.

---

## **Prerequisites**

* Visual Studio Code / Visual Studio 2022
* .NET SDK (LTS – .NET 8 recommended)
* GitHub Copilot (enabled)
* GitHub Copilot Chat extension installed

---

# **SECTION 1 — Inline Suggestions**

## **Goal:** Use AI-powered real-time code completions

---

### **Task 1: Create Web API Project**

#### **Steps**

1. Run:

   ```bash
   dotnet new webapi -n CopilotDotNetLab
   cd CopilotDotNetLab
   dotnet run
   ```

2. Open project in VS Code

---

### **Task 2: Generate Model using Inline Suggestions**

#### **Instructions**

Start typing the following and let Copilot complete it:

```csharp
public class User
{
```

#### **Expected Outcome**

Copilot suggests:

* Id
* Name
* Email

Accept suggestions using:

* `Tab` (VS Code)
* `Tab / Enter` (Visual Studio)

---

### **Task 3: Generate Endpoint with Inline Suggestions**

#### **Instructions**

Inside `Program.cs`, type:

```csharp
app.MapGet("/users", () =>
{
```

Let Copilot:

* Suggest list creation
* Return sample users

---

# **SECTION 2 — Copilot Chat**

## **Goal:** Use conversational AI for development

---

### **Task 1: Generate Endpoint via Chat**

#### **Prompt (Copilot Chat)**

Create a GET endpoint `/products` in ASP.NET Core that returns a list of products with id, name, and price.

---

### **Task 2: Explain Code**

#### **Prompt (Copilot Chat)**

Explain how dependency injection works in ASP.NET Core with examples.

---

### **Task 3: Improve Code**

#### **Prompt (Copilot Chat)**

Refactor this endpoint to follow clean code principles and add proper naming conventions.

---

# **SECTION 3 — Inline Chat**

## **Goal:** Perform contextual edits directly in code

---

### **Task 1: Enhance Existing Endpoint**

#### **Instructions**

1. Select the `/users` endpoint code
2. Trigger Inline Chat:

   * VS Code: `Ctrl + I`

#### **Prompt**

Add filtering support to return users based on query parameter `name`.

---

### **Task 2: Add Validation**

#### **Prompt (Inline Chat)**

Add validation to ensure user name is not null or empty. Return appropriate HTTP response.

---

# **SECTION 4 — Comments to Code**

## **Goal:** Convert natural language into working code

---

### **Task 1: Generate POST Endpoint**

#### **Instructions**

Write the following comment:

```csharp
// Create a POST endpoint to add a new user with validation and return 201 Created
```

Let Copilot generate:

* Endpoint logic
* Validation
* Response

---

### **Task 2: Generate Middleware**

#### **Instructions**

```csharp
// Create middleware to log request time, method, and path
```

Let Copilot generate middleware and integrate it.

---

### **Task 3: Generate Service Layer**

#### **Instructions**

```csharp
// Create a UserService class with methods to get all users and add a user
```

---

# **SECTION 5 — Challenge Exercise**

## **Goal:** Combine all Copilot features

---

### **Task**

Build a feature:

### **Requirement**

* Endpoint: `/orders`
* Fields: Id, ProductName, Quantity
* Add GET and POST endpoints
* Add validation
* Add logging

### **Constraints**

* Use:

  * Inline Suggestions for model
  * Comments-to-Code for endpoints
  * Inline Chat for enhancements
  * Copilot Chat for explanations

---

# **Summary**

In this lab, you practiced:

* **Inline Suggestions** → Faster coding with real-time completions
* **Copilot Chat** → Ask, explain, and refactor code
* **Inline Chat** → Context-aware editing
* **Comments-to-Code** → Convert natural language into working code

These features significantly improve productivity and reduce development effort in ASP.NET Core applications.
