# Safety Space — 안전 가상공간

[한국어](README.md) | **English**

A web prototype that visualizes a multi-agent AI system for construction-site safety through the **spatial metaphor of a library**.

![Title screen — full system diagram with role buttons](assets/title.png)

> **Core thesis — Distributed Accountability through Mutual Visibility.**
> Workers are invisible to one another (blocking collusion and conformity pressure) yet visible to the supervisor; the supervisor is visible to the director.
> This **asymmetric visibility structure** governs the entire spatial design of the system.

## Preface

This project was carried out in a graduate course at the Department of Space Design, Kookmin University (Prof. Seymin). The brief: take a GPTs persona built by another student as a client, and design a virtual space for that persona. I was assigned a GPTs for construction-site safety inspection and management, and through dialogue with it set the goal of building a multi-agent safety system as a virtual space.

The process surfaced a collision between space for AI agents — which need neither gravity nor transitional mediation — and space for human users, which requires correspondence with real space and mediating thresholds. The system's spatial logic was drawn from the library, where ordinary users and librarians face the same shared data — books — in fundamentally different ways. The documents below describe how the project was built.

## Live demo

- **GitHub Pages:** https://banhangsim.github.io/safety-space/
- **Vercel:** https://yangwook-final-0616.vercel.app

Recommended: desktop browser (Chrome / Safari). A single self-contained HTML file with no dependency other than Three.js (CDN).

## How to experience it

Start from the full diagram on the title screen.

1. **Role buttons** — Worker / Supervisor / Director → zoom into each room (a ritual of entry)
2. **Node click** — click the `CATALOGING` and `STACKS` labels on the diagram → enter the system rooms
3. In every room, `←` returns to the title — **moving between roles always passes through the whole diagram**

The purpose of this space is to come to know, bodily, *what is visible and what is not* from each position.

## The six rooms

| Room | System layer | Status |
|---|---|---|
| Reading Room (열람실) | Worker Input Layer | Built |
| Reference Librarian's Desk (참고사서 데스크) | Supervisor Review Layer | Built |
| Director's Office (관장실) | Authority Control Layer | Built |
| Cataloguing Room (목록실) | Agent Orchestration Layer | Built |
| Stacks (서고) | Raw Evidence Archive | Built |
| Return Desk (반납대) | Site Control Output Layer | **Not built (open question)** |

Details: [docs/02-rooms.en.md](docs/02-rooms.en.md)

## Documents

- [01 — Thesis and theoretical grounding](docs/01-thesis.en.md)
- [02 — The six rooms](docs/02-rooms.en.md)
- [03 — Design log](docs/03-design-log.en.md)

## Research context

This project explores *"how an extraordinary digital space borrows everyday spatial grammar to create trust."* If "who sees whom" is the grammar of community in physical space, in this system it is the grammar of safety.

It is also the first prototype toward **Banhangsim Design Studio's spatial-design multi-agent system** — a starting point for extending the methodology of spatial design into agent systems.

## Tech

- Single self-contained HTML (~245KB) — no build step
- Three.js r128 (CDN — title and entry screens)
- Dependency-free canvas Bayer 4×4 dither rendering engine (room screens)
- Fonts: Inter + Pretendard

## Author

유양욱 (반항심) — 국민대학교 대학원 공간디자인학과 박사과정 · 반항심 디자인 스튜디오
/프로토타입 구현: Claude (Anthropic) 와의 협업
