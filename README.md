# cparsing

A simple implementation of a C++ parser using Parsec. It is defined with a custom AST and parser.

The basic idea was to create a C++ representation that keeps its connection with the original
source code regardless of the preprocessor operations done on it. Each AST node that is expanded
from a macro expansion records that fact and their transformations are constrained to protect
the original structure of the program.

A preprocessor implementation is given that tracks the macro expansions and this helps to create
an AST where the nodes refer to the original source code from which they were generated.

The MiniC module contains the entry point of the parser, the CTransform package provides a transformation of the AST.
The C++ AST and parser and semantical analysis is defined in the MiniC package.
Traversing utilities are defined in the Data package.
General AST elements are defined in the SourceCode package.

This is an early project of mine, the ideas behind this project are fully developed in the
Haskell-Tools project. Regardless, this early experience led me to continue using this approach.

By the way, this is an old project I am no longer developing.