# Generals/Code/GameEngine/Source/GameLogic/Object/Locomotor.cpp

## Purpose
This file contains the implementation of locomotion logic for game objects in Command & Conquer Generals, including calculations for movement, rotation, and acceleration.

## Responsibilities
- Manage object movement based on templates.
- Calculate direction and speed adjustments.
- Handle different types of locomotion (e.g., thrust, legs, wheels).
- Maintain position and orientation of objects.

## Key Types
- **LocomotorTemplate**: Defines the properties of a locomotor template.
- **LocomotorSet**: Manages a set of locomotors for an object.
- **None**: No other significant types defined in this file.

## Key Functions
### calcSlowDownDist
- Purpose: Calculate the distance required to slow down from current speed to desired speed.
- Calls: `fabs`, `sqr`

### isNearlyZero
- Purpose: Check if a value is nearly zero.
- Calls: None

### isNearly
- Purpose: Check if two values are nearly equal.
- Calls: None

### tryToRotateVector3D
- Purpose: Rotate a vector towards another vector by a maximum angle.
- Calls: `Vector3::Dot_Product`, `clamp`, `ACos`, `Vector3::Cross_Product`, `Matrix3D`

### tryToOrientInThisDirection3D (2 overloads)
- Purpose: Orient an object towards a desired direction with a maximum turn rate.
- Calls: `tryToRotateVector3D`, `obj->setTransformMatrix`

### calcDirectionToApplyThrust
- Purpose: Calculate the direction to apply thrust to reach a goal position.
- Calls: `Vector3::Length2`, `sqrt`, `Vector3::Normalize`, `PhysicsBehavior::getVelocity`, `TheGlobalData->m_gravity`

## Globals
- **DONUT_TIME_DELAY_SECONDS (Real)**: Time delay for donut effect.
- **DONUT_DISTANCE (Real)**: Distance for donut effect.
- **TheLocomotorStore (LocomotorStore \*)**: The locomotor store definition.
- **BIGNUM (Real)**: A large number used as a default value.
- **TheLocomotorPriorityNames (const char \*\*)**: Array of locomotor priority names.

## Dependencies
- Key includes:
  - "Common/INI.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Object.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Module/PhysicsUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/AIUpdate.h"

- External symbols used:
  - `TheGlobalData`
  - `TheGameLogic`
  - `LOGICFRAMES_PER_SECOND`
  - `PI`
  - `Cos`, `Sin`
