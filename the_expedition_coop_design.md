# The Expedition — Co-op Squad Design Document
**Version 1.0 — Pre-build**
*This document defines mechanics only. No code is written until this is approved.*

---

## The Central Question

Solo play is a conversation between one Seeker and Dissolution. The tension is personal — how deep do I go, how much do I carry, when do I turn back.

Co-op must preserve that tension and add a second layer: *other people make you braver than you should be.* Squads go deeper than they should. They carry more than they should. They push each other past good judgment. That is the co-op experience — and Dissolution punishes it.

---

## Squad Structure

**2 to 4 players.** Each player is a Seeker. Each Seeker carries one Rune as their squad role. No two Seekers in the same squad can hold the same Rune. This is enforced at squad formation.

The five Runes become five roles:

| Rune | Role Name | Squad Function |
|---|---|---|
| Silence | The Carrier | Increases shared carry capacity. The squad's load-bearer. |
| Recovery | The Reader | Reveals hidden items for the whole squad. The scout. |
| Memory | The Archivist | Processes one fragment in the field per run, for the whole squad. |
| Witness | The Identifier | Marks distorted items before anyone touches them. Protects the squad from bad recoveries. |
| Thresholds | The Vanguard | Enables Wilds crossing for the whole squad. The one who leads into danger. |

A squad of two has two roles covered. A squad of four has four. A full squad of five covers everything — but five-player squads are endgame content, unlocked after completing the first full chain in co-op.

---

## Dissolution — Shared or Individual?

This is the most important mechanical decision in the document.

**Option A — Fully shared pool.** One Orientation bar for the whole squad. Everyone's burden contributes to the drain rate. Fast, brutal, requires constant communication.

**Option B — Individual bars, shared threshold.** Each Seeker has their own Orientation. But Dissolution events affect the whole squad simultaneously — if one player hits Level IV, everyone feels it.

**Option C — Individual bars, contagion model.** Each Seeker has their own Orientation. But Dissolution is contagious — a player at Level III passively drains nearby squadmates.

**Decision: Option C — Individual bars with contagion.**

Here is why. Option A removes individual agency — your careful play means nothing if your squadmate is reckless. Option B is too disconnected — you can ignore each other. Option C creates the right dynamic: you are responsible for yourself, but you cannot be indifferent to the state of your squadmates. A struggling player becomes a liability. A stable player becomes a resource. The squad has to manage each other, not just themselves.

---

## Contagion Mechanics

When a Seeker reaches **Dissolution Level II or higher**, they begin emitting a passive drain on squadmates within proximity.

- **Level II** — emits 0.5 drain per tick to adjacent Seekers
- **Level III** — emits 1.5 drain per tick to adjacent Seekers, visible warning indicator on all squad members' screens
- **Level IV** — emits 4 drain per tick, full screen edge pulse visible to all, squad-wide alarm tone

Proximity is defined by depth. Players at the same depth level are adjacent. Players one depth apart are distant — contagion halved. Players two depths apart are isolated — no contagion.

This means the squad can manage a struggling player by separating — send them back to the Node while the rest continue. Or stay together and absorb the cost. Both are valid decisions. Both have tradeoffs.

---

## Burden — Pooled or Individual?

**Decision: Individual burden, shared awareness.**

Each Seeker carries their own items. Their own burden. Their own drain rate. But every squadmate can see what everyone else is carrying — names, weight, and chain association — on a shared squad panel.

This creates informed decision-making without removing individual responsibility. The Carrier (Silence Rune) has higher carry capacity and should be carrying the heaviest items. The Reader (Recovery Rune) should be scouting light. The squad optimises together.

There is no forced item transfer. A Seeker cannot take an item from another Seeker's inventory. But a Seeker can **drop** an item at a shared recovery point, which another Seeker can then pick up. This is the squad's coordination mechanic — deliberate, not automatic.

---

## The Node — Squad Behaviour

When any Seeker returns to the Node, they return alone. They process their own recoveries. Their individual Orientation restores.

The squad Node state shows which Seekers are currently in the field and which are at the Node. A Seeker at the Node can see the live Orientation of squadmates still in the field.

