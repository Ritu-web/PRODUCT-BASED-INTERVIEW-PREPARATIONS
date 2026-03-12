# Spring Boot Interview Notes

## 1. Tight Coupling vs Loose Coupling
**Tight coupling** is a design situation where one class directly depends on the concrete implementation of another class. Because of this strong dependency, any change in one class can impact the other class, making the system harder to maintain and modify.

**Loose coupling** (not described above) typically means classes depend on abstractions (interfaces) rather than concrete implementations, improving flexibility and maintainability.

---

## 2. Concrete Class vs Abstract Class
- **Concrete class**: A fully implemented class whose objects can be created directly.
- **Abstract class**: An incomplete class that cannot be instantiated and is meant to be extended by other classes.

---

## 3. Why is a Framework Required?
Java provides a lot of features and methods, but when building enterprise-level or business applications, you want to focus on business logic rather than boilerplate code. Frameworks provide basic structure and functionality (e.g., logging, security, batching) so developers can concentrate on implementing business requirements.

---

## 4. What is IoC?
**IoC** stands for *Inversion of Control*. It refers to the design principle where the control of object creation and dependency management is delegated to a container or framework rather than handled directly by the application code.

---

## 5. What is `@SpringBootApplication`?
Using `@SpringBootApplication`:
- Performs auto-configuration
- Starts the IoC container
- Enables component scanning

---

## 6. ApplicationContext vs BeanFactory
*(Question listed but not answered in original notes.)*
- **BeanFactory**: Simple IoC container with lazy loading.
- **ApplicationContext**: Advanced container extending BeanFactory with eager loading and additional features (events, AOP, internationalization).

---

## 7. Types of IoC Containers in Spring Boot
There are two types of IoC containers available in a Spring Boot application:
1. **BeanFactory** (lazy loading)
2. **ApplicationContext** (eager loading)

> Note: Spring Boot primarily uses `ApplicationContext`.

---

## 8. What Does the IoC Container Do?
The IoC container is responsible for:
- Creating beans
- Injecting dependencies
- Managing the lifecycle of beans

### BeanFactory
- Basic IoC container
- Uses lazy loading
- Beans are created only when requested

### ApplicationContext
- Advanced IoC container (extends BeanFactory)
- Uses eager loading
- Provides extra features such as:
  - Event handling
  - AOP
  - Internationalization

### In Spring Boot
ApplicationContext is the primary container. It:
- Creates and manages beans
- Performs dependency injection
- Manages bean lifecycle
- Supports annotations, AOP, and events

---

## 9. Eager Loading vs Lazy Loading
- **Lazy Loading**: The object (bean) is created only when it is requested. This is typical of `BeanFactory`.
- **Eager Loading**: The object is created when the container starts. In `ApplicationContext`, beans are created eagerly by default.

**Quick Interview Answer:**
Eager loading means beans are created when the container starts, while lazy loading means beans are created only when they are requested.





