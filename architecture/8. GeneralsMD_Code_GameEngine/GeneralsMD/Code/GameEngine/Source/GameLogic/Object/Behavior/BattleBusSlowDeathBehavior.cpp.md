# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/BattleBusSlowDeathBehavior.cpp

## Purpose
Implements specialized death behavior for the Battle Bus, including a "fake" slow death before actual destruction.

## Responsibilities
- Handles two-phase death: initial throw/impact and final destruction
- Manages passenger damage during death sequence
- Checks for empty hull and triggers delayed destruction
- Controls physics and AI during death animations

## Key Types
- (anonymous enum) (Enum): Contains timing constants for ground checks and empty hull checks
- BattleBusSlowDeathBehaviorModuleData (Class): Configuration data for death behavior
- BattleBusSlowDeathBehavior (Class): Main behavior implementation

## Key Functions
### beginSlowDeath
- Purpose: Initiates the death sequence with special effects and physics
- Calls: FXList::doFXObj, ObjectCreationList::create, aiIdle, clearAcceleration, scrubVelocity2D, applyShock, applyRandomRotation, processDamageToContained

### update
- Purpose: Manages death state transitions and empty hull checks
- Calls: isAboveTerrain, setModelConditionState, aiIdle, clearAcceleration, scrubVelocity2D, setDisabled, kill

### xfer
- Purpose: Serializes behavior state for network sync
- Calls: SlowDeathBehavior::xfer, xferBool, xferUnsignedInt

## Globals
None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Module/BattleBusSlowDeathBehavior.h, Common/ModelState.h, GameClient/FXList.h, GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/ObjectCreationList.h, GameLogic/Module/AIUpdate.h, GameLogic/Module/ContainModule.h, GameLogic/Module/PhysicsUpdate.h
