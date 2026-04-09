# Generals/Code/GameEngine/Source/GameLogic/Object/Update/PhysicsUpdate.cpp

## Purpose
Handles physics calculations and updates for game objects, including forces, friction, gravity, and collision detection.

## Responsibilities
- Calculate object acceleration and velocity.
- Apply gravitational and frictional forces.
- Handle collisions and damage from crushing.
- Manage object sleep/wake states for performance optimization.

## Key Types
- None

## Key Functions
### angleBetweenVectors
- Purpose: Calculates the angle between two vectors.
- Calls: Vector3::Dot_Product, ACos, clamp

### heightToSpeed
- Purpose: Converts height to speed using gravitational acceleration.
- Calls: sqrt, fabs

### parseHeightToSpeed
- Purpose: Parses height from INI and converts it to speed.
- Calls: heightToSpeed

### parseFrictionPerSec
- Purpose: Parses friction per second from INI and converts it to per frame.
- Calls: None

### PhysicsBehaviorModuleData::buildFieldParse
- Purpose: Builds field parsing for physics behavior module data.
- Calls: UpdateModuleData::buildFieldParse

### getPui
- Purpose: Retrieves the projectile update interface for an object.
- Calls: None

### PhysicsBehavior::PhysicsBehavior
- Purpose: Constructor for PhysicsBehavior, initializes physics properties.
- Calls: None

### PhysicsBehavior::onObjectCreated
- Purpose: Called when the object is created, sets up projectile update interface.
- Calls: getPui

### PhysicsBehavior::~PhysicsBehavior
- Purpose: Destructor for PhysicsBehavior, cleans up resources.
- Calls: deleteInstance

### PhysicsBehavior::setIgnoreCollisionsWith
- Purpose: Sets an object to ignore collisions with another object.
- Calls: None

### PhysicsBehavior::isIgnoringCollisionsWith
- Purpose: Checks if the object is ignoring collisions with a specific ID.
- Calls: None

### PhysicsBehavior::getAerodynamicFriction, getForwardFriction, getLateralFriction, getZFriction
- Purpose: Retrieves friction values with bounds checking.
- Calls: clamp

### PhysicsBehavior::applyForce
- Purpose: Applies a force to the object's center of mass.
- Calls: applyYPRDamping, setWakeFrame

### PhysicsBehavior::isMotive
- Purpose: Checks if the motive force is still active.
- Calls: None

### PhysicsBehavior::applyMotiveForce
- Purpose: Applies a motive force with a limited duration.
- Calls: applyForce

### PhysicsBehavior::resetDynamicPhysics
- Purpose: Resets dynamic physics properties of the object.
- Calls: setWakeFrame, calcSleepTime

### PhysicsBehavior::applyGravitationalForces
- Purpose: Applies gravitational forces to the object.
- Calls: None

### PhysicsBehavior::applyFrictionalForces
- Purpose: Applies frictional forces based on object's state.
- Calls: applyYPRDamping

## Globals
- DEFAULT_MASS (Real): Default mass value for objects.
- DEFAULT_FORWARD_FRICTION, DEFAULT_LATERAL_FRICTION, DEFAULT_Z_FRICTION, DEFAULT_AERO_FRICTION (Real): Default friction values.
- MIN_AERO_FRICTION, MIN_NON_AERO_FRICTION, MAX_FRICTION (Real): Minimum and maximum friction bounds.
- MOTIVE_FRAMES (Int): Number of frames a motive force is active.
- INVALID_VEL_MAG (Real): Invalid velocity magnitude value.

## Dependencies
- Key includes: "Common/PerfTimer.h", "Common/ThingTemplate.h", "Common/Xfer.h", "GameLogic/GameLogic.h", "GameLogic/Module/AIUpdate.h", "GameLogic/Module/BodyModule.h", "GameLogic/Module/ContainModule.h", "GameLogic/Module/CrushDie.h", "GameLogic/Module/PhysicsUpdate.h",
