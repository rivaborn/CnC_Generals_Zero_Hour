# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StructureToppleUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the building destruction animation system, bridging game logic and visual effects. It handles the physics simulation of toppling structures, damage application, and phase-based effect triggering, making it a critical component in the destruction feedback pipeline.

## Cross-References
### Incoming
- **GameLogic/Module/StructureToppleUpdate.h**: Defines the class interface and module data structure
- **GameLogic/Object.h**: Uses Object for building reference and geometry access
- **GameClient/Drawable.h**: Accesses bone positions for particle attachment

### Outgoing
- **GameClient/FXList.h**: For visual/audio effect playback
- **GameLogic/Weapon.h**: Creates temporary weapons for crushing damage
- **GameLogic/ScriptEngine.h**: Adjusts topple direction via scripting
- **GameLogic/ObjectCreationList.h**: Spawns debris/particles during topple phases

## Design Patterns
- **State Pattern**: Uses `StructureToppleStateType` enum to manage different topple phases (standing, waiting, toppling, done)
- **Strategy Pattern**: Phase-specific behavior is delegated to `doPhaseStuff` with different `StructureTopplePhaseType` parameters
- **Observer Pattern**: Listens for damage events to trigger topple sequence via `beginStructureTopple`
