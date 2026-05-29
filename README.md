# constraint-instrument

A constraint-music instrument with seven playing modes inspired by jazz masters — from strict lattice practice to pure improvisational flow.

## What This Gives You

- **Seven musical modes** — Parker (practice), Miles (explore), Ellington (architect), Basie (real-time), Goodman (diagnose), Armstrong (liberate), Ella (flow)
- **Musical terrains** — blues, bebop, modal jazz, gospel, free improvisation, classical counterpoint, and more
- **Performance pipeline** — compose → play → render → diagnose in one API
- **Exercise generator** — structured practice routines for species counterpoint, voice leading, and rhythmic constraints
- **Self-diagnosing output** — the instrument analyzes its own performance against constraint-theory metrics

## Quick Start

```python
from constraint_instrument import Instrument

# Ella mode: pure flow, the tool disappears
inst = Instrument(mode='ella', terrain='blues', key='C', bpm=100, bars=4)
notes = inst.perform()      # generate notes
inst.play()                 # play through speakers
inst.render('output.wav')   # save audio
inst.diagnose()             # analyze against constraints
```

### All Seven Modes

```python
# Parker: practice & internalize the lattice
inst = Instrument(mode='parker', terrain='bebop', key='Bb', bpm=140)

# Miles: explore the frontier, always new
inst = Instrument(mode='miles', terrain='modal_jazz', key='D')

# Ellington: architect for emergence
inst = Instrument(mode='ellington', terrain='swing', key='F')

# Basie: real-time consensus
inst = Instrument(mode='basie', terrain='blues', key='C')

# Goodman: diagnostic, find what's missing
inst = Instrument(mode='goodman', terrain='delta_blues', key='E')

# Armstrong: liberation through constraint removal
inst = Instrument(mode='armstrong', terrain='free_jazz', key='A')

# Ella: pure flow
inst = Instrument(mode='ella', terrain='gospel', key='Ab')
```

### Exercises

```python
from constraint_instrument.exercises import generate_exercise

ex = generate_exercise("species_counterpoint", "beginner", seed=42)
print(ex["instructions"])
```

## API Reference

| Class / Function | Description |
|---|---|
| `Instrument(mode, terrain, key, bpm, bars)` | Main instrument API |
| `Instrument.perform()` | Generate a performance (returns note list) |
| `Instrument.play()` | Play through system audio |
| `Instrument.render(path)` | Save to WAV file |
| `Instrument.to_midi(path)` | Export as MIDI |
| `Instrument.diagnose()` | Analyze output against constraints |
| `Terrain` | Musical terrain definitions |
| `ChordProgression` | Chord sequence builder |
| `SeedManager` | Reproducible randomness |
| `ExerciseGenerator` | Practice exercise factory |

### Terrains

| Terrain | Description |
|---|---|
| `blues` | 12-bar blues with blue notes |
| `delta_blues` | Raw delta blues feel |
| `bebop` | Fast bebop lines with chromaticism |
| `modal_jazz` | Modal exploration (So What style) |
| `gospel` | Gospel voicings and progressions |
| `free_jazz` | Free improvisation |
| `classical_counterpoint` | Species counterpoint |
| `swing` | Swing-era big band |

## How It Fits

This is the **musician-facing API** of the constraint theory ecosystem:

- Built on [constraint-theory-core](https://github.com/SuperInstance/constraint-theory-core) for lattice, funnel, and rigidity primitives
- Uses [constraint-synth](https://github.com/SuperInstance/constraint-synth) for audio rendering
- Part of the [SuperInstance](https://github.com/SuperInstance) ecosystem

## Testing

```bash
python -m pytest constraint_instrument/test_integration.py -v
```

## Installation

```bash
pip install -e .
```

Requires Python ≥ 3.10.

## License

MIT

## Documentation

📚 [OpenConstruct Docs](https://github.com/SuperInstance/openconstruct-docs)
