# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ToppleUpdate.cpp

## Purpose
Handles the toppling behavior of objects (e.g., trees, streetlights) when hit, including physics, state transitions, and effects.

## Responsibilities
- Manages toppling physics (rotation, velocity, acceleration)
- Handles state transitions (upright â falling â toppled)
- Applies visual effects (FX) during toppling
- Creates stumps for certain objects (e.g., trees)
- Processes collisions to trigger toppling

## Key Types
- **ToppleUpdateModuleData (Class)**: Stores configuration for toppling behavior (FX, stump settings, etc.)
- **ToppleUpdate (Class)**: Core module implementing toppling logic
- **ToppleState (Enum)**: Tracks toppling state (upright, falling, toppled)
- **ToppleOptions (Enum)**: Flags for toppling behavior (e.g., no bounce, no FX)

## Key Functions
### `angleClosestTo`
- Purpose: Finds the angle closest to a desired angle between two options.
- Calls: `normalizeAngle`, `fabs`, `stdAngleDiff`

### `deathByToppling`
- Purpose: Applies special "toppled" damage to an object to trigger death.
- Calls: `DamageInfo` constructor, `obj->attemptDamage`

### `applyTopplingForce`
- Purpose: Initiates toppling with a force vector and options.
- Calls: `setWakeFrame`, `TheScriptEngine->adjustToppleDirection`, `FXList::doFXObj`, `TheThingFactory->newObject`

### `update`
- Purpose: Updates toppling physics each frame (rotation, bouncing, state checks).
- Calls: `getObject()->getTransformMatrix`, `Matrix3D::In_Place_Pre_Rotate_X/Y`, `FXList::doFXObj`, `TheGameLogic->findObjectByID`

### `onCollide`
- Purpose: Handles collisions to trigger toppling if conditions are met.
- Calls: `getObject()->topple`, `other->getPhysics()->getVelocity`

## Globals
- **ANGULAR_LIMIT (Real)**: Maximum rotation angle before bouncing/stopping.

## Dependencies
- **Includes**: `PreRTS.h`, `ThingTemplate.h`, `FXList.h`, `AI.h`, `ToppleUpdate.h`, `GameLogic.h`, `Drawable.h`, `SwayClientUpdate.h`, `PhysicsUpdate.h`, `ScriptEngine.h`, `Damage.h`
- **External**: `TheScriptEngine`, `TheThingFactory`, `TheAI`, `TheGameLogic`, `FXList`, `INI` parsing utilities
