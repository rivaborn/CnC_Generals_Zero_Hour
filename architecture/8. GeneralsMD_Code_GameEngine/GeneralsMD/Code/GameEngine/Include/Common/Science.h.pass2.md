# GeneralsMD/Code/GameEngine/Include/Common/Science.h - Enhanced Analysis

## Architectural Role
This file defines the core data structures and interface for the game's technology/science system, acting as a central registry for researchable upgrades. It bridges the gap between INI-based data definitions and runtime player progression logic.

## Cross-References
### Incoming
- **INI parsing system**: Calls `friend_parseScienceDefinition` during initialization
- **Player progression logic**: Uses `playerHasPrereqsForScience` and `getPurchasableSciences`
- **UI systems**: Accesses `getNameAndDescription` for display purposes
- **WorldBuilder**: Uses `friend_getScienceNames` for editor functionality

### Outgoing
- **Overridable system**: Inherits from `Overridable` for modding support
- **Player system**: Queries player state in prerequisite checks
- **INI system**: Uses `friend_lookupScience` for name resolution

## Design Patterns
- **Registry Pattern**: `ScienceStore` maintains a collection of `ScienceInfo` objects
- **Friend Pattern**: Uses `friend` methods to restrict INI parsing access
- **Dependency Injection**: Player state passed to methods rather than stored internally

*Not inferable*: Exact relationship with modding system's override mechanism.
