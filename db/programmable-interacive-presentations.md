# Programmable Interactive Presentations

**Tags:** web, interaction design, phoenix, liveview

## Introduction

It would seem that there is no good software for making presentations; just degrees of badness. PowerPoint is horrible for alligning things and it wants to fight you all the time. Beamer makes positioning an interactive process. For now, we accept that we won't design the perfect solution. Instead, we want to add a new point to the solution space.

Modern web frameworks provides easy means of:
- Interaction between users.
- Rendering text, tables, and images of decent quality.
- Providing the ability to produce such contents live.

## Problem

How can we make a software-defined presentation system with real-time audience interaction?

## Approach

Technology stack:
- Phoenix
- LiveView

Views:
- Main presentation view
  - Partial reveals
  - PNG, SVG and PDF support
- Presenter view
  - Time
  - Notes
  - View of next slide
- Audience view
  - Interaction (options are programmable)
  - Responses (e.g., like)
  - Voting (e.g., for polls)

## Related Work

