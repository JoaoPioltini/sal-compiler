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
.
├── src/
│   ├── lex.c
│   ├── parser.c
│   ├── symtab.c
│
├── include/
│   ├── lex.h
│   ├── token.h
│
├── main.c
└── README.md

---

##  How It Works

The compiler follows a modular architecture:

1. **Lexer (`lex.c`)**
   - Reads the source file character by character
   - Produces a stream of tokens

2. **Parser**
   - Consumes tokens from the lexer
   - Validates program structure based on SAL grammar

3. **Symbol Table**
   - Stores identifiers, types, and scope information

4. **Code Generator**
   - Produces instructions for a stack-based VM (MEPA)

---

## ▶️ Running the Lexer

Example:

```c
while(1){
    Token t = lex_next();

    printf("Type: %d | Lexeme: %s | Line: %d\n",
           t.type, t.lexema, t.line);

    if(t.type == TK_EOF) break;
}


