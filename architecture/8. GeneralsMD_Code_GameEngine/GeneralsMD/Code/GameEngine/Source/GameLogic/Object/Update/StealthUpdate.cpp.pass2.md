# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StealthUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the stealth and disguise system for game objects, bridging game logic, rendering, and AI subsystems. It handles visibility rules, detection mechanics, and network synchronization for stealthed units.

## Cross-References
### Incoming
- **AIUpdate**: Calls `setWakeupIfInRange` to wake units detecting stealthed objects
- **PhysicsUpdate**: Likely triggers stealth state checks via movement thresholds
- **ContainModule**: May interact with stealth when objects are transported
- **GameClient**: Uses `markAsDetected` for UI/radar updates

### Outgoing
- **Radar**: Updates object visibility via `removeObject`/`addObject`
- **ControlBar**: Triggers UI refreshes with `markUIDirty`
- **Audio**: Plays detection/reveal sounds via `TheAudio->addAudioEvent`
- **FXList**: Spawns visual effects during disguise transitions

## Design Patterns
- **State Pattern**: Stealth levels and disguise states are managed as discrete states with transition logic
- **Observer Pattern**: Listens for game state changes (e.g., movement) to update stealth visibility
- **Strategy Pattern**: Different stealth behaviors (innate vs. granted) are encapsulated in separate logic paths

*Not inferable: Exact use of Command or Visitor patterns not evident from truncated content.*
