# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ToppleUpdate.cpp

## Purpose
This file contains the implementation for the `ToppleUpdate` class, which handles the toppling behavior of game objects in Command & Conquer Generals.

## Responsibilities
- Manage the toppling state and physics of an object.
- Apply forces to initiate toppling.
- Handle collisions that trigger toppling.
- Update the object's orientation during toppling.
- Create stumps when an object topples.

## Key Types
- `ToppleUpdateModuleData` (struct): Stores configuration data for the toppling behavior.
- `ToppleState` (enum): Represents different states of the toppling process.

## Key Functions
### applyTopplingForce
- Purpose: Initiates the toppling process by applying a force vector to an object.
- Calls:
  - `normalizeAngle`
  - `stdAngleDiff`
  - `TheScriptEngine->adjustToppleDirection`
  - `stopSway`
  - `setModelConditionState`
  - `doFXObj`
  - `findTemplate`
  - `newObject`
  - `setPosition`
  - `setOrientation`

### deathByToppling
- Purpose: Handles the destruction of an object that has toppled.
- Calls:
  - `attemptDamage`

### update
- Purpose: Updates the toppling state and physics of the object.
- Calls:
  - `In_Place_Pre_Rotate_Z`
  - `In_Place_Pre_Rotate_X`
  - `In_Place_Pre_Rotate_Y`
  - `setTransformMatrix`
  - `setShadowsEnabled`

### onCollide
- Purpose: Handles collisions that trigger toppling.
- Calls:
  - `getCrusherLevel`
  - `topple`

## Globals
- `ANGULAR_LIMIT` (Real): The angular limit for the toppling process.

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `ThingTemplate.h`
  - `ThingFactory.h`
  - `PlayerList.h`
  - `Player.h`
  - `RandomValue.h`
  - `Xfer.h`
  - `FXList.h`
  - `AI.h`
  - `AIPathfind.h`
  - `ToppleUpdate.h`
  - `GameLogic.h`
  - `Object.h`
  - `Drawable.h`
  - `SwayClientUpdate.h`
  - `PhysicsUpdate.h`
  - `ScriptEngine.h`
  - `Damage.h`
