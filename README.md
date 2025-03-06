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
