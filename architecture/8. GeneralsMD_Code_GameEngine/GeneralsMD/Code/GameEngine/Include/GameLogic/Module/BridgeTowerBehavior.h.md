# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BridgeTowerBehavior.h

## Purpose
Defines behavior module for bridge towers that can be targeted and damaged.

## Responsibilities
- Manages bridge tower damage and destruction logic
- Handles bridge tower healing
- Tracks bridge tower type and associated bridge
- Provides interface for bridge tower interactions

## Key Types
- **BridgeTowerBehaviorInterface (Class)**: Interface for bridge tower behavior methods
- **BridgeTowerBehavior (Class)**: Behavior module implementing bridge tower functionality
- **BridgeTowerBehaviorMagicEnum (Enum)**: Not inferable (empty enum)
- **BridgeTowerBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### BridgeTowerBehavior::onDamage
- Purpose: Handles damage events for bridge towers
- Calls: Not inferable

### BridgeTowerBehavior::onDie
- Purpose: Handles destruction events for bridge towers
- Calls: Not inferable

### BridgeTowerBehavior::onBodyDamageStateChange
- Purpose: Handles state changes in bridge tower damage
- Calls: Not inferable

## Globals
- None

## Dependencies
- `BehaviorModule.h`
- `DamageModule.h`
- `Diemodule.h`
- `ObjectID`, `BridgeTowerType`, `DamageInfo`, `BodyDamageType`, `Object` (external types)
