# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PhysicsUpdate.cpp

## Purpose
Implements rigid-body physics simulation for game objects, including forces, collisions, and movement.

## Responsibilities
- Apply forces, friction, and shocks to objects
- Handle collisions and bouncing
- Manage object velocity and acceleration
- Support vehicle crushing mechanics
- Serialize physics state for networking

## Key Types
- PhysicsBehaviorModuleData (struct): Stores physics configuration (mass, friction, etc.)
- PhysicsBehavior (class): Main physics behavior module handling forces and movement
- PhysicsTurningType (enum): Tracks turning state (none, left, right)

## Key Functions
### angleBetweenVectors
- Purpose: Calculate angle between two 3D vectors
- Calls: Vector3::Dot_Product, ACos, clamp

### heightToSpeed
- Purpose: Convert fall height to speed using gravity
- Calls: TheGlobalData->m_gravity, sqrt, fabs

### applyForce
- Purpose: Apply force to object, converting to acceleration
- Calls: getMass, getObject, getUnitDirectionVector2D

### testStunnedUnitForDestruction
- Purpose: Check if stunned object should be destroyed (upside down, off-map, etc.)
- Calls: getObject, getPosition, getTransformMatrix, isOffMap, hasLocomotorForSurface

### xfer
- Purpose: Serialize physics state for networking
- Calls: UpdateModule::xfer, xferVersion, xferReal, xferCoord3D, xferObjectID, xferInt, xferUnsignedInt

## Globals
- DEFAULT_MASS (Real): Default object mass (1.0)
- DEFAULT_SHOCK_YAW/PITCH/ROLL (Real): Default shock response values
- DEFAULT_FORWARD/LATERAL/Z/AERO_FRICTION (Real): Default friction values
- MIN_AERO/NON_AERO_FRICTION (Real): Minimum friction clamping values
- MAX_FRICTION (Real): Maximum friction clamping value
- STUN_RELIEF_EPSILON (Real): Stun relief threshold
- MOTIVE_FRAMES (Int): Frames for motive force application
- INVALID_VEL_MAG (Real): Invalid velocity magnitude marker

## Dependencies
- Common/PerfTimer.h, Common/ThingTemplate.h, GameLogic/GameLogic.h
- GameLogic/Module/AIUpdate.h, BodyModule.h, ContainModule.h
- GameLogic/Module/CrushDie.h, PhysicsUpdate.h, Object.h
- GameLogic/ScriptEngine.h, TerrainLogic.h, Weapon.h
- GameLogic/LogicRandomValue.h, Common/Xfer.h, Common/CRCDebug.h
