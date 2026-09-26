# PATL — Pattern Language

## `.ptl`

### Pattern-Centric, Sequence-Oriented Systems Programming

**PATL**, the **Pattern Language**, is a compact, high-control programming language built around **patterns, patterning, pattern recognition, pattern matching, and sequential transformation**.

Its defining design contrast is deliberate:

> **Extremely thin surface. Extremely dense semantics.**

PATL keeps its visible syntax narrow, regular, necessity-driven, and easy to scan while placing substantial intelligence beneath that syntax.

The programmer writes relatively little.

The language derives considerably more.

PATL is simultaneously:

- pattern-oriented
- sequence-oriented
- systems-capable
- algebraic-equational
- state-aware
- explicitly mutable
- memory-controllable
- inference-capable
- hardware-conscious
- semantically high-level
- metal-level controllable

Its design does not attempt to hide the machine.

Nor does it force the programmer to continually describe machinery that the compiler already understands.

The language instead operates under a central principle:

> **State the pattern. State the sequence. State the exceptions. Control the machine where control matters.**

---

# 1. Core Philosophy

PATL treats most programming problems as combinations of:

**recognition → relation → transformation → sequence → state**

A conventional language often begins with instructions:

```text
do this
then test this
then call this
then modify this
```

PATL prefers expressing the relationship:

```text
pattern input
matches valid
transform valid to result
```

The compiler derives the mechanical path while preserving programmer control over its important consequences.

PATL therefore distinguishes between:

### Surface expression

What must be explicitly written.

### Semantic interpretation

What can be derived safely and unambiguously.

### Metal authority

What the programmer may explicitly control when abstraction is undesirable.

PATL never requires verbosity merely to prove that the programmer understands what the machine is doing.

---

# 2. The Primary Paradigm: Sequence-Oriented Programming

PATL's governing paradigm is **Sequence-Oriented Programming**.

A program is fundamentally understood as a progression of meaningful states.

```text
A
then B
then C
then D
```

But PATL sequences are richer than ordinary statement ordering.

A sequence can carry:

- values
- state
- ownership
- patterns
- conditions
- references
- errors
- transformations
- memory locations
- execution constraints
- synchronization state

The sequence therefore becomes the principal unit of computational reasoning.

For example:

```ptl
collect request
ping request for account
accept account
transform account
render result
```

This is interpreted as one related flow rather than five unrelated commands.

---

# 3. Patterns

Patterns are PATL's central semantic construct.

A pattern may describe:

- values
- structures
- states
- memory relationships
- execution behavior
- sequences
- types
- conditions
- ranges
- errors
- transformations
- data relationships
- temporal behavior
- resource ownership

Conceptually:

```ptl
pattern adult
    age from 18 to 130
```

A pattern is not merely a matching template.

It is a semantic object that the compiler can reason about.

Patterns may therefore participate in:

- validation
- optimization
- dispatch
- inference
- narrowing
- state analysis
- memory planning
- compile-time reasoning

---

# 4. Pattern Recognition

PATL distinguishes **pattern recognition** from simple pattern matching.

Matching asks:

> Does X fit pattern Y?

Recognition asks:

> Which known pattern best describes X?

Example:

```ptl
recognize input
```

The language can determine whether `input` resembles:

```text
integer
command
packet
record
image
error
request
state
known user-defined pattern
```

Recognition can be:

- static
- runtime
- inferred
- constrained
- manually directed

PATL therefore supports semantic classification without requiring enormous chains of explicit conditional logic.

---

# 5. Pattern Matching

Matching is intrinsic.

Conceptually:

```ptl
value matches pattern
```

or:

```ptl
when request matches login
    ...
```

Patterns can destructure automatically.

```ptl
pattern point
    x
    y

point matches [x y]
```

Matching can simultaneously perform:

- structural validation
- value extraction
- narrowing
- state selection
- type refinement

---

# 6. Patterning

**Patterning** means building behavior from relationships among recognizable structures.

Instead of repeatedly writing procedural machinery, the programmer defines reusable semantic relationships.

```ptl
pattern request
pattern authorized
pattern response

request -> authorized -> response
```

PATL's compiler can construct the required control path from those relationships.

This concept scales into:

- protocol handling
- state machines
- parsers
- compilers
- networking
- event processing
- AI pipelines
- simulation
- operating-system logic

---

# 7. Minimal Surface Syntax

PATL deliberately maintains a small grammatical surface.

The language avoids unnecessarily distinct syntax for concepts that are semantically related.

Its visible syntax relies primarily on:

- words
- indentation
- spacing
- directional symbols
- smart operators
- relationships
- declarations

Punctuation remains intentionally subordinate.

PATL does not turn punctuation density into language expressiveness.

Its source should resemble structured technical reasoning rather than encoded punctuation.

---

# 8. Algebraic-Equational Structure

PATL favors algebraic and equational expression.

For example:

```ptl
area = width * height
```

Relationships may also be expressed directly:

```ptl
distance = speed * time
```

Patterns can participate:

```ptl
valid = input matches specification
```

State equations remain readable:

```ptl
ready = connected and authenticated
```

PATL therefore treats many operations as relationships rather than ceremony-heavy commands.

---

# 9. Values and Assignment

PATL uses `assign` for deliberate value placement.

```ptl
assign 5 to x
```

The direction is intentionally readable:

```text
value → destination
```

Examples:

```ptl
assign 100 to limit
assign user to current
assign false to finished
```

Assignment remains conceptually distinct from mutation.

---

# 10. Variables

PATL treats variables as managed value locations with an explicit semantic lifecycle.

The primary variable operations are:

### Collect

Create or acquire.

```ptl
collect score
```

### Deposit

Place something into an existing location.

```ptl
deposit 5 into score
```

### Withdraw

Take a value from a location.

```ptl
withdraw score
```

### Recall

Recover an existing known value.

```ptl
recall score
```

### Transform

Produce a changed semantic form.

```ptl
transform score using normalize
```

### Mutate

Modify the existing object or state.

```ptl
mutate score
```

### Restore

Return a value or state to an earlier valid condition.

```ptl
restore score
```

These concepts make lifecycle intent visible without requiring large ownership grammars.

---

# 11. Dynamic Explicitness

PATL uses **dynamic explicitness**.

The language permits inference aggressively when meaning is stable.

However:

> When a definition changes meaning, state, interpretation, representation, or type, that change must become explicit.

Example:

```ptl
collect value
assign 5 to value
```

PATL understands `value` as an integer-compatible value.

If later:

```ptl
value becomes text
```

the transition must be declared.

PATL refuses silent semantic identity changes.

This gives inference convenience without sacrificing program comprehensibility.

---

# 12. Types

Types exist as strong semantic patterns rather than merely rigid labels.

A type describes:

- valid values
- representation
- permissible transformations
- operations
- state behavior
- memory expectations

Examples:

```ptl
define Count as integer
define Name as text
```

Types may be:

- explicit
- inferred
- refined
- pattern-derived
- structurally recognized

PATL's type system therefore combines explicit typing with powerful structural inference.

---

# 13. First-Class States

States are fundamental.

```ptl
state ready
state waiting
state failed
```

Booleans are directly related to state.

Instead of thinking only:

```text
true / false
```

PATL allows:

```text
present / absent
ready / not-ready
valid / invalid
open / closed
```

Boolean reasoning therefore integrates naturally with program state.

---

# 14. Conditions Are Inherent

Conditional behavior does not require one universal ceremonial keyword structure.

Patterns and states naturally imply conditions.

```ptl
when ready
    run
```

```ptl
in case of failure
    restore
```

```ptl
situational network unavailable
    retry
```

PATL understands conditional context from relationships.

---

# 15. Case-Based Mutability

Mutability is contextual.

Instead of declaring everything simply mutable or immutable, PATL can express when mutation is legitimate.

```ptl
mutable when loading
```

or:

```ptl
case editing
    mutable document
```

Conceptually supported forms include:

```text
situational
context
case
in case of
when
thus
then
```

This means mutation permissions can follow state.

A structure may therefore be immutable normally but mutable during an authorized transformation phase.

---

# 16. Intrinsic Scopes

Scope is inherent.

Indentation, ownership, sequence, and block relationships determine scope naturally.

PATL avoids requiring excessive syntactic scope markers.

```ptl
pattern request
    collect user
    validate user

    when valid
        render response
```

Each indentation level establishes clear semantic containment.

---

# 17. Indentation-Based Nesting

Nests use indentation.

```ptl
server
    request
        validate
        process
        respond
```

Indentation is semantic rather than decorative.

This eliminates unnecessary braces while preserving strict structural clarity.

---

# 18. Spacing Separates Tokens

Whitespace has a controlled grammatical role.

Spacing separates tokens and relationships cleanly.

PATL intentionally avoids highly compressed symbolic syntax where readability deteriorates.

The source representation should remain immediately inspectable.

---

# 19. Smart Operators

PATL supports **smart operators**.

Operators understand:

- operand types
- context
- patterns
- states
- ranges
- representations

For example:

```ptl
a + b
```

does not simply mean one globally fixed machine operation.

The compiler resolves the valid operation according to the semantic pattern of `a` and `b`.

PATL nevertheless requires resolution to remain deterministic.

Smart does not mean unpredictable.

---

# 20. Symbols

Symbols represent common semantic relationships.

They can indicate:

- direction
- flow
- transformation
- mapping
- derivation
- equivalence
- dependency
- specification

For example:

```ptl
input -> parse -> validate -> output
```

The arrow is understood as a sequence relationship.

Symbols are intentionally restricted to operations where visual representation improves clarity.

---

# 21. Ranges

Ranges support readable and compact forms.

Readable:

```ptl
from 0 to 100
```

Compact:

```ptl
0 ... 100
```

Ranges can represent:

- integer spans
- indexes
- memory regions
- time intervals
- durations
- iteration bounds
- valid domains

Examples:

```ptl
from 1 to 10
```

```ptl
5 ... 20
```

```ptl
from 2 seconds to 10 seconds
```

---

# 22. Iteration

Loops are expressed as iteration.

PATL emphasizes the object or range being traversed rather than loop machinery.

```ptl
iterate items
    process item
```

Range form:

```ptl
iterate 0 ... 100
    ...
```

Pattern-directed iteration can also operate on matching values only.

```ptl
iterate users matching active
    notify user
```

