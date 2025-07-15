# socratesian-js
Socratesian is a strict logic language aiming for bootstraping natural language formalization.
## A Quick Usage Example
1. The user may provide the `socrates` parser with **raw** information in natural language.
```bash
socrates% view: "Socrates is a mortal."
>> warning: the term "Socrates is a mortal" is not defined and therefore is-atomic-term automatically. 
>> "Socrates is a mortal" is-atomic-term

socrates% term: "Socrates is a mortal."
# enter the definition of the term "Socrates is a mortal.".
```
2. The user is requested to explicitly explain the **connotation** for the provieded information in a structured way, which has to be acceptable for the `socrates` **parser**.
```bash
socrates(term: "Socrates is a mortal.")% "socrates" is-a(term = "mortal")
>> the term "Socrates is a mortal." has been clarified and is no longer is-atomic-term anymore.
>> any term in ["socrates", "mortal"] is-atomic-term automatically.
# now the term "Socrates is a mortal." has been clarified and assigned to the proposition "socrates is-a mortal".
# here "is-a" is a predicate that describes the relation between terms "socrates" and "mortal".

# we can check that the term "Socrates is a mortal." has been assigned and is no longer an atomic term.
socrates% view: "Socrates is a mortal."
>> "Socrates is a mortal." is-equiv(term = "socrates" is-a(domain = "mortal"))

socrates% term: "socrates"
socrates(term: "socrates")% (any x) has-impl(condition = x is-socrates)
>> the term "socrates" has been clarified and is no longer is-atomic-term anymore.
>> the predicate "is-socrates" is-atomic-predicate automatically.
# "any" is a special predicate called quantifier that declare an individual in the domain of discourse. "some" is another quantifier.
# "has-impl" is a predicate that quivalent to "such that" in natural language
# "is-socrates" is a predicate that to be clarified.

socrates% predicate: "is-socrates"(x)
socrates(predicate: "is-socrates"(x))% (x is-unique) && (x is-human) && (x "is-male") && (x is-philosopher) && (x is-Greek) && (x has-birthday(time = 470BC)) && (x has-deathday(time = 399BC)) && (x has-student(name = "Plato")) && ...
>> the predicate "is-socrates" has been partially clarified and is no longer is-atomic-predicate anymore.
>> any predicate in ["is-unique", ...] is-atomic-predicate automatically.

socrates% term: "mortal"
socrates(term: "mortal")% (any x in-domain) has-impl(condition = x is-mortal)
>> the term "mortal" has been clarified and is no longer is-atomic-term anymore.
>> the predicate "is-mortal" has been added to the atomic predicate base.

socrates% predicate: "is-mortal"(x)
socrates(predicate: "is-mortal"(x))% (x is-immortal) || ((any x1 in-domain) && (x1 is-timestamp) has-impl(condition = x has-deathday(time = x1))) || ...
>> the predicate "is-mortal" has been partially clarified and is no longer is-atomic-predicate anymore.
>> the predicates ["is-immortal", ...] have been added to the atomic predicate base.
```

3. The structured information can then be used to create a mind-map of the concepts and ideas.

## Terminology
- `term`: A concept or idea that can be connected to other terms.
    - `individual`: A term that is not yet defined.
    - `proposition`: A term that can be true or false.
- `predicate`: An applicable to terms that describes a property or relation.
    - `property`/`binary`: A characteristic of a term. (e.g. `is-atomic-term`, `is-atomic-predicate`, `is-unique`, `is-null`, `is-male`, `is-philosopher`, `is-Greek`, `is-mortal`, `is-human`, etc.)
    - `relation`: A connection between other term(s) in the keyword arguments of predicate. (e.g. predicates with kwargs: `is-a`, `has-impl`, `is-equiv`, etc.)