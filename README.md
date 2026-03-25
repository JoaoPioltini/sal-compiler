# SAL Compiler (C)

A compiler for the **SAL (Simple Academic Language)** implemented in C.

This project was developed as part of a **Compiler Design** course and aims to build a complete compilation pipeline, from lexical analysis to code generation for a stack-based virtual machine (MEPA).

---

##  Features

-  Lexical Analysis (Lexer)
  - Token recognition (identifiers, keywords, literals)
  - Operators and delimiters
  - Support for:
    - Line comments (`//`)
    - Block comments (`/* ... */`)
    - Strings and char literals
  - Error detection (invalid tokens, unclosed strings/comments)

-  Syntactic Analysis (Parser) *(in progress)*
  - Recursive Descent Parser (ASDR)
  - Grammar-based validation

-  Symbol Table *(in progress)*
  - Identifier tracking
  - Scope management (global, local, procedures)

-  Code Generation *(planned)*
  - Target: MEPA (stack-based virtual machine)

---

##  Project Structure
