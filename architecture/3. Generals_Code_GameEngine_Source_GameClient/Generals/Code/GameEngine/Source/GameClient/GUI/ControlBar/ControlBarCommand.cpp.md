# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommand.cpp

## Purpose
Handles command bar UI logic for unit commands in Command & Conquer Generals.

## Responsibilities
- Manages command button visibility and state
- Handles transport inventory UI updates
- Evaluates command availability based on game state
- Updates UI for special abilities and upgrades

## Key Types
- **PopulateInvButtonData (struct)**: Holds data for transport inventory button population
- **ContainEntry (struct)**: Stores control and object ID for contained items

## Key Functions
### `populateInvDataCallback`
- Purpose: Populates transport inventory buttons with contained objects
- Calls: `getTemplate()`, `getButtonImage()`, `calculateVeterancyOverlayForObject()`

### `doTransportInventoryUI`
- Purpose: Updates UI for transport inventory commands
- Calls: `getContain()`, `getContainMax()`, `getExtraSlotsInUse()`, `iterateContained()`

### `getCommandAvailability`
- Purpose: Determines if a command is available/restricted for an object
- Calls: `getControllingPlayer()`, `canBuild()`, `canAffordBuild()`, `isReady()`, etc.

### `getRappellerCount`
- Purpose: Counts rappellers for combat drop command
- Calls: `getContain()`, `getContainCount()`, `getTemplate()`, `getName()`

## Globals
- **commandWindows (GameWindow*)**: Array of command windows
- **commandWindowsInitialized (Bool)**: Tracks initialization state
- **BuildClockColor (Color)**: Color for build clocks
- **m_containData (ContainEntry[])**: Stores contain data for inventory buttons

## Dependencies
- GameLogic modules (ProductionUpdate, SpecialPowerModule, etc.)
- UI components (GameWindow, GadgetButton)
- Common types (Player, Object, CommandSet)
- Weapon and upgrade systems
