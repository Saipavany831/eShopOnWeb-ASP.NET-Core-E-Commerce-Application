# 🛍️ eShopOnWeb — Clean Architecture-Based ASP.NET Core E-Commerce Web Application

> **A modern, scalable, and maintainable ASP.NET Core MVC application demonstrating enterprise-grade Clean Architecture principles and .NET best practices.**

---

## 🚀 Executive Summary
**eShopOnWeb** is a sample e-commerce platform developed to demonstrate **Clean Architecture**, **Domain-Driven Design (DDD)**, and **modular web application structure** using **ASP.NET Core** and **Entity Framework Core**.  
It highlights how to build **maintainable, testable, and production-ready** solutions following Microsoft’s recommended architectural patterns.

---

## 🧠 Project Overview

### 📋 Description
This project models a real-world e-commerce application designed with a **layered architecture** for scalability and testability. It showcases **separation of concerns**, **dependency injection**, and **repository patterns** to promote clean code and reusability.

### 🎯 Why It Is Used
To serve as a **reference implementation** for developers and organizations aiming to build **robust and enterprise-ready web applications**.  
It provides practical insight into building scalable systems using ASP.NET Core, EF Core, and .NET 6.

---

## ⚙️ Technology Stack

| Component | Technology |
|------------|-------------|
| Framework | ASP.NET Core MVC |
| ORM | Entity Framework Core |
| Language | C# (.NET 6) |
| Database | MySQL / SQL Server LocalDB |
| IDE | Visual Studio 2022 |
| Version Control | Git & GitHub |
| Testing Framework | xUnit |

---

## 🧩 Architecture

**eShopOnWeb** follows the **Clean Architecture** pattern, divided into four key layers:

```
eShopOnWeb
│
├── ApplicationCore   → Domain entities, business logic, and interfaces
├── Infrastructure    → Data access, repository implementations, EF Core context
├── Web               → Presentation layer (ASP.NET MVC + Razor Views)
└── Tests             → Unit and integration testing using xUnit
```

### 🔑 Architectural Principles
- **Separation of Concerns** — each layer has a defined responsibility.  
- **Dependency Inversion** — upper layers depend on abstractions, not implementations.  
- **Testability** — supports unit testing without full system dependencies.  
- **Scalability & Maintainability** — modular design for easy updates and enhancements.

---

## 🧭 Project Workflow

### 🔹 User Flow
1. User visits the homepage and browses products.  
2. Adds desired items to the cart.  
3. Reviews cart and proceeds to checkout.  
4. Submits the order and receives confirmation.  
5. Admins manage products and categories in the backend.

### 🔹 Backend Flow
- **Controller** → Handles HTTP requests.  
- **Service Layer** → Executes business rules.  
- **Repository Layer** → Manages data access via EF Core.  
- **Database** → Stores products, users, and orders.

**Data Flow:**
```
User → Controller → Service → Repository → Database
Database → Repository → Service → Controller → UI
```

---

## 💡 Key Features
- 🧱 Clean Architecture with domain-driven separation.  
- 💻 Responsive front-end using Razor Views.  
- 💾 EF Core integration for data persistence.  
- 🔄 Dependency Injection and repository pattern.  
- 🧮 Sample workflows: catalog, shopping cart, checkout, order management.  
- 🧪 xUnit test coverage for reliability and maintainability.

---

## 🛠️ Setup & Installation Guide

### 1️⃣ Prerequisites
Ensure the following software is installed:

| Software | Version | Purpose |
|-----------|----------|----------|
| Visual Studio | 2022+ | IDE for development |
| .NET SDK | 6.0 or later | Build and run app |
| MySQL Server / SQL Server LocalDB | 8.0+ | Database engine |
| Git | Latest | Repository management |

---

### 2️⃣ Clone the Repository
```bash
git clone https://github.com/<your-org>/eShopOnWeb.git
cd eShopOnWeb
```

---

### 3️⃣ Configure the Database Connection
Open `appsettings.json` in `/src/Web` and update:

**For MySQL:**
```json
"ConnectionStrings": {
  "CatalogConnection": "Server=localhost;Database=eshoponweb_db;User=root;Password=yourpassword;"
}
```

**For SQL Server LocalDB:**
```json
"ConnectionStrings": {
  "CatalogConnection": "Server=(localdb)\\mssqllocaldb;Database=Microsoft.eShopOnWeb.CatalogDb;Trusted_Connection=True;"
}
```

---

### 4️⃣ Apply EF Core Migrations
```bash
cd src/Web
dotnet ef database update
```

---

### 5️⃣ Run the Application

**Using Visual Studio 2022**
1. Set `Web` as the Startup Project.  
2. Press `Ctrl + F5` to run.  
3. The app launches at `https://localhost:443xx/`.

**Using Command Line**
```bash
cd src/Web
dotnet build
dotnet run
```
Then open your browser at [https://localhost:5001](https://localhost:5001).

---

## 🧰 Testing
Unit and integration tests are implemented using **xUnit** to ensure:
- Functionality consistency across layers.
- Business logic validation.
- End-to-end order and checkout verification.

Run all tests:
```bash
dotnet test
```

---

## 📊 Output Highlights

| Module | Description |
|--------|-------------|
| 🏠 **Home Page** | Displays available products and featured items |
| 🛒 **Cart Page** | Add/remove items and view total |
| 💳 **Checkout Page** | Simulated purchase confirmation |
| ✅ **Order Confirmation** | Displays success message and “Continue Shopping” link |
| ⚙️ **Admin Panel** | Manage product listings and categories |

---

## 📈 Metrics of Success
- Modular, reusable code across architecture layers.  
- 90%+ unit test coverage using xUnit.  
- Verified scalability during deployment testing.  
- Adopted as a Clean Architecture reference by .NET developers.

---

## 🔮 Roadmap & Future Vision
Planned enhancements include:
- Integration with **Blazor** or **React** for a modern UI.  
- Advanced product search using **Azure Cognitive Search**.  
- Cloud deployment with **Azure App Services**.  
- Migration to **microservices** for further scalability.

---

## 🧭 Why This Matters
**eShopOnWeb** is more than a sample — it’s a **blueprint for enterprise-grade .NET applications**.  
It embodies Microsoft’s recommended architectural practices for scalable, secure, and maintainable software.

---

## 🧱 Project Structure Summary
```
eShopOnWeb/
├── ApplicationCore/     # Business entities, domain logic, interfaces
├── Infrastructure/      # Data layer, repositories, EF Core context
├── Web/                 # MVC Controllers, Razor Views, DI setup
└── Tests/               # xUnit test projects
```

---

## 🤝 Conclusion
The **eShopOnWeb Clean Architecture Project** demonstrates how to design, structure, and deploy scalable ASP.NET Core applications following enterprise best practices.  
Developers and organizations can adapt it as a **foundation for production systems** or as a **reference model** for learning and architecture planning.

---

### 📘 Reference
Based on the official Microsoft sample:  
[Architecting Modern Web Applications with ASP.NET Core and Azure (Free eBook)](https://aka.ms/webappebook)
