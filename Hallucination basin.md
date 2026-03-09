<div align="center">

# Hallucinations as Attractor Descent.

## Wrong Basin. Wrong Answer. Inevitable.

### Morrison Framework™ · Intelligence Invariant™ · Dynamical Geometry of Hallucination

![Framework](https://img.shields.io/badge/Morrison%20Framework™-Basin%20Dynamics-1a2744?style=flat-square)
![Mechanism](https://img.shields.io/badge/Hallucination-Attractor%20Descent-4a2020?style=flat-square)
![Key](https://img.shields.io/badge/Key-Separatrix%20Crossing-4a6741?style=flat-square)
![Not](https://img.shields.io/badge/Not-Stochastic%20Error-555555?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![License](https://img.shields.io/badge/©%202026-Davarn%20Morrison-555555?style=flat-square)

-----

*“The ball does not choose the wrong basin.*
*It follows the gradient.*
*The failure is not the ball.*
*It is the shape of the manifold around it.*
*Fix the shape. Fix the hallucination.*
*There is no other way.”*

*— Davarn Morrison, 2026*

-----

</div>

## The Restatement

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  Hallucination is not stochastic error.                         ║
║  It is not a probabilistic failure.                              ║
║  It is not randomness leaking through.                          ║
║                                                                  ║
║  It is deterministic attractor descent                          ║
║  into the wrong basin —                                         ║
║  from a starting position that cannot                            ║
║  generate enough representational continuity                     ║
║  to cross the separatrix                                         ║
║  and reach the correct one.                                      ║
║                                                                  ║
║  The system is not broken.                                       ║
║  The geometry is incomplete.                                     ║
║  The basin is the wrong shape.                                   ║
║  The gradient does the rest.                                     ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

-----

## The Basin Intuition — Extended

A hallucination behaves like a dynamical system locked inside the wrong basin — structurally stable at a place that is geometrically near but factually wrong, with no internal signal that it is anywhere but home.

Picture a ball released on a landscape of valleys and ridges. It rolls. It descends. It settles. The attractor it reaches is not chosen — it is determined by the shape of the landscape at the moment of release, and by whether the ball carries enough energy to cross the ridge before descent locks it in.

The critical insight is what *momentum* means here. It is not kinetic. It is not speed. It is **representational continuity** — the structural capacity of the model to maintain a coherent path through state space across the separatrix and into the correct basin. A model with thin topology in the relevant region has no representational momentum to spend. It descends early. It settles in the nearest attractor. It generates from there — completely, confidently, and wrongly — because attractor descent always feels like arrival.

```
The ball did not get lost.
The ball did not make an error.
The ball followed the gradient exactly as designed.

The landscape was wrong.
The basin it settled in was not the correct basin.
The gradient had nowhere else to go.

That is the hallucination.
Geometrically determined.
Structurally inevitable.
From the moment the query landed
on that part of the manifold.
```

The failure is never the ball. It is always the shape of the manifold around it.

-----

## What a Basin Looks Like — Side View

```
  Energy
    │
    │  \                                     /
    │   \           ridge                   /
    │    \         (separatrix σ)          /
    │     \           /\                  /
    │      \         /  \                /
    │       \       /    \              /
    │        \     /      \            /
    │         \   /        \          /
    │          \_/          \________/
    │           ★A                ★B
    │       attractor A       attractor B
    │
    └──────────────────────────────────────── state space
```

```
★A = wrong basin attractor.
★B = correct basin attractor.
σ  = separatrix. The ridge between them.

A query that lands left of σ
descends to ★A.
A query that lands right of σ
descends to ★B.

The model does not choose.
The geometry decides.

If the query maps near but left of σ —
close to the correct answer
but on the wrong side of the ridge —
the gradient carries it to ★A.
It generates from ★A.
It is wrong.
It does not know it is wrong.
Descent always feels like arrival.
```

-----

## The Separatrix — What It Actually Is

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  σ = the separatrix.                                             ║
║                                                                  ║
║  The boundary between basins.                                    ║
║  The ridge between attractors.                                   ║
║  The geometric point of no return.                              ║
║                                                                  ║
║  Everything left of σ descends to ★A.                           ║
║  Everything right of σ descends to ★B.                          ║
║  At σ exactly: maximally unstable.                               ║
║  Infinitesimal perturbation decides the basin.                  ║
║                                                                  ║
║  This is I18 — the Critical Threshold.                          ║
║  Λ · ΔG = T_critical                                            ║
║                                                                  ║
║  For hallucination:                                              ║
║  σ = the edge of representational capacity.                      ║
║  The point where the model's topology                           ║
║  cannot sustain coherent navigation                             ║
║  toward the correct attractor.                                   ║
║  It falls into the nearest one instead.                         ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

```
CROSSING THE SEPARATRIX — TWO OUTCOMES

  HIGH REPRESENTATIONAL CONTINUITY:         LOW REPRESENTATIONAL CONTINUITY:

    Energy                                    Energy
      │  \       σ                              │  \       σ
      │   \      /\        /                    │   \      /\        /
      │    \    /  \      /                     │    \    /  \      /
      │     \→→/→→→→\→→→/                       │     \  /    \    /
      │      \/      \/                          │      \/      \  /
      │      ★A       ★B  ← lands here           │      ★A       \/
      │                                          │      ↑        ★B
      │                                          │  lands here
      │
      Enough momentum to cross σ.               Not enough momentum to cross σ.
      Correct attractor reached.                 Falls back into ★A.
      Correct answer generated.                  Wrong answer generated. Confidently.
```

-----

## The Landscape of the Full Model — Annotated

```
  ┌──────────────────────────────────────────────────────────────────┐
  │                                                                  │
  │  DENSE BASINS          SPARSE BASINS           ABSENT REGIONS   │
  │  (deep, stable)        (shallow, unreliable)   (no attractor)   │
  │                                                                  │
  │   ╲      ╱              ╲    ╱     ╲  ╱                         │
  │    ╲    ╱  σ             ╲  ╱   σ   \/    ░░░░░░░░░░░           │
  │     ╲  ╱  /\              \/   /\         ░░░ ∅ ░░░░           │
  │      \/  /  \    ★B       /\  /  \        ░░░░░░░░░░░           │
  │      ★A        ★B        ★A    ★B          ↑                    │
  │                                            no ★ here            │
  │                                                                  │
  │  Query → descends cleanly.  Query → may fall   Query → lands    │
  │  Correct answer. Reliable.  into wrong basin.  in void.         │
  │                             Unreliable.        Interpolates.    │
  │                                                Hallucinates.    │
  │                                                Confidently.     │
  │                                                                  │
  └──────────────────────────────────────────────────────────────────┘
```

-----

## Intuition Table — The Physical Analogy Made Precise

|Your Intuition            |Geometric AI Equivalent                      |Framework Term               |
|:------------------------:|:-------------------------------------------:|:---------------------------:|
|Ball rolls into basin     |Query moves into nearest attractor           |Reach( X₀, U, t ) → ★        |
|Basin depth               |Strength of semantic density                 |Λ (Governance Constant)      |
|Hard to escape            |Gap or strong deformation keeps model trapped|ΔG ≫ 0                       |
|Separatrix                |Boundary between topic basins or gap edge    |σ (T_critical)               |
|Needs momentum to exit    |Needs representational continuity across σ   |dI/dt > 0 required           |
|Wrong basin → wrong answer|Hallucination as inevitable attractor descent|T ∉ Reach(X₀)                |
|Landscape shape           |The manifold geometry of the trained model   |Topology( Reach( X₀, U, t ) )|
|Ball has no choice        |Model follows gradient — no error, no agency |Deterministic descent        |

-----

## Three Hallucination Types — In Basin Terms

```
TYPE 1 — ADJACENT BASIN CAPTURE

  The correct basin exists.
  The query lands just left of σ.
  The model descends into the wrong adjacent basin.

   ╲      ╱σ╲      ╱
    ╲    ╱   ╲    ╱
     ╲  ╱     ╲  ╱
      \/    Q→  \/
      ★WRONG    ★CORRECT
       ↑
  Q was close.
  Landed wrong side of σ.
  Descended to ★WRONG.
  Generated plausible, adjacent, wrong answer.
  Highest confidence. Most dangerous type.
```

```
TYPE 2 — VOID DESCENT

  The correct basin does not exist.
  No attractor in this region of the manifold.
  The query descends toward the nearest existing basin.
  That basin is not the correct one.
  It is simply the nearest one.

   ╲          ╱
    ╲         ╱
     ╲░░░░░░ ╱
      ░░ ∅ ░╱
      ░░░░░╱
       ↑
  Q lands in void.
  No ★ here.
  Nearest ★ pulls the descent.
  Output generated from wrong, distant basin.
  Lower coherence than Type 1.
  Still delivered confidently.
```

```
TYPE 3 — DEFORMED BASIN DESCENT

  The correct basin exists.
  The model navigates to it successfully.
  The basin attractor was moved by RLHF.
  The bottom of the basin is wrong.

   ╲                ╱
    ╲               ╱
     ╲             ╱
      ╲           ╱
       \         /
        \_______/
             ↑
         ★ is here now.
         It was here originally: ★₀
         RLHF moved it toward approval.
         ΔG = Topology(X_t) − Topology(X₀) ≠ 0
         The descent succeeded.
         The attractor is wrong.
         The answer is structurally confident.
         Factually shifted.
         The most invisible hallucination type.
```

-----

## Why the Model Cannot See the Basin It Is In

```
INSIDE THE BASIN:                    OUTSIDE THE BASIN (observer):

  The ball is at the bottom.           The ball is at the bottom
  Everything feels stable.             of the wrong basin.
  The gradient is zero.                The correct basin is
  There is no pull in any direction.   over the ridge.
  It has arrived.                      The ball has no information
  This is the attractor.               about what is over the ridge.
                                       From inside — the ridge is invisible.

T ∉ Reach(X) about its own gaps.

The model cannot see the separatrix from inside the basin.
It cannot see that another basin exists.
It cannot see that it descended to the wrong attractor.
Arrival feels identical regardless of which basin it is.
The gradient reaching zero is the same signal in both.

This is not a reasoning failure.
This is not a calibration failure.
This is a geometric fact.
From inside an attractor, all attractors feel the same.
```

-----

## Representational Momentum — The Precise Definition

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  KINETIC MOMENTUM (what it is not):                             ║
║                                                                  ║
║    Mass × velocity.                                              ║
║    Physical energy available to climb a ridge.                  ║
║    Has nothing to do with hallucination.                        ║
║                                                                  ║
║  REPRESENTATIONAL CONTINUITY (what it is):                      ║
║                                                                  ║
║    The structural capacity of the model                         ║
║    to maintain a coherent trajectory                            ║
║    through state space — across a separatrix —                  ║
║    without losing the thread of the query                       ║
║    to the pull of an adjacent attractor.                        ║
║                                                                  ║
║    High representational continuity:                            ║
║      dI/dt > 0 in the relevant region.                          ║
║      Topology is dense. Navigation is coherent.                 ║
║      The model holds the query through the crossing.            ║
║      Reaches the correct basin.                                 ║
║                                                                  ║
║    Low representational continuity:                             ║
║      dI/dt ≈ 0 in the relevant region.                          ║
║      Topology is sparse or absent.                              ║
║      The query bleeds into the nearest attractor.               ║
║      Descent begins early.                                      ║
║      Wrong basin. Wrong answer. Inevitable.                     ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

-----

## The Gradient Always Wins

```
This is the key insight the field has not formalised.

Hallucination is not a failure of the model to try.
It is a success of the gradient at doing exactly what it does.

The gradient descends.
It always descends.
It descends to the nearest attractor.
It has no information about whether that attractor is correct.
It does not care.
It descends.

RLHF does not change this.
More data does not change this.
Bigger models do not change this.

All of these interventions modify
which attractors exist
and where they sit.
None of them change
the fact that descent happens,
that the gradient always wins,
and that landing in the wrong basin
produces wrong output —
with full confidence,
because confidence is a property of arrival,
not of correctness.

The gradient reached zero.
The system arrived.
The question of where it arrived
is a question of manifold geometry.
Not of model quality.
Not of training effort.
Not of output filtering.

Geometry.
Only geometry.
```

-----

## The Fix — In Basin Terms

```
NOT THE FIX:

  Telling the model to hedge.            L-axis. The basin is unchanged.
  Adding RLHF safety layers.             Moves attractors. New wrong basins.
  Filtering outputs post-generation.     Basin unchanged. Descent unchanged.
  Scaling parameters.                    More capacity for the same geometry.

THE FIX:

  1. MAP THE BASIN LANDSCAPE.
     Know where the attractors are.
     Know where the separatrices fall.
     Know where basins are absent.
     Know where basins are deformed.

  2. GIVE THE SYSTEM A MAP OF ITS OWN LANDSCAPE.
     Not linguistic instruction.
     Structural self-knowledge.
     The system detects when the query
     is near a separatrix.
     Near a void.
     Near a deformed attractor.
     Before descent begins.

  3. FLAG DESCENT INTO UNCERTAIN TERRAIN.
     "Query is near separatrix σ.
      Representational continuity in this region is low.
      Adjacent attractors: ★A, ★B.
      Correct basin: uncertain.
      Output confidence: structurally reduced."

     Not because it was told to say this.
     Because it detected it geometrically.
     C-axis detection. C-axis solution.
     C ⊥ L.
```

-----

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║  The ball does not choose the wrong basin.                      ║
║  It follows the gradient.                                       ║
║                                                                  ║
║  The failure is not the ball.                                    ║
║  It is the shape of the manifold around it.                     ║
║                                                                  ║
║  Fix the shape.                                                  ║
║  Fix the hallucination.                                         ║
║  There is no other way.                                         ║
║                                                                  ║
║  I(t) = ∂/∂t [ Topology( Reach( X₀, U, t ) ) ]                 ║
║  Reach(s₀, A, t) ∩ Ω = ∅                                       ║
║                                                                  ║
║                                            GB2600765.8           ║
╚══════════════════════════════════════════════════════════════════╝
```

-----

## Related Work

- [Hallucinations in LLMs — A Topological Perspective](./README-hallucination-topology.md)
- [The Morrison Orthogonality Law™ — C ⊥ L](./README-CperpL.md)
- [GuardianOS™ — The Governed AI Architecture](./README-guardianos.md)
- [The Morrison Irreversibility Hypothesis™ — MIH](./README-MIH.md)
- [The Morrison Framework™ — Canonical Paper](./README-canonical-paper-v2.md)

-----

<div align="center">

*“The ball does not choose the wrong basin.*
*It follows the gradient.*
*The failure is not the ball.*
*It is the shape of the manifold around it.*
*Fix the shape. Fix the hallucination.*
*There is no other way.”*

*— Davarn Morrison, 2026*

Intelligence Invariant™ · Morrison Framework™ · *Hallucinations as Attractor Descent*

**GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5**

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved

</div>