---

# 23. Comparison Is Relative

PATL treats comparison as a relationship.

Comparison may consider:

- equality
- ordering
- structure
- pattern similarity
- state
- magnitude
- identity

Examples:

```ptl
compare a to b
```

or:

```ptl
a > b
```

Relative comparison allows the language to apply domain-sensitive semantics while retaining explicit resolution rules.

---

# 24. Manual Switch

PATL supports switch-like dispatch but treats it as a deliberate manual construct.

Automatic pattern recognition should normally handle simple structural branching.

Manual switching is used when the programmer specifically wants to define dispatch behavior.

Conceptually:

```ptl
switch mode
    debug
        ...
    release
        ...
    test
        ...
```

The distinction is intentional:

**recognition discovers**

**switch decides**

---

# 25. Memory Model

PATL memory revolves around **containers** and **slots**.

A container is a logical memory-holding structure.

A slot is a location within or associated with a container.

Example:

```ptl
container users
    slot current
    slot previous
```

Slots may be delegated to physical storage strategies.

---

# 26. Memory Delegation

A slot can be assigned to:

- register
- stack
- arena
- heap

For example:

```ptl
slot counter in register
slot scratch in stack
slot packet in arena network
slot database in heap
```

PATL permits the compiler to select storage automatically when no explicit placement is given.

The programmer retains the authority to override placement.

This creates two levels:

### Semantic memory

What the value represents.

### Physical memory

Where the value resides.

PATL keeps those concepts separate until physical control matters.

---

# 27. Absolute Metal Rulership

PATL retains complete low-level authority.

The programmer can control:

- allocation
- deallocation
- alignment
- representation
- registers
- memory placement
- pointer behavior
- aliasing
- layout
- calling boundaries
- bit manipulation
- raw memory
- hardware interaction

This authority is not the default syntax burden.

Instead:

> High-level control is normal. Metal-level control is available everywhere it is legitimate.

PATL therefore does not force programmers to choose between abstraction and machine control.

---

# 28. Allocation and Deallocation

Allocation is inherent.

The language understands allocation requirements from memory patterns.

Explicit control remains available.

Conceptually:

```ptl
make buffer
```

PATL can derive allocation from context.

Explicit lifetime operations can also be requested when necessary.

Blocks, allocation, and deallocation belong to the language itself rather than an external memory-management library.

---

# 29. `make`

`make` represents active construction.

```ptl
make server
make buffer
make packet
make worker
```

`make` implies that a usable entity is actively being constructed according to its definition.

It differs from assignment.

```ptl
make packet
assign data to packet
```

---

# 30. References

Pointers are unified beneath the concept:

```ptl
ref
```

PATL recognizes different reference patterns internally.

These include equivalents of:

- raw pointers
- nullable pointers
- smart pointers
- borrowed references
- owned references
- shared references

Examples:

```ptl
ref object
```

```ptl
ref? object
```

The semantic reference pattern determines guarantees and behavior.

---

# 31. Null References

Nullability must remain visible where relevant.

A nullable reference is understood as a distinct state pattern.

The language can therefore reason about:

```text
present
missing
valid
invalid
expired
owned
borrowed
```

without requiring unrelated pointer syntaxes.

---

# 32. Aliasing

Aliasing is legal and intentionally supported.

PATL does not assume all aliasing is undesirable.

The compiler tracks enough information to optimize safely where possible.

Where the programmer intentionally permits unsafe aliasing, that authority remains available.

---

# 33. Undefined Behavior

Undefined behavior is accepted as a legitimate high-performance tool.

PATL does not attempt to eliminate every possibility of programmer-induced undefined behavior.

Instead, it distinguishes:

- defined behavior
- constrained behavior
- implementation behavior
- intentionally unchecked behavior
- undefined behavior

Unsafe performance contracts remain available where they materially benefit systems programming.

They are not disguised as ordinary safe semantics.

---

# 34. Indexing

Lists, tuples, arrays, and groups use a unified indexing model.

```ptl
items[5]
```

PATL understands the structural category from the target.

Indexing can therefore apply to:

- lists
- tuples
- arrays
- groups
- memory regions
- pattern collections

Bounds behavior may be selected by context or explicitly overridden.

---

# 35. Groups

A group is a general-purpose collection pattern.

Groups may be:

- ordered
- unordered
- homogeneous
- heterogeneous
- indexed
- pattern-filtered

PATL therefore does not require a large number of surface-level collection keywords.

---

# 36. Chains

Chains connect related code blocks.

```ptl
chain request
    receive
    validate
    authorize
    process
    respond
```

A chain establishes semantic continuity.

The compiler knows these blocks belong to one computational progression.

Chains can assist with:

- data propagation
- optimization
- error flow
- ownership
- scheduling
- diagnostics

---

# 37. Smart Trees

Trees are native semantic structures.

A **smart tree** carries additional structural knowledge.

The compiler can reason about:

- parents
- children
- paths
- hierarchy
- dependency
- transformations
- inherited patterns

Smart trees are particularly suitable for:

- parsers
- syntax trees
- scene graphs
- file systems
- decision trees
- compiler IR
- hierarchical configuration

---

# 38. Lattices

Lattices extend ordinary tree relationships.

Where a tree assumes primarily hierarchical ancestry, a lattice permits overlapping and multi-directional relationships.

A value may participate in multiple related semantic paths simultaneously.

Lattices are useful for:

- dataflow
- compiler analysis
- dependency resolution
- state propagation
- knowledge systems
- pattern networks
- constraint solving

---

# 39. Error Handling

PATL's primary error model is:

```text
attempt
accept
deny
```

Example:

```ptl
attempt load file

accept file
    process file

deny error
    handle error
```

This structure treats failure as an explicit outcome rather than an invisible exception path.

---

# 40. Error Decisions Are Manual

PATL does not impose one universal philosophy of error handling.

An error can be:

### Confronted

Explicitly handled.

```ptl
confront error
```

### Bypassed

Continue without resolving it.

```ptl
bypass error
```

### Deleted

Discard it deliberately.

```ptl
delete error
```

These are conscious programmer decisions.

The compiler can warn when a consequential error path is ignored unintentionally.

---

# 41. Inference

Inference is deeply integrated.

PATL can infer:

- types
- lifetimes
- patterns
- storage
- states
- relationships
- dispatch
- transformations

However, PATL follows an important constraint:

> Inference may eliminate redundant declarations, but it may not hide meaningful semantic change.

This prevents inference from becoming semantic guesswork.

---

# 42. Reflection

Reflection is **semi-automatic by default**.

PATL can expose enough metadata to inspect:

- types
- structures
- patterns
- members
- fields
- states
- operations

The compiler determines routine reflection information automatically.

Manual reflection remains available when programmers require exact control.

This prevents ordinary reflection from becoming repetitive metadata maintenance.

---

# 43. Derivatives

A distinctive PATL feature is the **derivative**.

A derivative exists to resolve ambiguity.

It can:

- establish a rule
- clarify meaning
- choose interpretation
- constrain inference
- resolve conflicting patterns
- extrapolate from incomplete information
- establish a local semantic rule

Conceptually:

```ptl
derive packet as network packet
```

or:

```ptl
derive ambiguous value using numeric
```

Derivatives therefore tell the compiler:

> When ordinary semantic inference reaches multiple legitimate interpretations, use this rule.

They are not ordinary casts.

They are **semantic resolution instructions**.

---

# 44. `define`

`define` extends or clarifies PATL.

It can define:

- types
- patterns
- operations
- relationships
- meanings
- domain concepts
- local language rules

Example:

```ptl
define Celsius as decimal
```

More advanced:

```ptl
define warm as temperature from 20 to 30
```

PATL therefore supports controlled language extension without needing a massive core keyword vocabulary.

---

# 45. `ping`

PATL unifies searching beneath:

```ptl
ping
```

`ping` can mean:

- search
- explore
- locate
- discover
- find
- inspect

Its exact interpretation follows the target.

Examples:

```ptl
ping users for Alice
```

```ptl
ping tree for node
```

```ptl
ping memory for pattern
```

```ptl
ping files matching "*.ptl"
```

The language resolves the appropriate search operation through the target's pattern.

---

# 46. Built-In Structural Operations

PATL treats several universally useful operations as intrinsic semantic concepts rather than library conveniences.

These include:

- extraction
- injection
- inlining
- import
- export
- call
- use
- render
- allocation
- deallocation
- search
- matching
- transformation

The implementation may lower these operations to platform or runtime facilities, but the programmer does not need a library merely to express their fundamental semantics.

---

# 47. Extraction

Extraction removes meaningful data or structure from another structure.

```ptl
extract header from packet
```

Pattern extraction can simultaneously validate and destructure.

---

# 48. Injection

Injection inserts behavior or data into a compatible structure.

```ptl
inject metadata into packet
```

Injection may operate on:

- data
- code
- behavior
- patterns
- configuration

---

# 49. Inlining

Inlining is language-native.

```ptl
inline function
```

PATL permits explicit control while retaining automatic optimizer-directed inlining.

---

# 50. Imports and Exports

Import and export belong to the module model directly.

```ptl
import network
export parser
```

They do not depend upon a separate package syntax layer.

---

# 51. Calls

Calls are semantically direct.

```ptl
call render
```

Where the structure is unambiguous, normal expression usage can imply the call.

PATL does not require ceremonial function invocation syntax merely for uniformity.

---

# 52. `use`

`use` indicates intentional adoption of a capability, definition, resource, or semantic context.

```ptl
use network
use arena temporary
use pattern packet
```

---

# 53. Render

`render` transforms an internal result into its outward representation.

```ptl
render response
```

Depending on the target, rendering can mean:

- text production
- UI construction
- serialization
- graphics
- output formatting
- code generation

---

# 54. Channels

Parallelism is represented through **channels**.

Channels describe independently executable computational paths with controlled communication.

```ptl
channel decode
channel process
channel render
```

Channels can execute simultaneously where dependencies allow.

---

# 55. Lanes

Concurrency uses **lanes**.

A lane represents an independently progressing sequence.

```ptl
lane network
lane interface
lane storage
```

Multiple lanes may coexist even when they do not execute physically in parallel.

The distinction is intentional:

**lane = concurrency**

**channel = parallelism**

A channel concerns simultaneous work.

