# Architecture vs design

## Overview

This page discusses the difference between the terms *architecture* and *design* when discussing decision making about how software is made.

## Architecture

Architecture is a higher-level concern that typically happens more up-front, i.e. decisions at this level are often being made before code is written. Architecture is interested in how the application is structured. Examples of architecture questions include:

- How should the software be hosted?
- How will communication between different elements of the system be done?
- What are the deployable units of the system?

Typical software architecture patterns include:
- Microservices
- Event-driven
- Serverless

Software architecture answers the question 'What are we building?' and typically includes infrastructure as well as or instead of code.

Software architecture decisions might typically be implemented by an entire team of developers, all working together on some new application or major enhancement.

## Design

Design is a lower-level and more frequent concern. Design is the decisions about how code is structured and written in order to achieve work at the level of user stories. Examples of design questions include:

- Should we use inheritance or composition here?
- What shape do the objects have in this domain and how do we convert between them?
- How can this query be written in an efficient way?

Typical software design patterns include:
- Factory
- Decorator
- Command

(See [here](https://www.gofpattern.com/design-patterns/module2/three-types-design-patterns.php) for more information about these kinds of design patterns.)

Software design answers the question 'how are we building this?' and is usually about what code gets written.

It would be typical for a software design decisions to be implemented by a simple developer, perhaps as part of a user stories or series of user stories.

## Uncertainty

A couple of the resources linked below make the point that software design *avoids* uncertainty whereas software architecture *manages* it. I'm not sure what is meant by this.

## Resources

| Link      | Description |
| ----------- | ----------- |
| https://www.geeksforgeeks.org/system-design/difference-between-software-design-and-software-architecture/ | Differences between Software Design and Software Architecture |
| https://appsero.com/tips-tricks/difference-software-architecture-vs-design/ | Software Architecture vs Design: Key Relationship and Differences You Must Know |
| https://www.lucidchart.com/blog/software-architecture-vs-design | Software design vs. software architecture |
| https://www.gofpattern.com/design-patterns/module2/three-types-design-patterns.php | The three types of design pattern defined by Gang of Four |