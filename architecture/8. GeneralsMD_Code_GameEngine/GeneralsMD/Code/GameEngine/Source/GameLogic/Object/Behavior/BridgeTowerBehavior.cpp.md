# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeTowerBehavior.cpp

## Purpose
Manages behavior for bridge towers, handling damage propagation, healing, and bridge association.

## Responsibilities
- Links tower to its parent bridge
- Propagates damage/healing to other towers and bridge
- Handles tower destruction (kills bridge)
- Provides interface for bridge tower queries

## Key Types
- **BridgeTowerBehavior (Class)**: Manages bridge tower behavior
- **BridgeTowerType (Enum)**: Tower type identifier (not shown in code)
- **BridgeTowerBehaviorInterface (Interface)**: Access to tower behavior (not shown)

## Key Functions
### `setBridge(Object *bridge)`
- Purpose: Associates tower with a bridge
- Calls: None

### `onDamage(DamageInfo *damageInfo)`
- Purpose: Propagates damage to other towers and bridge
- Calls: `getObject()`, `getBodyModule()`, `findObjectByID()`, `getBehaviorModules()`, `getBridgeBehaviorInterface()`, `attemptDamage()`

### `onHealing(DamageInfo *damageInfo)`
- Purpose: Propagates healing to other towers and bridge
- Calls: `getObject()`, `getBodyModule()`, `findObjectByID()`, `getBehaviorModules()`, `getBridgeBehaviorInterface()`, `attemptHealing()`

### `onDie(const DamageInfo *damageInfo)`
- Purpose: Destroys the bridge when tower dies
- Calls: `findObjectByID()`, `kill()`

### `getBridgeTowerBehaviorInterfaceFromObject(Object *obj)`
- Purpose: Retrieves bridge tower interface from object
- Calls: `getBehaviorModules()`, `getBridgeTowerBehaviorInterface()`

## Globals
- **m_bridgeID (ObjectID)**: Stores associated bridge ID
- **m_type (BridgeTowerType)**: Tower type identifier

## Dependencies
- `BehaviorModule`, `Object`, `BodyModuleInterface`, `BridgeBehaviorInterface`
- `TheGameLogic`, `DamageInfo`, `Xfer`, `ThingTemplate`
