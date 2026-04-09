# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ProneUpdate.cpp

## Purpose
This file implements the `ProneUpdate` module, which manages the prone state of game objects in Command & Conquer Generals. It handles updating prone frames and applying effects when an object goes prone.

## Responsibilities
- Manage the prone state of game objects.
- Update prone frames based on damage received.
- Apply visual and status effects when an object becomes or stops being prone.

## Key Types
- `ProneUpdateModuleData (struct)`: Stores configuration data for the prone update module, such as the ratio of damage to prone frames.
- `ProneUpdate (class)`: Inherits from `UpdateModule` and implements the logic for managing the prone state.

## Key Functions
### ProneUpdate::update
- Purpose: Decrements prone frames and stops prone effects if frames reach zero.
- Calls: `stopProneEffects`

### ProneUpdate::goProne
- Purpose: Increases prone frames based on damage received and starts prone effects if not already prone.
- Calls: `startProneEffects`

### ProneUpdate::startProneEffects
- Purpose: Applies visual and status effects when an object becomes prone.
- Calls: None

### ProneUpdate::stopProneEffects
- Purpose: Removes visual and status effects when an object stops being prone.
- Calls: None

## Globals
- None

## Dependencies
- `PreRTS.h`
- `Common/Xfer.h`
- `GameClient/Drawable.h`
- `GameLogic/Damage.h`
- `GameLogic/Object.h`
- `GameLogic/Module/ProneUpdate.h`
