# Domain-Specific Extensions

## Overview
Specialized features and vocabularies for different knowledge domains.

## Mathematical Logic
- **Number Theory**: Natural numbers, integers, rationals, reals
- **Set Theory**: Set operations, cardinality, power sets
- **Function Theory**: Domain, range, composition, inverse
- **Algebraic Structures**: Groups, rings, fields, vector spaces

## Philosophical Logic
- **Existence and Identity**: Being, existence, identity criteria
- **Causation**: Causal relationships, causal chains
- **Modality**: Necessity, possibility, counterfactuals
- **Ethics**: Moral predicates, ethical reasoning

## Scientific Logic
- **Hypothesis Formation**: Testable statements, predictions
- **Evidence Evaluation**: Support, confirmation, falsification
- **Causal Inference**: Cause-effect relationships
- **Theory Construction**: Coherent explanatory frameworks

## Legal Logic
- **Legal Rules**: Statutes, regulations, precedents
- **Exceptions**: Conditions that override rules
- **Precedent System**: Case-based reasoning
- **Burden of Proof**: Evidence requirements

## Temporal and Spatial Logic
- **Time**: Moments, intervals, duration, sequence
- **Space**: Location, distance, containment, topology
- **Spatiotemporal**: Events, processes, changes
- **Relative References**: Context-dependent positioning

## Usage Examples
```
# Mathematical logic
socrates% define: prime(n) := (n > 1) && (all d)(divides(d, n) -> (d = 1 || d = n))
socrates% query: prime(17)
>> true [17 satisfies primality conditions]

# Philosophical logic
socrates% define: necessarily(P) := (all w in possible-worlds)(P holds-in w)
socrates% query: necessarily(socrates is-human)
>> false [socrates might not exist in all possible worlds]

# Scientific logic
socrates% define: supports(evidence, hypothesis) := 
    probability(hypothesis | evidence) > probability(hypothesis)
socrates% query: supports(observe-swan-white, all-swans-white)
>> true [but support is not proof]

# Legal logic
socrates% define: guilty(person, crime) := 
    committed(person, crime) && 
    proven(beyond-reasonable-doubt) && 
    no-valid-defense(person)

# Temporal logic
socrates% define: eventually(P) := (some t > now)(P holds-at t)
socrates% query: eventually(socrates is-dead)
>> true [assuming mortality]
```

## Priority: Medium
Valuable for specialized applications but not essential for core system.