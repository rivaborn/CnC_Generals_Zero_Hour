# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudioSaveLoad.h - Enhanced Analysis

## Architectural Role
This file defines the save/load subsystem interfaces for audio data in the SAGE engine, bridging the audio system with the game's serialization framework. It handles both static (pre-loaded) and dynamic (runtime-generated) audio assets, ensuring they persist across game saves/loads.

## Cross-References
### Incoming
- Likely called by the game's save/load manager (e.g., `SaveLoadSubSystemClass` users)
- Potentially referenced by audio system initialization code

### Outgoing
- Inherits from `SaveLoadSubSystemClass`, calling its virtual methods
- Uses `ChunkSaveClass` and `ChunkLoadClass` for serialization

## Design Patterns
- **Singleton**: Global instances (`_StaticAudioSaveLoadSubsystem`, `_DynamicAudioSaveLoadSubsystem`) ensure single access points.
- **Template Method**: Overrides `SaveLoadSubSystemClass` methods for chunk-based serialization.
- **Interface Segregation**: Separates static/dynamic audio handling into distinct classes.

*Not inferable*: Exact serialization format or audio data structure details.
