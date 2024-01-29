# Clean Architecture Cheat Sheet

A quick reference guide to the principles of Clean Architecture, ensuring maintainable and scalable software design.

## Overview

- **Objective**: Separate concerns by dividing the software into layers.
- **Independent of Frameworks**: The architecture does not depend on the existence of some library or framework.
- **Testable**: Business rules can be tested without the UI, database, web server, or any external element.

## Layers

### 1. Entities
- Represent the business objects of the application.
- Plain Kotlin/Java classes (in the context of Android/Java development).

### 2. Use Cases
- Contain application-specific business rules.
- Orchestrate the flow of data to and from the entities.
- Are independent of UI, database, and external interfaces.

### 3. Interface Adapters
- Convert data from the format most convenient for use cases and entities, to the format most convenient for external agencies such as databases or the web.
- Include presenters, views, and controllers.

### 4. Frameworks and Drivers
- The outermost layer consisting of frameworks and tools such as the Database, the Web Framework, etc.
- Generally composed of frameworks/libraries that provide low-level details (like UI frameworks, database access libraries, etc.).

## Dependency Rule
- Source code dependencies only point inwards.
- Nothing in an inner circle can know anything at all about something in an outer circle.

## Principles

- **Single Responsibility Principle (SRP)**: A class should have only one reason to change.
- **Open/Closed Principle (OCP)**: Software entities should be open for extension, but closed for modification.
- **Liskov Substitution Principle (LSP)**: Objects in a program should be replaceable with instances of their subtypes without altering the correctness of the program.
- **Interface Segregation Principle (ISP)**: Many client-specific interfaces are better than one general-purpose interface.
- **Dependency Inversion Principle (DIP)**: Depend upon abstractions, not concretions.

## Benefits

- Easy to understand and maintain.
- Flexibility and future-proofing.
- Business logic and application can be tested independently of external elements.

## Tips

- Keep code at a level within its layer.
- Don’t skip layers - jumping from entities directly to frameworks, for example, violates the Clean Architecture.
- Follow the Dependency Rule rigorously.

This cheat sheet provides a quick overview of Clean Architecture. For a comprehensive understanding, consider reading Robert C. Martin's book on Clean Architecture.
