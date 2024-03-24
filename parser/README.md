# Lexer and parser

The **lexer** and **parser** are two related components of a compiler that are
responsible for reading source code and building up the structure of the
programme.

These components are related, but perform somewhat different tasks:

- a **lexer** takes a raw stream of characters and converts this to a stream
  of **tokens**, which are meaningful to the language itself. This might include
  picking out keywords (`for`, `if`, `while`, ...), literal elements like
  numbers (`123`, `123.45`, `0x143523`, `"string literals too"`, ...), and other
  things like identifiers (variable names, function names, ...).
- a **parser** takes a stream of tokens and resolves this into a syntax tree
  according to the grammer. This step often includes checking for syntatic
  errors within the source.

Lexing and Parsing are very common operations, and there are even tools that
automate their construction using only the grammar (plus possibly some
additional metadata). For example, **Lex and Yacc** are well-established tools
for making these first components of the compiler. (Yacc stands for "yet
another compiler compiler".) We aren't going to use these tools because we're
interested in learning how to build them ourselves, but we can use them to
experiment with the grammer and test our own implementation.
