# GeneralsMD/Code/GameEngine/Include/Common/AudioEventInfo.h - Enhanced Analysis

## Architectural Role
This header defines the core data structure (`AudioEventInfo`) for the game's audio system, serving as the contract between audio event definitions (parsed from INI files) and the audio playback subsystem. It bridges the gap between static audio configuration and dynamic runtime behavior.

## Cross-References
### Incoming
- Audio playback manager (likely in `Audio.cpp`) - uses `AudioEventInfo` to configure sound playback
- INI parsing system - consumes `getFieldParse()` to load audio definitions
- Dynamic audio system (`DynamicAudioEventInfo.h`) - extends this base class for runtime overrides

### Outgoing
- Memory pool system (`GameMemory.h`) - for object allocation
- Bit manipulation utilities (`BitTest`) - for flag checks
- STL containers (`vector`) - for sound list storage

## Design Patterns
- **Data Transfer Object (DTO)**: `AudioEventInfo` encapsulates all audio configuration data for serialization/deserialization
- **Type Object**: Enums (`AudioType`, `SoundType`) define discrete audio categories for runtime switching
- **Template Method**: `getFieldParse()` provides a standardized way to parse INI data (likely used by a generic parser)

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns in this header alone.
