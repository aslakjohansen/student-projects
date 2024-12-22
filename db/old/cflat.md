# C♭ (pronounced see-flat)

**Tags:** domain specific language, language design

## Introduction

At our software educations, C# is replacing Java. However, neither are a good fit for introducing people to programming. They come with lots of complexities that add to the confusion. These include:
- Classes are necessary for small programs.
- Use of the `static` keyword.
- Access modifiers are needed for main.
- ?

## Problem

How can we make the transition from non-programmer to young C# programmer easier? In particular, how can we keep the set of foreign elements needed at any point in the learning process as small (and simple) as possible?

## Approach

Introduce a new language that compiles to C#, and translate any errors (compile time as well as runtime) to the source (so that references -- e.g., line numbers -- match). An interpreter wrapper is needed for translating runtime errors.

The new language differs from C# in that:
- There are no classes
- A `struct` type is added that looks a lot like the C counterpart. Using this, programmers can define types as sets of named and typed fields. The format should match that of a class without methods and constructors.
- A function that takes a `struct` type as first argument is compiled to a instance method to the class matching that `struct` type.
- A function that does not take a `struct` type as first argument is compiled into a `static` method in a class named after the source file hosting it.
- There are no access modifiers (everything will translate to `public`).

There should be syntax highlighting support for a basic text editor (e.g., sublime text). An IDE is less attractive as it allows students to get by without actually understanding.

## Related Work

