# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AnimationSteeringUpdate.cpp

## Purpose
Handles animation state transitions for vehicle steering based on physics turning input.

## Responsibilities
- Manages animation state transitions for left/right turns
- Coordinates with physics and drawable components
- Handles timing for animation transitions
- Clears animation states when turning completes

## Key Types
- **AnimationSteeringUpdateModuleData (Class)**: Stores transition frame count
- **AnimationSteeringUpdate (Class)**: Manages steering animations
- **PhysicsTurningType (Enum)**: Represents turning states (TURN_NONE, TURN_POSITIVE, TURN_NEGATIVE)

## Key Functions
### AnimationSteeringUpdate::update
- Purpose: Updates steering animations based on current turning state
- Calls: getAnimationSteeringUpdateModuleData, getObject, getPhysics, getDrawable, TheGameLogic->getFrame, draw->setModelConditionState, draw->clearAndSetModelConditionState, draw->clearModelConditionFlags

### AnimationSteeringUpdate::crc
- Purpose: Serialization CRC calculation
- Calls: UpdateModule::crc

### AnimationSteeringUpdate::xfer
- Purpose: Serialization/deserialization
- Calls: UpdateModule::xfer, xfer->xferVersion

### AnimationSteeringUpdate::loadPostProcess
- Purpose: Post-load initialization
- Calls: UpdateModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h, ModelState.h, Xfer.h, Drawable.h, GameLogic.h, Object.h, AnimationSteeringUpdate.h, PhysicsUpdate.h
- TheGameLogic (external), UpdateModule (base class), PhysicsBehavior, Drawable, Xfer, XferVersion
