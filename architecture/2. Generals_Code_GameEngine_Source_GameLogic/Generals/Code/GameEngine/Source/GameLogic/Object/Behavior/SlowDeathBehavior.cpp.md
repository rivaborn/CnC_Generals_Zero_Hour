# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/SlowDeathBehavior.cpp

## Purpose
This file implements the `SlowDeathBehavior` class, which handles the slow death sequence for game objects in Command & Conquer Generals. It manages various effects and delays associated with an object's destruction.

## Responsibilities
- Parse configuration data for slow death behavior.
- Manage the timing and execution of different phases of the slow death process.
- Apply random forces to simulate flinging or bouncing during death.
- Handle AI updates and deselect objects upon death.

## Key Types
- `SlowDeathBehaviorModuleData (struct)`: Stores configuration data for slow death behavior.
- `SlowDeathBehavior (class)`: Implements the slow death logic for game objects.

## Key Functions
### parseFX
- Purpose: Parses FX lists from INI files and associates them with specific phases of the slow death process.
- Calls: `INI::scanIndexList`, `TheFXListStore->findFXList`

### parseOCL
- Purpose: Parses Object Creation Lists (OCLs) from INI files and associates them with specific phases of the slow death process.
- Calls: `INI::scanIndexList`, `TheObjectCreationListStore->findObjectCreationList`

### parseWeapon
- Purpose: Parses weapon templates from INI files and associates them with specific phases of the slow death process.
- Calls: `INI::scanIndexList`, `TheWeaponStore->findWeaponTemplate`

### calcRandomForce
- Purpose: Calculates a random force vector for flinging objects during the slow death sequence.
- Calls: `GameLogicRandomValueReal`

### beginSlowDeath
- Purpose: Initiates the slow death process, setting up timing and initial conditions.
- Calls: `getObject`, `getSlowDeathBehaviorModuleData`, `setShadowsEnabled`, `setTerrainDecalFadeTarget`, `TheGameLogic->destroyObject`, `calcRandomForce`, `applyForce`, `setExtraBounciness`, `setExtraFriction`, `setAllowBouncing`, `setAngles`, `setModelConditionState`

### doPhaseStuff
- Purpose: Executes effects associated with a specific phase of the slow death process.
- Calls: `GameLogicRandomValue`, `FXList::doFXObj`, `ObjectCreationList::create`, `TheWeaponStore->createAndFireTempWeapon`

### update
- Purpose: Updates the slow death sequence, handling sinking, flinging, and destruction phases.
- Calls: `getSlowDeathBehaviorModuleData`, `getObject`, `TheGameLODManager->getSlowDeathScale`, `setDisabled`, `setPosition`, `getLastCollidee`, `findObjectByID`, `clearAndSetModelConditionFlags`, `clearModelConditionFlags`, `setModelConditionFlags`

### onDie
- Purpose: Handles the death event, determining whether to initiate the slow death sequence.
- Calls: `getAIUpdateInterface`, `isAiInDeadState`, `markAsDead`, `deselectObject`, `getBehaviorModules`, `getSlowDeathBehaviorInterface`, `beginSlowDeath`

## Globals
- `BEGIN_MIDPOINT_RATIO (Real)`: Ratio for calculating the midpoint frame of the slow death sequence.
- `END_MIDPOINT_RATIO (Real)`: Ratio for calculating the endpoint frame of the slow death sequence.

## Dependencies
- Key includes: "PreRTS.h", "Common/GameLOD.h", "Common/INI.h", "Common/RandomValue.h", "Common/Thing.h", "Common/ThingTemplate.h", "Common/Xfer.h", "GameClient/Drawable.h", "GameClient/FXList.h", "GameLogic/GameLogic.h", "GameLogic/Module/BodyModule.h", "GameLogic/Module/PhysicsUpdate.h", "GameLogic/Module/SlowDeathBehavior.h", "GameLogic/Module/A
