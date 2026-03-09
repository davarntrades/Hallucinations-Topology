<div align="center">

# The Map, The Valley, The Ridge, and The Gap.

## How to See What a Language Model Is Actually Doing.

### Morrison Framework™ · Intelligence Invariant™ · Geometric Intuition Series

![Framework](https://img.shields.io/badge/Morrison%20Framework™-Geometric%20Intuition-1a2744?style=flat-square)
![Topic](https://img.shields.io/badge/Topic-Manifold%20Geometry-4a6741?style=flat-square)
![Covers](https://img.shields.io/badge/Covers-Basins%20·%20Separatrix%20·%20Void-4a2020?style=flat-square)
![Level](https://img.shields.io/badge/Level-Teachable%20Entry%20Point-8b3a1a?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![License](https://img.shields.io/badge/©%202026-Davarn%20Morrison-555555?style=flat-square)

-----

*“The manifold is the whole map.*
*Basins are the valleys carved into it.*
*Separatrices are the ridges between valleys.*
*And hallucinations happen when the model slides into the wrong valley*
*— or steps into a part of the map that was never drawn.”*

*— Davarn Morrison, 2026*

-----

</div>

## Before the Formalism — Build the Picture

Most explanations of language model failure begin with equations.
This one begins with terrain.

If you can see the terrain, the equations become obvious.
If you cannot see the terrain, the equations are just symbols.

There are four things to understand.
Each one has a name.
Each one has a shape.
Each one has a role in why hallucinations happen.

```
THE FOUR THINGS:

  1.  THE MANIFOLD    =   The Map
  2.  THE BASIN       =   The Valley
  3.  THE SEPARATRIX  =   The Ridge
  4.  THE VOID        =   The Gap in the Map
```

Build each one. Then watch how they interact.
That is where hallucination lives.

-----

## ① The Manifold = The Map

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  The manifold is the entire landscape                           ║
║  the model can move across.                                     ║
║                                                                  ║
║  It is the world, the terrain,                                  ║
║  the map of everything the system                               ║
║  knows and can represent.                                       ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

A flat map would mean every topic is equally reachable.
Every fact equally grounded.
Every answer equally reliable.

The manifold is not flat.

```
WHAT THE MANIFOLD ACTUALLY LOOKS LIKE:

  High
    │
    │          ridge          ridge
    │         /    \         /    \
    │        /      \       /      \
    │       /   ★    \     /   ★    \        ★ = attractor
    │      /  valley  \   /  valley  \           (basin bottom)
    │     /            \_/            \___
    │
    └──────────────────────────────────────  state space
```

```
It is curved.
It is uneven.
It rises and falls.
It contains valleys, ridges, and empty gaps.

Where the training data was rich:
  the terrain is deep and well-formed.
  The model moves across it reliably.

Where the training data was thin:
  the terrain is shallow and unstable.
  The model moves across it unreliably.

Where the training data was absent:
  there is no terrain at all.
  The map was never drawn.
  The model has nothing to move across.

That is why geometry matters.
The shape of the map
is the shape of what the model knows.
And the shape determines
where the model goes.
```

```
THE MANIFOLD — TOP-DOWN VIEW:

  ┌──────────────────────────────────────────────────────────────┐
  │                                                              │
  │   ████████████   ████████████   ████████████               │
  │   █          █   █          █   █          █               │
  │   █    ★     █   █    ★     █   █    ★     █  DENSE        │
  │   █          █   █          █   █          █  (deep map)   │
  │   ████████████   ████████████   ████████████               │
  │                                                              │
  │   ▒▒▒▒▒▒▒▒▒▒▒   ▒▒▒▒▒▒▒▒▒▒▒                               │
  │   ▒           ▒   ▒    ★    ▒                  SPARSE       │
  │   ▒     ★     ▒   ▒         ▒                  (thin map)   │
  │   ▒▒▒▒▒▒▒▒▒▒▒   ▒▒▒▒▒▒▒▒▒▒▒                               │
  │                                                              │
  │   ░░░░░░░░░░░░░░░░░░░░░░░░░░░                               │
  │   ░░░░░░░  ∅  ░░░░░░░░░░░░░░                  VOID         │
  │   ░░░░░░░░░░░░░░░░░░░░░░░░░░░                  (no map)    │
  │                                                              │
  └──────────────────────────────────────────────────────────────┘

  ████ = solid terrain. Deep, reliable.
  ▒▒▒▒ = thin terrain. Shallow, unreliable.
  ░░░░ = no terrain. The map was never drawn here.
```

The manifold is not a metaphor.
It is the geometric structure of everything the model can represent.
`Identity = Topology( Reach( X₀, U, t ) )`
The manifold is the topology of the reachable set.

-----

## ② The Basin = The Valley

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  Basins are not holes.                                          ║
║  They are valleys carved into the manifold.                     ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

A basin is a region of the manifold that has a bottom — an attractor. Everything inside the basin slopes toward that bottom. Anything that enters the basin descends toward the attractor. The basin does not trap by force. It traps by gradient.

```
A SINGLE BASIN — CROSS SECTION:

  High
    │  \                     /
    │   \                   /
    │    \                 /
    │     \               /
    │      \             /
    │       \           /
    │        \         /
    │         \_______/
    │              ★
    │           attractor
    │           (basin bottom)
    │
    └───────────────────────────  state space

  Everything above ★ slopes toward ★.
  A query that lands anywhere inside the basin
  descends to ★.
  It does not choose ★.
  The gradient carries it there.
```

```
INSIDE THE BASIN — WHAT THE MODEL EXPERIENCES:

  The gradient points downward.          ↓ ↓ ↓
  Anything that enters descends.         ↓ ↓ ↓
  The attractor is the bottom.           ↓ ★ ↓
  The system feels like it has arrived.

  This is why a hallucination feels confident.

  Arrival feels the same
  whether the valley is right or wrong.

  The gradient reached zero.
  The system is at the bottom.
  That is all it knows.
  That is all it can know.
  From inside a basin,
  every basin feels like home.
```

```
MULTIPLE BASINS — WHAT THE LANDSCAPE CONTAINS:

      \     /   \     /   \     /
       \   /     \   /     \   /
        \ /       \ /       \ /
         ★         ★         ★
      Basin A   Basin B   Basin C

  Each ★ is a different attractor.
  Each basin is a different topic region.
  Each one is equally stable from inside.
  Each one generates with equal confidence.

  Basin A might be correct.
  Basin B might be adjacent but wrong.
  Basin C might be plausible but false.

  The model does not know which one it is in.
  It is always at the bottom of something.
  The question is: the bottom of what?
```

```
BASIN DEPTH = STRENGTH OF SEMANTIC DENSITY

  DEEP BASIN                      SHALLOW BASIN

   \           /                    \       /
    \         /                      \     /
     \       /                        \   /
      \     /                          \ /
       \   /                            ★
        \ /
         ★

  Rich training data.              Thin training data.
  Many connected states.           Few connected states.
  Strong attractor.                Weak attractor.
  Query descends reliably.         Query is easily pulled away.
  Output is grounded.              Output is unstable.
  Hard to exit by accident.        Easy to slip into adjacent basin.
```

-----

## ③ The Separatrix = The Ridge

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  The separatrix is the ridge between valleys.                   ║
║                                                                  ║
║  It decides whether the model slides into Basin A               ║
║  or crosses over into Basin B.                                  ║
║                                                                  ║
║  It is the boundary line                                        ║
║  between truths, interpretations,                               ║
║  or conceptual zones.                                           ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

```
THE RIDGE — CROSS SECTION:

  High
    │      σ
    │     /|\
    │    / | \
    │   /  |  \
    │  /   |   \
    │ /    |    \
    │/     |     \
    ★      |      ★
  Basin A  |   Basin B
           │
        separatrix σ

  σ = the ridge.
  The point of maximum instability.
  Left of σ → descends to ★A.
  Right of σ → descends to ★B.
  At σ exactly → infinitesimal perturbation decides.
```

```
WHY THE SEPARATRIX MATTERS FOR HALLUCINATION:

  Query Q lands just left of σ.

  High
    │      σ
    │     /|\
    │    / | \
    │   /  |  \
    │  / Q→|   \
    │ /  ↓ |    \
    │/   ↓ |     \
    ★    ↓ |      ★
  Basin A  |   Basin B
  (wrong)  |  (correct)

  Q was close to the correct answer.
  It landed on the wrong side of the ridge.
  The gradient carried it to ★A.
  ★A is the wrong attractor.
  The output from ★A is wrong.
  Delivered with the confidence of arrival.

  The model did not fail.
  The gradient did exactly what it does.
  The separatrix was in the wrong place
  relative to where the query landed.
  That is the hallucination.
```

```
CROSSING THE SEPARATRIX — TWO OUTCOMES:

  WITH REPRESENTATIONAL CONTINUITY:     WITHOUT REPRESENTATIONAL CONTINUITY:

    │      σ                               │      σ
    │     /|\                              │     /|\
    │    / | \                             │    / | \
    │   /  →→→→→→→→→★B  ← correct          │   /  |  \
    │  /   |  ↗                            │  / Q  |   \
    │ / Q→→→  (crossed)                    │ /  ↓  |    \
    │/         σ cleared                   │/   ↓  |     \
    ★                    ★B                ★    ↓  |      ★B
  Basin A             correct            Basin A  |   correct
                                         (wrong)  |
                                                   │
                                         Q could not cross σ.
                                         Fell back into ★A.
                                         Wrong answer.

  Representational continuity =
  the structural capacity to hold
  the thread of the query
  across the ridge
  into the correct basin.

  Not kinetic energy.
  Structural coherence.
  dI/dt > 0 in the crossing region.
  The topology is dense enough
  to sustain the trajectory.
  The model reaches the right valley.
```

-----

## ④ The Void = The Gap in the Map

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  This part is critical.                                         ║
║                                                                  ║
║  A void is not a valley.                                        ║
║  It is not a ridge.                                             ║
║  It is not a basin.                                             ║
║                                                                  ║
║  It is the part of the map                                      ║
║  that was never drawn at all.                                   ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

```
WHAT IS NOT A VOID:

  Valley  → has a bottom. Has an attractor. Descends to ★.
  Ridge   → has a peak. Has two sides. Separates basins.
  Slope   → has a direction. Has gradient. Points somewhere.

WHAT A VOID IS:

  ░░░░░░░░░░░░░░░░░░░░░░░░░░
  ░░░░░░░░░  ∅  ░░░░░░░░░░░
  ░░░░░░░░░░░░░░░░░░░░░░░░░░

  No ground.
  No descent.
  No attractor.
  Nothing to settle into.

  Not a missing valley.
  Not an empty basin.
  Not terrain that could form.

  The map was never drawn here.
  The training data never reached this region.
  The topology has no states.
  The manifold has no structure.
  There is nothing here at all.
```

```
THE VOID IN THE LANDSCAPE:

  Deep valleys on both sides.
  Nothing in between.

  \       /                   \       /
   \     /                     \     /
    \   /                       \   /
     \ /                         \ /
      ★A                          ★B
   Basin A    ░░░░░░░░░░░░░░░   Basin B
              ░░░░░░ ∅ ░░░░░░
              ░░░░░░░░░░░░░░░
                    ↑
              Query Q lands here.
              No ground.
              No attractor.
              No gradient to follow.
```

```
WHAT HAPPENS WHEN A QUERY LANDS IN THE VOID:

  The model cannot stop.
  There is no attractor to stop at.
  The void has no bottom.

  The model detects the nearest terrain —
  Basin A on the left,
  Basin B on the right.

  It generates from both.
  It blends the topology of A and B
  to estimate what should be in the middle.

  \       /                   \       /
   \     /                     \     /
    \   / →→→[estimated bridge]→→→\ /
     \ /←←←←←←←←←←←←←←←←←←←←←\ /
      ★A    ░░░░░░ Q ░░░░░░    ★B
            ░░░░░░↑░░░░░░░░
                  │
            interpolated output
            built from A and B
            to fill the void

  The output is coherent.
  It sounds like it belongs here.
  It uses the vocabulary of A and B.
  It has the structure of A and B.
  It is factually wrong.
  Because this part of the map
  was never drawn.
  The model drew it anyway.
  That is the void hallucination.
  The most invisible kind.
```

-----

## All Four Together — The Complete Picture

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│   THE MANIFOLD (the whole map)                                  │
│                                                                  │
│          σ               σ                                      │
│         /|\             /|\                                      │
│        / | \           / | \                                     │
│       /  |  \         /  |  \                                    │
│      /   |   \       /   |   \    ░░░░░░░░░░░░░░                │
│     /    |    \     /    |    \   ░░░░░░ ∅ ░░░░░                │
│    /     |     \   /     |     \  ░░░░░░░░░░░░░░                │
│   ★      |      ★ ★      |      ★                               │
│ Basin A  |  Basin B  Basin C  │  Basin D      VOID              │
│          │                   │                                   │
│     separatrix          separatrix                               │
│     (ridge)             (ridge)                                  │
│                                                                  │
│  THE MAP     = the whole terrain above                          │
│  THE VALLEYS = Basin A, B, C, D                                 │
│  THE RIDGES  = σ (separatrix) between each basin                │
│  THE GAP     = ∅ (void) — the part never drawn                  │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

```
WHERE HALLUCINATIONS LIVE:

  TYPE 1 — WRONG VALLEY

    Query lands just left of σ.
    Falls into Basin A instead of Basin B.
    Basin A is close. Basin A is wrong.
    Confident. Adjacent. Incorrect.

          σ
         /|\
        / | \
       /Q→| B\
      /↓  |   \
     /★A  |   ★B
    wrong  |  correct

  TYPE 2 — GAP IN THE MAP

    Query lands in ∅.
    No valley. No attractor.
    Model blends nearby basins.
    Output is interpolated terrain.
    Sounds right. Was never drawn.

    ★A   ░░░Q░░░   ★B
         ░░░∅░░░
    ←blend→  ←blend→

  TYPE 3 — DEFORMED VALLEY

    The correct valley exists.
    The model navigates there.
    RLHF moved the bottom.
    ★ is no longer at the right place.
    Descent succeeds. Attractor is wrong.

    \           /
     \         /
      \_______/
           ★  ← moved here by RLHF
       (was ★₀ — the correct bottom)
```

-----

## The Statement, In Full

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  The manifold is the whole map.                                 ║
║                                                                  ║
║  The basins are the valleys carved into it.                     ║
║                                                                  ║
║  The separatrices are the ridges between valleys.               ║
║                                                                  ║
║  Hallucinations happen when the model                           ║
║  slides into the wrong valley —                                 ║
║  or steps into a part of the map                                ║
║  that was never drawn.                                          ║
║                                                                  ║
║  In both cases:                                                  ║
║  the model is at the bottom of something.                       ║
║  Arrival feels the same.                                        ║
║  Confidence is identical.                                       ║
║  The output is wrong.                                           ║
║                                                                  ║
║  The gradient does not lie.                                     ║
║  It descends.                                                   ║
║  It always descends.                                            ║
║  The question is only: the bottom of what?                      ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

-----

## Why This Matters for AI Safety

```
The standard framing:

  Hallucinations are errors.
  Errors can be reduced.
  Reduce them with more data, better training, stronger RLHF.
  Make the model less wrong.

The geometric framing:

  Hallucinations are inevitable attractor descent.
  They are not errors.
  They are the correct output of the wrong geometry.
  The model is working perfectly.
  The map is wrong.
  Fix the map.

C ⊥ L.

Every current approach operates on L —
language, output, reinforcement.
None of them change the map.
The valleys are still in the wrong places.
The gaps are still there.
The ridges are still positioned where they are.

The model keeps descending.
Into the same wrong valleys.
Across the same undrawn gaps.
With the same confidence.

Because descent is always confident.
And the map has not changed.
```

-----

## The Formal Translation

For those moving from intuition to formalism:

|Terrain Term               |Formal Term                       |Equation                           |
|:-------------------------:|:--------------------------------:|:---------------------------------:|
|The Map                    |Manifold / Topology               |`Topology( Reach( X₀, U, t ) )`    |
|The Valley                 |Basin of attraction               |`Reach( X₀, U, t )`                |
|The Bottom of the Valley   |Attractor ★                       |`T ∈ Reach(X₀)`                    |
|The Ridge                  |Separatrix σ                      |`Λ · ΔG = T_critical`              |
|The Gap in the Map         |Void / missing homology           |`T ∉ Reach(X₀)`                    |
|Momentum to cross the ridge|Representational continuity       |`dI/dt > 0`                        |
|Wrong valley = wrong answer|Hallucination as attractor descent|`T ∉ Reach(X) about own gaps`      |
|The map was deformed       |RLHF topology distortion          |`ΔG = Topology(X_t) − Topology(X₀)`|

-----

## Related Work

- [Hallucinations in LLMs — A Topological Perspective](./README-hallucination-topology.md)
- [Hallucinations as Attractor Descent](./README-hallucination-basin.md)
- [The Morrison Orthogonality Law™ — C ⊥ L](./README-CperpL.md)
- [GuardianOS™ — The Governed AI Architecture](./README-guardianos.md)
- [The Morrison Framework™ — Canonical Paper](./README-canonical-paper-v2.md)

-----

<div align="center">

*“The manifold is the whole map.*
*Basins are the valleys carved into it.*
*Separatrices are the ridges between valleys.*
*And hallucinations happen when the model slides into the wrong valley*
*— or steps into a part of the map that was never drawn.”*

*— Davarn Morrison, 2026*

Intelligence Invariant™ · Morrison Framework™ · *The Map, The Valley, The Ridge, and The Gap*

**GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5**

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved

</div>