A lane concerns independently progressing work.

---

# 56. Bitwise Operations

PATL provides readable prompt-words for bitwise manipulation.

Rather than requiring punctuation-heavy notation everywhere, operations can be written using explicit bit-oriented terms.

Conceptually:

```ptl
bit and
bit or
bit xor
bit shift left
bit shift right
bit invert
```

Compact operators may still exist where they improve systems code.

The prompt-word representation remains canonical and readable.

---

# 57. Masking

Masking is inherent.

It applies to:

- bits
- values
- patterns
- fields
- structures
- permissions
- visibility

Example:

```ptl
mask flags with permission
```

The language recognizes the target domain and applies the appropriate semantics.

---

# 58. Flows

PATL flows are intended to read naturally.

```ptl
input
    recognize request
    validate
    transform
    render output
```

Or symbolically:

```ptl
input -> recognize -> validate -> transform -> output
```

Both forms describe the same conceptual flow.

The compiler treats flow as meaningful semantic information rather than simple source ordering.

---

# 59. Function-Like Behavior

PATL does not require traditional function syntax to dominate every reusable behavior.

Reusable operations can arise from:

- definitions
- patterns
- sequences
- chains
- transformations
- named operations

For example:

```ptl
define square x
    x * x
```

PATL favors semantic purpose over ceremonial function declaration.

---

# 60. Pattern-Directed Dispatch

Rather than requiring extensive overloading machinery, PATL can dispatch according to recognized patterns.

```ptl
render image
render text
render packet
```

The correct implementation follows the recognized semantic pattern.

This provides polymorphism naturally.

---

# 61. Sequence Intelligence

Because PATL understands sequences semantically, it can detect relationships across operations.

Given:

```ptl
collect input
validate input
transform input
render input
```

the compiler understands that these statements describe the lifecycle of the same conceptual entity.

This knowledge supports:

- dead-operation removal
- lifetime shortening
- register reuse
- allocation elimination
- automatic inlining
- branch reduction
- vectorization
- pipeline optimization

---

# 62. Pattern Optimization

PATL's compiler optimizes recognized computational patterns rather than only individual instructions.

For example, a familiar sequence:

```text
iterate
filter
transform
collect
```

may be recognized as one pipeline.

PATL may fuse the sequence into a single traversal where semantics permit.

Pattern recognition therefore exists not only for programmer convenience but also for optimization.

---

# 63. Metal Escape

PATL provides explicit escape into machine-level control.

A programmer may replace derived behavior with exact requirements.

For example, conceptually:

```ptl
metal
    slot x in rax
```

The surrounding program can remain high-level.

This produces PATL's central control model:

> **Derive everything routine. Specify everything critical. Permit everything legitimate.**

---

# 64. Safety Model

PATL is not built around absolute safety.

It is built around **understood control**.

The language seeks to make ordinary code robust through:

- semantic inference
- state awareness
- pattern verification
- explicit changes
- clear ownership
- reference analysis
- scope reasoning

But PATL intentionally preserves:

- raw memory
- aliasing
- unchecked access
- low-level references
- explicit allocation
- undefined behavior

when requested.

Safety is therefore **graduated rather than ideological**.

---

# 65. Grammar Philosophy

PATL's grammar follows four requirements:

### Narrow

Few constructs should perform many coherent jobs.

### Predictable

The same concept should look similar wherever it appears.

### Semantic

Syntax should represent meaning rather than compiler bookkeeping.

### Extensible

`define`, patterns, and derivatives allow the language to grow without endlessly expanding the keyword list.

---

# 66. Keyword Philosophy

PATL deliberately maintains a lean vocabulary.

Important concepts include words such as:

```text
pattern
define
collect
deposit
withdraw
recall
transform
mutate
restore
assign
attempt
accept
deny
ping
make
ref
use
import
export
render
call
channel
lane
switch
compare
derive
```

Additional semantic concepts are preferably created through composition rather than keyword proliferation.

---

# 67. PATL's Structural Character

PATL code should visually exhibit three properties:

### Vertical clarity

Indentation exposes ownership and scope.

### Horizontal relationships

Equations, smart operators, and arrows expose relationships.

### Semantic compression

Few tokens carry substantial meaning.

This produces programs that are compact without becoming cryptic.

---

# 68. Example

A small conceptual PATL program might look like:

```ptl
define User
    name text
    age integer
    state active | inactive

pattern adult
    age from 18 to 130

collect users
ping users matching adult

attempt transform users
    accept result
        render result

    deny error
        confront error
```

A systems-oriented example:

```ptl
container network
    slot packet in arena packets
    slot cursor in register

lane receive
    collect packet
    deposit packet into network

channel decode
    recognize packet
    transform packet

channel validate
    packet matches protocol

chain response
    decode -> validate -> render
```

The surface remains small.

The compiler, however, understands:

- allocation policy
- sequencing
- data dependency
- parallelism
- concurrency
- pattern constraints
- state
- structural matching
- ownership
- error propagation
- optimization opportunities

That contrast is intentional.

---

# 69. The PATL Principle

PATL's design can ultimately be reduced to one idea:

> **Programs are recognizable patterns moving through sequences of states.**

The programmer describes those patterns precisely.

The compiler recognizes their relationships.

The language derives everything that can be reliably derived.

And whenever the abstraction is insufficient, PATL gives the programmer direct authority over the machine.

PATL is therefore neither merely a pattern-matching language nor merely another systems language.

It is a **Pattern Language**:

a language in which recognition, transformation, state, sequence, structure, memory, and execution are all different expressions of the same underlying idea.

**Find the pattern. Establish the sequence. Control the result.**

## *** ##

# PATL 1.0

## Pattern Language — `.ptl`

### Formal Syntax, Executable Grammar, and Core Semantic Model

---

# 1. Language Identity

PATL is a:

**Pattern-Centric, Sequence-Oriented, Native Systems Language**

Its fundamental model is:

```text
recognize
→ relate
→ sequence
→ transform
→ resolve
```

PATL deliberately separates three layers:

```text
Surface
    what the programmer writes

Semantic Layer
    what PATL recognizes and derives

Metal Layer
    what the programmer explicitly commands
```

The surface remains small.

The semantic layer is intentionally enormous.

The metal layer retains final authority.

---

# 2. Canonical PATL Style

A PATL source file should visually look like this:

```ptl
define User struct
    name text
    age u32
    active bool = true

pattern Adult(user User)
    user.age >= 18

define greet(user Adult) -> text
    "Hello, " + user.name

define main() -> i32
    collect person = make User(
        name = "Maya",
        age = 27
    )

    when person matches Adult
        render greet(person)

    0
```

PATL uses:

- indentation for nesting
- spacing for token separation
- equations for bindings and relations
- words for semantic operations
- symbols where symbols are clearer
- punctuation only where structural ambiguity would otherwise increase

---

# 3. Source Encoding

PATL source is UTF-8.

Identifiers use Unicode XID identifier rules.

Identifiers are normalized to NFC before comparison.

Examples:

```ptl
account
packet_count
résumé
Κατάσταση
```

Keywords themselves use their ASCII spellings.

---

# 4. Indentation

Indentation is syntax.

Tabs are not permitted for indentation.

Canonical indentation is four spaces.

```ptl
when valid
    process value

    when finished
        render result
```

The lexer produces:

```text
NEWLINE
INDENT
DEDENT
```

tokens.

This keeps indentation out of the parser's semantic logic.

---

# 5. Comments

Single-line comments begin with `#`.

```ptl
# Create the initial packet.
collect packet = make Packet
```

Comments end at the newline.

Comments do not influence indentation.

---

# 6. Statement Termination

A newline normally terminates a statement.

Semicolons are unnecessary.

```ptl
collect x = 10
collect y = 20
collect result = x + y
```

Expressions enclosed inside:

```text
(...)
[...]
<...>
```

may continue across lines.

Example:

```ptl
collect user = make User(
    name = "Anna",
    age = 31,
    active = true
)
```

---

# 7. Core Literals

## Integers

```ptl
0
42
1_000_000
-92
```

Hexadecimal:

```ptl
0xFF
0x7FFF_FFFF
```

Binary:

```ptl
0b1010
0b1111_0000
```

Octal:

```ptl
0o755
```

---

# 8. Floating-Point Literals

```ptl
3.14
0.5
12.0
1.5e10
6.02e23
```

---

# 9. Text

```ptl
"Hello"
"Pattern Language"
```

Escaping:

```ptl
"\n"
"\t"
"\""
"\\"
"\u{03BB}"
```

Raw text:

```ptl
r"C:\projects\PATL\source"
```

---

# 10. Booleans

```ptl
true
false
```

`bool` is simultaneously a value type and the simplest state domain.

---

# 11. Null

PATL does not permit arbitrary nullability.

`null` exists only where the receiving type permits absence.

```ptl
collect owner ref? User = null
```

This is valid.

This is not:

```ptl
collect count i64 = null
```

---

# 12. Duration Literals

PATL has intrinsic duration quantities.

```ptl
20ns
15us
4ms
3s
10min
2h
```

Examples:

```ptl
collect timeout = 5s
collect retry_window = 100ms ... 2s
```

Durations are strongly typed.

---

# 13. Primitive Types

The core numeric types are:

```text
i8
i16
i32
i64
i128

u8
u16
u32
u64
u128

isize
usize

f32
f64

decimal
```

Other intrinsic types include:

```text
bool
text
rune
bytes
duration
void
never
any
```

PATL does not silently alter the declared semantic type of an existing binding.

---

# 14. Binding Versus Assignment

PATL deliberately distinguishes:

```text
binding
```

from:

```text
assignment
```

`=` primarily establishes a relationship or initial binding.

```ptl
collect x = 5
```

means:

> establish `x` with initial value `5`

Later replacement uses:

```ptl
assign 10 to x
```

This distinction is fundamental.

---

# 15. Variables

The canonical declaration operation is:

```ptl
collect
```

Examples:

```ptl
collect x
collect x i64
collect x = 10
collect x i64 = 10
```

Formal form:

```text
collect identifier [type] [= expression]
```

Examples:

```ptl
collect name text = "Ari"
collect count usize = 0
collect active bool = true
```

---

# 16. Assignment

Assignment is directional.

```ptl
assign 5 to x
```

Example:

```ptl
collect x i64 = 1
assign 9 to x
```

