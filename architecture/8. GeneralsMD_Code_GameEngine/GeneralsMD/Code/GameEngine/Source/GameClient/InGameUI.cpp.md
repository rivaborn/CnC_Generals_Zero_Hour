# GeneralsMD/Code/GameEngine/Source/GameClient/InGameUI.cpp

## Purpose
Implements the in-game user interface singleton for Command & Conquer Generals Zero Hour, handling UI elements, unit selection, and game controls.

## Responsibilities
- Manages unit selection and idle worker systems
- Controls replay UI visibility
- Handles superweapon display and timers
- Manages world animations and tooltips
- Maintains control bar and UI state

## Key Types
- **KindOfSelectionData (struct)**: Stores selection criteria for filtering units
- **MatchingUnitSelectionData (struct)**: Stores criteria for selecting similar units
- **SuperweaponInfo (class)**: Manages superweapon display information
- **InGameUI (class)**: Main UI singleton class (not shown in snippet)

## Key Functions
### kindOfUnitSelection
- Purpose: Filters and selects units based on kind criteria
- Calls: `object->isKindOfMulti()`, `TheInGameUI->selectDrawable()`, `TheInGameUI->message()`

### similarUnitSelection
- Purpose: Selects units matching a template or car bomb status
- Calls: `object->getTemplate()->isEquivalentTo()`, `TheInGameUI->selectDrawable()`, `TheInGameUI->message()`

### showReplayControls / hideReplayControls / toggleReplayControls
- Purpose: Manages replay UI visibility
- Calls: `TheGameLogic->isInReplayGame()`, `m_replayWindow->winHide()`

### selectNextIdleWorker
- Purpose: Cycles through idle workers for selection
- Calls: `ThePlayerList->getLocalPlayer()`, `TheInGameUI->getFirstSelectedDrawable()`, `TheMessageStream->appendMessage()`

### updateAndDrawWorldAnimations
- Purpose: Updates and renders world animations
- Calls: `TheGameLogic->getFrame()`, `ThePartitionManager->getShroudStatusForPlayer()`, `TheTacticalView->worldToScreen()`

## Globals
- **placementOpacity (Real)**: Opacity value for placement indicators
- **illegalBuildColor (RGBColor)**: Color for illegal build indicators
- **TheInGameUI (InGameUI*)**: Singleton instance of InGameUI
- **m_replayWindow (GameWindow*)**: Replay controls window
- **FRAMES_BEFORE_EXPIRE_TO_FADE (UnsignedInt)**: Frames before animation fade

## Dependencies
- Common: ActionManager, GameAudio, GameEngine, Player, Radar, ThingFactory
- GameClient: Anim2D, ControlBar, DisplayStringManager, Eva, GameText
- GameLogic: AIGuard, Weapon, Object, GameLogic, PartitionManager
- UI: GameWindowManager, GadgetPushButton, WindowLayout
- External: Xfer, UnicodeString, AsciiString, NameKeyType
