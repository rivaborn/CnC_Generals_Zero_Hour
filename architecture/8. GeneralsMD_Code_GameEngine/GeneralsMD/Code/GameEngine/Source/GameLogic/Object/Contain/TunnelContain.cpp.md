# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/TunnelContain.cpp

## Purpose
Manages tunnel-based containment for units in Command & Conquer Generals Zero Hour, delegating storage and queries to the player's TunnelTracker.

## Responsibilities
- Overrides OpenContain to use TunnelTracker for storage and capacity checks
- Handles unit entry/exit from tunnels with special positioning logic
- Manages tunnel destruction/capture events and unit healing
- Provides iteration and removal of contained units

## Key Types
- **TunnelContain (Class)**: Manages tunnel containment logic
- **TunnelContainModuleData (Struct)**: Module-specific data (not shown in file)

## Key Functions
### TunnelContain::TunnelContain
- Purpose: Constructor initializing tunnel containment
- Calls: OpenContain constructor

### TunnelContain::addToContainList
- Purpose: Adds object to player's tunnel system
- Calls: TunnelTracker::addToContainList

### TunnelContain::removeFromContain
- Purpose: Removes object from tunnel system with event triggers
- Calls: OpenContain::onRemoving, Object::onRemovedFrom, TunnelTracker::removeFromContain

### TunnelContain::harmAndForceExitAllContained
- Purpose: Damages and removes all contained units
- Calls: removeFromContain, Object::attemptDamage

### TunnelContain::onDie
- Purpose: Handles tunnel destruction, unregistering from tunnel system
- Calls: TunnelTracker::onTunnelDestroyed

### TunnelContain::update
- Purpose: Per-frame update for healing and nemesis tracking
- Calls: OpenContain::update, TunnelTracker::healObjects, TunnelTracker::updateNemesis

## Globals
- **m_needToRunOnBuildComplete (Bool)**: Tracks if onBuildComplete should run
- **m_isCurrentlyRegistered (Bool)**: Tracks tunnel registration status

## Dependencies
- Common/Player.h, Common/TunnelTracker.h
- GameLogic/Module/OpenContain.h, GameLogic/Module/TunnelContain.h
- GameLogic/Object.h, GameLogic/PartitionManager.h
- GameClient/Drawable.h, GameLogic/Module/AIUpdate.h
