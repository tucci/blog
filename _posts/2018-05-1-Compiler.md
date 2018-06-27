---
layout: post
title:  "Compiler Written in C++"
author: "Steven"
---

The compiler was written from scratch and no tools like yacc, or lex were used.
Everything from the lexer to the code generator are all from scratch and unit tested.


The language is toy language that has the common language constructs. It is also a  staticly typed class(OOP) based language. 

The compiler is a LL1 top down table driven parser with multiple passes. This removes the need for forward declaring, and can allow for independant ordering of declarations.

The code generated is built for the moon processor. It is a very simple RISC language. The backend can be reconfigured to output any instruction set, as their is  a intermediate representation.


[See On Github](https://github.com/tucci/comp442-compiler)

##  The Challenges

- Implementing the lexer using a dfa 
- Generating the  parser from the BNF grammar file
- Building the first and follow sets
- Embdeding semantic actions into the grammar
- Building The symbol table
- Syntax and Semantic Error checking and recovery
- AST to object code generation, with register spill over



## Lexical Analysis
- Lexical Error checking
- Processes integer and floating point tokens properly
- Handles comments, and nested multi line comments

## Syntactic Analysis
- Error detection, reporting, and recovery
- Support for free functions
- Support for ints, floats, classes, and arrays.
- Handles complex expressions
- Class methods,data memebers, and chaining

## Semantic Analysis
- Semantic Error checking, reporting, and recovery
	- undefined vars, classes, functions
	- undefined data memembers, methods, deeply nested
	- forward declarions, and circular references
	- duplicates
- Proper Type checking
	- complex expressions(sub expression are all of the same type)
	- assignment statements / lhs = rhs 
	- returns match the function declaration
	- function calls match the function declaration

## Code Generation
- Simple optimizations
- Register spill over
- Built from AST
- Generates simplified RISC Code. (Load/Store)