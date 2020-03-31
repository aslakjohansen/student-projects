# Education Composition and Layout System

**Tags:** optimization, ui, compiler theory, graph theory

## Introduction

Deciding which courses are needed, what they should cover and which order they should be offered in is a complex, time consuming and potentially error-prone task to do manually. In this project we try to build the tooling for a computer-aided education composition and layout system.

An education is made up of a number of semesters, and has a goal. That goal could be to generate software engineers for the industry. Such a goal is accomplished by making sure that students have a certain set of qualifications. Such qualifications could be broadly termed (such as “Object Oriented Programming”).

## Problem

How can we make a tool that aids the structuring of an education?

## Approach

How would a system supporting our workflow look?

We imagine a workflow of the form:
1. An education is named and the end qualifications are entered
2. Qualifications are successively subdivided until the remaining pieces represents a single unit of knowledge representing an insignificant amount of information.
3. Dependencies between the pieces should be added. Example “branching” depends on “types” because a condition evaluates to a boolean value. 
4. A human will then define themes which clusters these pieces of information. Alternative definitions may result. Such alternatives represents pieces of information being moved between themes. All pieces of informations should belong to a theme.
5. The themes are then mapped to courses. Multiple mapping alternatives may result. Such alternatives represents themes being moved between courses. All themes should belong to a course.
6. An optimizer will try to map courses to semesters without breaking dependencies. The trick is to make sure that each piece of information is covered by choosing between the multiple definitions of themes and courses.
7. Finally, a visual representation of the solution is presented to a human who can adjust.

## Related Work

