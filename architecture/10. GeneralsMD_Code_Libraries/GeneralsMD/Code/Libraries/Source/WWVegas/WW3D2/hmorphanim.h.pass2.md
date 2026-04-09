# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hmorphanim.h - Enhanced Analysis

## Architectural Role
This file defines the morph animation system for the W3D engine, specifically handling facial animation through pose interpolation. It bridges the animation pipeline (Magpie/W3dView) with runtime playback, supporting multi-channel morphing for complex facial expressions.

## Cross-References
### Incoming
- Animation playback systems (likely in rendering or character subsystems)
- W3D file loading/saving infrastructure (ChunkLoadClass/ChunkSaveClass)
- Facial animation controllers (phoneme/expression systems)

### Outgoing
- HAnimClass (base animation class)
- SimpleDynVecClass (dynamic array for morph keys)
- ChunkLoadClass/ChunkSaveClass (W3D I/O)

## Design Patterns
- **Composite**: HMorphAnimClass aggregates multiple TimeCodedMorphKeysClass instances for channel separation
- **Strategy**: Morph interpolation logic (Get_Morph_Info) abstracts frame-to-pose mapping
- **Not inferable**: No clear use of Observer or Factory patterns in header

*Cross-cutting insight*: The dual-channel design (phoneme/expression) suggests tight coupling with speech/audio systems, likely coordinated via external animation controllers.
