# **GitHub Copilot Lab — Building REST APIs with .NET (End-to-End with Structure & Instructions)**

## **Objective**

Build a production-ready ASP.NET Core Web API using GitHub Copilot with:

* REST API generation
* Models, DAL, and Design Patterns
* Error Handling & Security
* Copilot Instructions for consistency
* **Step-by-step folder & file creation**

---

## **Prerequisites**

* Visual Studio Code / Visual Studio 2022
* .NET SDK (.NET 8 recommended)
* GitHub Copilot (Chat + Inline + Agent enabled)

---

# **SECTION 0 — Project Setup**

---

## **Step 1: Create Project**

```bash
dotnet new webapi -n CopilotApiLab
cd CopilotApiLab
code .
```

---

## **Step 2: Clean Default Files**

* Delete:

  * `WeatherForecast.cs`
  * `Controllers/WeatherForecastController.cs`

---

## **Step 3: Create Folder Structure**

Create the following folders:

```text
CopilotApiLab/
│
├── Controllers/
├── Models/
├── Data/
├── Repositories/
├── Services/
├── DTOs/
├── Middleware/
├── Exceptions/
├── Tests/
└── .github/
```

---

## **Step 4: Create Required Files**

Create empty files:

```text
Controllers/
 └── ProductController.cs

Models/
 └── Product.cs

Data/
 └── AppDbContext.cs

Repositories/
 ├── IProductRepository.cs
 └── ProductRepository.cs

Services/
 ├── IProductService.cs
 └── ProductService.cs

DTOs/
 └── ProductDto.cs

Middleware/
 └── ExceptionMiddleware.cs

Exceptions/
 └── NotFoundException.cs

.github/
 └── copilot-instructions.md
```

---

# **SECTION 1 — Copilot Instructions Setup**

---

## **Step 1: Add Instructions File**

Open:

```text
.github/copilot-instructions.md
```

---

## **Step 2: Paste Instructions**

```md
# Copilot Instructions for ASP.NET Core API

## Architecture
- Use Controllers, Services, Repositories
- Follow Clean Architecture

## API Standards
- Use REST conventions
- Return IActionResult
- Use proper HTTP status codes

## Naming
- PascalCase for classes
- camelCase for variables

## Error Handling
- Use global exception middleware
- Return JSON:
  { "status": "error", "message": "details" }

## Security
- Use JWT authentication
- Protect endpoints with [Authorize]

## Validation
- Use Data Annotations

## Logging
- Use ILogger

## Testing
- Use xUnit
```

---

## **Step 3: Validate**

### Prompt (Copilot Chat)

```text
Create ProductController based on copilot-instructions.md
```

---

# **SECTION 2 — Model & DbContext**

---

## **Step 1: Generate Model**

Open `Models/Product.cs`

```csharp
// Create Product model with Id, Name, Price, Category
```

---

## **Step 2: Create DbContext**

Open `Data/AppDbContext.cs`

```csharp
// Create DbContext with DbSet<Product>
```

---

## **Step 3: Register DbContext**

In `Program.cs`:

```csharp
// Add DbContext with SQL Server connection
```

---

# **SECTION 3 — Repository Layer**

---

## **Step 1: Interface**

Open `Repositories/IProductRepository.cs`

```csharp
// Define CRUD operations for Product
```

---

## **Step 2: Implementation**

Open `Repositories/ProductRepository.cs`

```csharp
// Implement repository using EF Core
```

---

# **SECTION 4 — Service Layer**

---

## **Step 1: Interface**

```csharp
// Define business logic methods for Product
```

---

## **Step 2: Implementation**

```csharp
// Implement ProductService using repository and ILogger
```

---

# **SECTION 5 — DTOs**

---

## **Step 1: Create DTO**

Open `DTOs/ProductDto.cs`

```csharp
// Create DTO with Id, Name, Price
```

---

## **Step 2: Mapping**

```csharp
// Map Product to ProductDto in service
```

---

# **SECTION 6 — Controller**

---

## **Step 1: Generate Controller**

Open `Controllers/ProductController.cs`

```csharp
// Create CRUD endpoints using ProductService
```

---

# **SECTION 7 — Dependency Injection**

---

## **Step 1: Register Services**

In `Program.cs`:

```csharp
// Register repository and service
```

---

# **SECTION 8 — Error Handling**

---

## **Step 1: Custom Exception**

Open `Exceptions/NotFoundException.cs`

```csharp
// Create custom exception
```

---

## **Step 2: Middleware**

Open `Middleware/ExceptionMiddleware.cs`

```csharp
// Create global exception handler middleware
```

---

## **Step 3: Register Middleware**

In `Program.cs`:

```csharp
app.UseMiddleware<ExceptionMiddleware>();
```

---

# **SECTION 9 — Security**

---

## **Step 1: Add JWT**

```csharp
// Configure JWT authentication
```

---

## **Step 2: Protect APIs**

```csharp
// Add [Authorize] to POST, PUT, DELETE
```

---

# **SECTION 10 — Testing**

---

## **Step 1: Create Test Project**

```bash
dotnet new xunit -n CopilotApiLab.Tests
dotnet add CopilotApiLab.Tests reference CopilotApiLab
```

---

## **Step 2: Generate Tests**

```csharp
// Create unit tests for ProductService
```

---

# **SECTION 11 — Challenge Exercise**

---

## **Task**

Add **Order module**:

### Steps:

1. Create folders/files:

   * Models/Order.cs
   * Services/OrderService.cs
   * Controllers/OrderController.cs

2. Use Copilot prompts:

```csharp
// Create Order model with Id, ProductId, Quantity, TotalPrice
```

```csharp
// Create CRUD APIs for Order using service layer
```

---

# **Key Takeaways**

* Structured folders improve maintainability
* Copilot Instructions enforce consistency
* Layered architecture = scalable apps
* Security + error handling = production-ready

---

# **Summary**

You have built a **complete enterprise-grade ASP.NET Core API** using:

* GitHub Copilot (Chat, Inline, Comments-to-Code)
* Clean Architecture principles
* Repository & Service patterns
* Error handling & security
* Copilot Instructions for AI governance

---
