# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptConditions.h - Enhanced Analysis

## Architectural Role
This header defines the core scripting condition evaluation system, bridging the game's scripting engine with its logic subsystems. It enables dynamic game state checks for AI, missions, and skirmish rules, acting as a critical abstraction layer between scripted behaviors and underlying game mechanics.

## Cross-References
### Incoming
- **Scripting Engine**: Calls `evaluateCondition` and specialized methods for mission logic.
- **AI System**: Uses condition checks for decision-making (e.g., `evaluateTeamEnteredAreaEntirely`).
- **Skirmish Mode**: Relies on skirmish-specific conditions (e.g., `evaluateSkirmishCommandButtonIsReady`).

### Outgoing
- **Player System**: Calls `playerFromParam` to resolve player references.
- **Object/Unit Systems**: Uses `objectTypesFromParam` for type filtering.
- **Trigger/Area Systems**: Interacts with area-based conditions (e.g., `evaluateNamedInsideArea`).

## Design Patterns
- **Singleton**: `TheScriptConditions` ensures global access to condition evaluation.
- **Strategy Pattern**: Each `evaluate*` method acts as a strategy for specific condition types.
- **Visitor-like**: `evaluateCondition` dispatches to type-specific handlers (though not a pure visitor due to C++ constraints).
