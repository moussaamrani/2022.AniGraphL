# 2022.AniGraphL

## Progression notes

### § Motivation

1. On the xDSL specification

- The DSL specification is expected to follow the ___ [Combemale] pattern: an MM allows the definition of a (static) model; which is augmented with so-called dynamic information to handle the "internal" "dynamic" state of the DSL during execution.
- This brings the question of specialisation. In order to obtain an accurate MM, one should specialise it towards MA. This means that three activities are now in conflict: generting an editor; handling the execution; and providing MA.


2. On Concrete Syntax (CS)

- Specifying a CS should go beyond simply associating icons to classes. Complex rendering patterns should be possible depending on the values of structural properties.
- Having a MM renderer does not guarantee the ability to animate MM's conformant models, since MA adds a "dynamic" dimension absent from the edition.

3. On the MA

- The MA engine should be independent of how the MT is defined, albeit it should have a minimal interface with the MTL
- The specification of MA steps should not be tightly coupled with MT micro-steps, otherwise it becomes as cumbersome as specifying the MT itself.
- MA units should be modular and easily composable, and mappable to elements in AS
- The MA Engine should be able to perform dynamic/online animation, but also offline animation as well, without redifining the whole engine.

### § AniGraphL

1. CS

2. Animation specification

3. Mapping


