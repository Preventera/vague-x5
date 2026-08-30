<div align="center">

<img src="assets/logo.png" alt="AgenticX5" width="110">

# vague-x5

**L0-L4 registry and pre-registered protocols**

![status](https://img.shields.io/badge/status-demonstration-orange) ![governance](https://img.shields.io/badge/governance-HITL-blue) ![license](https://img.shields.io/badge/license-TBD-lightgrey)

[Lire en français](README.md)

</div>

---

> [!WARNING]
> **Architectural demonstration.** This repository is not a shipped product. Nothing
> here constitutes actuarial, medical or legal advice. No real-world deployment
> without calibration on Quebec data, third-party validation, a Law 25 agreement and
> human-in-the-loop governance.

## Contents

The apparatus that lets an OHS measure rollout **produce evidence** instead of a
mere implementation record.

Principle: comparison comes from the schedule, not from withholding. Nobody gives
up a safety measure — the control is whoever is **not yet** equipped. Everyone
ends up equipped.

## The five principles

1. Nothing is proven without comparison.
2. Comparison comes from the schedule, not from withholding.
3. Measure usage, not possession.
4. Write down what you are looking for before looking.
5. Start where the data already exists.

## Layered architecture

| Layer | Contents | Regime |
|:---:|---|---|
| **L0** | Registry — entities, context, schedule | Versioned, never overwritten |
| **L1** | Seal — frozen protocol | Write-once, timestamped |
| **L2** | Observation — rollout, dose, outcome | Provenance mandatory |
| **L3** | Analysis — execution of the sealed protocol | Reads L1 only in full |
| **L4** | Evidence — PreuveX5 records | Conditional on a valid seal |

### Flow rules

> [!CAUTION]
> **No going back up.** L3 does not modify L1. L4 does not modify L3.
> If a result displeases, the protocol is not rewritten — a new wave is launched
> with a new seal.

An analysis not declared in L1 comes out labelled **exploratory** and can never
feed L4. No coefficient in `trajectoire-x5` without a `sceau_id`.

These rules should be enforced by branch protection, not discipline alone:
`l1-sceaux/` should never receive a commit modifying an existing file.

## The field everyone forgets

`definition_non_concluant`, **distinct from "no effect"**. Without it, insufficient
power reads as absence of effect. It is the costliest field to omit.

## First seal — VX5-001

**Temporary assignment.** Chosen because the data already exists (administrative
claim files), the event is frequent, no sensor is required, and a result is
reachable within 18 months. See [`l1-sceaux/VX5-001.md`](l1-sceaux/VX5-001.md).

> [!IMPORTANT]
> **Ethical reservation.** A reduction in indemnity duration may reflect better
> return to work — or pressure on the worker. The protocol includes a
> counterweight outcome: recurrence rate and dispute rate. A duration decrease
> accompanied by a recurrence increase is not a success.

## Watch points

**The main risk is L2, not L3.** The temptation will be to clean the doses. Each
step is defensible in isolation; cumulatively they make the result indefensible.

**The population will be self-selected.** Establishments that adopt nothing —
often the most at risk — stay invisible. Every record must say so.

**Conflict of interest.** Producing evidence about your own tools requires a
third-party analyst. Public pre-registration and external validation are not
ornaments: they are the conditions for the result to be read at all.

## External vocabulary

Internally: wave, dose, seal. Toward a public body, a mutual insurer or a research
institute, translate — *stepped rollout*, *effective usage rate*, *pre-registered
protocol*. These terms pass without explanation.

---

<div align="center">

**AgenticX5 · NordicX5** — Montréal, Québec
[team@agenticx5.com](mailto:team@agenticx5.com)

*Sources are linked, never reproduced. AI proposes, humans decide.*

</div>
