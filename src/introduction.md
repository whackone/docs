# Introduction

The Jet engine is a multi-media platform targetting WebAssembly. It supports an ECMAScript 4 like language, a very modified version of ActionScript 3; and a Cascading Style Sheet 3 dialect.

Unlike Adobe Flex, Jet uses reactive user interface.

## Features

### Event model

When compared to standard ActionScript 3, the event model has been simplified due to type inference, and uses shorter notation for the event listener methods.

### Documentation comments

Documentation comments support Markdown and referencing local images.

### Package manager

A productive package manager is supported which facilitates creating new projects and building them. In addition, published packages are automatically queued for documentation generation in the online documentation host.

### Reactivity

The ECMAScript for XML (E4X) feature of ActionScript is modified such that the markup syntax is used for implementing UI components, similiar to ReactJS, but tied to Jet Display List.

The E4X markup supports comments and XML namespaces.

## Comparison to JavaScript

- Vanilla JavaScript ∉ typed
- Vanilla JavaScript ∉ proper custom events
- JavaScript ∈ immediate classes
- TypeScript ∉ custom event inheritance (requires `...BaseClassEvents`)
- TypeScript ∉ built-in reactivity