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
  - [Event-Driven Architecture](#event-driven-architecture)
- [Conclusion](#conclusion)

## Introduction

Software architectures in .NET define how code is structured to promote **maintainability, testability, and scalability**. This guide covers six widely used architectures:

- **Clean Architecture** – Domain-centric with independent layers.
- **Onion Architecture** – Layered with dependencies pointing inward.
- **Hexagonal Architecture** – Isolates core logic via ports and adapters.
- **Layered Architecture** – Traditional stacked layers.
- **Three-Tier Architecture** – Physically separates UI, logic, and data.
- **Event-Driven Architecture** – Centers on events to trigger and coordinate processes.

Each architecture integrates key components like **Unit of Work, Generic Repository, Services, External Services, Specification, and CQRS** to enhance functionality and maintainability.

## Architectures

### Clean Architecture
**Overview:**  
Clean Architecture focuses on a domain-driven design, isolating core business logic from external systems. It uses dependency inversion to ensure high testability and maintainability.

**Key Principles:**
- Separation into distinct layers: Domain, Application, Infrastructure, and Presentation.
- Utilizes dependency injection and interfaces for decoupling.
- Supports patterns like **CQRS** for clear separation between command and query operations.

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
- **Inward Dependency Flow:** Outer layers depend on inner layers only.
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
Also known as Ports and Adapters Architecture, this style isolates core business logic from external systems through well-defined ports (interfaces) and adapters (implementations).

**Key Concepts:**
- **Ports:** Define how external systems interact with the application.
- **Adapters:** Implement these interfaces to connect with external services like databases or APIs.
- Encourages modularity and ease of replacing external components.

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
This traditional approach organizes the system into layers such as Presentation, Business Logic, and Data Access, each with distinct responsibilities.

**Characteristics:**
- Clear separation of concerns.
- Common in enterprise applications.
- Requires careful design to prevent tight coupling between layers.

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
A variation of layered architecture that physically separates the system into three tiers: user interface, business logic, and data storage. This separation can improve scalability and manageability.

**Components:**
- **Presentation Tier:** Handles the user interface (e.g., web or desktop UI).
- **Business Logic Tier:** Contains application logic and services.
- **Data Tier:** Manages data storage (e.g., SQL Server, MongoDB).

**Example Structure:**
```
MySolution/
├── ClientApp/   # Frontend
├── API/         # Backend
└── Database/    # Data storage
```

---

### Event-Driven Architecture
**Overview:**  
Event-Driven Architecture centers around the production, detection, and consumption of events. It allows systems to respond to real-time events, decoupling the event producers from the consumers.

**Key Concepts:**
- **Event Producers:** Components that generate events when something significant occurs.
- **Event Consumers:** Components that subscribe to and process events.
- **Event Bus/Message Broker:** Facilitates the transmission of events between producers and consumers (e.g., using tools like RabbitMQ, Kafka, or Azure Event Grid).

**Benefits:**
- Promotes high scalability and responsiveness.
- Allows asynchronous communication between services.
- Enhances decoupling, making the system more resilient and flexible.

**Example Workflow:**
```
[User Action] --> [Event Producer] --> [Message Broker] --> [Event Consumer] --> [Business Logic Execution]
```

---

## Conclusion

Each .NET architecture serves a unique purpose based on your project's size, complexity, and maintainability needs:

- **Clean & Onion Architectures:** Ideal for enterprise-level applications with a strong domain focus.
- **Hexagonal Architecture:** Best for systems that require high modularity and ease of replacing external components.
- **Layered & Three-Tier Architectures:** Suitable for traditional applications needing clear separation of concerns.
- **Event-Driven Architecture:** Excellent for building responsive, decoupled, and scalable systems that react to real-time events.

Feel free to contribute by opening a Pull Request or suggesting improvements. Happy coding!
