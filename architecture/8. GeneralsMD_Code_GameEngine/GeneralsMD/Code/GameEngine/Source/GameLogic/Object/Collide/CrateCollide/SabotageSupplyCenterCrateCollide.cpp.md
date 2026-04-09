# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageSupplyCenterCrateCollide.cpp

## Purpose
Handles collision behavior for sabotage supply center crates (terrorists) that steal money from enemy supply centers.

## Responsibilities
- Validates collision targets (must be enemy supply centers)
- Steals money from target supply center
- Provides visual/audio feedback (EVA messages, floating text)
- Manages serialization (CRC, Xfer, loadPostProcess)

## Key Types
- **SabotageSupplyCenterCrateCollide (Class)**: Handles sabotage crate collision logic
- **SabotageSupplyCenterCrateCollideModuleData (Struct)**: Not inferable (used in base class)

## Key Functions
### `isValidToExecute`
- Purpose: Checks if collision target is valid for sabotage
- Calls: `CrateCollide::isValidToExecute`, `getObject()`, `getRelationship`

### `executeCrateBehavior`
- Purpose: Executes sabotage behavior (money theft, feedback)
- Calls: `getObject()`, `getAIUpdateInterface()`, `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `getControllingPlayer()`, `getMoney()`, `withdraw`, `deposit`, `getScoreKeeper()`, `addMoneyEarned`, `TheEva->setShouldPlay`, `TheInGameUI->addFloatingText`

### `crc`
- Purpose: Serialization CRC handler
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization handler
- Calls: `CrateCollide::xfer`, `xferVersion`

### `loadPostProcess`
- Purpose: Post-load processing
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **TheRadar (Radar)**: Global radar system
- **TheEva (Eva)**: Global EVA system
- **TheGameText (GameText)**: Global text system
- **TheInGameUI (InGameUI)**: Global UI system

## Dependencies
- Common: `GameAudio`, `MiscAudio`, `Player`, `PlayerList`, `Radar`, `ThingTemplate`, `Xfer`
- GameClient: `Drawable`, `Eva`, `GameText`, `InGameUI`
- GameLogic: `ExperienceTracker`, `Object`, `PartitionManager`, `ScriptEngine`
- GameLogic/Module: `AIUpdate`, `ContainModule`, `DozerAIUpdate`, `HijackerUpdate`, `OCLUpdate`, `SabotageSupplyCenterCrateCollide`
