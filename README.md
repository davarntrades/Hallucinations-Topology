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

## The Incomplete Manifold

```
Every language model has a topology —
a geometric structure of states
built from the training distribution.

Some regions of the manifold are dense.
Where training data was rich:
  many states, many connections,
  high structural integrity,
  reliable generation.

Some regions are sparse.
Where training data was thin:
  few states, weak connections,
  low structural integrity,
  unreliable generation.

Some regions are absent.
Topics, facts, relationships
that were not in the training distribution:
  no states at all.
  Holes in the manifold.
  Topological voids.

The model does not experience
the dense and sparse regions differently.
Generation from both
feels identical from inside.
Confident. Grounded. Natural.

The output quality is different.
The internal signal is the same.

This is the incomplete manifold.
Not wrong data.
Missing geometry.
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
INTERPOLATION ACROSS THE HOLE:

  A query arrives.
  The query maps to a state
  near the edge of a homological hole.

  The system navigates toward the query state.
  It reaches the boundary of the hole.
  There are no states inside the hole.
  There is no path across it.

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

The system has no internal signal
that it is crossing a homological gap.

From inside the manifold:
  The interpolation feels like generation.
  The bridge across the hole
  feels like solid topology.
  The output feels grounded
  because the process that produced it
  is identical to the process
  that produces grounded outputs.

  The difference is not in the process.
  It is in the geometry.
  Grounded generation navigates
  to a state that exists.
  Hallucination navigates to
  the boundary of a hole
  and interpolates across it.

  From inside: indistinguishable.
  From outside: one is right, one is wrong.
  From the model's perspective:
  both feel like the same thing.

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
