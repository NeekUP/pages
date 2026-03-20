---
title: Layered Architecture
layout: post
slug: layered-architecture
category: software design pattern  
---
Layered architecture is one of the fundamental concepts in programming. Like all other patterns, approaches, and architectures, its main goal is to reduce complexity during code development and reading. To understand what layers are and why they are needed, it is essential to know what abstractions are.

An abstraction is the separation of what an entity does from its implementation, simplifying the entity to its characteristics that distinguish it from the rest of the world. Using abstractions is quite natural for us. A road, a house, a car, a monitor – these are abstractions. We know what they are and how to interact with them, while often not fully understanding how they work. There can be many implementations of each abstraction. For example, there is the abstraction of a car; there are many different models, and not everyone knows how it works or what it consists of. But what is called a car, in one way or another, will serve to transport a person from one place to another.

Abstractions themselves consist of abstractions, forming a hierarchical structure where each level reveals more details.

In the diagram below, all the rectangles are abstractions.

![Abstractions](assets/layered-architecture/abstractions.png)

A proper description of abstractions is a separate topic, but if an abstraction accurately describes an entity, it can be used anywhere it is needed; only the implementations differ. It is important to remember this and not to adjust the abstraction being created for the convenience of its implementation.

Layered architecture is built upon abstractions. In this architecture, the application is divided into layers, and there can be any number of layers. *Each layer is not an abstraction in itself, but a level of abstractions.* Each layer can also be subdivided into sub-layers if necessary.

![Layers](assets/layered-architecture/layers.png)

Layered architecture implies that the program's execution flow cannot skip layers. *All interactions happen from the upper layer to the lower ones. Each layer interacts only with the one directly below it.* Using programming language tools, you can separate the layers into different assemblies and control their connections with each other.
