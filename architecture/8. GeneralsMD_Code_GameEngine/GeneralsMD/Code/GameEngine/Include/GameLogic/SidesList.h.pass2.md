# GeneralsMD/Code/GameEngine/Include/GameLogic/SidesList.h - Enhanced Analysis

## Architectural Role
This header defines core data structures for player factions (sides), teams, and build lists, serving as the bridge between game setup (WorldBuilder) and runtime (Player/AI subsystems). It encapsulates serialization logic for map data while exposing interfaces for both editor and game logic.

## Cross-References
### Incoming
- **WorldBuilder tools** (BuildListTool, WBDocUndoable) - Use BuildListInfo for editor manipulation
- **Player subsystem** - Consumes SidesInfo for runtime player initialization
- **AI systems** (AISideBuildList, AISkirmishPlayer) - Query build lists for strategic decisions
- **Scripting system** - Accesses ScriptList via SidesInfo

### Outgoing
- **Common utilities** (Dict, Snapshot, MemoryPoolObject) - Inherits/uses for data management
- **Rendering** (RenderObjClass, Shadow) - For editor visualization
- **INI parsing** - BuildListInfo::parseStructure reads template data

## Design Patterns
- **Composite** - SidesList manages collections of SidesInfo/TeamsInfo with hierarchical relationships
- **Singleton** - TheSidesList provides global access to side/team data
- **Flyweight** - BuildListInfo uses MemoryPoolObject for efficient instantiation of build items

*Not inferable: Exact observer relationships with AI/Player systems*
