# 💻 Serverest API Testing with Postman

This repository contains a **Postman Collection** for automated testing of the [ServeRest API](https://serverest.dev/). The project aims to demonstrate robust API testing practices using Postman's powerful features for request organization, environment management, and script-based assertions.

---

## 🧱 Project Structure

```
Serverest-API/
├── ServeRest Dev.postman_environment.json  # Postman Environment for development
├── ServeRest.postman_collection.json       # Main Postman Collection for ServeRest API tests
└── README.md
```

---

## 🎯 Key Practices and Patterns

### 📌 Postman Collections

-   The `ServeRest.postman_collection.json` file organizes all API requests into logical folders, mirroring the ServeRest API's structure (e.g., Login, Users, Products, Carts).
-   **Goal:** Group related requests, define common authorization methods, and share variables across requests within the collection.

### 📌 Postman Environments

-   The `ServeRest Dev.postman_environment.json` file stores environment-specific variables, such as the base URL of the ServeRest API.
-   **Goal:** Enable easy switching between different environments (e.g., development, staging, production) without modifying individual requests.

### 📌 Pre-request and Test Scripts

-   **Pre-request Scripts:** Used for setting up test data, generating dynamic values (e.g., unique user emails), or handling authentication before a request is sent.
-   **Test Scripts:** Executed after a request receives a response, these scripts contain assertions to validate the response status, data, and structure. They are crucial for automated verification of API behavior.

### 📌 Data-Driven Testing (DDT) with Postman

-   Postman allows for data-driven testing by importing external data files (CSV or JSON) to run the same collection or folder multiple times with different data sets.
-   **Goal:** Efficiently test various scenarios and edge cases without duplicating requests, ensuring comprehensive coverage.

---

### 💡 Best Practices Applied

| Practice | Description |
|----------|-------------|
| **DRY** (Don't Repeat Yourself) | Environment variables and collection-level scripts are reused across multiple requests. |
| **Modularity** | Requests are organized into folders within the collection, reflecting API endpoints. |
| **Readability** | Test scripts are focused and clearly assert expected outcomes. |
| **Maintainability** | Centralized environment variables and structured collections simplify updates and debugging. |

---

### 🚀 Running the Tests

To run this Postman collection, follow these steps:

1.  **Install Postman:** If you don't have Postman installed, download it from the [official Postman website](https://www.postman.com/downloads/).
2.  **Import Collection and Environment:**
    *   Open Postman.
    *   Click on `File > Import`.
    *   Select both `ServeRest.postman_collection.json` and `ServeRest Dev.postman_environment.json` from this repository.
3.  **Select Environment:** In the top-right corner of Postman, select `ServeRest Dev` from the environment dropdown.
4.  **Run Collection:**
    *   In the left sidebar, navigate to `Collections`.
    *   Hover over the `ServeRest` collection and click on the `...` (more actions) icon.
    *   Select `Run collection`.
    *   In the Collection Runner, you can choose to run all requests or specific folders. Click `Run ServeRest` to start the tests.

---

### 🔧 Tools Used

*   **Postman**: For API request management, testing, and automation.
*   **ServeRest API**: The target API for testing, providing a simulated e-commerce backend.

---

### 📌 Notes

-   The Postman collection includes requests for user registration, login, product management, and shopping cart operations.
-   Pre-request scripts are utilized for dynamic data generation (e.g., unique email addresses for user registration) and token management for authenticated requests.
-   Test scripts include assertions for status codes, response body content, and data validation.
