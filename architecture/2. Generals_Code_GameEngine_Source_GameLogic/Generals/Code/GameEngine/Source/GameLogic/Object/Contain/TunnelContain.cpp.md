# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/TunnelContain.cpp

## Purpose
This file implements the `TunnelContain` class, which manages objects contained within a tunnel structure in Command & Conquer Generals. It overrides default container behavior to use the player's `TunnelTracker`.

## Responsibilities
- Manage objects stored in a tunnel.
- Handle adding and removing objects from the tunnel.
- Redirect queries about capacity and contents to the `TunnelTracker`.
- Ensure proper events are triggered when objects enter or exit the tunnel.

## Key Types
- **TunnelContain (Class)**: Manages objects within a tunnel, overriding default container behavior.

## Key Functions
### TunnelContain::addToContainList
- Purpose: Adds an object to the player's `TunnelTracker`.
- Calls: `Player::getTunnelSystem()->addToContainList`

### TunnelContain::removeFromContain
- Purpose: Removes an object from the tunnel and triggers necessary events.
- Calls: `Object::onRemovedFrom`, `TunnelTracker::removeFromContain`

### TunnelContain::removeAllContained
- Purpose: Removes all objects from the tunnel.
- Calls: `TunnelContain::removeFromContain`

### TunnelContain::iterateContained
- Purpose: Iterates over contained objects and calls a callback function.
- Calls: `TunnelTracker::iterateContained`

### TunnelContain::onContaining
- Purpose: Handles events when an object is added to the tunnel.
- Calls: `Object::setDisabled`

### TunnelContain::onRemoving
- Purpose: Handles events when an object is removed from the tunnel.
- Calls: `ThePartitionManager->registerObject`, `Object::setPosition`, `Drawable::setDrawableHidden`

### TunnelContain::onSelling
- Purpose: Removes all contained objects if this is the last tunnel.
- Calls: `TunnelTracker::removeAllContained`, `TunnelTracker::onTunnelDestroyed`

### TunnelContain::isValidContainerFor
- Purpose: Checks if an object can be added to the tunnel.
- Calls: `TunnelTracker::isValidContainerFor`

### TunnelContain::getContainCount
- Purpose: Returns the number of objects in the tunnel.
- Calls: `TunnelTracker::getContainCount`

### TunnelContain::getContainMax
- Purpose: Returns the maximum capacity of the tunnel.
- Calls: `TunnelTracker::getContainMax`

### TunnelContain::getContainedItemsList
- Purpose: Retrieves the list of contained objects.
- Calls: `TunnelTracker::getContainedItemsList`

## Globals
- None

## Dependencies
- **Includes**: 
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/RandomValue.h"
  - "Common/ThingTemplate.h"
  - "Common/TunnelTracker.h"
  - "Common/Xfer.h"
  - "GameClient
