# Constraint Instrument

A constraint-music toolset inspired by jazz masters. **7 modes, 17 terrains, infinite music.**

The Constraint Instrument maps musical traditions onto constraint surfaces — bathymetric charts of harmonic, melodic, and rhythmic space. Each mode is a different way of relating to constraint space, named after a jazz legend whose playing embodied that relationship.

## The Seven Modes

| Mode | Named After | Philosophy |
|------|------------|------------|
| **Parker** | Charlie Parker | Practice & internalize the lattice — repetition until the constraints become reflex |
| **Miles** | Miles Davis | Explore the frontier — always find something new at the edge |
| **Ellington** | Duke Ellington | Architect for emergence — design constraints that produce surprises |
| **Basie** | Count Basie | Real-time consensus — let the band decide together |
| **Goodman** | Benny Goodman | Diagnostics — find what's missing, what's under-constrained |
| **Armstrong** | Louis Armstrong | Liberation through constraint removal — what happens when you let go? |
| **Ella** | Ella Fitzgerald | Pure flow — the tool disappears, only music remains |

## The 17 Terrains

Terrain maps define the topology of a musical landscape — scale degrees, weights, rhythmic skeletons, register tendencies, and chromatic density.

### Legacy Terrains
- **blues** — The deep water. 12-bar form, blue notes, call-and-response.
- **bebop** — Fast, dense, chromatic. The lattice at speed.
- **modal** — Sparse constraints, wide open spaces.
- **classical** — Tonal architecture. Voice-leading as constraint.
- **free_jazz** — Minimal constraints. Maximum freedom.

### Rich Bathymetric Terrains
- **delta_blues** — Deep delta, slide guitar, vocal cry
- **bebop_rich** — Full bebop bathymetry with chromatic fields
- **modal_jazz** — Miles's Kind of Blue territory
- **classical_counterpoint** — Species counterpoint as constraint system
- **bluegrass** — High lonesome sound, Appalachian modal mixture
- **hip_hop_trap** — 808 gravity, hi-hat tessellation, auto-tuned attractors
- **afro_cuban** — Clave-based polyrhythmic constraint system
- **indian_raga** — Raga as constraint: vadi, samvadi, alankar
- **chinese_silk_bamboo** — Pentatonic lattice, qin ornamentation constraints
- **electronic_techno** — Grid-based, four-on-the-floor, filtered constraint
- **gospel** — Call-response, melismatic, harmonic gravity wells
- **free_improvisation** — Structured freedom: timbral and textural constraints

## Installation

```bash
pip install -e .
```

For audio output:
```bash
pip install -e ".[audio]"
```

## Quick Start

```python
from constraint_instrument import Instrument, TERRAINS

# Create an instrument with a terrain
inst = Instrument(terrain=TERRAINS["bebop"])

# Use different modes
inst.parker(bars=8)        # Practice mode — internalize
inst.miles(bars=8)         # Explore mode — frontier
inst.ellington(bars=8)     # Architect mode — emergence
inst.basie(bars=8)         # Consensus mode — group
inst.goodman()             # Diagnose mode — find gaps
inst.armstrong(bars=8)     # Liberation mode — remove constraints
inst.ella(bars=8)          # Flow mode — disappear
```

## Examples

See `src/constraint_instrument/examples/`:
- `parker_practice.py` — Practice mode walkthrough
- `miles_explore.py` — Frontier exploration
- `goodman_diagnose.py` — Diagnostic output

## Architecture

```
src/constraint_instrument/
├── __init__.py          # Package entry, exports Instrument, Terrain, TERRAINS
├── instrument.py        # Core Instrument class
├── terrain.py           # Terrain dataclass + legacy definitions + registry
├── terrains/            # 12 rich bathymetric terrain maps
├── parker.py            # Practice mode
├── miles.py             # Explore mode
├── ellington.py         # Architect mode
├── basie.py             # Consensus mode
├── goodman.py           # Diagnostic mode
├── armstrong.py         # Liberation mode
├── ella.py              # Flow mode
├── monitor.py           # Real-time constraint monitoring
├── genre_brain.py       # Genre-aware constraint generation
├── chords.py            # Chord voicing constraint system
├── texture.py           # Textural constraint analysis
├── liner_notes.py       # Programmatic liner notes generation
├── exercises.py         # Constraint-based practice exercises
├── nomenclature.py      # Musical nomenclature reference
├── terrain_morph.py     # Smooth terrain morphing between landscapes
├── seed_manager.py      # Deterministic seed management for reproducibility
├── analyzer.py          # Constraint surface analysis tools
├── tracks.py            # Multi-track constraint composition
└── examples/            # Usage examples
```

## Documentation

- [`docs/INVISIBLE-ENGINEER.md`](docs/INVISIBLE-ENGINEER.md) — *The Invisible Engineer*: essay on monitor engineering as metaphor for constraint-based tools
- [`docs/NOMENCLATURE.md`](docs/NOMENCLATURE.md) — Musical nomenclature reference
- [`docs/USER-REPORTS/`](docs/USER-REPORTS/) — User feedback from jazz saxophonists, electronic producers, hip-hop producers, and math educators
- [`site/`](site/) — Web playground and audio demos

## Connection to Conservation Spectral Analysis

The Constraint Instrument embodies a core principle of the conservation spectral ecosystem: that creative constraints are not limitations but *spectral signatures* — unique fingerprints of a musical tradition's relationship to harmonic, rhythmic, and textural space. Each terrain map is a conservation law in miniature, defining what quantities remain invariant (tonal center, groove skeleton, register balance) while allowing everything else to vary. The monitor and house modes parallel spectral analysis techniques: reading the system state, detecting deviations from the constraint surface, and providing corrective feedback that preserves the conserved quantities.

## License

MIT

## Related Repos

- **[plato-room-musician](https://github.com/SuperInstance/plato-room-musician)** — Sonify PLATO fleet activity via MIDI
- **[flux-tensor-midi](https://github.com/SuperInstance/flux-tensor-midi)** — INT8-saturated MIDI for neural synthesis
- **[tensor-spline](https://github.com/SuperInstance/tensor-spline)** — Compressed neural network layers (Eisenstein lattice splines)
- **[penrose-memory](https://github.com/SuperInstance/penrose-memory)** — Aperiodic memory palace (another aperiodic-math-meets-AI project)
- **[holonomy-harmony](https://github.com/SuperInstance/holonomy-harmony)** — Chord progression analysis via holonomy

Part of the [SuperInstance OpenConstruct](https://github.com/SuperInstance/OpenConstruct) ecosystem.
