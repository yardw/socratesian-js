# Logical Operators & Constructs

## Overview
Core logical operators and constructs for the Socratesian language.

## Basic Operators
- **Conjunction**: `&&` (logical AND)
- **Disjunction**: `||` (logical OR)
- **Negation**: `!` (logical NOT)

## Implication Operators
- **Material Implication**: `->` (if-then)
- **Biconditional**: `<->` (if and only if)
- **Reverse Implication**: `<-` (only if)

## Quantifiers
- **Universal**: `any` (for all)
- **Existential**: `some` (there exists)
- **Negative Universal**: `none` (for no)
- **Negative Existential**: `not-some` (there does not exist)

## Modal Logic Operators
- **Necessity**: `necessarily` (must be true)
- **Possibility**: `possibly` (might be true)
- **Impossibility**: `impossibly` (cannot be true)

## Temporal Logic Operators
- **Temporal Order**: `before`, `after`, `during`
- **Temporal Extent**: `until`, `since`, `while`
- **Temporal Frequency**: `always`, `sometimes`, `never`

## Usage Examples
```
# Basic conjunction
(x is-human) && (x is-mortal)

# Implication
(x is-human) -> (x is-mortal)

# Quantified statement
(any x) has-impl(condition = x is-human, conclusion = x is-mortal)

# Modal logic
necessarily((any x) has-impl(condition = x is-human, conclusion = x is-mortal))

# Temporal logic
always((any x) has-impl(condition = x is-human, conclusion = x is-mortal))
```

## Priority: High
Essential for basic logical reasoning and formal representation.