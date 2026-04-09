# Generals/Code/GameEngine/Source/GameLogic/AI/AIDock.cpp

## Purpose
This file implements the AI behavior for docking operations in Command & Conquer Generals, including state transitions and interactions with dock interfaces.

## Responsibilities
- Manage docking states such as approaching, waiting for clearance, advancing position, moving to entry, processing dock, moving to exit, and moving to rally.
- Handle communication with dock update interfaces to coordinate docking actions.
- Ensure proper cleanup and interruption handling during docking processes.

## Key Types
- **DroneInfo (Class)**: Stores information about a drone associated with the AI owner.

## Key Functions
### findDrone
- Purpose: Searches for a drone produced by the AI owner within the player's objects.
- Calls: None

## Globals
- None

## Dependencies
- Includes:
  - "Common/Module.h"
  - "Common/Player.h"
  - "GameLogic/Object.h"
  - "GameLogic/AIDock.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/SupplyTruckAIUpdate.h"
  - "GameLogic/Module/UpdateModule.h"
