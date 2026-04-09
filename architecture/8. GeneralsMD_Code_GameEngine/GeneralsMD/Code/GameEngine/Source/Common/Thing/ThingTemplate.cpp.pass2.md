# GeneralsMD/Code/GameEngine/Source/Common/Thing/ThingTemplate.cpp - Enhanced Analysis

## Architectural Role
This file is the central hub for game object template definition and parsing, bridging the INI configuration system with runtime object instantiation. It implements the core `ThingTemplate` class, which serves as the blueprint for all game entities (units, buildings, etc.) and manages their properties, prerequisites, and module attachments.

## Cross-References
### Incoming
- **Game Logic**: `Object.cpp` (uses templates for object creation)
- **UI System**: `ProductionMenu.cpp` (queries build costs/times)
- **AI System**: `AIUpdate.cpp` (checks build restrictions)
- **Networking**: `GameClient.cpp` (syncs template data)

### Outgoing
- **INI System**: Direct parsing via `INI.h` functions
- **Module System**: `ModuleFactory.h` for module attachment
- **Game Audio**: `GameAudio.h` for sound event registration
- **FX System**: `FXList.h` for effect definitions

## Design Patterns
- **Factory Pattern**: `ThingTemplate` acts as a factory for object creation via `ThingFactory`
- **Composite Pattern**: Modules are composed into templates (e.g., `ModuleInfo` managing attached behaviors)
- **Strategy Pattern**: Different parsing strategies for various INI fields (e.g., `parsePrerequisiteUnit` vs `parsePrerequisiteScience`)

*Not inferable*: Exact implementation of template overriding/reskinning (e.g., `m_reskinnedFrom` usage).
