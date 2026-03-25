# **GitHub Copilot Lab — React UI Toolkit (Frontend Only)**

## **Objective**

This lab focuses on building a **frontend-only React UI application** using GitHub Copilot, covering:

* Reusable UI components
* UI toolkit usage (Material UI / Tailwind)
* State management (local state only)
* UI interactions (search, modal, forms)
* Copilot Instructions for consistent frontend code

> ⚠️ No backend or API integration is used in this lab.

---

## **Prerequisites**

* Node.js (LTS)
* Visual Studio Code
* GitHub Copilot (Chat + Inline enabled)
* Basic React knowledge

---

# **SECTION 0 — Project Setup**

---

## **Step 1: Create React App**

```bash id="8w8r6q"
npx create-react-app copilot-react-ui
cd copilot-react-ui
npm start
```

---

## **Step 2: Install UI Toolkit**

### Option 1: Material UI

```bash id="rqm5rw"
npm install @mui/material @emotion/react @emotion/styled
```

### Option 2: Tailwind CSS

```bash id="mt3eqh"
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

---

## **Step 3: Create Folder Structure**

```text id="nt2t6v"
src/
│
├── components/
├── pages/
├── hooks/
├── utils/
├── data/
└── styles/
```

---

## **Step 4: Create Required Files**

```text id="n9k3nh"
components/
 ├── Button.js
 ├── Card.js
 ├── Navbar.js
 ├── Modal.js
 └── Input.js

pages/
 └── Home.js

data/
 └── users.js

styles/
 └── theme.js

.github/
 └── copilot-instructions.md
```

---

# **SECTION 1 — Copilot Instructions Setup**

---

## **Step 1: Create Instructions File**

```bash id="g4r8fh"
.github/copilot-instructions.md
```

---

## **Step 2: Add Instructions**

```md id="fq4d5h"
# Copilot Instructions for React Frontend

## Framework
- Use React functional components
- Use hooks (useState, useEffect)

## Styling
- Use Material UI or Tailwind CSS
- Maintain consistent spacing and layout

## Component Design
- Build reusable and small components
- Use props for customization

## State Management
- Use local state only (no backend)
- Keep state simple and minimal

## UI Behavior
- Handle loading, empty, and error states (UI only)
- Provide responsive design

## Naming Conventions
- PascalCase for components
- camelCase for variables

## Code Quality
- Keep JSX clean
- Avoid complex logic inside UI

## Testing
- Use React Testing Library
```

---

## **Step 3: Validate Instructions**

### Prompt (Copilot Chat)

```text id="zt3qz8"
Create a reusable Input component with label and validation using copilot-instructions.md
```

---

# **SECTION 2 — Static Data (Frontend Only)**

---

## **Step: Create Local Data**

Open `src/data/users.js`

```javascript id="1ytg1s"
// Create a static array of users with id, name, email, role
```

---

# **SECTION 3 — Build Reusable Components**

---

## **Task 1: Button Component**

```javascript id="eqz9ci"
// Create a reusable Button component with props: label, onClick, variant
```

---

## **Task 2: Card Component**

```javascript id="21n0sd"
// Create a Card component to display user details
```

---

## **Task 3: Navbar**

```javascript id="avxr9y"
// Create a responsive Navbar with title and menu
```

---

## **Task 4: Input Component**

```javascript id="jnd8t6"
// Create an Input component with label and validation message
```

---

## **Task 5: Modal Component**

```javascript id="1ayrbb"
// Create a modal to display detailed user information
```

---

# **SECTION 4 — Build Home Page**

---

## **Task 1: Display Users**

Open `pages/Home.js`

```javascript id="6gn40s"
// Display list of users using Card component
```

---

## **Task 2: Add Search Feature**

```javascript id="sg7g3x"
// Add search input to filter users by name (case-insensitive)
```

---

## **Task 3: Add Modal Interaction**

```javascript id="ptz9iq"
// Open modal when a card is clicked and show user details
```

---

# **SECTION 5 — UI Enhancements (Inline Chat)**

---

## **Task 1: Improve Design**

Select code → `Ctrl + I`

### Prompt

```text id="0h56w9"
Improve UI with spacing, responsive grid layout, and better typography
```

---

## **Task 2: Empty State**

```text id="g3skqz"
Add empty state UI when no users match search
```

---

## **Task 3: Loading Skeleton (Simulated)**

```text id="xajb6y"
Add loading skeleton UI using timeout simulation
```

---

# **SECTION 6 — Comments to Code**

---

## **Task 1: Add Form**

```javascript id="lgw7yw"
// Create a form to add a new user to local state with validation
```

---

## **Task 2: Add Delete Feature**

```javascript id="shwz9c"
// Add delete button to remove user from UI state
```

---

# **SECTION 7 — State Management (Frontend Only)**

---

## **Task**

```javascript id="5j1xyj"
// Manage users state in Home component using useState
// Handle add, delete, and search
```

---

# **SECTION 8 — Testing (Frontend)**

---

## **Step 1: Create Test File**

```text id="ry0nfa"
components/Button.test.js
```

---

## **Step 2: Generate Tests**

```javascript id="5f8s9d"
// Test Button renders correctly
// Test click event triggers function
```

---

## **Step 3: Test Search Functionality**

```javascript id="8l4h1g"
// Test filtering users based on input value
```

---

# **SECTION 9 — Challenge Exercise**

---

## **Build Feature: User Dashboard**

### Requirements:

* Display user list
* Search users
* Add new user
* Delete user
* View user details in modal

---

### Constraints:

* No backend
* Use local state only
* Follow Copilot Instructions
* Use reusable components

---

# **Key Takeaways**

* Frontend can be fully developed without backend
* Copilot accelerates UI creation
* Reusable components improve scalability
* Instructions file ensures consistency

---

# **Summary**

You built a **complete frontend React UI application** using:

* Component-based architecture
* Local state management
* UI toolkit (MUI / Tailwind)
* Copilot features (Chat, Inline, Comments-to-Code)
* Copilot Instructions

This enables **fast, scalable frontend development without backend dependency** 🚀

---