The value appears first.

The destination appears second.

This makes data direction explicit.

---

# 17. Deposit

`deposit` transfers a value into an existing storage target.

```ptl
deposit packet into queue
deposit value into container.slot
```

Unlike ordinary assignment, deposit can have ownership semantics.

For an owning destination:

```ptl
deposit packet into outgoing
```

may transfer ownership.

The compiler derives copy-versus-move behavior from the involved patterns.

---

# 18. Withdraw

`withdraw` removes a value from a location.

```ptl
withdraw packet from queue
```

With a binding:

```ptl
withdraw packet from queue as next
```

After successful ownership withdrawal, `next` owns the removed value.

---

# 19. Recall

`recall` observes or recovers a currently available value.

```ptl
collect current = recall cache
```

Unlike `withdraw`, recall does not inherently remove the value.

Its actual access mode depends on the target:

- copy for copyable values
- borrow/reference for non-copy values
- synchronization for lane results
- load for ordinary memory

---

# 20. Transform

Transformation creates a semantically changed value.

```ptl
transform input using normalize
```

Binding the result:

```ptl
transform input using normalize as normalized
```

Equivalent expression form:

```ptl
collect normalized = transform input using normalize
```

A transformation does not imply in-place mutation.

---

# 21. Mutation

`mutate` explicitly means:

> modify this existing entity.

```ptl
mutate counter using increment
```

or:

```ptl
mutate user.name using normalize_name
```

Mutation is permitted only when the current semantic case grants mutable access.

---

# 22. Restoration

`restore` reinstates a known prior or supplied state.

Explicit form:

```ptl
restore snapshot to document
```

A type can define a natural restoration source, allowing:

```ptl
restore document
```

The one-argument form is legal only when the compiler can unambiguously identify a restoration state.

Otherwise it is a compile error.

---

# 23. Structs

Structs are declared through `define`.

```ptl
define Point struct
    x f64
    y f64
```

Default fields are allowed:

```ptl
define User struct
    name text
    age u32
    active bool = true
```

Fields are declared:

```text
name type [= default]
```

---

# 24. Construction

`make` actively creates an object.

```ptl
collect origin = make Point(
    x = 0.0,
    y = 0.0
)
```

Another example:

```ptl
collect user = make User(
    name = "Maya",
    age = 28
)
```

Unspecified fields use their declared defaults.

Missing required fields are compile-time errors when construction is statically visible.

---

# 25. Struct Methods

Definitions can exist inside structs.

```ptl
define Rectangle struct
    width f64
    height f64

    define area(self ref Rectangle) -> f64
        self.width * self.height
```

Call:

```ptl
collect box = make Rectangle(
    width = 10.0,
    height = 4.0
)

render box.area()
```

The dot call is syntactic lowering of:

```ptl
area(ref box)
```

when applicable.

---

# 26. Functions

PATL does not use a separate `function` keyword.

Functions are definitions.

```ptl
define add(a i64, b i64) -> i64
    a + b
```

The final expression is the normal result.

```ptl
define square(x i64) -> i64
    x * x
```

Invocation:

```ptl
collect result = square(9)
```

---

# 27. Explicit Early Return

Most PATL functions use tail expressions.

When early termination is required:

```ptl
return expression
```

Example:

```ptl
define absolute(x i64) -> i64
    when x < 0
        return -x

    x
```

`return` is contextual rather than globally reserved.

---

# 28. Void Definitions

```ptl
define announce(message text)
    render message
```

This infers:

```text
void
```

An explicit return type can be supplied:

```ptl
define announce(message text) -> void
    render message
```

---

# 29. Generic Definitions

Generic parameters use angle brackets.

```ptl
define Box<T> struct
    value T
```

Construction:

```ptl
collect number = make Box<i64>(
    value = 42
)
```

Type inference can remove the explicit specialization:

```ptl
collect number = make Box(
    value = 42
)
```

The compiler recognizes:

```text
Box<i64>
```

---

# 30. Generic Functions

```ptl
define identity<T>(value T) -> T
    value
```

Example:

```ptl
collect a = identity(10)
collect b = identity("hello")
```

The first specialization uses `i64` or the inferred integer type.

The second uses `text`.

---

# 31. Generic Pattern Constraints

Patterns constrain generics.

```ptl
define maximum<T matches Ordered>(a T, b T) -> T
    when a > b
        a
    otherwise
        b
```

Multiple constraints:

```ptl
define process<T matches Serializable and Comparable>(value T)
    ...
```

PATL does not need a separate concept equivalent to a large conventional interface hierarchy for every generic constraint.

Patterns provide the semantic boundary.

---

# 32. Pattern Definitions

Patterns use `pattern`.

```ptl
pattern Adult(user User)
    user.age >= 18
```

Another:

```ptl
pattern Positive(value i64)
    value > 0
```

Another:

```ptl
pattern WorkingAge(user User)
    user.age from 18 to 70
```

A pattern evaluates to recognition success or failure.

Patterns can additionally narrow their input.

---

# 33. Structural Patterns

Patterns can describe structure.

```ptl
pattern Named(value)
    value.name matches text
```

This can match unrelated types that expose the required structural relationship.

For example:

```ptl
define User struct
    name text

define Company struct
    name text
```

Both can satisfy `Named`.

PATL does not require them to explicitly inherit from `Named`.

---

# 34. Pattern Matching

General form:

```ptl
value matches Pattern
```

Example:

```ptl
when user matches Adult
    render "adult"
```

Binding during recognition:

```ptl
when input matches Packet as packet
    process packet
```

The binding exists only inside the recognized scope.

---

# 35. Pattern Dispatch

PATL supports multiple definitions with the same operation name.

```ptl
define describe(value i64) -> text
    "integer"

define describe(value text) -> text
    "text"

define describe(value Adult) -> text
    "adult user"
```

Call:

```ptl
render describe(value)
```

Dispatch is selected from the argument's recognized pattern.

This is not ordinary textual overloading.

It is **pattern-directed dispatch**.

---

# 36. Dispatch Specificity

PATL chooses an implementation using semantic specificity.

The canonical order is:

```text
exact concrete pattern
explicit named pattern
structural pattern
generic constrained pattern
unconstrained generic
any
```

Two equally specific matches create a compile-time ambiguity.

PATL does not silently choose according to declaration order.

---

# 37. Derivatives

A derivative resolves an ambiguity intentionally.

Example:

```ptl
derive render when ImageLike and BinaryData as ImageLike
```

Meaning:

> When `render` receives something satisfying both of these patterns and no stronger rule exists, resolve it through `ImageLike`.

A more general form is:

```ptl
derive target when condition as resolution
```

Example:

```ptl
derive payload when header.kind == "image" as ImagePayload
```

Derivatives are part of semantic resolution.

They are not runtime casts.

---

# 38. References

All pointer-like concepts begin with:

```ptl
ref
```

Borrowed reference:

```ptl
ref User
```

Nullable reference:

```ptl
ref? User
```

Owned reference:

```ptl
ref own User
```

Shared reference:

```ptl
ref share User
```

Weak reference:

```ptl
ref weak User
```

Raw reference:

```ptl
ref raw User
```

Examples:

```ptl
collect current ref User
collect optional ref? User = null
collect owner ref own Document
collect observer ref weak Document
```

---

# 39. Default `ref` Meaning

Unqualified:

```ptl
ref T
```

means:

> scoped non-owning reference to `T`

Its lifetime is inferred.

PATL prevents an ordinary reference from outliving its target.

---

# 40. Raw References

```ptl
ref raw T
```

enters a lower guarantee level.

Example:

```ptl
collect address ref raw u8
```

Raw references permit:

- unchecked offsets
- manual lifetime relationships
- explicit aliasing
- reinterpretation where permitted
- undefined behavior

They remain visibly different from normal references.

---

# 41. Reference Mutation

PATL does not require a completely separate `mut ref` type family.

Mutability follows semantic capability.

Example:

```ptl
define increment(value ref i64)
    mutate value using + 1
```

This operation is valid only if the caller provides a reference whose current case permits mutation.

This permits context-sensitive mutability rather than permanently branding every pointer with an independent mutability taxonomy.

---

# 42. States

States can be declared directly.

```ptl
define Connection state
    disconnected
    connecting
    connected
    failed
```

State values:

```ptl
collect status Connection = disconnected
```

Transition:

```ptl
assign connecting to status
```

---

# 43. Boolean-State Relationship

Boolean expressions are state recognitions.

```ptl
ready = connected and authenticated
```

PATL therefore treats:

```ptl
when ready
```

as semantic state testing rather than an entirely separate control construct.

---

# 44. Conditionals

Canonical conditional syntax is:

```ptl
when condition
    ...
```

Example:

```ptl
when age >= 18
    render "adult"
```

Alternate branch:

```ptl
when score >= 90
    render "A"
otherwise when score >= 80
    render "B"
otherwise
    render "C"
```

---

# 45. Inline Conditionals

Short conditions may use `then`.

```ptl
when ready then render "ready"
```

Equivalent:

```ptl
when ready
    render "ready"
```

---

# 46. Situational Conditionals

PATL recognizes contextual conditional phrases.

```ptl
in case of connection == failed
    reconnect()
```

and:

```ptl
situational cache.empty
    refill(cache)
```

These lower to the same conditional IR as `when`.

`when` is the canonical spelling.

The alternatives exist where they improve domain readability.

---

# 47. Case-Based Mutation

A type can restrict a field to particular mutable situations.

```ptl
define Document struct
    title text
    body text
    revision u64

    mutable title when editing
    mutable body when editing
    mutable revision when committing
```

Then:

```ptl
case editing
    mutate document.title using trim
    mutate document.body using normalize
```

Outside that case:

```ptl
mutate document.title using trim
```

is rejected.

This is compile-time capability control whenever the case is statically knowable.

---

# 48. Iteration

The canonical loop construct is:

```ptl
iterate
```

Collection:

```ptl
iterate item in items
    render item
```

Range:

```ptl
iterate i in 0 ... 100
    process i
```

Readable range:

```ptl
iterate i in from 0 to 100
    process i
```

Conditional iteration:

```ptl
iterate while running
    update()
```

Infinite iteration:

```ptl
iterate
    service()
```

---

# 49. Range Semantics

Canonical compact range:

```ptl
0 ... 100
```

