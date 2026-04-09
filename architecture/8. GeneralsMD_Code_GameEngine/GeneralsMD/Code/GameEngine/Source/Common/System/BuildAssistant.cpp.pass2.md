# GeneralsMD/Code/GameEngine/Source/Common/System/BuildAssistant.cpp - Enhanced Analysis

## Architectural Role
This file implements the core construction/deconstruction logic for the game, acting as a bridge between the game logic layer and the object management systems. It handles validation, placement, and lifecycle management of buildable objects while coordinating with AI, production, and UI systems.

## Cross-References
### Incoming
- **Game Logic**: `Mission.cpp` (for construction validation during missions)
- **UI Systems**: `ControlBar.cpp` (for build queue management)
- **AI Modules**: `AIUpdate.cpp` (for unit movement during construction)
- **Production System**: `ProductionUpdate.cpp` (for build cost calculations)

### Outgoing
- **Game Logic**: `GameLogic.cpp` (for object creation/destruction)
- **AI System**: `AI.cpp` (for unit behavior during construction)
- **Object Management**: `ThingFactory.cpp` (for object instantiation)
- **UI System**: `InGameUI.cpp` (for build feedback)

## Design Patterns
- **Singleton Pattern**: `TheBuildAssistant` ensures global access to construction services
- **Command Pattern**: Construction/selling actions are encapsulated in method calls
- **Observer Pattern**: Notifications to AI/Production modules during selling process

*Not inferable*: Exact implementation of strategy pattern for different build types.
