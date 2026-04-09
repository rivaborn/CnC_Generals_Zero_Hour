# GeneralsMD/Code/GameEngine/Include/Common/AudioEventRTS.h - Enhanced Analysis

## Architectural Role
This file defines the core audio event abstraction in the SAGE engine, bridging the game logic layer with the audio subsystem. It encapsulates all runtime state for audio playback, including positional logic, ownership tracking, and playback sequencing.

## Cross-References
### Incoming
- Audio subsystem (GameAudio.h) - uses AudioEventRTS for playback management
- Game logic (e.g., unit/drawable systems) - creates events for sound effects/voiceovers
- Scripting system - likely triggers logical audio events

### Outgoing
- AudioEventInfo (not shown) - for event configuration data
- GameMemory subsystem - via MemoryPoolObject inheritance
- Localization system - through adjustForLocalization calls

## Design Patterns
- **State Pattern**: PortionToPlay enum and related methods manage playback state transitions
- **Strategy Pattern**: Position retrieval varies by owner type (positional/drawable/object)
- **Flyweight Pattern**: DynamicAudioEventRTS uses memory pooling for frequent allocations

Rules followed. Output under 400 tokens.
