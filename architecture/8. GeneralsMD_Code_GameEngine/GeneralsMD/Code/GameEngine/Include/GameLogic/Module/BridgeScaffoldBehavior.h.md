# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BridgeScaffoldBehavior.h

## Purpose
Defines behavior for bridge scaffold objects, controlling their motion states and positions.

## Responsibilities
- Manages scaffold motion states (rise, build, tear down, sink)
- Handles position updates for scaffold components
- Provides interface for controlling scaffold behavior
- Implements update logic for motion transitions

## Key Types
- ScaffoldTargetMotion (Enum): motion states (still, rise, build, tear down, sink)
- BridgeScaffoldBehaviorInterface (Class): abstract interface for scaffold control
- BridgeScaffoldBehavior (Class): concrete implementation of scaffold behavior

## Key Functions
### BridgeScaffoldBehavior::update
- Purpose: Updates scaffold position based on current motion state
- Calls: doVerticalMotion, doLateralmotion

### BridgeScaffoldBehavior::setPositions
- Purpose: Sets scaffold position targets
- Calls: None

### BridgeScaffoldBehavior::setMotion
- Purpose: Changes scaffold motion state
- Calls: None

### BridgeScaffoldBehavior::reverseMotion
- Purpose: Reverses current motion direction
- Calls: None

### BridgeScaffoldBehavior::doVerticalMotion
- Purpose: Handles vertical rise/sink motion
- Calls: None

### BridgeScaffoldBehavior::doLateralmotion
- Purpose: Handles lateral build/tear-down motion
- Calls: None

## Globals
- None

## Dependencies
- BehaviorModule.h
- UpdateModule.h
- Coord3D (from external)
- Real (from external)
- Thing (from external)
- Object (from external)
- ModuleData (from external)
