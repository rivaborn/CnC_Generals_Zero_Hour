# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/CrateCollide.cpp

## Purpose
Handles collision logic for supply crates in the game, including pickup validation and effects.

## Responsibilities
- Manages crate collision behavior with units/buildings
- Validates pickup conditions (player type, science requirements, etc.)
- Triggers visual/audio effects on crate pickup
- Handles sabotage feedback for crates

## Key Types
- **CrateCollideModuleData (Class)**: Stores crate behavior configuration (pickup rules, effects)
- **CrateCollide (Class)**: Implements crate collision logic

## Key Functions
### `onCollide`
- Purpose: Handles crate collision events with other objects
- Calls: `isValidToExecute`, `executeCrateBehavior`, `FXList::doFXObj`, `TheInGameUI->addWorldAnimation`

### `isValidToExecute`
- Purpose: Validates if a crate can be picked up by a given object
- Calls: `getAIUpdateInterface`, `isKindOfMulti`, `isEffectivelyDead`, `isAboveTerrain`, `getControllingPlayer`, `hasScience`, `isKindOf`

### `doSabotageFeedbackFX`
- Purpose: Plays audio/visual feedback for sabotaged crates
- Calls: `TheAudio->getMiscAudio()`, `TheAudio->addAudioEvent`, `getDrawable()->flashAsSelected`

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance
- **TheAnim2DCollection (Anim2DCollection**)**: Global animation collection
- **TheInGameUI (InGameUI**)**: Global in-game UI
- **TheAudio (GameAudio**)**: Global audio system

## Dependencies
- `PreRTS.h`, `Common/BitFlagsIO.h`, `Common/Player.h`, `Common/Xfer.h`, `Common/GameAudio.h`, `Common/MiscAudio.h`
- `GameClient/Anim2D.h`, `GameClient/FXList.h`, `GameClient/InGameUI.h`, `GameClient/Drawable.h`
- `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/CrateCollide.h`
