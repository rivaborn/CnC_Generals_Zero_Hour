# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/OverlordContain.cpp

## Purpose
This file implements the `OverlordContain` class, which manages containment behavior for Overlord units in Command & Conquer Generals. It extends transport functionality to redirect queries to its first passenger when full.

## Responsibilities
- Manage containment and redirection of passengers.
- Handle death and deletion processes with proper order.
- Override various methods to ensure correct behavior when containing other objects.

## Key Types
- `OverlordContainModuleData` (struct): Data structure for Overlord contain module.
- `OverlordContain` (class): Manages containment and redirection logic for Overlord units.

## Key Functions
### OverlordContain::onBodyDamageStateChange
- Purpose: Handles damage state changes, ensuring the first passenger's body state is updated if applicable.
- Calls: `setDamageState`

### OverlordContain::getRedirectedContain
- Purpose: Returns the redirected contain module interface if redirection is active.
- Calls: None

### OverlordContain::onDie
- Purpose: Handles death process, ensuring passengers are killed before the Overlord itself.
- Calls: `deactivateRedirectedContain`, `kill`

### OverlordContain::onDelete
- Purpose: Handles deletion process, ensuring contained objects are removed correctly.
- Calls: `removeAllContained`

## Globals
- None

## Dependencies
- Includes: `PreRTS.h`, `Player.h`, `Xfer.h`, `ControlBar.h`, `Drawable.h`, `BodyModule.h`, `OverlordContain.h`, `Object.h`, `PartitionManager.h`
- External symbols: Various classes and functions from included headers.
