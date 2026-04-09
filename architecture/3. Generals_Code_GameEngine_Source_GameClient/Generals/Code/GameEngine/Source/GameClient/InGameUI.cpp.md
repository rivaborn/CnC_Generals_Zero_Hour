# Generals/Code/GameEngine/Source/GameClient/InGameUI.cpp

## Purpose
Implements the in-game user interface singleton for Command & Conquer Generals, handling UI elements, selection logic, and game state management.

## Responsibilities
- Manages unit selection and idle worker systems
- Controls replay UI visibility
- Handles superweapon timers and display
- Manages world animations and tooltips
- Provides game state synchronization via Xfer

## Key Types
- **TypeSelectionData (Class)**: Holds message and template data for type selection
- **SelectionData (Class)**: Contains template and drawable list for similar unit selection
- **SuperweaponInfo (Class)**: Manages superweapon timer display information
- **InGameUI (Class)**: Main UI singleton handling game interface

## Key Functions
### similarUnitSelection
- Purpose: Selects similar units based on template matching
- Calls: `TheInGameUI->selectDrawable`, `TheInGameUI->getMaxSelectCount`, `TheInGameUI->getSelectCount`, `TheInGameUI->setDisplayedMaxWarning`, `TheInGameUI->message`

### showReplayControls
- Purpose: Shows replay controls window if in replay mode
- Calls: `TheGameLogic->isInReplayGame`, `m_replayWindow->winHide`

### hideReplayControls
- Purpose: Hides replay controls window
- Calls: `m_replayWindow->winHide`

### toggleReplayControls
- Purpose: Toggles replay controls visibility
- Calls: `TheGameLogic->isInReplayGame`, `m_replayWindow->winIsHidden`, `m_replayWindow->winHide`

### IdleWorkerSystem
- Purpose: Handles idle worker button input events
- Calls: `TheInGameUI->selectNextIdleWorker`

## Globals
- **placementOpacity (Real)**: Opacity value for placement indicators
- **illegalBuildColor (RGBColor)**: Color for illegal build indicators
- **TheInGameUI (InGameUI**)**: Singleton instance of InGameUI
- **m_replayWindow (GameWindow**)**: Pointer to replay controls window
- **FRAMES_BEFORE_EXPIRE_TO_FADE (UnsignedInt)**: Frames before animation fade

## Dependencies
- Common: ActionManager, GameAudio, GameEngine, GameType, MessageStream, PerfTimer, Player, PlayerList, Radar, Team, ThingFactory, ThingTemplate, BuildAssistant, Recorder, SpecialPower
- GameClient: Anim2D, ControlBar, DisplayStringManager, Diplomacy, GameText, GameWindowManager, Drawable, GadgetPushButton, GameClient, GameWindowGlobal, GameWindowID, GUICallbacks, InGameUI, VideoPlayer, Mouse, GadgetStaticText, View, TerrainVisual, WindowLayout, LookAtXlat, SelectionXlat, Shadow, GlobalLanguage
- GameLogic: AIGuard, Weapon, Object, GameLogic, PartitionManager, ScriptEngine, ContainModule, SpecialPowerModule, StealthUpdate, SupplyWarehouseDockUpdate, MobMemberSlavedUpdate
