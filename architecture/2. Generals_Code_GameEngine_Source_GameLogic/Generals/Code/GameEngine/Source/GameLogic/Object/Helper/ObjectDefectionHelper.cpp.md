# Generals/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectDefectionHelper.cpp

## Purpose
This file contains the implementation of the `ObjectDefectionHelper` class, which manages the logic for objects that are undetected defectors in the game.

## Responsibilities
- Manages the state and behavior of undetected defector objects.
- Handles the detection timer and visual effects for these objects.
- Updates the object's status based on various conditions like being attacked or dead.

## Key Types
- `ObjectDefectionHelper` (Class): Manages the logic for undetected defectors.

## Key Functions
### update
- Purpose: Updates the state of the undetected defector, including checking if the timer has expired and handling visual effects.
- Calls:
  - `getObject()`
  - `getDrawable()`
  - `getIsUndetectedDefector()`
  - `friend_setUndetectedDefector()`
  - `flashAsSelected()`
  - `addAudioEvent()`

### startDefectionTimer
- Purpose: Starts the deflection timer for an object and sets up visual effects.
- Calls:
  - `getObject()`
  - `setWakeFrame()`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/MiscAudio.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/ObjectDefectionHelper.h"
