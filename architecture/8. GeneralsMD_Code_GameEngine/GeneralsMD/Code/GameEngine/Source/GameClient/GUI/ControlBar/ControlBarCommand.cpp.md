# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarCommand.cpp

## Purpose
Handles command button logic for the control bar in the game UI, including transport inventory management and command availability checks.

## Responsibilities
- Manages transport inventory UI display
- Determines command button availability based on game state
- Handles special cases for different command types (build, upgrade, weapon fire, etc.)
- Updates button states (enabled/disabled, clocks for cooldowns)

## Key Types
- **PopulateInvButtonData (Struct)**: Holds data for populating transport inventory buttons
- **ContainEntry (Struct)**: Stores control and object ID for contained items

## Key Functions
### `populateInvDataCallback`
- Purpose: Populates transport inventory buttons with contained object data
- Calls: `getTemplate()`, `getButtonImage()`, `calculateVeterancyOverlayForObject()`, `GadgetButtonSetEnabledImage()`, `GadgetButtonDrawOverlayImage()`

### `doTransportInventoryUI`
- Purpose: Manages UI display for transport inventory slots
- Calls: `getContain()`, `getContainMax()`, `getExtraSlotsInUse()`, `iterateContained()`, `winHide()`, `winEnable()`, `setControlCommand()`, `GadgetButtonDrawOverlayImage()`

### `getCommandAvailability`
- Purpose: Determines if a command button should be available/enabled based on game state
- Calls: `getControllingPlayer()`, `canBuild()`, `canAffordBuild()`, `isReady()`, `getPercentReady()`, `isOverchargeActive()`, etc.

### `getRappellerCount`
- Purpose: Counts rappellers for combat drop command availability
- Calls: `getContain()`, `getContainCount()`, `getTemplate()`, `getName()`

## Globals
- **commandWindows (GameWindow*)**: Array of command windows
- **commandWindowsInitialized (Bool)**: Tracks if command windows are initialized
- **BuildClockColor (Color)**: Color for build clocks
- **m_containData (ContainEntry[])**: Stores contain data for inventory buttons

## Dependencies
- GameLogic modules (BattlePlanUpdate, DozerAIUpdate, etc.)
- UI components (GameWindow, GadgetButton)
- Common game types (Player, ThingTemplate, SpecialPower)
- InGameUI for selection queries
