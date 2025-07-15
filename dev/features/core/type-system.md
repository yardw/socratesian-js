# Type System

## Overview
Comprehensive type system for terms, predicates, and values in Socratesian.

## Primitive Types
- **Individual**: Basic entities in the domain of discourse
- **Proposition**: Statements that can be true or false
- **Predicate**: Functions that map to truth values
- **Relation**: Multi-argument predicates connecting terms

## Complex Types
- **Set**: Collections of individuals `{x1, x2, x3}`
- **Sequence**: Ordered collections `[x1, x2, x3]`
- **Function**: Mappings between domains `f: A -> B`
- **Domain**: Universes of discourse `domain(humans)`

## Type Constraints
- **Domain Restrictions**: `(any x in-domain D)`
- **Cardinality Constraints**: `|S| = n`, `|S| > n`, `|S| < n`
- **Type Inheritance**: Subtypes and supertypes
- **Type Compatibility**: Rules for type mixing

## Polymorphic Types
- **Generic Predicates**: Work across multiple types
- **Type Variables**: `(any x of-type T)`
- **Bounded Polymorphism**: Type constraints on generics

## Type Inference
- **Automatic Detection**: Infer types from usage
- **Type Checking**: Validate type consistency
- **Type Coercion**: Automatic type conversion rules

## Usage Examples
```
# Domain restriction
(any x in-domain humans) has-impl(condition = x is-mortal)

# Set operations
S1 = {socrates, plato, aristotle}
S2 = {philosophers} 
S1 subset-of S2

# Function types
age: humans -> natural-numbers
age(socrates) = 70

# Polymorphic predicate
(any x of-type T) has-property(property = exists)
```

## Priority: High
Critical for maintaining logical consistency and enabling advanced reasoning.