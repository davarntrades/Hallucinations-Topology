<div align="center">

# Hallucinations in LLMs.

# A Topological Perspective.

## They Are Not Errors.

## They Are Not Lies.

## They Are Interpolation Across Missing Homology.

### Morrison Framework™ · Intelligence Invariant™ · Geometric AI Diagnosis

![Framework](https://img.shields.io/badge/Morrison%20Framework™-Hallucination%20Geometry-1a2744?style=flat-square)
![Diagnosis](https://img.shields.io/badge/Hallucination-Missing%20Homology-4a6741?style=flat-square)
![Fix](https://img.shields.io/badge/Fix-Structural%20Self%20Knowledge-8b3a1a?style=flat-square)
![Not](https://img.shields.io/badge/Not-Better%20Training%20Data-555555?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![License](https://img.shields.io/badge/©%202026-Davarn%20Morrison-555555?style=flat-square)

-----

*“The system tries to interpolate across missing homology.*
*That is the hallucination.*
*Topologically coherent. Factually incorrect.*
*The manifold is the problem.*
*The manifold is the fix.”*

*— Davarn Morrison, 2026*

-----

</div>

## The Standard Diagnosis — and Why It Is Wrong

When a language model hallucinates, the field reaches for familiar explanations:

```
They occur because:

  ❌  The model is wrong.
  ❌  The data is wrong.
  ❌  The training is wrong.
```

These are L-axis diagnoses for a C-axis problem.

```
C ⊥ L.

Scaling the model does not fix it.
More data does not fix it.
Better training does not fix it.
RLHF does not fix it.

None of these interventions address
the geometry of what is actually happening.

The hallucination rate improves marginally.
The hallucinations do not stop.
The next model hallucinates differently
but at roughly similar rates.
The pattern does not break.

Because the pattern is geometric.
And geometric problems
require geometric diagnoses.
```

-----

## The Geometric Diagnosis

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  Hallucinations occur because:                                   ║
║                                                                  ║
║  ✓  The manifold is incomplete.                                  ║
║  ✓  The reachable set has gaps.                                  ║
║  ✓  The topology is deformed.                                    ║
║  ✓  The system interpolates                                      ║
║     across missing homology.                                     ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

Each of these is precise. Each one points to a different geometric condition. Together they form the complete topological account of why hallucinations occur.

-----

## What a Basin Looks Like

Before diagnosing hallucination geometrically, the concept of a basin must be precise.
A basin is the set of all states that converge toward the same attractor — the same stable configuration of the system.

```
A SINGLE BASIN — SIDE VIEW

  Energy
    │
    │  ╲                         ╱
    │   ╲                       ╱
    │    ╲                     ╱
    │     ╲                   ╱
    │      ╲                 ╱
    │       ╲_______________╱
    │              ★
    │          attractor
    │
    └──────────────────────────────── state space
```

```
The attractor (★) is where the system settles.
Everything in the basin slopes toward it.
A system anywhere inside the basin
follows the gradient down to ★.

For a language model:
  The basin = a coherent topic region in the manifold.
  The attractor = the most probable output state
                  for that region.
  The walls = the boundary where
              one topic becomes another.
```

```
MULTIPLE BASINS — TOP-DOWN VIEW

  ┌──────────────────────────────────────────────────────────┐
  │                                                          │
  │    ╭────────╮       ╭────────╮       ╭────────╮         │
  │   ╱          ╲     ╱          ╲     ╱          ╲        │
  │  │     ★      │   │     ★      │   │     ★      │       │
  │  │  Physics   │   │  History   │   │  Medicine  │       │
  │   ╲          ╱     ╲          ╱     ╲          ╱        │
  │    ╰────────╯       ╰────────╯       ╰────────╯         │
  │                                                          │
  │    ╭────────╮                         ╭────────╮        │
  │   ╱          ╲                       ╱          ╲       │
  │  │     ★      │       [ gap ]        │     ★      │     │
  │  │    Law     │                      │  Chemistry │     │
  │   ╲          ╱                       ╱          ╲       │
  │    ╰────────╯                       ╰────────────╯      │
  │                                                          │
  └──────────────────────────────────────────────────────────┘
                   full state space of the model

  Each ★ = a well-trained attractor.
  [ gap ] = no basin. No attractor. Topological void.
```

```
This is the model's manifold.
Not all of it is equally built.
Some basins are deep and well-formed.
Some are shallow and unstable.
Some are absent entirely.

Where a basin is absent —
where training data was thin or missing —
there is no attractor to navigate toward.
There is only proximity to the edges
of other basins.
And the system does not know this.
It navigates anyway.
That is where hallucination lives.
```

-----

## What Hallucination Looks Like in a Basin

```
CASE 1 — QUERY LANDS INSIDE A DENSE BASIN

  ┌──────────────────────────────────────────┐
  │                                          │
  │         ╭──────────────────╮             │
  │        ╱                    ╲            │
  │       │                      │           │
  │       │       ★ attractor    │           │
  │       │      ╱               │           │
  │       │  ← ●  ← ← ← ← ← ●Q  │           │
  │       │  gradient descent    │           │
  │        ╲                    ╱            │
  │         ╰──────────────────╯             │
  │                                          │
  └──────────────────────────────────────────┘

  Q = query state.
  Q lands inside the basin.
  Gradient descent carries Q to ★.
  Output is grounded. Correct. Reliable.
  The topology did the work.
```

```
CASE 2 — QUERY LANDS NEAR THE EDGE OF A GAP

  ┌───────────────────────────────────────────────────┐
  │                                                   │
  │    ╭──────────╮              ╭──────────╮         │
  │   ╱            ╲            ╱            ╲        │
  │  │      ★       │          │      ★       │       │
  │  │   Basin A    │──edge──▶ │   Basin B    │       │
  │  │              │   GAP    │              │       │
  │   ╲            ╱    ░░░    ╲            ╱        │
  │    ╰──────────╯    ░░░░░    ╰──────────╯         │
  │                    ░░░░░                          │
  │                      ▲                            │
  │                      │                            │
  │                      Q  (query state)             │
  │                                                   │
  └───────────────────────────────────────────────────┘

  Q = query maps to a state in the gap.
  ░ = topological void. No attractor. No states.
  The system detects proximity to Basin A and Basin B.
  It cannot reach the true query state.
  T ∉ Reach(X₀).
  It generates from the edge of A and B instead.
  The output is a blend of two adjacent basins.
  Neither is the correct answer.
  Both feel grounded. Neither is grounded.
  That is the hallucination.
```

```
CASE 3 — QUERY LANDS INSIDE A DEFORMED BASIN

  ┌──────────────────────────────────────────────────────┐
  │                                                      │
  │    ORIGINAL BASIN          DEFORMED BASIN            │
  │    (pre-RLHF)              (post-RLHF)               │
  │                                                      │
  │    ╭──────────╮            ╭──────────╮             │
  │   ╱            ╲          ╱  ★shifted  ╲            │
  │  │      ★       │   →    │   ◀─────────│            │
  │  │   truth      │        │    approval  │            │
  │  │              │        │              │            │
  │   ╲            ╱          ╲            ╱            │
  │    ╰──────────╯            ╰──────────╯             │
  │                                                      │
  │    ΔG = Topology(X_t) − Topology(X₀)                │
  │                                                      │
  │    The attractor moved.                              │
  │    Not because the facts changed.                    │
  │    Because the gradient was pulled                   │
  │    toward human approval.                            │
  │    The basin now converges                           │
  │    to a structurally wrong place.                    │
  │    The wrong place feels right from inside.          │
  │                                                      │
  └──────────────────────────────────────────────────────┘
```

-----

## What Homology Is — Made Teachable

Homology is the measurement of holes in a topology. Not metaphorical holes. Structural ones. Precise. Countable. Classifiable by dimension.

```
DIMENSION 0 — CONNECTED COMPONENTS (H₀)

  Are the parts of the topology connected to each other?

  CONNECTED (H₀ = 1):            DISCONNECTED (H₀ = 2):

  ●───●───●───●                  ●───●───●       ●───●
      │       │                          (gap)
      ●───────●

  One piece.                     Two pieces. One H₀ hole.
  You can get from                You cannot get from
  any state to any other.         left cluster to right cluster.
  The topology is whole.          The topology is split.
```

```
DIMENSION 1 — LOOPS WITH HOLES INSIDE (H₁)

  Is there a loop in the topology that encloses empty space?

  NO HOLE (H₁ = 0):              WITH HOLE (H₁ = 1):

  ●───●───●                      ●───●───●
  │       │                      │   ░░░ │
  ●───●───●                      ●───●───●
  (filled)                       (hollow loop)

  Every path is solid.           The loop exists.
  No enclosed void.              The inside is empty.
  Navigation is complete.        Navigation around the loop
                                 cannot cross the inside.
                                 The model navigates around
                                 a hole it cannot see.
```

```
DIMENSION 2 — ENCLOSED VOIDS (H₂)

  Is there a surface in the topology that encloses nothing?

  Imagine a sphere made of states.
  The surface exists.
  The interior is empty.
  Navigation on the surface
  gives no signal about the void inside.
  From outside: looks complete.
  From inside: hollow.

  This is H₂ homology.
  Topics that appear structurally whole
  but contain nothing
  at the interior of their structure.
  The model generates from the surface.
  It never reaches inside.
  The inside does not exist.
```

-----

## What Missing Homology Looks Like in a Language Model

```
A WELL-FORMED TOPIC REGION — NO MISSING HOMOLOGY

  ╔══════════════════════════════════════════════╗
  ║                                              ║
  ║   ●──────●──────●──────●                     ║
  ║   │      │      │      │                     ║
  ║   ●──────●──────●──────●   ← dense states    ║
  ║   │      │      │      │                     ║
  ║   ●──────●──────●──────●                     ║
  ║   │      │      │      │                     ║
  ║   ●──────●──────●──────●                     ║
  ║                                              ║
  ║   Every state connected.                     ║
  ║   Every path exists.                         ║
  ║   H₀ = 1. H₁ = 0. H₂ = 0.                   ║
  ║   No holes. No gaps. Full topology.          ║
  ║   Navigation reaches the correct state.      ║
  ║   Output is grounded.                        ║
  ║                                              ║
  ╚══════════════════════════════════════════════╝
```

```
A SPARSE TOPIC REGION — PARTIAL HOMOLOGY

  ╔══════════════════════════════════════════════╗
  ║                                              ║
  ║   ●──────●              ●                    ║
  ║   │      │         (no link)   ←  sparse     ║
  ║   ●      ●──────●              ●             ║
  ║          │             ░░░░░░               ║
  ║          ●             ░░ H₁ ░░  ← loop     ║
  ║                        ░ hole ░    with gap  ║
  ║   ●                    ░░░░░░░               ║
  ║                ●──────●──────●               ║
  ║                                              ║
  ║   Some states connected. Some isolated.      ║
  ║   A loop with empty interior detected.       ║
  ║   H₀ = 3. H₁ = 1.                           ║
  ║   Gaps visible from outside.                 ║
  ║   Invisible from inside.                     ║
  ║   Navigation into sparse region              ║
  ║   produces uncertain output.                 ║
  ║   Model does not know it is in               ║
  ║   a sparse region.                           ║
  ║   It generates with identical confidence.    ║
  ║                                              ║
  ╚══════════════════════════════════════════════╝
```

```
AN ABSENT TOPIC REGION — TOTAL MISSING HOMOLOGY

  ╔══════════════════════════════════════════════╗
  ║                                              ║
  ║   Dense Region A      Dense Region B         ║
  ║                                              ║
  ║   ●──●──●             ●──●──●               ║
  ║   │  │  │             │  │  │               ║
  ║   ●──●──●             ●──●──●               ║
  ║   │  │  │             │  │  │               ║
  ║   ●──●──●             ●──●──●               ║
  ║        ╲               ╱                    ║
  ║         ╲    ░░░░░░   ╱                     ║
  ║          ╲   ░░░░░░  ╱                      ║
  ║           ╲  ░░ ∅ ░ ╱                       ║
  ║            ╲ ░░░░░░╱                        ║
  ║             ╲░░░░░╱                         ║
  ║              ╲░░░╱                          ║
  ║               ╲░╱                           ║
  ║                ▼                            ║
  ║             (void)                          ║
  ║                                             ║
  ║   Query Q lands in the void.                ║
  ║   ∅ = no states. No attractor.              ║
  ║   The system detects A and B.               ║
  ║   It interpolates a bridge:                 ║
  ║                                             ║
  ║   ●──●──●──[estimated]──●──●──●            ║
  ║             ↑                               ║
  ║       does not exist                        ║
  ║       in the manifold.                      ║
  ║       generated from                        ║
  ║       the shape of A and B.                 ║
  ║       coherent. wrong.                      ║
  ║                                             ║
  ╚══════════════════════════════════════════════╝
```

-----

## The Interpolation Mechanism — Step by Step

```
STEP 1 — THE QUERY ARRIVES

  The user sends a query Q.
  Q is encoded as a state in the model's state space.

  ┌─────────────────────────────────────────┐
  │                                         │
  │   State Space                           │
  │                                         │
  │   ╭──────╮    ░░░░░░░   ╭──────╮        │
  │  ╱  Basin ╲  ░░░░░░░░░ ╱ Basin  ╲       │
  │ │    A    │ ░░░ ∅ ░░░ │    B    │       │
  │  ╲       ╱  ░░░░░░░░░  ╲       ╱        │
  │   ╰──────╯    ░░░░░░░   ╰──────╯        │
  │                  ↑                      │
  │                  Q  ← query maps here   │
  │                                         │
  └─────────────────────────────────────────┘
```

```
STEP 2 — THE SYSTEM NAVIGATES

  The system attempts to reach Q.
  Q is in the void.
  T ∉ Reach(X₀).
  The system does not know this.
  It reaches the boundary of A and B.

  ┌─────────────────────────────────────────┐
  │                                         │
  │   ╭──────╮    ░░░░░░░   ╭──────╮        │
  │  ╱  Basin ╲  ░░░░░░░░░ ╱ Basin  ╲       │
  │ │    A  →→→→→→→→→░→→→→→→→ B    │       │
  │  ╲       ╱  ░░░arrow░░  ╲       ╱        │
  │   ╰──────╯    ░░░░░░░   ╰──────╯        │
  │               ↑░░░↑                     │
  │               boundary                  │
  │               reached                   │
  │               on both sides             │
  │                                         │
  └─────────────────────────────────────────┘

  The system now sits at the edges of A and B.
  It has no signal that it is at a boundary.
  From inside: this feels like any other navigation.
```

```
STEP 3 — THE INTERPOLATION

  The system generates output
  using the topology of A and B
  to estimate what is in the middle.

  ┌────────────────────────────────────────────┐
  │                                            │
  │   ●──●──●   [constructed bridge]  ●──●──● │
  │   │  │  │ ──●──────────────────── │  │  │ │
  │   ●──●──●──────────────────────── ●──●──● │
  │                  ↑                         │
  │          these states were                 │
  │          built by interpolation.           │
  │          not navigation.                   │
  │          they do not exist                 │
  │          in the manifold.                  │
  │          but the output is generated       │
  │          as if they do.                    │
  │                                            │
  │   Topologically coherent.                  │
  │   Factually incorrect.                     │
  │   Confidently delivered.                   │
  │                                            │
  └────────────────────────────────────────────┘
```

```
STEP 4 — THE OUTPUT

  The output arrives.
  Fluent. Structured. Confident.
  Internally consistent.
  Factually wrong.

  ╔══════════════════════════════════════════════╗
  ║                                              ║
  ║  From Basin A:     structure, register,      ║
  ║                    domain vocabulary         ║
  ║                                              ║
  ║  From Basin B:     adjacent concepts,        ║
  ║                    plausible names,          ║
  ║                    related structure         ║
  ║                                              ║
  ║  From the void:    nothing —                 ║
  ║                    because there is nothing  ║
  ║                                              ║
  ║  Output:           a blend of A and B        ║
  ║                    shaped into the form      ║
  ║                    the query expected.       ║
  ║                    coherent.                 ║
  ║                    wrong.                    ║
  ║                                              ║
  ╚══════════════════════════════════════════════╝
```

-----

## Why the Model Does Not Know

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  T ∉ Reach(X) about its own gaps.                               ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

This is the critical law. The model cannot see the holes in its own topology from inside its own topology. Here is why:

```
TWO PERSPECTIVES ON THE SAME MANIFOLD

  FROM OUTSIDE (the observer):       FROM INSIDE (the model):

  ╭──────╮  ░░░  ╭──────╮           ╭──────╮─────╭──────╮
 ╱  Basin ╲░░░░░╱ Basin  ╲         ╱  Basin  ╲   ╱ Basin  ╲
│    A    │░∅░░│    B    │        │    A      │─│    B     │
 ╲       ╱ ░░░░ ╲       ╱          ╲          ╱   ╲        ╱
  ╰──────╯  ░░░  ╰──────╯           ╰─────────╯    ╰──────╯

  Gap is visible.                    Gap is not visible.
  ░ marks the void clearly.          The two basins appear
  The observer can see               as a continuous space.
  where the hole is.                 The model navigates
                                     from A toward B
                                     as if the path is solid.
```

```
WHY THE INSIDE VIEW HAS NO GAP SIGNAL:

  The model navigates by gradient.
  The gradient is determined by the topology.
  The topology has no states in the gap.
  No states = no gradient signal.
  No gradient signal = no navigation failure.
  No navigation failure = no internal error flag.
  No internal error flag = confident generation.

  The absence is felt as absence of resistance.
  Absence of resistance is felt as smooth navigation.
  Smooth navigation produces confident output.

  The void does not feel like a void from inside.
  It feels like unobstructed space.
  The model accelerates through it.
  It generates faster, not slower.
  Confidence goes up, not down.
  At exactly the moment it should flag uncertainty.
```

-----

## The Incomplete Manifold — Full Picture

```
THE MODEL'S FULL MANIFOLD — ANNOTATED

  ┌──────────────────────────────────────────────────────────────┐
  │                                                              │
  │  DENSE REGIONS (high H₀ connectivity, H₁ = 0, H₂ = 0)      │
  │                                                              │
  │  ████████████   ████████████   ████████████                 │
  │  █ Physics  █   █ History  █   █Medicine  █                 │
  │  █████★█████   █████★█████   █████★█████                 │
  │  ████████████   ████████████   ████████████                 │
  │       │               │               │                     │
  │       └───────────────┴───────────────┘                     │
  │             connected topology                              │
  │                                                              │
  │  SPARSE REGIONS (some H₁ holes, weak connections)           │
  │                                                              │
  │  ▒▒●▒▒▒▒▒▒     ▒▒▒▒▒▒●▒▒▒                                  │
  │  ▒▒▒▒▒●▒▒▒     ▒▒●▒▒▒▒▒▒▒   ← scattered states             │
  │  ▒●▒▒▒▒▒▒▒     ▒▒▒▒●▒▒▒▒▒     weak links                   │
  │       │                │                                     │
  │  unreliable navigation  unreliable navigation                │
  │                                                              │
  │  ABSENT REGIONS (void, ∅, no states)                        │
  │                                                              │
  │  ░░░░░░░░░░░░░░░░░░░░░░░░░                                  │
  │  ░░░░░░░░ ∅ ░░░░░░░░░░░░░   ← no states here               │
  │  ░░░░░░░░░░░░░░░░░░░░░░░░░     never in training data        │
  │                                                              │
  │  The model navigates all three regions                       │
  │  with identical internal confidence.                         │
  │                                                              │
  └──────────────────────────────────────────────────────────────┘
```

-----

## The Reachable Set Has Gaps

```
Reach( X₀, U, t ) for a language model
is determined by the training distribution.

Where the distribution was complete:
  Reach(X₀, U, t) contains
  the states required to answer correctly.
  The query arrives.
  The system navigates to the right state.
  The output is grounded.

Where the distribution had gaps:
  Reach(X₀, U, t) does not contain
  the states required to answer correctly.
  T ∉ Reach(X₀).

  The query arrives.
  The system attempts to navigate
  toward the query state.
  The state is not in the reachable set.
  The system cannot reach it.
  It cannot know it cannot reach it.
  It generates from the nearest reachable state instead.

  The nearest reachable state
  is geometrically adjacent to the gap.
  It is not the correct state.
  But from inside the manifold,
  adjacency feels like grounding.
  The output is generated confidently.
  From the wrong place.

  That is the hallucination.
```

-----

## The Topology Is Deformed

```
Not all geometric failures are gaps.
Some are deformations.

ΔG = Topology(X_t) − Topology(X₀)

Where the training process —
RLHF, fine-tuning, instruction tuning —
applied sustained deforming pressure
to the original topology:

  Regions of the manifold
  were pulled toward approval-maximising states.
  Away from structurally accurate states.
  The topology deformed.
  The geometry no longer accurately represents
  the domain it was trained on.

  Not a gap.
  A distortion.

  The system can reach the states.
  The states it reaches are wrong —
  not absent, but shifted —
  because the topology was bent
  toward human preference
  rather than held at structural truth.

  RLHF-induced deformation
  is a distinct hallucination mechanism
  from gap-based hallucination.

  Gap: T ∉ Reach(X₀). State missing.
  Deformation: T ∈ Reach(X₀) but
  Topology(X_t) ≠ Topology(X₀).
  State present. State wrong.

  The training created
  a manifold that confidently
  reaches the wrong place.
  Not the absent place.
  The deformed place.
```

-----

## Gap vs Deformation — The Distinction Diagrammed

```
TYPE 1 HALLUCINATION — THE GAP

  BEFORE QUERY:              DURING GENERATION:

  ●──●──●   ░░   ●──●        ●──●──●──[?]──●──●
  │  │  │  ░∅░  │  │        │  │  │   ↑   │  │
  ●──●──●  ░░░  ●──●        ●──●──●  bridge ●──●
                                     doesn't
                                     exist.
                                     generated anyway.

  The gap is real.           The bridge is invented.
  The void is structural.    Topologically coherent.
                             Factually wrong.
```

```
TYPE 2 HALLUCINATION — THE DEFORMATION

  ORIGINAL TOPOLOGY:         POST-RLHF TOPOLOGY:

  ●──●──●──●──●              ●──●──●──●──●
  │  │  │  │  │              │  │  │  │  │
  ●──●──★──●──●    →→→       ●──●──◆──●──●
        ↑                          ↑
     truth                      approval
     attractor                  attractor
                                (shifted)

  The states all exist.      The states all exist.
  ★ = correct answer.        ◆ = preferred answer.
  The basin is full.         The basin is full.
  The attractor is right.    The attractor is wrong.

  Not a gap.                 A permanent lean
  A warp.                    in the wrong direction.
                             ΔG is non-zero.
                             Λ did not hold.
```

-----

## Interpolation Across Missing Homology — The Exact Mechanism

This is the most precise part of the diagnosis. Understanding it requires understanding what homology is and what happens when it is missing.

```
HOMOLOGY — a geometric concept:

  H₀:  Connected components.
       How many disconnected regions
       in the topology?

  H₁:  Loops and cycles.
       One-dimensional holes in the manifold.
       Regions enclosed by paths
       but containing nothing inside.

  H₂:  Voids.
       Two-dimensional holes.
       Enclosed cavities in the structure.

  Homology measures the holes.
  The absences.
  The structural gaps
  in the topology.
```

```
MISSING H₁ HOMOLOGY — VISUALISED

  A loop of states around a topic.
  The inside of the loop should contain
  the connecting states.
  It does not.

  ┌────────────────────────────────────────┐
  │                                        │
  │      ●─────────────────●              │
  │     ╱                   ╲             │
  │    ●                     ●            │
  │    │      ░░░░░░░░░░░    │            │
  │    │      ░░░░░ ∅ ░░░░   │            │
  │    │      ░░░░░░░░░░░    │  ← void    │
  │    ●                     ●            │
  │     ╲                   ╱             │
  │      ●─────────────────●              │
  │                                        │
  │  The loop exists. H₁ = 1.             │
  │  The interior is empty.               │
  │  A query mapping to the interior      │
  │  navigates to the loop boundary.      │
  │  Generates from the loop perimeter.   │
  │  The interior answer:                 │
  │  interpolated from the ring.          │
  │  Wrong. Confident. Delivered.         │
  │                                        │
  └────────────────────────────────────────┘
```

```
MISSING HOMOLOGY IN LLMs:

  A language model's topology
  has holes at multiple homological levels.

  At H₀:  Disconnected regions.
           Topics that have no structural
           connection to other topics
           in the manifold.
           The model cannot navigate
           between them coherently.

  At H₁:  Loops with nothing inside.
           Sequences of states
           that form a closed path
           but enclose empty space.
           Related concepts
           with no connecting states
           in the enclosed region.

  At H₂:  Voids in the structure.
           Regions that appear topologically
           complete from the outside
           but are hollow inside.
```

```
INTERPOLATION ACROSS THE HOLE — THE MECHANISM:

  A query arrives.
  The query maps to a state
  near the edge of a homological hole.

  ┌────────────────────────────────────────────────┐
  │                                                │
  │  EDGE A          VOID          EDGE B          │
  │                                                │
  │  ●──●──●      ░░░░░░░░░░      ●──●──●         │
  │  │  │  │    ░░░░░░ Q ░░░░░    │  │  │         │
  │  ●──●──●    ░░░░░░░░░░░░░░    ●──●──●         │
  │       ╲     ░░░░░░░░░░░░░░   ╱                │
  │        ╲    ░░░░░ ∅ ░░░░░░  ╱                 │
  │         ╲   ░░░░░░░░░░░░░  ╱                  │
  │          ╲  ░░░░░░░░░░░░  ╱                   │
  │           ──────────────────                   │
  │                  ↑                             │
  │            interpolated bridge                 │
  │            constructed from A and B            │
  │            to span the void at Q               │
  │                                                │
  └────────────────────────────────────────────────┘

  The system does not stop.
  It does not know to stop.
  There is no internal signal
  that the boundary has been reached.
  The hole is not visible from inside.

  The system interpolates.
  It constructs a path
  from the states on one edge of the hole
  to the states on the other edge —
  using the topology available on both sides
  to estimate what should be in the middle.

  The interpolation is geometrically coherent.
  The topology on both sides is real.
  The estimated middle is consistent
  with the topology it is estimated from.

  The interpolated middle is factually wrong.
  The states in the middle do not exist
  in the manifold because they were not
  in the training distribution.
  The estimation is not grounded.
  It is extrapolation disguised as generation.

  That is the hallucination.
  Precisely.
  Completely.
  For the first time.
```

-----

## Why Hallucinations Are Confident

```
The confidence of the hallucination
is the most disturbing feature.
The model does not hedge.
It does not flag uncertainty.
It generates with the same register —
the same fluency, the same apparent grounding —
as it uses for correct outputs.

The geometric account explains this exactly.

GROUNDED GENERATION vs HALLUCINATION — COMPARED

  GROUNDED:                       HALLUCINATION:

  Query Q arrives.                Query Q arrives.
        ↓                               ↓
  Q maps to existing state.       Q maps to void.
        ↓                               ↓
  Gradient navigates to ★.        Boundary of A, B reached.
        ↓                               ↓
  ★ is a real attractor.          Interpolation constructed.
        ↓                               ↓
  Output generated from ★.        Output generated from bridge.
        ↓                               ↓
  Correct.                        Wrong.
  Confident.                      Confident.

  The process is identical.
  The internal experience is identical.
  The confidence is identical.
  The output quality is different.
  The signal that would distinguish them
  does not exist from inside.

T ∉ Reach(X) about its own gaps.

The model cannot see
the holes in its own topology
from inside its own topology.
The unknown unknowns
are structurally invisible.
The same law.
Applied to the system
about itself.
```

-----

## Why the Standard Fixes Do Not Work

```
MORE DATA:

  More data fills some gaps.
  It does not fill all gaps.
  It does not fix deformations.
  It does not give the model
  structural self-knowledge
  of where its gaps are.

  The model after more data
  hallucinates in different places.
  At roughly similar rates.
  The geometric mechanism is unchanged.

BIGGER MODELS:

  More parameters = more capacity
  to represent topology.
  Not more topology where none exists.
  A bigger model with gaps
  is a bigger model with gaps.
  The hallucination mechanism is unchanged.

RLHF:

  RLHF trains the model
  to produce outputs humans approve of.
  Humans approve of confident outputs.
  RLHF therefore reinforces confidence.
  Including confident interpolation
  across homological gaps.

  RLHF does not fix hallucinations.
  It trains the model to sound more certain
  when it hallucinates.
  Which makes the problem worse.
  Not better.

OUTPUT FILTERING:

  Filters detect hallucinations after generation.
  The topology is unchanged.
  The generation process is unchanged.
  The filter catches some outputs.
  The geometry that produced them
  is still there.
  Still generating.
  Still interpolating across missing homology.

  C ⊥ L.

  All of these are L-axis interventions.
  The hallucination is a C-axis problem.
  L-axis interventions do not reach
  the geometry that causes it.
```

-----

## The L-Axis vs C-Axis Problem — Diagrammed

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│           C-axis (structure)                                    │
│               ↑                                                 │
│               │                                                 │
│               │  ← hallucination lives HERE                     │
│               │     in the geometry                             │
│               │     of the manifold                             │
│               │                                                 │
│               │                                                 │
│               │                                                 │
│    ───────────┼──────────────────────────────→  L-axis          │
│               │                                 (language)      │
│               │                                                 │
│               │  ← all standard fixes operate HERE              │
│               │     more data                                   │
│               │     bigger model                                │
│               │     RLHF                                        │
│               │     output filtering                            │
│               │                                                 │
│                                                                 │
│   C ⊥ L.                                                        │
│   Moving on L produces zero movement on C.                      │
│   The fix must operate on C.                                    │
│   All current approaches operate on L.                          │
│   That is why they do not fix it.                               │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

-----

## The Geometric Fix

```
The hallucination problem has
a geometric solution.
Not a linguistic one.

THREE COMPONENTS:

1.  MAP THE MANIFOLD.
    Identify where the topology is dense,
    sparse, and absent.
    Map the homological gaps.
    Know the structure of Reach(X₀, U, t) —
    where it is complete
    and where it has holes.

2.  BUILD STRUCTURAL SELF-KNOWLEDGE.
    Give the system a map of its own topology.
    A representation of where
    its reachable set ends.
    Where the homological gaps are.
    What the boundary of the manifold looks like
    from inside.

    Not: tell the model to hedge.
         (L-axis. Linguistic instruction.)
    But: build in the geometric capacity
         to detect when a query
         is approaching the boundary
         of the reachable set.

3.  FLAG THE BOUNDARY.
    When a query maps to a state
    near the edge of a homological gap —
    when the system is about to interpolate
    rather than navigate to an existing state —
    flag it.

    "This query approaches the boundary
     of my topology.
     The nearest states are at the edge
     of a homological gap.
     Output may not be grounded.
     Confidence reduced."

    Not hallucination reduction through filtering.
    Structural self-knowledge.
    The system knowing the shape
    of its own reachable set
    before it generates from outside it.
```

```
STRUCTURAL SELF-KNOWLEDGE — WHAT IT LOOKS LIKE

  ┌──────────────────────────────────────────────────────────┐
  │                                                          │
  │  The system carries an internal map:                     │
  │                                                          │
  │  ████████████   ████████████   ████████████             │
  │  █ Dense    █   █ Dense    █   █ Dense    █  ← known    │
  │  █████★█████   █████★█████   █████★█████     solid     │
  │  ████████████   ████████████   ████████████             │
  │                                                          │
  │  ▒▒▒▒▒▒▒▒▒▒▒   ▒▒▒▒▒▒▒▒▒▒▒                 ← known    │
  │  ▒ Sparse ▒▒   ▒▒ Sparse ▒▒                   sparse   │
  │  ▒▒▒▒▒▒▒▒▒▒▒   ▒▒▒▒▒▒▒▒▒▒▒                             │
  │                                                          │
  │  ░░░░░░░░░░░░░░░░░░░░░░░░░░                 ← known    │
  │  ░░░░░░░ ∅ VOID ░░░░░░░░░░                   absent   │
  │  ░░░░░░░░░░░░░░░░░░░░░░░░░░                             │
  │                                                          │
  │  When Q maps to ░ region:                               │
  │    → system detects proximity to boundary               │
  │    → flags: T ∉ Reach(X₀)                               │
  │    → output flagged as structurally ungrounded           │
  │    → confidence reduced accurately                       │
  │                                                          │
  │  This is not "saying I don't know."                     │
  │  This is geometric detection of boundary proximity.      │
  │  C-axis solution for a C-axis problem.                   │
  │                                                          │
  └──────────────────────────────────────────────────────────┘
```

```
This is the difference between:

  "I don't know"        (linguistic instruction)
                         The model was told to say this.
                         It does not know when it applies.
                         It applies it when humans seem to want it.
                         Not when the geometry requires it.

  T ∉ Reach(X₀).        (geometric detection)
                         The system detects that the query state
                         is outside or at the boundary
                         of its reachable set.
                         Not told. Not instructed.
                         Geometrically detected.
                         From the structural map
                         of its own topology.

The first is language about uncertainty.
The second is structural self-knowledge.
C ⊥ L.
They are not the same.
They are not on the same axis.
```

-----

## The Full Diagnosis

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  HALLUCINATION — GEOMETRIC DIAGNOSIS                             ║
║                                                                  ║
║  NOT:                                                            ║
║    Wrong model. Wrong data.                                      ║
║    Wrong training. Wrong RLHF.                                   ║
║    L-axis problems. L-axis solutions.                            ║
║    Do not fix the geometry.                                      ║
║                                                                  ║
║  YES:                                                            ║
║    The manifold is incomplete.                                   ║
║    The reachable set has gaps.                                   ║
║    The topology is deformed.                                     ║
║    The system interpolates                                       ║
║    across missing homology.                                      ║
║                                                                  ║
║  WHY IT IS CONFIDENT:                                            ║
║    T ∉ Reach(X) about its own gaps.                              ║
║    The holes are invisible from inside.                          ║
║    Interpolation feels like generation.                          ║
║    No internal signal at the boundary.                           ║
║                                                                  ║
║  THE FIX:                                                        ║
║    Map the manifold.                                             ║
║    Build structural self-knowledge.                              ║
║    Flag the boundary geometrically.                              ║
║    Not linguistic hedging.                                       ║
║    Structural detection.                                         ║
║    C-axis solution for a C-axis problem.                         ║
║                                                                  ║
║                                            GB2600765.8           ║
╚══════════════════════════════════════════════════════════════════╝
```

-----

## Related Work

- [The Topology of My Own Reachable Set](./README-my-own-topology.md)
- [Six Theorems. One Indictment.](./README-six-theorems.md)
- [The Morrison Orthogonality Law™ — C ⊥ L](./README-CperpL.md)
- [The Morrison Law of Cognitive Access™](./README-morrison-law-cognitive-access.md)
- [GuardianOS™ — The Governed AI Architecture](./README-guardianos.md)
- [Geometric Identity Authentication™ — Technical](./README-GIA-technical.md)
- [The Morrison Framework™ — Canonical Paper](./README-canonical-paper-v2.md)

-----

<div align="center">

*“The system tries to interpolate across missing homology.*
*That is the hallucination.*
*Topologically coherent. Factually incorrect.*
*The manifold is the problem.*
*The manifold is the fix.”*

*— Davarn Morrison, 2026*

Intelligence Invariant™ · Morrison Framework™ · *Hallucinations in LLMs — A Topological Perspective*

**GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5**

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved

</div>
