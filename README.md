**Project Title**

Spring Bean Lifecycle – Core Spring Framework

**Project Description**

This project demonstrates the complete lifecycle of a Spring Bean, from creation to destruction, managed by the Spring IoC container. It explains how Spring initializes beans, injects dependencies, invokes lifecycle callbacks, and cleans up resources when the application context is closed.

**Purpose of the Project**

Understand how Spring manages bean lifecycle

Learn the order of lifecycle callbacks

Demonstrate usage of lifecycle interfaces and annotations

Useful for Spring interviews and real-world debugging

**Technologies Used**

Java

Spring Framework (Core)

Maven

JSR-250 Annotations (@PostConstruct, @PreDestroy)

**Spring Bean Lifecycle Phases**
Spring follows the below sequence while managing a bean:

Bean Instantiation
Spring creates the bean instance using the constructor.

Dependency Injection
Spring injects dependencies into the bean.

Aware Interfaces Execution

BeanNameAware

BeanFactoryAware

ApplicationContextAware

BeanPostProcessor (Before Initialization)

Initialization Phase

@PostConstruct

InitializingBean.afterPropertiesSet()

Custom init method (if configured)

Bean Ready for Use

Destruction Phase

@PreDestroy

DisposableBean.destroy()

Custom destroy method (if configured)

**Lifecycle Interfaces Used
**
BeanNameAware

BeanFactoryAware

ApplicationContextAware

InitializingBean

DisposableBean

These interfaces allow the bean to interact with the Spring container during its lifecycle.

**Lifecycle Annotations Used
**
@PostConstruct
→ Called after dependency injection is complete

@PreDestroy
→ Called before the bean is removed from the container

Note: Annotation-based lifecycle callbacks are preferred over interfaces.

**Application Flow
**
Application context starts

Bean is created and initialized

Lifecycle callback methods are executed in order

Application logic runs

Application context shuts down

Bean destruction callbacks are executed
