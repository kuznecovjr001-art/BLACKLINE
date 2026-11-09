# BLACKLINE

**A living-city survival game built with Godot.** Project documentation and development contracts for a fictional, geographically inspired city built from a curated, license-compliant modular asset library.

> **State:** Godot is the current active development engine (2026-11-09). Prior Unreal experiments remain archived as research; they are not the implementation target. **This repository is public.** Do not publish private Google Drive documents, secrets, paid/source assets, personally identifying data, or restricted geodata.

## Vision

- Plausible large-scale urban geography: street topology, paths, courtyards, industrial areas, parks, railways and water; visual architecture is reauthored, **not copied**.
- **Causal simcade realism:** physical mass, material, inertia, friction, impacts, resource flows, injury and wear affect outcomes. Responsive controls and accessible vehicle driving remain non-negotiable.
- WASD character movement, independent mouse aiming, hybrid rotatable isometric camera, automatic floor cutaway with visibility/occlusion rules preserved.
- Modular buildings and explorable multi-storey interiors; context-sensitive loot, repair, production, utilities, persistent world, zombies, seasonal and permanent modes.
- Build a testable **vertical slice** before generating an entire city. The map does not become a grey-block final asset.

## Start here

1. [Product canon](docs/00_PROJECT_CANON.md): what is approved vs open.
2. [GrillMe traceability](docs/01_GRILLME_TRACEABILITY.md): design decisions and their original ADR ranges (full originals remain in private project storage).
3. [World design](docs/world/CITYFORGE.md) and [asset policy](docs/art/ASSET_AND_LICENSES.md).
4. [Physics and gameplay](docs/engineering/PHYSICS.md), [character and animation](docs/character/ANIMATION_AND_CAMERA.md), [vehicles](docs/vehicles/SIMCADE.md).
5. [Roadmap](docs/ROADMAP.md), [agent roles](docs/agents/AGENT_TEAM_AND_TOOLS.md), [Claude instructions](CLAUDE.md) and [contributing rules](AGENTS.md).

## Repository boundary

This repository is initialized as **documentation-first** to avoid overwriting the already-running local Godot project. When importing game files, keep `project.godot` at the repository root and reconcile `.gitignore`, `addons/`, `assets/`, `scenes/` and `scripts/` in a dedicated reviewed change. Do not replace the real Godot project with a fabricated starter scene.

## Governing rule

**No unapproved design changes masquerading as implemented features.** Every change cites its requirement, includes acceptance tests and records asset provenance. A written plan is not proof of a working build.
