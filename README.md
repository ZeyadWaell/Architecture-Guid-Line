````markdown
# .NET Software Architectures Guide

Welcome to the **.NET Software Architectures Guide** repository! This guide covers multiple architectural styles used in .NET development to promote **maintainability, testability, and scalability**.

## Table of Contents
- [Introduction](#introduction)
- [Architectures](#architectures)
  - [Clean Architecture](#clean-architecture)
  - [Onion Architecture](#onion-architecture)
  - [Hexagonal Architecture (Ports & Adapters)](#hexagonal-architecture-ports--adapters)
  - [Layered Architecture](#layered-architecture)
  - [Three-Tier Architecture](#three-tier-architecture)
- [Conclusion](#conclusion)

## Introduction

Software architectures in .NET define how code is structured to promote **maintainability, testability, and scalability**. This guide covers five widely used architectures:

- **Clean Architecture** – Domain-centric with independent layers.
- **Onion Architecture** – Layered with dependencies pointing inward.
- **Hexagonal Architecture** – Isolates core logic via ports and adapters.
- **Layered Architecture** – Traditional stacked layers.
- **Three-Tier Architecture** – Physically separates UI, logic, and data.

Each architecture integrates key components like **Unit of Work, Generic Repository, Services, External Services, Specification, and CQRS** to enhance functionality and maintainability.

## Architectures

### Clean Architecture
**Overview:**  
Clean Architecture focuses on a domain-driven design, where the core business logic is isolated from external systems. It uses dependency inversion to ensure high testability and maintainability.

**Key Principles:**
- Separation into distinct layers: Domain, Application, Infrastructure, and Presentation.
- Utilizes dependency injection and interfaces for decoupling.
- Supports patterns like **CQRS** for command and query separation.

**Example Folder Structure:**
```
MyProject/
├── Application/
├── Domain/
├── Infrastructure/
└── Presentation/
```

---

### Onion Architecture
**Overview:**  
Onion Architecture enforces a strict separation of concerns by ensuring that dependencies flow inward, keeping the core domain independent of external layers.

**Core Features:**
- **Inward dependency flow:** Outer layers depend on inner layers.
- Promotes loose coupling and high testability.
- Centers on domain models as the core of the application.

**Example Structure:**
```
MyProject/
├── Core/
├── Application/
├── Infrastructure/
└── UI/
```

---

### Hexagonal Architecture (Ports & Adapters)
**Overview:**  
Also known as Ports and Adapters Architecture, this style isolates core business logic from external systems by using well-defined ports (interfaces) and adapters (implementations).

**Key Concepts:**
- **Ports:** Define how external systems interact with your application.
- **Adapters:** Implement these interfaces to connect with external systems.
- Promotes modularity and ease of component replacement.

**Example Structure:**
```
MyProject/
├── Core/
├── Adapters/
├── Ports/
└── Infrastructure/
```

---

### Layered Architecture
**Overview:**  
This is the traditional approach, organizing the system into layers such as Presentation, Business Logic, and Data Access.

**Characteristics:**
- Clear separation of concerns.
- Commonly used in enterprise applications.
- Requires careful design to avoid tight coupling between layers.

**Example Structure:**
```
MyProject/
├── UI/
├── BusinessLogic/
└── DataAccess/
```

---

### Three-Tier Architecture
**Overview:**  
A variation of the layered architecture that physically separates the system into three tiers: user interface, business logic, and data storage.

**Components:**
- **Presentation Tier:** Handles the user interface (e.g., web or desktop UI).
- **Business Logic Tier:** Contains the application logic and services.
- **Data Tier:** Manages data storage (e.g., SQL Server, MongoDB).

**Example Structure:**
```
MySolution/
├── ClientApp/   # Frontend
├── API/         # Backend
└── Database/    # Data storage
```

---

## Conclusion

Each .NET architecture serves a unique purpose depending on your project's size, complexity, and maintainability needs:

- **Clean & Onion Architectures:** Ideal for enterprise-level applications.
- **Hexagonal Architecture:** Best for systems requiring high modularity and testability.
- **Layered & Three-Tier Architectures:** Suitable for traditional application development.

Feel free to contribute by opening a Pull Request or suggesting improvements. Happy coding!
