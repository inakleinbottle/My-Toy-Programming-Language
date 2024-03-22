# My Toy Programming Language

This project is all about creating a programming language from scratch,
including formulating the grammar, building a lexer and parser, working with the
abstract syntax tree, type checking, and code generation.

There are lots of parts to this, so we're going to take this one step at a time.

## Anatomy of a programming language

Making a programming language has lots of parts, here's a very brief outline of
how the source code is read and compiled.

```
             +---------------+
             |  source code  |
             +---------------+
                     |
                     | lexer and parser
                     v
          +----------------------+
          | abstract syntax tree |
          +----------------------+
                     |
                     | Type checking
                     v
      +-----------------------------+
      | intermediate representation |
      +-----------------------------+
                     |
                     | (Optimisation and) code generation
                     V
            +-----------------+
            | executable code |
            +-----------------+

```
