---
title: TinyS Compiler
date: 2025-10-15 12:00:00 -0300
categories: [compiler]
tags: [
    compiler, 
    open source,
    low level programming, 
    java,
    assembly,
    mips]     
description: Made a compiler form scratch using Java and Assembly

image:
  path: /assets/tinys-compiler/sample.png
---

![##TinyS](/assets/tinys-compiler/sample.png)

TinyS is a custom-built compiler that translates a subset of the Swift programming language into MIPS assembly. Developed in Java, this project focuses on the implementation of core Object-Oriented Programming (OOP) principles at the machine level.

- Object-Oriented Logic: Full support for class inheritance, method overriding, and dynamic polymorphism.
- MIPS Code Generation: Translates high-level constructs directly into assembly, managing stack frames and register allocation.
- Verified Reliability: The codebase is fully covered by a Maven (mvn) test suite, ensuring each stage of the pipeline functions correctly under various edge cases.

### Compiler Pipeline

The compiler follows a modular architecture to transform source code into assembly source:

- **Lexical Analysis**: Uses the State Pattern to break source code into a stream of tokens.
- **Syntactical Analysis**: A Top-Down Parser that validates the structure against the TinyS grammar.
- **Semantic Analysis**: Builds a Symbol Table and an Abstract Syntax Tree (AST) to manage scope and variable visibility.
- **Type Checking**: A dedicated traversal of the AST to enforce type safety and validate inheritance hierarchies.
- **Code Generation**: An AST visitor that outputs MIPS assembly, handling the low-level details of method dispatch and memory.


### Project Stack
- Implementation Language: Java
- Target Architecture: MIPS
- Build & Test Tooling: Maven

### About the source code
The source code is currently private to respect the project timeline of other students.