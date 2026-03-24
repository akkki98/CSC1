# **GitHub Copilot Lab — Ask, Edit & Agent Mode for .NET (ASP.NET Core)**

## **Objective**

This lab teaches how to use GitHub Copilot's **Ask**, **Edit**, and **Agent Mode** features to build and enhance an ASP.NET Core Web API application.

---

## **Prerequisites**

* Visual Studio Code / Visual Studio
* GitHub Copilot enabled (Chat + Agent mode)
* .NET SDK (LTS version, e.g., .NET 8)
* GitHub Copilot Chat extension installed

---

# **SECTION 1 — Using Copilot ASK**

## **Goal:** Learn how to use *Ask* to generate and understand code.

---

### **Task 1: Create a .NET Web API Project**

#### **Prompt (Ask Mode)**

Create an ASP.NET Core Web API project with a health check endpoint `/health` returning `{ status: "ok" }`. Provide the folder structure, commands, and code.

---

### **Task 2: Understand Code**

#### **Prompt (Ask Mode)**

Explain how `app.Run()` and `app.MapGet()` work in ASP.NET Core and how request routing is processed internally.

---

# **SECTION 2 — Using Copilot EDIT**

## **Goal:** Modify existing code using Edit instructions.

---

### **Task 1: Add a Users Endpoint**

#### **Prompt (Edit Mode)**

Add a new endpoint `/users` that returns a list of users from an in-memory collection. Format the response as JSON. Do not modify the existing `/health` endpoint.

---

### **Task 2: Add Request Logging Middleware**

#### **Prompt (Edit Mode)**

Add middleware that logs the HTTP method and URL for every request. Apply it globally.

---

### **Task 3: Generate Unit Tests**

#### **Prompt (Ask/Edit Mode)**

Generate xUnit tests for the `/users` endpoint, including:

* Status code validation
* Response count
* JSON structure validation

---

# **SECTION 3 — Using Copilot AGENT MODE**

## **Goal:** Use Copilot as an autonomous coding agent to perform multi-step tasks.

---

### **Task 1: Refactor Project into Modular Architecture**

#### **Prompt (Agent Mode)**

You are my coding agent. Refactor this ASP.NET Core Web API into a modular architecture with:

* /Controllers
* /Services
* /Models

Move the `/users` logic into:

* UsersController.cs
* UsersService.cs

Update dependency injection and ensure the app runs exactly as before. Explain the changes after refactoring. Begin only after confirming you understand the task.

---

### **Task 2: Add Centralized Error Handling**

#### **Prompt (Agent Mode)**

Add centralized error handling using middleware.

* Implement global exception handling middleware
* Update the UsersService to throw an exception if the user list is empty
* Modify the controller to handle and propagate errors

Ensure API responses return structured JSON:

```json
{
  "status": "error",
  "message": "error message"
}
```

---

### **Task 3: Add Search Feature End-to-End**

#### **Prompt (Agent Mode)**

Add a new endpoint:

```
/users/search?name=
```

Requirements:

* Return users matching the search query
* Implement logic in the service layer
* Update controller and routing
* Add unit tests for search functionality
* Validate functionality using test execution

---

# **Summary**

This lab demonstrates how GitHub Copilot can be used effectively in **Ask**, **Edit**, and **Agent Mode** to accelerate development in ASP.NET Core. It covers project creation, code understanding, refactoring, middleware implementation, error handling, and feature development.
