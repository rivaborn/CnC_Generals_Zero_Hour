# Generals/Code/GameEngine/Source/GameLogic/Object/Update/StickyBombUpdate.cpp

## Purpose
This file contains the implementation for the `StickyBombUpdate` class, which handles the behavior of sticky bombs in the game, including their attachment to targets and countdown to detonation.

## Responsibilities
- Initialize sticky bomb targeting and position.
- Update the sticky bomb's position to follow its target.
- Handle the countdown timer and play ping sounds.
- Detonate the sticky bomb when conditions are met.

## Key Types
- `StickyBombUpdate` (Class): Manages the update logic for sticky bombs.
- None

## Key Functions
### StickyBombUpdate::StickyBombUpdate
- Purpose: Constructor for the `StickyBombUpdate` class.
- Calls: 
  - `setWakeFrame`
  - `getObject`

### StickyBombUpdate::onObjectCreated
- Purpose: Initializes the sticky bomb with its target and sets up the countdown timer.
- Calls:
  - `findObjectByID`
  - `getAIUpdateInterface`
  - `getGoalObject`
  - `init`

### StickyBombUpdate::init
- Purpose: Sets the target for the sticky bomb and initializes its position and countdown timer.
- Calls:
  - `setProducer`
  - `getFrame`
  - `findUpdateModule`
  - `getDieFrame`
  - `setPosition`

### StickyBombUpdate::update
- Purpose: Updates the sticky bomb's position to follow its target and plays ping sounds at regular intervals.
- Calls:
  - `isEffectivelyDead`
  - `destroyObject`
  - `getPosition`
  - `setGroundHeight`
  - `addAudioEvent`

### StickyBombUpdate::getTargetObject
- Purpose: Retrieves the current target object of the sticky bomb.
- Calls:
  - `findObjectByID`

### StickyBombUpdate::detonate
- Purpose: Detonates the sticky bomb by killing it.
- Calls:
  - `kill`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `ThingTemplate.h`
  - `Xfer.h`
  - `Drawable.h`
  - `InGameUI.h`
  - `Object.h`
  - `StickyBombUpdate.h`
  - `LifetimeUpdate.h`
  - `AIUpdate.h`
  - `BodyModule.h`
  - `GameLogic.h`