Readable equivalent:

```ptl
from 0 to 100
```

By default both endpoints are inclusive.

Half-open forms are available through pattern modifiers:

```ptl
from 0 to 100 excluding end
```

The standard index pattern is half-open:

```ptl
index from 0 to count
```

and therefore safely maps to:

```text
0 <= index < count
```

The compiler recognizes index context.

---

# 50. Duration Ranges

```ptl
collect acceptable = 50ms ... 2s
```

Pattern:

```ptl
pattern FastResponse(time duration)
    time from 0ms to 100ms
```

---

# 51. Loop Control

Contextual operations:

```ptl
break
continue
```

Example:

```ptl
iterate item in items
    when item.invalid
        continue

    when item.final
        break

    process item
```

They are contextual and do not consume global grammar outside iteration.

---

# 52. Lists

List literal:

```ptl
[1, 2, 3, 4]
```

Example:

```ptl
collect numbers = [1, 2, 3, 4]
```

Type:

```ptl
List<i64>
```

---

# 53. Arrays

Fixed array:

```ptl
collect values Array<i32, 4> = [1, 2, 3, 4]
```

Arrays have fixed extent.

Lists have dynamic extent.

---

# 54. Tuples

```ptl
collect coordinate = (10, 20)
```

Type:

```ptl
Tuple<i64, i64>
```

Indexing:

```ptl
coordinate[0]
```

Named destructuring:

```ptl
coordinate matches (x, y)
```

---

# 55. Groups

A group is a general semantic collection.

```ptl
collect workers Group<Worker>
```

Groups do not inherently promise:

- order
- contiguous storage
- unique membership

Those properties arise from additional patterns.

---

# 56. Indexing

Indexing has one visible syntax:

```ptl
items[index]
```

It applies to:

- arrays
- lists
- tuples
- groups supporting indexed access
- byte ranges
- memory blocks
- custom indexable patterns

---

# 57. Slices

Range indexing creates a view when possible:

```ptl
values[10 ... 20]
```

PATL selects:

- slice
- copied range
- view
- custom indexed result

according to the target's pattern.

Explicit extraction overrides inference.

---

# 58. Member Access

```ptl
user.name
packet.header.size
```

Method-like dispatch:

```ptl
user.label()
```

remains syntactic convenience over pattern dispatch.

---

# 59. Smart Operators

Operators are semantically resolved.

Arithmetic:

```text
+
-
*
/
%
```

Comparison:

```text
==
!=
<
<=
>
>=
```

Logical:

```text
and
or
not
```

Pattern recognition:

```text
matches
```

Range:

```text
...
```

Sequence:

```text
->
```

Meaning depends on recognized operands but must resolve to exactly one valid operation.

Ambiguous operators are compile-time errors.

---

# 60. Relative Comparison

`compare` returns ordering state instead of merely Boolean truth.

```ptl
collect relation = compare a to b
```

The result is one of:

```text
less
equal
greater
unordered
```

where the underlying pattern permits those states.

Example:

```ptl
when compare temperature to target == less
    heat()
```

---

# 61. Manual Switch

`switch` is explicitly manual dispatch.

```ptl
switch command
    case "start"
        start()

    case "stop"
        stop()

    case "restart"
        restart()

    otherwise
        render "unknown command"
```

PATL does not rewrite ordinary recognition into `switch`.

Use pattern dispatch when semantic recognition is intended.

Use `switch` when explicit programmer-selected branching is intended.

---

# 62. Containers

Containers represent logical memory ownership/layout domains.

```ptl
define Frame container
    slot width u32 in stack
    slot height u32 in stack
    slot pixels Array<Pixel> in heap
```

The container itself is semantic.

Its slots may occupy different physical memory domains.

---

# 63. Slots

General form:

```ptl
slot name type [in placement]
```

Example:

```ptl
define RequestContext container
    slot request Request in stack
    slot scratch Buffer in arena request
    slot lookup Cache in heap
    slot cursor usize in register
```

---

# 64. Slot Placements

The core placements are:

```text
stack
heap
arena
register
```

Without a placement:

```ptl
slot value Widget
```

the compiler derives placement.

Explicit placement constrains lowering.

---

# 65. Stack Slots

```ptl
slot request Request in stack
```

The value belongs to the container's stack-valid lifetime.

It cannot escape unless converted to an appropriate owned representation.

---

# 66. Heap Slots

```ptl
slot tree Tree<Node> in heap
```

The heap strategy follows the owning container or allocator policy.

PATL does not require every heap allocation to use a library API.

Heap storage is intrinsic.

---

# 67. Arenas

Create an arena:

```ptl
collect temp = make arena(4MiB)
```

Use it:

```ptl
define ParserState container
    slot tokens List<Token> in arena temp
    slot nodes List<Node> in arena temp
```

Named arenas may also be passed into construction:

```ptl
collect state = make ParserState using temp
```

Arena destruction destroys all live contained allocations according to their destruction pattern.

---

# 68. Register Slots

```ptl
slot cursor usize in register
```

This requests semantic register residency.

The ordinary PATL compiler still chooses the physical register.

If an actual hardware register is required, use `metal`.

---

# 69. Container Construction

```ptl
collect context = make RequestContext
```

Container values can expose slots:

```ptl
assign request to context.request
```

or:

```ptl
deposit request into context.request
```

The latter may transfer ownership.

---

# 70. Allocation

Normal allocation is derived from construction:

```ptl
collect user = make User
```

Explicit region control:

```ptl
collect user = make User in heap
```

```ptl
collect user = make User in arena request
```

Stack residency:

```ptl
collect user = make User in stack
```

---

# 71. Deallocation

Explicit destruction uses:

```ptl
delete value
```

Example:

```ptl
delete buffer
```

For owned managed values, PATL normally derives destruction from scope.

Explicit deletion shortens the lifetime.

Using a deleted value is invalid.

---

# 72. Error-Carrying Types

PATL has a native attempt type:

```ptl
attempt Value deny Error
```

Example:

```ptl
define read(path text) -> attempt bytes deny IOError
    ...
```

This corresponds conceptually to a typed success-or-error result without requiring an imported result container.

---

# 73. Attempt

Handling:

```ptl
attempt read(path)
    accept data
        process data

    deny error
        confront error
```

`attempt` evaluates an attempt-producing expression.

---

# 74. Accept

`accept` handles successful completion.

```ptl
attempt parse(source)
    accept tree
        render tree
```

Multiple pattern-aware accept arms are legal:

```ptl
attempt decode(packet)
    accept value matches Image
        render value

    accept value matches Text
        render value

    deny error
        confront error
```

---

# 75. Deny

`deny` handles error completion.

```ptl
attempt connect()
    accept connection
        use connection

    deny Timeout as error
        retry()

    deny error
        confront error
```

Pattern-specific error selection occurs before the general arm.

---

# 76. Error Deletion

An error may deliberately be discarded:

```ptl
deny error
    delete error
```

This explicitly means:

> consume this failure and continue.

The compiler never interprets this as accidental omission.

---

# 77. Error Bypass

```ptl
deny error
    bypass error
```

This propagates the unresolved error to the enclosing attempt-capable context.

Example:

```ptl
define load_config(path text) -> attempt Config deny IOError
    attempt read(path)
        accept data
            parse_config(data)

        deny error
            bypass error
```

---

# 78. Error Confrontation

```ptl
deny error
    confront error
        render error.message
        record error
```

A confronted error is explicitly handled.

A confrontation block must leave the surrounding path in a valid state.

---

# 79. Error Transformation

Errors can be transformed normally.

```ptl
deny error
    transform error using ConfigError as converted
    bypass converted
```

---

# 80. Chains

Chains represent a related semantic sequence.

```ptl
chain request
    receive
    validate
    authorize
    process
    render
```

Explicit flow notation is also legal:

```ptl
chain request
    receive -> validate -> authorize -> process -> render
```

Stages are resolved through callable or transform patterns.

---

# 81. Value-Carrying Chains

```ptl
chain image from source
    decode
    resize
    normalize
    encode
```

The result of each stage becomes the default input to the next.

Equivalent conceptual lowering:

```text
encode(
    normalize(
        resize(
            decode(source)
        )
    )
)
```

without requiring nested syntax.

---

# 82. Explicit Chain Mapping

When a stage requires several inputs:

```ptl
chain packet from input
    decode
    validate using schema
    encrypt using key
    send using connection
```

---

# 83. Lanes

A lane represents an independently progressing sequential computation.

```ptl
lane network
    collect response = fetch(url)
    parse response
```

The lane itself remains sequential internally.

Other lanes may progress concurrently.

---

# 84. Lane Results

The final expression of a lane becomes its result.

```ptl
lane fetch_user
    collect data = fetch("/user/42")
    parse_user(data)
```

Retrieve it using `recall`:

```ptl
collect user = recall fetch_user
```

If the lane is unfinished, recall synchronizes until the result exists.

No separate `await` keyword is required.

---

# 85. Structured Concurrency

Lanes belong to their enclosing scope.

```ptl
define load_page()
    lane profile
        load_profile()

    lane messages
        load_messages()

    collect user = recall profile
    collect inbox = recall messages

    render_page(user, inbox)
```

A normal lane cannot outlive the scope that owns it.

Escaping concurrency requires an explicitly owned scheduling object rather than accidental task leakage.

---

# 86. Channels

Channels express parallel work.

Canonical data-parallel form:

```ptl
channel decode packet in packets
    decode(packet)
```

Each `packet` may execute simultaneously with other instances.

---

# 87. Channel Example

```ptl
collect images = load_images()

channel resize image in images
    mutate image using resize_to_thumbnail
```

The channel finishes when all participating work units complete.

---

# 88. Channel Results

A channel can deposit results into a parallel-safe target.

```ptl
collect decoded Group<Frame>

channel decoder packet in packets
    collect frame = decode(packet)
    deposit frame into decoded
```

The compiler requires `decoded` to satisfy the appropriate concurrent-deposit pattern.

An unsafe shared mutation produces a compile-time diagnostic unless explicitly lowered to unchecked behavior.

---

# 89. Lanes Versus Channels

PATL gives them deliberately different meanings.

```text
lane
    concurrent independent progress

channel
    actual parallel work domain
```

A lane does not promise physical parallel execution.

A channel requests parallel execution when the target supports it.

