# **GitHub Copilot Lab — Prompt Engineering Best Practices**

## **Objective**

This lab teaches how to write effective prompts for GitHub Copilot using four key principles:

* **Single** → One clear task
* **Specific** → Clear requirements and constraints
* **Short** → Concise and focused
* **Surround (Context)** → Provide relevant code or context

---

## **Prerequisites**

* Visual Studio Code / Visual Studio
* GitHub Copilot (Chat + Inline enabled)
* Basic knowledge of any programming language (.NET / Node.js preferred)

---

# **SECTION 1 — SINGLE (One Task at a Time)**

## **Goal:** Avoid combining multiple tasks in one prompt

---

### ❌ **Poor Prompt**

```
Create an API, add authentication, connect to database, and write tests
```

### ✅ **Good Prompt**

```
Create a GET endpoint /users in ASP.NET Core that returns a static list
```

---

### **Hands-on Task**

#### Prompt

```
Create a POST endpoint /users that accepts name and email and returns 201 Created
```

👉 Observe how Copilot gives a **clear and focused response**

---

# **SECTION 2 — SPECIFIC (Clear Requirements)**

## **Goal:** Provide detailed and unambiguous instructions

---

### ❌ **Poor Prompt**

```
Create a user API
```

### ✅ **Good Prompt**

```
Create an ASP.NET Core Web API endpoint /users that returns a list of users with id, name, and email in JSON format
```

---

### **Hands-on Task**

#### Prompt

```
Create a PUT endpoint /users/{id} to update user name and email. Return 404 if user not found.
```

👉 Notice better:

* Structure
* Error handling
* Response clarity

---

# **SECTION 3 — SHORT (Concise Prompts)**

## **Goal:** Avoid unnecessary verbosity

---

### ❌ **Poor Prompt**

```
I am building a very large enterprise-grade scalable application and I need you to help me generate a simple API endpoint which should ideally return a list of users in JSON format and should be written in ASP.NET Core with best practices
```

### ✅ **Good Prompt**

```
Create a GET /users endpoint in ASP.NET Core returning JSON list of users
```

---

### **Hands-on Task**

#### Prompt

```
Create a DELETE /users/{id} endpoint with proper status codes
```

👉 Short prompts = faster, cleaner suggestions

---

# **SECTION 4 — SURROUND (Provide Context)**

## **Goal:** Improve output by giving surrounding code

---

### ❌ **Poor Prompt**

```
Add validation
```

### ✅ **Good Prompt (with Context)**

```csharp
public record User(string Name, string Email);

// Add validation to ensure Name and Email are not empty
```

---

### **Hands-on Task**

#### Code + Prompt

```csharp
app.MapPost("/users", (User user) =>
{
    // Add validation and return 400 if invalid
});
```

👉 Copilot uses:

* Existing code
* Types
* Structure


---

# **Summary**

Effective prompt engineering dramatically improves GitHub Copilot output quality. By following these four principles, developers can:

* Reduce ambiguity
* Get accurate code suggestions
* Improve productivity
* Write maintainable code faster

---
