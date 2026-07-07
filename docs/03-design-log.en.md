# 03 · Design Log

[한국어](03-design-log.md) | **English**

This project proceeded on three working principles.

1. **Theory first, code later** — every decision is justified theoretically before implementation.
2. **One axis at a time** — no simultaneous decisions; one axis is settled through dialogue before moving on.
3. **Restraint** — whenever the work slides toward cinematic excess, pull back. Doing less is doing.

Below is a chronological record of the major decisions.

---

## 2026-04-21 — Establishing the metaphor

Analyzed dialogues with a ChatGPT construction-safety persona (in the role of risk manager) to extract
the structure of a multi-agent system, and mapped it onto the **six rooms of a library**.
Produced a supervisor dashboard wireframe (Figma, 1440×1040) and an interactive interim-review HTML.

Key decisions at this stage:

- **Asymmetric mutual visibility** — workers invisible to one another (data purity), workers visible to the supervisor.
  The researcher's own insight; it governs all subsequent design.
- **The dual-language system** — answering the persona's critique of "delayed metaphor interpretation in emergencies."
  Internal narration speaks library language; screen labels and emergency alerts speak functional language. Switched by a UI toggle.
- **"Surface is message"** — for site legibility, state is conveyed by background change, not text color.
- **Selecting the most essential interaction** — the red pulse of the mismatched row. Chosen as the one interaction
  that works without demanding attention — the one that operates like architecture.
- **The AI persona as design peer-reviewer** — a verification cycle of submission → persona critique → response → resubmission.
  Four critiques (metaphor delay / habituation to "no anomaly" / supervisor screen overload / alarm fatigue), each answered.

## 2026-04-22 — Review feedback and theoretical realignment

Review feedback: *"This is virtual-space design, yet it leans toward structural design."*
Translated into the axis of **System-as-space vs. Designed space** — describing a system through
spatial metaphor versus spatial properties becoming variables of the system.

After evaluating four directions in which "space becomes a variable" (zoom = observation distance,
dwelling = authority, the memory of space, wall thickness = information speed), a third direction
free of that pressure was taken as the working hypothesis —
**a space in which the visitor moves between roles and comes to know each position's field of view bodily,
with the asymmetry of visibility itself as the design variable.**
The question was deliberately kept unresolved.

## 2026-04-23 — Organizing the theoretical ground

Organized the theoretical vocabulary — Mattern (Library as Infrastructure), Hillier (space syntax),
Fujimoto (intimate exterior), engawa · ma · oku — and distributed it across the rooms.
Confirmed the points where Western theory and Japanese concepts say the same thing
(node ≈ oku, gradations of intimacy ≈ engawa) — the stage at which asymmetric visibility
was grounded in both traditions at once.

Fixed the final form of the web app: **a role-selection SPA**, single HTML, a five-minute experience,
built in collaboration with Claude without a developer.

## Late 2026-04 — Blueprint for the worker's screen

A detailed blueprint (`worker_chamber_blueprint.md`) preceded implementation. Key decisions:

- **The five intervals of mediation** — input (1s), sealed transit (2–3s), entry (0.5–1s),
  own response (3–4s), control order (4–5s). The principle that each interval must create
  at least one of: awareness, review, intervention.
- **Fluid vs. crystal** — the everyday and danger distinguished by *states of matter*, not color.
  The foundation of the visual language.
- **Branches A/B** — the system's processing and the visitor's position diverge by whether one reports.
  The experiential proof of the thesis.
- **The guide window stays outside the system** — since the demo's captions compensate for the absence
  of site experience, they are visually separated from the system, in the tone of museum captions.
- **Control orders address the environment, not the individual** — why the crystalline form of an order
  lodges at the capsule's boundary instead of being absorbed inside.

## 2026-05 ~ 06 — Implementation and integration

Following the worker and supervisor screens, built the director's office, stacks, and cataloguing room,
and merged everything into a single file.

- **A shared rendering engine** — a dependency-free canvas Bayer 4×4 dither engine shared by all rooms.
  The single red `#E24B4A` is reserved for danger and mismatch only (no decorative use).
- **Director's office** — the vertical spine of the whole hierarchy. The beams of the three decisions
  (stop/continue/return) reach different ranges — the scope of authority expressed as the reach of light.
- **Stacks** — the record ↔ place interaction. Clicking a record on the index lights its location deep among the shelves.
- **Cataloguing room** — orchestration graph + synchronized step log + replay.
- **How the system rooms are entered** — the cataloguing room and stacks are entered by clicking nodes
  of the diagram, not role buttons. The distinction between people's places and the system's places,
  expressed by the mode of entry itself.
- The technical resolution of integration: separating SVG labels redrawn every frame from click targets
  (visuals in SVG; clicks on fixed DOM hotspots realigned every frame via `getScreenCTM()`).

Deployed the final build to Vercel on 2026-06-16.

---

## Unresolved

- **System-as-space vs. Designed space** — the open question, to be addressed in the dissertation
- **Return Desk (Site Control Output Layer)** — not built as an independent room
- Further refinement of transitions between rooms and viewpoint consistency
