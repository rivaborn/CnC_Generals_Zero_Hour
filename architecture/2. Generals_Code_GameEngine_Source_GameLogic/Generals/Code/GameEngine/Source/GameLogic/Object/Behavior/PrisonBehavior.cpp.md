# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/PrisonBehavior.cpp

## Purpose
This file implements the behavior for prison objects in Command & Conquer Generals, managing prisoner visuals and interactions.

## Responsibilities
- Manages prisoner visuals within a prison yard.
- Handles adding and removing prisoners from the prison.
- Ensures prisoners are visually represented and disabled when contained.

## Key Types
- **PrisonVisual (Class)**: Represents visual data for prisoners.
- **PrisonBehaviorModuleData (Struct)**: Configuration data for prison behavior.
- **PrisonBehavior (Class)**: Manages prisoner behavior within a prison.

## Key Functions
### PrisonBehavior::onDelete
- Purpose: Cleans up resources when the prison is deleted.
- Calls: `OpenContain::onDelete`, `TheGameClient->findDrawableByID`, `TheGameClient->destroyDrawable`.

### PrisonBehavior::onContaining
- Purpose: Handles adding a prisoner to the prison.
- Calls: `OpenContain::onContaining`, `Object::setDisabled`, `addVisual`.

### PrisonBehavior::onRemoving
- Purpose: Handles removing a prisoner from the prison.
- Calls: `removeVisual`, `Object::clearDisabled`, `OpenContain::onRemoving`.

### PrisonBehavior::pickVisualLocation
- Purpose: Picks a random location inside the prison yard for prisoner visuals.
- Calls: `Object::getPosition`, `Object::getMultiLogicalBonePosition`, `GameLogicRandomValueReal`, `PointInsideArea2D`.

### PrisonBehavior::addVisual
- Purpose: Adds a visual representation of a prisoner to the prison yard.
- Calls: `TheThingFactory->newDrawable`, `Drawable::setIndicatorColor`, `pickVisualLocation`, `Drawable::setPosition`, `Drawable::setOrientation`, `newInstance(PrisonVisual)`.

### PrisonBehavior::removeVisual
- Purpose: Removes a visual representation of a prisoner from the prison yard.
- Calls: `findDrawableByID`, `destroyDrawable`.

## Globals
- None

## Dependencies
- **Includes**: "PreRTS.h", "Common/GameState.h", "Common/Player.h", "Common/RandomValue.h", "Common/ThingFactory.h", "Common/Xfer.h", "GameClient/Drawable.h", "GameClient/InGameUI.h", "GameClient/GameClient.h", "GameClient/Line2D.h", "GameLogic/Object.h", "GameLogic/Module/PrisonBehavior.h".
