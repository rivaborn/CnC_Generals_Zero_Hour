# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/EjectPilotDie.cpp - Enhanced Analysis

## Architectural Role
This file implements the pilot ejection behavior when a vehicle is destroyed, bridging the game logic layer with audio and object creation systems. It extends the `DieModule` base class to handle vehicle-specific death events, including conditional ejection based on altitude and synchronized audio playback.

## Cross-References
### Incoming
- **GameLogic/Object/Die/DieModule.cpp**: Inherits from `DieModule`, called via `DieModule::crc`, `DieModule::xfer`, `DieModule::loadPostProcess`.
- **GameLogic/ObjectCreationList.cpp**: Uses `ObjectCreationList::create` for spawning pilot objects.
- **Common/GameAudio.cpp**: Interacts with `TheAudio` for sound/voice playback.

### Outgoing
- **GameLogic/GameLogic.cpp**: Queries `TheGameLogic` for damage dealer objects via `findObjectByID`.
- **Common/ThingTemplate.cpp**: Accesses template sounds via `getPerUnitSound`.

## Design Patterns
- **Template Method**: Extends `DieModule` with `onDie`, overriding base behavior for pilot ejection.
- **Strategy**: Uses `ObjectCreationList` as a configurable strategy for spawning different pilot types (air/ground).
- **Observer**: Reacts to `onDie` events, decoupling ejection logic from object destruction.
