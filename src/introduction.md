# Introduction

The Jet engine is a multi-media platform targetting WebAssembly. It supports an ECMAScript 4 like language, ActionScript 3; an eXtensible Markup Language for the user interface, MXML; and a Cascading Style Sheet 3 dialect.

## Features

### Event model

When compared to standard ActionScript 3, the event model has been simplified due to type inference, and uses shorter notation for the event listener methods.

### Documentation comments

Documentation comments support Markdown and referencing local images.

### Package manager

A productive package manager is supported which facilitates creating new projects and building them. In addition, published packages are automatically queued for documentation generation in the online documentation host.

## Comparison to JavaScript

Vanilla JavaScript has some limitations, such as not being typed and not supporting documenting custom events properly unless JSDoc tags are used.

JavaScript classes, to extend upon the other, require the base class to have been pre-evaluated by the JavaScript engine.

TypeScript allows to define custom events through its extensive type system, but requires inheriting events from base classes manually through a rest operator.

JavaScript or TypeScript are not well suited for interactive applications where reactive frameworks are not used; instead of reactivity, Jet uses a hierarchic component model in a Display List, which is inspired by Adobe Flex, and allows implementing UI components in MXML files.