This distinction is part of PATL's execution model.

---

# 90. Nested Parallelism

```ptl
lane loader
    collect files = load_manifest()

    channel parser file in files
        parse(file)
```

The loader progresses concurrently with surrounding lanes.

Its parser work is itself parallelized.

---

# 91. `ping`

`ping` is PATL's generalized discovery operation.

```ptl
ping collection for value
```

Examples:

```ptl
ping users for "Maya"
```

```ptl
ping tree for Node
```

```ptl
ping files matching "*.ptl"
```

```ptl
ping memory for pattern Header
```

The target's pattern determines the search mechanism.

---

# 92. Ping Binding

```ptl
ping users for "Maya" as result
```

The result type depends on the search pattern.

Explicit expected type can constrain it:

```ptl
collect user ref? User = ping users for "Maya"
```

---

# 93. Extraction

```ptl
extract header from packet
```

Binding:

```ptl
extract header from packet as h
```

Expression:

```ptl
collect h = extract header from packet
```

Extraction can combine:

- destructuring
- validation
- reference creation
- ownership transfer

depending upon the recognized pattern.

---

# 94. Injection

```ptl
inject metadata into packet
```

Code-oriented definitions may also permit:

```ptl
inject tracing into service
```

when the involved patterns define such an operation.

---

# 95. Import

```ptl
import math
import network.http
```

Alias:

```ptl
import network.http as http
```

Imports are compile-time namespace/module operations.

They are not library function calls.

---

# 96. Export

```ptl
export define User struct
    name text
```

```ptl
export define parse(source text) -> Tree
    ...
```

`export` exposes a definition through the current package/module boundary.

---

# 97. Use

`use` intentionally activates or adopts a definition or resource.

```ptl
use math
```

```ptl
use arena scratch
```

```ptl
use pattern Serializable
```

`import` makes something available.

`use` selects it into the active semantic context.

---

# 98. Render

`render` means:

> materialize an outward representation.

Examples:

```ptl
render "Hello"
```

```ptl
render document
```

```ptl
render scene
```

```ptl
render response
```

Its concrete meaning is pattern-dispatched.

For `text`, the default executable host rendering operation is standard output.

---

# 99. Calls

Conventional calls are legal:

```ptl
process(value)
```

PATL also permits:

```ptl
call process with value
```

The parenthesized form is canonical in expression contexts.

The word form is useful in sequence-heavy code.

---

# 100. Masking

Masking is intrinsic.

Bit mask:

```ptl
mask flags with permission_mask
```

Pattern mask:

```ptl
mask record with PublicFields
```

Visibility mask:

```ptl
mask document with UserView
```

Its meaning is resolved from operand patterns.

---

# 101. Bitwise Operations

Readable forms are canonical:

```ptl
bit and a with b
bit or a with b
bit xor a with b
bit invert value
bit shift value left 4
bit shift value right 2
```

Expression examples:

```ptl
collect masked = bit and flags with 0xFF
collect moved = bit shift value left 8
```

Compact forms may be enabled in metal-oriented source:

```text
&
|
^
~
<<
>>
```

The prompt-word forms remain universally valid.

---

# 102. Reflection

PATL reflection is available without importing a reflection library.

```ptl
ping type User
```

```ptl
ping fields of User
```

```ptl
ping patterns of value
```

Semi-automatic reflection metadata is generated for normal definitions.

Exact metadata can be overridden or masked.

---

# 103. Automatic Inlining

Inlining is ordinarily compiler-selected.

Manual request:

```ptl
inline define clamp(value i64, low i64, high i64) -> i64
    ...
```

Or at a call site:

```ptl
inline clamp(value, 0, 100)
```

This is a strong optimization directive unless target limitations prevent legal lowering.

---

# 104. Undefined Behavior

PATL accepts intentional undefined behavior as part of low-level programming.

Ordinary semantic PATL operations retain their specified behavior.

Undefined behavior arises from explicitly low-guarantee actions such as:

- invalid `ref raw`
- illegal metal memory access
- violating explicitly unchecked alias contracts
- invalid unchecked index access
- broken foreign ABI obligations

The compiler is not required to preserve sensible behavior after undefined behavior occurs.

---

# 105. Direct Metal

The direct-machine construct is:

```ptl
metal
```

Target-qualified form:

```ptl
metal x86_64
```

A metal block establishes an explicit low-level boundary.

---

# 106. Metal Function Example

```ptl
define add_fast(a u64, b u64) -> u64
    metal x86_64(a -> rcx, b -> rdx) -> rax
        mov rax, rcx
        add rax, rdx
```

The header means:

```text
PATL a enters RCX
PATL b enters RDX
function result leaves RAX
```

The indented body is parsed by the registered `x86_64` metal grammar rather than ordinary PATL expression grammar.

---

# 107. Clobbers

```ptl
define multiply_fast(a u64, b u64) -> u64
    metal x86_64(a -> rax, b -> rcx) -> rax
        clobber rdx
        clobber flags

        mul rcx
```

PATL verifies the declared machine effects against the surrounding high-level context.

---

# 108. Memory Through Metal

```ptl
define first_byte(data ref raw u8) -> u8
    metal x86_64(data -> rsi) -> al
        mov al, byte [rsi]
```

The operation is intentionally capable of undefined behavior when the supplied address is invalid.

PATL does not pretend otherwise.

---

# 109. Metal Is Not Inline-Assembly String Injection

The compiler understands:

```text
target
inputs
outputs
clobbers
memory effects
control effects
```

around the raw instruction region.

Therefore this:

```ptl
metal x86_64(...)
```

is still part of PATL's semantic model.

Only the actual machine instruction body becomes architecture-specific.

---

# 110. Complete Generic Example

```ptl
pattern Ordered(value)
    value supports compare

define maximum<T matches Ordered>(a T, b T) -> T
    when compare a to b == greater
        a
    otherwise
        b

define main() -> i32
    collect answer = maximum(40, 91)
    render answer
    0
```

---

# 111. Complete Pattern Dispatch Example

```ptl
define Circle struct
    radius f64

define Rectangle struct
    width f64
    height f64

pattern Shape(value)
    value matches Circle or value matches Rectangle

define area(shape Circle) -> f64
    3.141592653589793 * shape.radius * shape.radius

define area(shape Rectangle) -> f64
    shape.width * shape.height

define main() -> i32
    collect a = make Circle(radius = 5.0)

    collect b = make Rectangle(
        width = 10.0,
        height = 4.0
    )

    render area(a)
    render area(b)

    0
```

---

# 112. Complete Reference Example

```ptl
define Counter struct
    value i64

define increment(counter ref Counter)
    mutate counter.value using value -> value + 1

define main() -> i32
    collect counter = make Counter(value = 0)

    increment(ref counter)
    increment(ref counter)
    increment(ref counter)

    render counter.value

    0
```

Expected result:

```text
3
```

---

# 113. Nullable Reference Example

```ptl
define Node struct
    value i64
    next ref? Node = null

define print_next(node ref Node)
    when node.next != null
        render node.next.value
    otherwise
        render "none"
```

Recognition of:

```ptl
node.next != null
```

narrows `node.next` from:

```text
ref? Node
```

to:

```text
ref Node
```

inside the recognized branch.

---

# 114. Container Example

```ptl
define DecoderMemory container
    slot input bytes in stack
    slot cursor usize in register
    slot scratch bytes in arena decoder
    slot output bytes in heap

define decode(input bytes) -> bytes
    collect decoder = make arena(8MiB)

    collect memory = make DecoderMemory using decoder

    assign input to memory.input
    assign 0 to memory.cursor

    transform memory.input using decode_stream as result

    assign result to memory.output

    memory.output
```

---

# 115. Attempt Example

```ptl
define load_user(id u64) -> attempt User deny DatabaseError
    attempt database.find(id)
        accept record
            make User(
                name = record.name,
                age = record.age
            )

        deny error
            bypass error
```

Calling code:

```ptl
define main() -> i32
    attempt load_user(42)
        accept user
            render user.name

        deny NotFound as error
            render "User not found"
            delete error

        deny error
            confront error
                render error.message

    0
```

---

# 116. Lane Example

```ptl
define load_dashboard(user_id u64) -> Dashboard
    lane profile
        load_profile(user_id)

    lane notifications
        load_notifications(user_id)

    lane statistics
        load_statistics(user_id)

    collect user = recall profile
    collect notices = recall notifications
    collect stats = recall statistics

    make Dashboard(
        user = user,
        notifications = notices,
        statistics = stats
    )
```

There is no `async`.

There is no `await`.

The lane declares concurrency.

`recall` expresses the point at which its result is needed.

---

# 117. Channel Example

```ptl
define convert(images List<Image>) -> List<Thumbnail>
    collect output ConcurrentList<Thumbnail>

    channel thumbnails image in images
        collect thumbnail = resize(image, 256, 256)
        deposit thumbnail into output

    output.to_list()
```

The data-parallel intent is structural and explicit.

---

# 118. Lane and Channel Together

```ptl
define build_gallery(paths List<text>) -> Gallery
    lane metadata
        load_gallery_metadata()

    lane imagery
        collect images ConcurrentList<Image>

        channel loading path in paths
            collect image = load_image(path)
            deposit image into images

        images

    collect info = recall metadata
    collect loaded = recall imagery

    make Gallery(
        metadata = info,
        images = loaded
    )
```

---

# 119. Chain Example

```ptl
define process_request(request Request) -> Response
    chain request from request
        parse
        validate
        authorize
        execute
        serialize
```

The compiler can see this as one semantic pipeline.

It can therefore perform transformations such as:

```text
stage fusion
temporary elimination
lifetime shortening
branch simplification
allocation removal
register forwarding
inlining
vectorization
```

when legal.

---

# 120. Pattern-Aware Parser Example

```ptl
define Token struct
    kind TokenKind
    text text

pattern NumberToken(token Token)
    token.kind == number

pattern NameToken(token Token)
    token.kind == identifier

define parse(token NumberToken) -> Expression
    make NumberExpression(
        value = convert<i64>(token.text)
    )

define parse(token NameToken) -> Expression
    make NameExpression(
        name = token.text
    )
```

This is PATL's pattern dispatch doing the work that many languages distribute across:

- visitor patterns
- type switches
- overload tables
- enum dispatch
- explicit casts

---

