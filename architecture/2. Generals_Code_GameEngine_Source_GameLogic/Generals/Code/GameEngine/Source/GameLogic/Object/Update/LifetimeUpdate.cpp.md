# Generals/Code/GameEngine/Source/GameLogic/Object/Update/LifetimeUpdate.cpp

## Purpose
This file implements the `LifetimeUpdate` class, which manages the lifetime of game objects. It counts down a specified time and destroys the object when the countdown reaches zero.

## Responsibilities
- Initialize and manage the lifetime of an object.
- Calculate a random delay for the object's destruction.
- Update the object's state based on the elapsed time.
- Handle serialization and deserialization of the object's state.

## Key Types
- `LifetimeUpdate` (Class): Manages the lifetime of a game object.
- None

## Key Functions
### LifetimeUpdate::LifetimeUpdate
- Purpose: Constructor for `LifetimeUpdate`, initializes the object's lifetime.
- Calls: 
  - `calcSleepDelay`
  - `setWakeFrame`

### LifetimeUpdate::setLifetimeRange
- Purpose: Sets a new range for the object's lifetime delay.
- Calls: 
  - `calcSleepDelay`
  - `setWakeFrame`

### LifetimeUpdate::calcSleepDelay
- Purpose: Calculates a random delay within a specified range.
- Calls: 
  - `GameLogicRandomValue`

### LifetimeUpdate::update
- Purpose: Updates the object's state, destroying it if its lifetime has expired.
- Calls: 
  - `getObject()->kill`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/LifetimeUpdate.h"
  - "GameLogic/Object.h"
