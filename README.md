# 2022.AniGraphL

## Progression notes

### § Motivation

1. On the xDSL specification

- The DSL specification is expected to follow the ___ [Combemale] pattern: an MM
allows the definition of a (static) model; which is augmented with so-called
dynamic information to handle the "internal" "dynamic" state of the DSL during
execution.

- This brings the question of specialisation. In order to obtain an accurate MM,
one should specialise it towards MA. This means that three activities are now in
conflict: generting an editor; handling the execution; and providing MA.


2. On Concrete Syntax (CS)

- Specifying a CS should go beyond simply associating icons to classes. Complex
rendering patterns should be possible depending on the values of structural
properties.

- Having a MM renderer does not guarantee the ability to animate MM's conformant
models, since MA adds a "dynamic" dimension absent from the edition.

- Usually, the CS is itself metamodelled explicitly, with eventually a
canonical, in-memory representation that serves for reconciling operations on
the model.

3. On the MA

- The MA engine should be independent of how the MT is defined, albeit it should
have a minimal interface with the MTL

- The specification of MA steps should not be tightly coupled with MT micro-
steps, otherwise it becomes as cumbersome as specifying the MT itself.

- MA units should be modular and easily composable, and mappable to elements in
AS

- The MA Engine should be able to perform dynamic/online animation, but also
offline animation as well, without redifining the whole engine.

### § AniGraphL

1. CS

Simple combination of Shape on Canva:

- Shape < Form, Connector
- Form < TextBox, Rectangle, RoundedRectangle, Oval, Triangle, Parallelogram, Trapezoid, Rhombus
- Connector < Line, Elbow, Curve, FreeForm

Canva:: size(x, y); background: Color, grid: ??. SHOULD ADD: layers, validation rules, filters

Shape <> position, fill, line, size, text

Position : hpos, vpos: Float

Size : height, width : Float

Fill : color: Color; transparency: Ratio

Line: color: Color, transparency: Ratio, width: Float, compound: Compound, dash: Dash
<> begin, end: Arrow
Dash may be simple: solid, dash, dot, dash-dot (from Sirius)

Arrow: type: AType, size: ASize
(type may be called decorator, eg in Sirius)

Text: color: Color, valigne: VAlign, halign: HAlign, left,right,bottom,top: Float, font: Font
Font: name, format (Bold, Italic, Normal, Underlined); 




1. HOW ABOUT CONNECTION POINTS?
2. REFINE TEXT: a TextBox vs. Text components


-------------------
AtoMPM
-------------------

1. Parser/Mapper link CS and AS attribute values. Ex: the text value displayed
in a component is linked to the name attribute of the represented class

2. Constraints put constraints on components (just like OCL); Actions allow to
define actions performed during edition, when a trigger is triggered, i.e.

- Dis-/Connecting two instances
- C(R)UDing an instance
- Verify (i.e. check for conformance) a model

All these triggers have a pre- and post- definition (for the first two).


-------------------
Sirius
-------------------

Common needs for visually representing models:

1. Identify elements that need representation
2. Associate them to a description
3. Link them with behaviour and actions (from the "palette")

1. Concept of "Mapping" with a *context*, a *type*, a *navigation expression*,
and a *filter predicate*. This basic behaviour for finding elements may be
altered by "Semantic Candidates", specified with an expression.

2. Different basic "representations": diagram, table, tree, etc.

DIAGRAM

- A Diagram contains (i) layers, which can contribute tools and/or mappings (ii) validation rules; (iii)
filters, to hide some elements; (iv) others.
 
- Node is a geometric shape. Very classic

- Container is a "box" that may contain ports (aka. BorderedNode). List is a
special kind of Container, that displays text vertically.

- Edge establishes a connection between nodes, containers and/or edges
themselves (special edge: BracketEdge, with attachement to elements, supporting
the edge). Two types: RelationBased, which provides a Connector/Edge
representation for an element that is a reference; and ElementBased, for one
that is a class. 
One has to provide the src/tgt (i.e. how they are computed from the Edge's
context, i.e. the MM element, either a Class or a Reference).






2. Animation specification

3. Mapping

### 
