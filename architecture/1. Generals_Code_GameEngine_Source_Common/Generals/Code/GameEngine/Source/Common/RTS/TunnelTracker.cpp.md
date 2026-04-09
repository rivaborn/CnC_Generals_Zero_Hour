# Generals/Code/GameEngine/Source/Common/RTS/TunnelTracker.cpp

## Purpose
This file implements the `TunnelTracker` class, which manages tunnel-related data for a player in Command & Conquer Generals. It tracks tunnels, their contents, and handles various operations like adding/removing objects from tunnels.

## Responsibilities
- Track and manage tunnel IDs.
- Maintain a list of objects contained within tunnels.
- Update nemesis targets based on game logic.
- Handle tunnel creation and destruction events.
- Perform healing operations on objects within tunnels.

## Key Types
- `TunnelTracker` (Class): Manages tunnel-related data for a player.
- `ContainedItemsList` (Type): List of objects contained within tunnels.

## Key Functions
### TunnelTracker::iterateContained
- Purpose: Iterates over the list of contained objects and applies a callback function to each.
- Calls: None

### TunnelTracker::updateNemesis
- Purpose: Updates the current nemesis target based on game logic.
- Calls: `getCurNemesis`, `TheGameLogic->getFrame`

### TunnelTracker::addToContainList
- Purpose: Adds an object to the list of contained objects.
- Calls: None

### TunnelTracker::removeFromContain
- Purpose: Removes an object from the list of contained objects.
- Calls: `std::find`, `m_containList.erase`

### TunnelTracker::onTunnelCreated
- Purpose: Handles the creation of a new tunnel by updating internal lists.
- Calls: None

### TunnelTracker::onTunnelDestroyed
- Purpose: Handles the destruction of a tunnel, including cleaning up contained objects.
- Calls: `iterateContained`, `TheGameLogic->findObjectByID`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameState.h"
  - "Common/GlobalData.h"
  - "Common/TunnelTracker.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