**The Recall Signal.** Any Seeker at the Node can send a recall signal to the squad in the field. This appears as a gentle amber pulse on the field Seekers' screens — not an alarm, not a command. A suggestion. The field Seekers decide whether to heed it.

This mechanic exists because the most common co-op failure is someone at the Node watching a squadmate deteriorate in real time and having no way to communicate urgency. The recall signal gives them one tool. It respects the field Seeker's autonomy.

---

## Chain Investigation in Co-op

Chains belong to the squad, not to individuals. Fragment progress is shared — any Seeker recovering a chain item advances the chain for everyone.

However, the **hypothesis is individual.** When the 50% threshold is reached, each Seeker sees the hypothesis prompt independently. Each Seeker commits their own answer. The revelation shows each Seeker's verdict separately — who was right, who was incomplete.

This creates the possibility of disagreement within the squad. Two players choose different hypotheses. One is correct. This is intentional. It generates conversation, debate, and replay motivation.

**Chain mastery in co-op** is harder than solo — a chain is only marked complete for a Seeker when they have personally committed a hypothesis and seen the revelation. Completing a chain as a squad does not substitute for individual understanding.

---

## Voidborn Encounters in Co-op

Voidborn encounters in solo are individual — you face them alone, you make the choice alone.

In co-op, Voidborn encounters are **squad events.** All Seekers at the same depth level see the encounter simultaneously. The choice is put to the squad — each Seeker votes. The majority choice executes after a 12-second window.

If the squad is split across depth levels, only the Seekers at the encounter depth participate. Seekers at other depths see a notification: *"Squad encountering Voidborn at depth [X]."*

**Unanimous choices** receive a small Orientation bonus for all participating Seekers. Divided squads receive no bonus — the cost of disagreement.

---

## Rune Synergy — Specific Combinations

These are the designed synergies. When these combinations are active in the same squad, additional effects unlock:

**Silence + Recovery** (Carrier + Reader)
The Reader's hidden item reveals now also show weight, reducing the Carrier's burden calculation risk. *"Knowing what you're carrying before you carry it."*

**Memory + Witness** (Archivist + Identifier)
The Archivist's field processing can now process items that the Identifier has marked as distorted — normally field processing only works on clean items. *"Understanding what is broken is still understanding."*

**Thresholds + any two others** (Vanguard active squad)
The Vanguard's Wilds crossing now applies to the entire squad simultaneously. Without this, each Seeker would need the Thresholds Rune to cross. With it, the Vanguard leads and the squad follows. *"One person's courage can carry others across."*

**Full squad of five — all Runes represented**
Unlocks The Deep Run — a special expedition type where the site generates at depth 5 rather than depth 4 maximum. Available only in five-player squads. High risk, high fragment yield, high chain acceleration.

---

## Squad Roles at the Node — Async Play

Co-op does not require all players to be online simultaneously. The squad shares a persistent Node state. A Seeker can run a solo expedition and their recoveries contribute to the shared chain progress.

However, certain squad actions require presence:
- Voidborn votes require all Seekers at that depth to be active
- The recall signal only works in live sessions
- Rune synergy bonuses only activate when both Rune holders are in the same session

Async play is valid and supported. Live play unlocks additional mechanics.

---

## What Co-op Changes About the World

The Expedition's philosophy is that recovery is more important than possession, and understanding is more valuable than accumulation.

Co-op adds a fourth law — unstated in the game, but present in every session:

*Continuity is maintained together or not at all.*

No single Seeker can complete the full chain of understanding alone — not because they lack access, but because the act of comparing hypotheses, of watching another Seeker make a different choice, of being recalled by someone who can see what you cannot — this is itself a form of understanding. The co-op layer is not a multiplayer mode. It is an argument, made mechanically, that some things can only be known in relation to others.

---

## Build Sequence

When approved, build in this order:

1. Squad formation screen — Rune assignment, role display
2. Shared chain progress sync
3. Individual Orientation with contagion drain
4. Squad panel — live burden visibility
5. Recall signal
6. Voidborn squad vote
7. Individual hypothesis in shared chain
8. Rune synergy effects
9. Async session state
10. Five-player Deep Run unlock

---

*Document status: Draft — awaiting creative director approval before any code is written.*