# 121. Ping Example

```ptl
define find_admin(users List<User>) -> ref? User
    ping users matching user -> user.role == admin
```

Another:

```ptl
collect matches = ping filesystem for "*.ptl"
```

Another:

```ptl
collect nodes = ping syntax_tree matching FunctionDefinition
```

One verb covers semantic search without implying one underlying algorithm.

---

# 122. Direct Systems Example

```ptl
define MemoryBlock struct
    address ref raw u8
    size usize

define clear(block MemoryBlock)
    metal x86_64(
        block.address -> rdi,
        block.size -> rcx
    )
        xor eax, eax
        rep stosb
```

PATL sees:

```text
MemoryBlock
```

Metal sees:

```text
RDI = address
RCX = size
AL  = zero
REP STOSB
```

The transition is explicit and narrow.

---

# 123. Executable Hello World

The complete PATL program:

```ptl
define main() -> i32
    render "Hello, world."
    0
```

Nothing else is required.

---

# 124. Executable Fibonacci

```ptl
define fibonacci(n u64) -> u64
    when n <= 1
        return n

    fibonacci(n - 1) + fibonacci(n - 2)

define main() -> i32
    iterate n in 0 ... 10
        render fibonacci(n)

    0
```

---

# 125. Executable Iterative Fibonacci

```ptl
define fibonacci(n u64) -> u64
    when n <= 1
        return n

    collect a u64 = 0
    collect b u64 = 1

    iterate i in 2 ... n
        collect next = a + b
        assign b to a
        assign next to b

    b
```

PATL recognizes the assignments as state transitions rather than new bindings.

---

# 126. Formal Core Grammar

The following grammar uses:

```text
NEWLINE
INDENT
DEDENT
```

provided by the lexer.

EBNF:

```text
program
    ::= NEWLINE* top_level* EOF


top_level
    ::= import_decl
     | export_decl
     | definition
     | pattern_decl
     | derive_decl
     | top_statement


import_decl
    ::= "import" qualified_name alias_clause? NEWLINE


alias_clause
    ::= "as" identifier


export_decl
    ::= "export" (
           definition
         | pattern_decl
       )


definition
    ::= function_def
     | struct_def
     | state_def
     | container_def


function_def
    ::= modifier*
        "define"
        identifier
        generic_params?
        "(" parameter_list? ")"
        return_clause?
        NEWLINE
        INDENT
        statement*
        DEDENT


modifier
    ::= "inline"


generic_params
    ::= "<" generic_param ("," generic_param)* ">"


generic_param
    ::= identifier generic_constraint?


generic_constraint
    ::= "matches" pattern_expression


parameter_list
    ::= parameter ("," parameter)*


parameter
    ::= identifier type


return_clause
    ::= "->" type


struct_def
    ::= "define"
        identifier
        generic_params?
        "struct"
        NEWLINE
        INDENT
        struct_member*
        DEDENT


struct_member
    ::= field_decl
     | function_def
     | mutable_rule


field_decl
    ::= identifier type default_clause? NEWLINE


default_clause
    ::= "=" expression


mutable_rule
    ::= "mutable"
        target
        "when"
        expression
        NEWLINE


state_def
    ::= "define"
        identifier
        "state"
        NEWLINE
        INDENT
        state_member+
        DEDENT


state_member
    ::= identifier type_arguments? NEWLINE


container_def
    ::= "define"
        identifier
        generic_params?
        "container"
        NEWLINE
        INDENT
        slot_decl+
        DEDENT


slot_decl
    ::= "slot"
        identifier
        type
        placement_clause?
        NEWLINE


placement_clause
    ::= "in" placement


placement
    ::= "stack"
     | "heap"
     | "register"
     | "arena" identifier


pattern_decl
    ::= "pattern"
        identifier
        generic_params?
        "(" parameter_list? ")"
        NEWLINE
        INDENT
        pattern_body
        DEDENT


pattern_body
    ::= statement* expression NEWLINE
     | pattern_statement+


derive_decl
    ::= "derive"
        qualified_name
        "when"
        expression
        "as"
        qualified_name
        NEWLINE


statement
    ::= collect_stmt
     | assign_stmt
     | deposit_stmt
     | withdraw_stmt
     | transform_stmt
     | mutate_stmt
     | restore_stmt
     | delete_stmt
     | bypass_stmt
     | return_stmt
     | render_stmt
     | use_stmt
     | import_decl
     | attempt_stmt
     | when_stmt
     | switch_stmt
     | iterate_stmt
     | lane_stmt
     | channel_stmt
     | chain_stmt
     | metal_stmt
     | expression_stmt
     | break_stmt
     | continue_stmt


top_statement
    ::= statement


collect_stmt
    ::= "collect"
        identifier
        type?
        initializer?
        NEWLINE


initializer
    ::= "=" expression


assign_stmt
    ::= "assign"
        expression
        "to"
        target
        NEWLINE


deposit_stmt
    ::= "deposit"
        expression
        "into"
        target
        NEWLINE


withdraw_stmt
    ::= "withdraw"
        expression
        "from"
        target
        ("as" identifier)?
        NEWLINE


transform_stmt
    ::= "transform"
        expression
        "using"
        expression
        ("as" identifier)?
        NEWLINE


mutate_stmt
    ::= "mutate"
        target
        "using"
        expression
        NEWLINE


restore_stmt
    ::= "restore"
        expression
        ("to" target)?
        NEWLINE


delete_stmt
    ::= "delete"
        expression
        NEWLINE


bypass_stmt
    ::= "bypass"
        expression
        NEWLINE


return_stmt
    ::= "return"
        expression?
        NEWLINE


render_stmt
    ::= "render"
        expression
        NEWLINE


use_stmt
    ::= "use"
        expression
        NEWLINE


when_stmt
    ::= "when"
        expression
        inline_then?
        NEWLINE?
        conditional_body
        otherwise_clause*


inline_then
    ::= "then" statement_without_newline


conditional_body
    ::= NEWLINE INDENT statement* DEDENT


otherwise_clause
    ::= "otherwise"
        ("when" expression)?
        NEWLINE
        INDENT
        statement*
        DEDENT


switch_stmt
    ::= "switch"
        expression
        NEWLINE
        INDENT
        switch_case+
        otherwise_switch?
        DEDENT


switch_case
    ::= "case"
        expression
        NEWLINE
        INDENT
        statement*
        DEDENT


otherwise_switch
    ::= "otherwise"
        NEWLINE
        INDENT
        statement*
        DEDENT


iterate_stmt
    ::= "iterate"
        iteration_spec?
        NEWLINE
        INDENT
        statement*
        DEDENT


iteration_spec
    ::= identifier "in" expression
     | "while" expression


break_stmt
    ::= "break" NEWLINE


continue_stmt
    ::= "continue" NEWLINE


attempt_stmt
    ::= "attempt"
        expression
        NEWLINE
        INDENT
        attempt_arm+
        DEDENT


attempt_arm
    ::= accept_arm
     | deny_arm


accept_arm
    ::= "accept"
        accept_pattern?
        NEWLINE
        INDENT
        statement*
        DEDENT


accept_pattern
    ::= identifier
     | identifier "matches" pattern_expression
     | pattern_expression "as" identifier


deny_arm
    ::= "deny"
        deny_pattern?
        NEWLINE
        INDENT
        statement*
        DEDENT


deny_pattern
    ::= identifier
     | pattern_expression "as" identifier


lane_stmt
    ::= "lane"
        identifier
        NEWLINE
        INDENT
        statement*
        DEDENT


channel_stmt
    ::= "channel"
        identifier
        identifier
        "in"
        expression
        NEWLINE
        INDENT
        statement*
        DEDENT


chain_stmt
    ::= "chain"
        identifier
        ("from" expression)?
        NEWLINE
        INDENT
        chain_body
        DEDENT


chain_body
    ::= chain_stage*
     | chain_sequence NEWLINE


chain_stage
    ::= expression NEWLINE


chain_sequence
    ::= expression ("->" expression)+


metal_stmt
    ::= "metal"
        target_name
        metal_signature?
        NEWLINE
        INDENT
        metal_line*
        DEDENT


metal_signature
    ::= "(" metal_binding_list? ")"
        ("->" metal_location)?


metal_binding_list
    ::= metal_binding ("," metal_binding)*


metal_binding
    ::= expression "->" metal_location


metal_location
    ::= identifier


metal_line
    ::= TARGET_SPECIFIC_TOKENS NEWLINE


expression_stmt
    ::= expression NEWLINE
```

---

# 127. Expression Grammar

```text
expression
    ::= logical_or


logical_or
    ::= logical_and ("or" logical_and)*


logical_and
    ::= recognition ("and" recognition)*


recognition
    ::= comparison
        ("matches" pattern_expression ("as" identifier)?)?


comparison
    ::= range_expression
        (
          "==" range_expression
        | "!=" range_expression
        | "<"  range_expression
        | "<=" range_expression
        | ">"  range_expression
        | ">=" range_expression
        )*


range_expression
    ::= additive
        ("..." additive)?
     | "from" additive "to" additive


additive
    ::= multiplicative
        (("+" | "-") multiplicative)*


multiplicative
    ::= unary
        (("*" | "/" | "%") unary)*


unary
    ::= ("-" | "+" | "not") unary
     | reference_expression
     | primary


reference_expression
    ::= "ref" primary


primary
    ::= literal
     | identifier
     | qualified_name
     | call_expression
     | make_expression
     | recall_expression
     | ping_expression
     | extract_expression
     | transform_expression
     | compare_expression
     | bit_expression
     | "(" expression ")"
     | list_literal
     | tuple_literal


call_expression
    ::= postfix "(" argument_list? ")"


postfix
    ::= primary_base postfix_op*


postfix_op
    ::= "." identifier
     | "[" expression "]"


make_expression
    ::= "make"
        type_reference
        constructor_args?
        placement_clause?
        ("using" expression)?


recall_expression
    ::= "recall" expression


ping_expression
    ::= "ping"
        expression
        (
            "for" expression
          | "matching" expression
        )


extract_expression
    ::= "extract"
        expression
        "from"
        expression


transform_expression
    ::= "transform"
        expression
        "using"
        expression


compare_expression
    ::= "compare"
        expression
        "to"
        expression


argument_list
    ::= argument ("," argument)*


argument
    ::= expression
     | identifier "=" expression
```

