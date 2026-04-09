# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/ScriptConditions.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the scripting condition evaluation system, bridging the game's scripting engine with the underlying game state. It translates abstract script conditions into concrete game logic checks, serving as the decision-making backbone for scripted events and AI behaviors.

## Cross-References
### Incoming
- **ScriptEngine.cpp**: Calls `evaluateCondition` to process script conditions
- **AIUpdate.cpp**: Uses conditions for AI decision-making (e.g., `evaluateAllDestroyed`)
- **GameLogic.cpp**: Likely calls conditions for victory/defeat checks
- **Skirmish AI**: Uses skirmish-specific conditions (e.g., `evaluateSkirmishPlayerHasDiscoveredPlayer`)

### Outgoing
- **Player/PlayerList**: For player state checks (`playerFromParam`)
- **Object/ThingTemplate**: For unit/building existence checks
- **Audio System**: For media completion checks (`evaluateMusicHasCompleted`)
- **PartitionManager**: For spatial queries (e.g., area-based conditions)
- **SpecialPowerModule**: For power-related conditions

## Design Patterns
- **Strategy Pattern**: Each condition type is handled by a dedicated `evaluate*` function, allowing dynamic condition evaluation without conditional logic bloat.
- **Facade Pattern**: Abstracts complex game state queries (e.g., player discovery, object counts) behind simple condition checks.
- **Singleton-like Global**: `TheScriptConditions` acts as a global interface, though not a strict singleton (created/destroyed explicitly).

**Not inferable**: Factory pattern for `ObjectTypesTemp` (likely a temporary wrapper for testing/debugging).
