# GeneralsMD/Code/GameEngine/Include/Common/ThingTemplate.h - Enhanced Analysis

## Architectural Role
This header defines the core `ThingTemplate` class, serving as the blueprint system for all game entities (units, buildings, etc.). It bridges the data-driven INI parsing system with runtime entity instantiation, acting as the central registry for entity properties, modules, and inheritance chains.

## Cross-References
### Incoming
- **GameLogic**: Uses `ThingTemplate` for entity creation and behavior resolution
- **GameClient**: References templates for UI rendering and selection portraits
- **AI**: Consumes template data for decision-making and threat evaluation
- **Networking**: Serializes template IDs for synchronization

### Outgoing
- **ModuleFactory**: Instantiates behavior/draw/client modules via `ModuleInfo`
- **INI Parsing**: Drives data loading through static parse methods
- **Audio System**: Resolves sounds via `AudioArray` and `PerUnitSoundMap`
- **Geometry/Physics**: Uses `GeometryInfo` for collision and placement

## Design Patterns
- **Composite**: `ThingTemplate` aggregates multiple `ModuleInfo` instances (behavior, draw, client) with inheritance support
- **Flyweight**: Templates are shared across instances, with per-unit overrides via `PerUnitSoundMap`/`PerUnitFXMap`
- **Factory Method**: Static parse methods (`parseArmorTemplateSet`, etc.) delegate INI parsing to specialized handlers

*Not inferable*: Exact inheritance chain resolution (e.g., `reskinnedFrom` handling) or runtime template instantiation flow.
