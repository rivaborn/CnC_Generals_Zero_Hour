# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBar.cpp

## Purpose
Manages the in-game control bar UI, including command buttons, science purchases, and special power shortcuts.

## Responsibilities
- Handles command button tooltips and availability
- Manages science purchase UI and player rank progression
- Controls special power shortcut buttons and animations
- Updates radar attack glow effects
- Populates and updates various control bar contexts

## Key Types
- `ControlBar` (Class): Main control bar manager
- `CommandButton` (Class): Represents individual command buttons with associated data
- `RADAR_ATTACK_GLOW_FRAMES` (Enum): Defines radar attack glow animation frames
- `RADAR_ATTACK_GLOW_NUM_TIMES` (Enum): Defines number of glow animation cycles

## Key Functions
### `commandButtonTooltip`
- Purpose: Shows build tooltip layout for command buttons
- Calls: `TheControlBar->showBuildTooltipLayout`

### `ControlBarPopupDescriptionUpdateFunc`
- Purpose: Updates popup descriptions (implementation not shown in snippet)
- Calls: Not inferable

### `populatePurchaseScience`
- Purpose: Populates science purchase windows based on player rank and availability
- Calls: `TheControlBar->findCommandSet`, `setControlCommand`, `updateContextPurchaseScience`

### `triggerRadarAttackGlow`
- Purpose: Initiates radar attack glow animation
- Calls: None

### `updateRadarAttackGlow`
- Purpose: Updates radar attack glow animation state
- Calls: None

### `populateSpecialPowerShortcut`
- Purpose: Populates special power shortcut buttons
- Calls: `TheControlBar->findCommandSet`, `setControlCommand`

### `updateSpecialPowerShortcut`
- Purpose: Updates special power shortcut button states
- Calls: `getCommandAvailability`

## Globals
- `TheControlBar` (ControlBar*): Global instance of the control bar
- `m_rankVeteranIcon` (const Image*): Veteran rank icon
- `m_rankEliteIcon` (const Image*): Elite rank icon
- `m_rankHeroicIcon` (const Image*): Heroic rank icon

## Dependencies
- Common game types (Player, CommandSet, etc.)
- Game logic modules (ProductionUpdate, etc.)
- GUI components (GadgetButton, WindowManager)
- Game text and localization
- HotKey system
- Science store and player templates
- Script engine for game state checks
