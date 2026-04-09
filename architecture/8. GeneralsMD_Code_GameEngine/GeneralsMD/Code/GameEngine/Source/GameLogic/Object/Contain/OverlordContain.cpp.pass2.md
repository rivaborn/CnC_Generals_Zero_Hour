# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/OverlordContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the containment logic for the Overlord unit, a specialized transport that dynamically redirects containment queries to its first passenger when full. It bridges the game's containment system with the Overlord's unique behavior, handling payload creation, experience management, and death sequences.

## Cross-References
### Incoming
- **GameClient/Drawable.cpp**: Calls `friend_getRider()` for draw order dependency handling
- **GameLogic/ExperienceTracker.cpp**: Uses `isEnclosingContainerFor()` for experience sink determination
- **GameLogic/Module/BodyModule.cpp**: Invokes `clientVisibleContainedFlashAsSelected()` for selection visualization

### Outgoing
- **GameLogic/Module/TransportContain.cpp**: Extends base containment functionality
- **GameLogic/ThingFactory.cpp**: Uses `TheThingFactory` for object creation
- **GameLogic/GameLogic.cpp**: Accesses `TheGameLogic` for object lookup

## Design Patterns
- **Proxy Pattern**: Implements dynamic redirection to delegate containment operations to the first passenger
- **Template Method**: Extends base class methods while preserving core containment logic
- **Strategy Pattern**: Configurable payload templates allow runtime behavior customization