---

# 128. Type Grammar

```text
type
    ::= type_reference
     | reference_type
     | attempt_type
     | tuple_type


type_reference
    ::= qualified_name type_arguments?


type_arguments
    ::= "<" type_argument ("," type_argument)* ">"


type_argument
    ::= type
     | integer_literal


reference_type
    ::= "ref" reference_mode? nullable? type


reference_mode
    ::= "own"
     | "share"
     | "weak"
     | "raw"


nullable
    ::= "?"


attempt_type
    ::= "attempt"
        type
        "deny"
        type


tuple_type
    ::= "Tuple"
        "<"
        type
        ("," type)+
        ">"
```

Canonical nullable spelling remains:

```ptl
ref? User
```

although the parser internally tokenizes this as:

```text
REF QUESTION TYPE
```

---

# 129. Literal Grammar

```text
literal
    ::= integer_literal
     | float_literal
     | text_literal
     | rune_literal
     | duration_literal
     | boolean_literal
     | "null"


boolean_literal
    ::= "true"
     | "false"
```

---

# 130. Operator Precedence

Highest to lowest:

```text
member access / indexing / call
unary
multiplication / division / remainder
addition / subtraction
range
comparison
matches
and
or
```

Assignment is not an expression operator.

That means PATL intentionally rejects:

```ptl
x = y = 5
```

Value replacement must say:

```ptl
assign 5 to y
assign y to x
```

The distinction prevents accidental assignment inside conditions.

---

# 131. Tail Values

The final expression of a value-producing block becomes its value.

Example:

```ptl
define double(x i64) -> i64
    x * 2
```

PATL therefore does not require:

```ptl
return x * 2
```

unless early termination is desired.

The same applies to:

- functions
- lanes
- selected pattern transformations
- expression-capable blocks

---

# 132. Scope

Every indentation block establishes intrinsic lexical scope.

Example:

```ptl
when ready
    collect temp = 5
    render temp
```

This is illegal afterward:

```ptl
render temp
```

unless `temp` was explicitly exported from the block through its result.

---

# 133. Shadowing

PATL does not silently shadow an existing name in the same semantic sequence.

This:

```ptl
collect value = 5

when ready
    collect value = 10
```

produces a diagnostic.

Explicit semantic replacement uses:

```ptl
assign 10 to value
```

A deliberately independent nested binding requires qualification or explicit derivation.

This prevents thin syntax from hiding variable identity changes.

---

# 134. Dynamic Explicitness

Consider:

```ptl
collect value = 5
```

PATL infers an integer type.

This is invalid:

```ptl
assign "five" to value
```

A change in semantic definition must be explicit.

Example:

```ptl
transform value using to_text as text_value
```

or:

```ptl
collect text_value text = transform value using to_text
```

PATL infers aggressively.

PATL does not silently redefine identity.

---

# 135. Pattern Recognition and Type Narrowing

```ptl
collect value any = source()

when value matches User as user
    render user.name
```

Inside the block:

```text
user : User
```

There is no cast.

Recognition establishes the narrowed semantic identity.

---

# 136. Pattern Exhaustiveness

Where the compiler can prove a finite state domain, PATL checks exhaustiveness.

Example:

```ptl
define Status state
    idle
    running
    stopped
```

Then:

```ptl
switch status
    case idle
        ...
    case running
        ...
```

produces a diagnostic because `stopped` is unhandled.

An `otherwise` branch makes it exhaustive.

---

# 137. Smart Trees

PATL's built-in tree relationship can be expressed through:

```ptl
Tree<Node>
```

A node can participate in compiler-known:

```text
parent
children
root
path
depth
```

patterns.

Example:

```ptl
ping syntax_tree matching FunctionDefinition
```

No tree-search library is needed merely to express the operation.

---

# 138. Lattices

Lattices allow multiply-related nodes.

```ptl
Lattice<State>
```

Example:

```ptl
collect flow Lattice<Block>
```

PATL may use lattice reasoning for:

- dataflow
- compiler IR
- state analysis
- dependency propagation
- constraint solving

The language semantics remain more general than one fixed implementation.

---

# 139. Sequence Semantics

Consider:

```ptl
collect request = receive()
validate(request)
authorize(request)
process(request)
render request
```

PATL does not view these merely as unrelated statements.

The semantic analyzer establishes:

```text
request₀
  ↓ validate
request₁
  ↓ authorize
request₂
  ↓ process
request₃
  ↓ render
```

where transformations exist.

This permits sequence-sensitive optimization and diagnostics.

---

# 140. Sequence-Oriented Optimization

Because semantic sequence is explicit, the optimizer can recognize:

```ptl
iterate item in values
    when item matches Valid
        transform item using normalize as result
        deposit result into output
```

as one pattern:

```text
source
→ filter
→ transform
→ collect
```

The compiler may legally lower it into one fused machine loop.

---

# 141. Pattern IR

A practical PATL compiler should lower source into a semantic representation resembling:

```text
PATL Source
    ↓
Lexical Tokens
    ↓
Indentation Tree
    ↓
AST
    ↓
Pattern Resolution
    ↓
Sequence Graph
    ↓
Type / State / Ownership Resolution
    ↓
PIR
    ↓
Machine-Oriented IR
    ↓
Backend
```

The middle representation can be called:

**PIR — Pattern Intermediate Representation**

PIR should explicitly represent:

- recognized pattern
- sequence identity
- state
- ownership
- memory placement
- reference guarantees
- concurrency
- parallel domains
- error edges
- dispatch candidates
- derivatives
- metal boundaries

This is where PATL becomes substantially more powerful than its surface grammar suggests.

---

# 142. Canonical Compiler Pipeline

A production PATL compiler therefore follows:

```text
.ptl
 ↓
scanner
 ↓
offside lexer
 ↓
parser
 ↓
structural AST
 ↓
semantic pattern engine
 ↓
PIR
 ↓
sequence optimization
 ↓
memory placement
 ↓
parallel/concurrency lowering
 ↓
target IR
 ↓
machine optimization
 ↓
object code
 ↓
native executable/library
```

PATL's sophistication belongs primarily between:

```text
AST
```

and:

```text
target IR
```

—not in the source syntax.

---

# 143. Minimal Keyword Model

PATL's permanently structural words remain relatively small:

```text
define
pattern
struct
state
container
slot
collect
assign
attempt
accept
deny
when
otherwise
iterate
lane
channel
chain
ref
metal
make
derive
switch
```

Words such as:

```text
to
from
into
with
using
as
in
matches
case
then
mutable
return
break
continue
render
ping
transform
mutate
restore
deposit
withdraw
recall
extract
inject
import
export
use
delete
bypass
confront
```

can be implemented primarily as **contextual keywords**.

They remain valid ordinary identifiers where their grammatical role cannot be confused.

This keeps PATL's truly reserved vocabulary narrow.

---

# 144. Full Example Program

```ptl
import network.http as http

define User struct
    id u64
    name text
    age u32
    active bool = true

pattern Adult(user User)
    user.age >= 18

pattern ActiveAdult(user User)
    user matches Adult and user.active

define UserCache container
    slot users List<User> in heap
    slot cursor usize in register
    slot scratch bytes in arena cache

define decode_user(data bytes) -> attempt User deny DecodeError
    attempt decode_json(data)
        accept object
            make User(
                id = object.id,
                name = object.name,
                age = object.age,
                active = object.active
            )

        deny error
            transform error using DecodeError as converted
            bypass converted

define fetch_user(id u64) -> attempt User deny NetworkError
    attempt http.get("/users/" + id)
        accept response
            decode_user(response.body)

        deny error
            bypass error

define label(user ActiveAdult) -> text
    user.name + " — active adult"

define label(user User) -> text
    user.name

define load_users(ids List<u64>) -> List<User>
    collect users ConcurrentList<User>

    channel loading id in ids
        attempt fetch_user(id)
            accept user
                deposit user into users

            deny NotFound as error
                delete error

            deny error
                confront error
                    render error.message

    users.to_list()

define main() -> i32
    collect ids = [10, 11, 12, 13, 14]

    lane loading
        load_users(ids)

    lane banner
        render "PATL Pattern Service"

    collect users = recall loading
    recall banner

    iterate user in users
        render label(user)

    0
```

That program demonstrates:

```text
imports
structs
patterns
pattern inheritance/composition
containers
slots
heap placement
arena placement
register placement
typed errors
attempt
accept
deny
error conversion
pattern dispatch
channels
lanes
recall synchronization
iteration
rendering
generic collections
sequence-oriented execution
```

while still using a comparatively small grammatical surface.

---

# 145. PATL's Central Syntax Rule

PATL should reject the temptation to continuously add syntax whenever the semantic engine gains a feature.

The hierarchy is:

```text
Can a known pattern express it?
    use the pattern

Can a contextual word clarify it?
    use the word

Can an existing relation express it?
    use the relation

Is direct control genuinely necessary?
    expose it explicitly

Only then:
    add syntax
```

This protects PATL from becoming punctuation-heavy or keyword-heavy as the language matures.

---

# 146. Final Language Shape

PATL source stays narrow enough that a programmer encounters code such as:

```ptl
define normalize<T matches Numeric>(value T) -> T
    value / maximum(value)

pattern ValidPacket(packet Packet)
    packet.size > 0 and packet.checksum == calculate(packet)

define receive() -> attempt Packet deny NetworkError
    ...

define process(packet ValidPacket)
    transform packet using decode as data
    render data

define main() -> i32
    attempt receive()
        accept packet matches ValidPacket
            process(packet)

        accept packet
            render "invalid packet"

        deny error
            confront error
                render error

    0
```

Yet below those few constructs the compiler understands:

```text
type identity
pattern identity
structural recognition
state
ownership
aliasing
lifetimes
reference validity
memory placement
error edges
sequence relationships
dispatch specificity
inference
generic specialization
control flow
dataflow
parallel domains
concurrent lanes
allocation
deallocation
optimization opportunity
target architecture
metal boundaries
```

That is the defining architectural achievement of PATL.

The programmer does not write the compiler's bookkeeping.

The programmer writes the **pattern of the computation**.

PATL determines the mechanical form until the programmer explicitly takes control.

## PATL

**Recognize the pattern.  
Sequence the work.  
Command the machine.**

## *** ##

