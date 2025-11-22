# kodilla-basic-tests

![Java](https://img.shields.io/badge/Java-21-blue)
![Gradle](https://img.shields.io/badge/Gradle-8-green)
![JUnit](https://img.shields.io/badge/JUnit-5.9.1-purple)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

This repository contains exercises, homework tasks, examples and unit tests created as part of a module in the **Kodilla "Automated Tester" Java course**, focusing on **Java Testing Basics** in Java 21.

The module focuses on:

- inheritance and method overriding
- abstract classes and polymorphism
- composition vs inheritance
- introduction to unit testing
- static vs dynamic testing
- JUnit 5 configuration and writing first test suites

The project was developed in **IntelliJ IDEA** as part of the learning path for future **QA/Test Automation Engineers**.

---

## Description

This module includes a wide range of Java examples and exercises, grouped into logical packages.

### Main topics covered

- building class hierarchies using `extends`
- constructors, `super()`, private fields and getters
- abstract classes & abstract methods
- polymorphism (`Animal animal = new Dog()`)
- composition vs inheritance ("has-a" vs "is-a")
- writing first manual assertions (`ResultChecker`)
- configuring **JUnit 5** in Gradle
- writing automated unit tests using:
    - `assertEquals`
    - `assertTrue` / `assertFalse`
    - delta for comparing doubles
    - test suites structure

---

## Project Structure

```
kodilla-basic-tests/
├── src/
│   ├── main/java/com/kodilla/
│   │   ├── abstracts/
│   │   │   ├── Animal.java
│   │   │   ├── AnimalProcessor.java
│   │   │   ├── Dog.java
│   │   │   ├── Duck.java
│   │   │   └── homework/
│   │   │       ├── Shape.java
│   │   │       ├── Circle.java
│   │   │       ├── Triangle.java
│   │   │       ├── Square.java
│   │   │       ├── Job.java
│   │   │       ├── Person.java
│   │   │       ├── Lawyer.java
│   │   │       ├── Firefighter.java
│   │   │       └── Teacher.java
│   │   ├── inheritance/
│   │   │   ├── Car.java
│   │   │   ├── Convertible.java
│   │   │   └── homework/
│   │   │       ├── OperatingSystem.java
│   │   │       ├── OldSystems.java
│   │   │       ├── NewSystems.java
│   │   │       └── SystemsApp.java
│   │   ├── basic_assertion/
│   │   │   ├── Calculator.java
│   │   │   ├── PrimeChecker.java
│   │   │   ├── ResultChecker.java
│   │   │   └── Application.java
│   │   ├── bank/homework/
│   │   │   ├── Bank.java
│   │   │   └── CashMachine.java
│   │   ├── MyExercises/
│   │   │   ├── ShoppingList.java
│   │   │   ├── StudentGrades.java
│   │   │   ├── ToDoList.java
│   │   │   └── more exercises...
│   │   └── school/
│   │       ├── Student.java
│   │       └── Grades.java
│   └── test/java/com/kodilla/
│       ├── bank/homework/BankTestSuite.java
│       ├── basic_assertion/CalculatorTestSuite.java
│       ├── basic_assertion/PrimeCheckerTestSuite.java
│       ├── MyExercises/...TestSuite.java
│       └── school/...TestSuite.java
│
├── build.gradle
├── settings.gradle
├── gradlew / gradlew.bat
├── LICENSE
└── README.md
```

---

## Getting Started

### Dependencies

This module uses **Gradle** as the build system.

**build.gradle (core configuration):**

```gradle
plugins {
    id 'java'
}

group = 'com.kodilla'
version = '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation platform('org.junit:junit-bom:5.9.1')
    testImplementation 'org.junit.jupiter:junit-jupiter'
}

test {
    useJUnitPlatform()
}
```

### Explanation of components

- **Java plugin** – enables compilation and running Java code
- **JUnit 5 (Jupiter)** – used for writing automated unit tests
- **Maven Central** – dependency repository
- **Gradle Wrapper (./gradlew)** – ensures the project builds on any machine

All classes run directly through IntelliJ IDEA, and tests can run through either the built-in test runner or Gradle.

---

## Test Suites Overview

This module introduces automated unit testing and contains several organized test suites covering core concepts from the module.

### **basic_assertion**
- verifies correctness of arithmetic operations in `Calculator`
- tests prime number validation logic in `PrimeChecker`
- checks manual assertion helper (`ResultChecker`)
- includes positive, negative, and boundary-value scenarios

### **bank/homework**
- tests `Bank` and `CashMachine` logic
- verifies balance calculations
- validates deposit/withdrawal rules
- ensures that edge cases (e.g., no transactions) produce correct results

### **school**
- verifies student grade averaging
- checks correct handling of empty grade sets
- tests logic related to class grade summarization

### **MyExercises**
- verifies correctness of custom utility classes
- tests data processing, filtering, and validation logic

These suites demonstrate the fundamentals of automated testing:  
assertions, test structure, separation of concerns, and validating both typical and edge-case scenarios.

---

## Optional Terminal Commands

**Build project:**

```bash
./gradlew build
```

**Run all tests:**

```bash
./gradlew test
```

**Clean project:**

```bash
./gradlew clean
```

---

## Authors

Created by:

**Joanna Kamińska**  
GitHub: https://github.com/joanna-kaminska-qa

---

## Version History

- **0.2** – README added, structural improvements
- **0.1** – Initial upload

---

## License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

---

## Acknowledgments

- Kodilla Automated Tester Java course
- JUnit documentation
- Java official documentation  
