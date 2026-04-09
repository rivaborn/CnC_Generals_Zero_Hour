# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PrisonBehavior.cpp

## Purpose
Implements the PrisonBehavior module, which manages prisoner visuals inside prison structures.

## Responsibilities
- Manages prisoner visual representations in prison yards
- Handles containment logic for prisoners
- Serializes/deserializes prisoner visual data
- Manages visual display based on configuration

## Key Types
- PrisonVisual (Class): Tracks object-drawable pairs for prisoner visuals
- PrisonBehaviorModuleData (Class): Configuration data for prison behavior
- PrisonBehavior (Class): Main behavior class handling prison logic

## Key Functions
### PrisonBehavior::onContaining
- Purpose: Handles object containment in prison
- Calls: OpenContain::onContaining, obj->setDisabled

### PrisonBehavior::addVisual
- Purpose: Creates visual representation for prisoner
- Calls: TheThingFactory->newDrawable, pickVisualLocation

### PrisonBehavior::removeVisual
- Purpose: Removes prisoner visual representation
- Calls: TheGameClient->findDrawableByID, TheGameClient->destroyDrawable

### PrisonBehavior::pickVisualLocation
- Purpose: Selects random valid location within prison yard
- Calls: us->getMultiLogicalBonePosition, PointInsideArea2D

## Globals
- None

## Dependencies
- Common/GameState.h
- Common/Player.h
- Common/RandomValue.h
- Common/ThingFactory.h
- Common/Xfer.h
- GameClient/Drawable.h
- GameClient/InGameUI.h
- GameClient/GameClient.h
- GameClient/Line2D.h
- GameLogic/Object.h
- GameLogic/Module/PrisonBehavior.h
