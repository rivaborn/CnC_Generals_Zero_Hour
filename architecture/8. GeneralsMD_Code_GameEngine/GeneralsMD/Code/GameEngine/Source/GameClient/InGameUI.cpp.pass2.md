# GeneralsMD/Code/GameEngine/Source/GameClient/InGameUI.cpp - Enhanced Analysis

## Architectural Role
This file implements the core in-game UI system, acting as the bridge between player input and game state. It manages unit selection, UI state (replay controls, tooltips), and visual feedback (animations, placement indicators), while coordinating with the game logic and rendering systems.

## Cross-References
### Incoming
- **GameClient/ControlBar.cpp**: Calls `InGameUI::recreateControlBar()` during control bar initialization
- **GameClient/GameClient.cpp**: Invokes `InGameUI::toggleReplayControls()` for replay mode toggling
- **GameLogic/Object.cpp**: Uses `kindOfUnitSelection()` for unit filtering in selection logic
- **GameClient/GadgetPushButton.cpp**: Triggers `IdleWorkerSystem()` callback for idle worker button interactions

### Outgoing
- **Common/GameLogic.cpp**: Queries `GameLogic::isInReplayGame()` and `GameLogic::getFrame()`
- **GameClient/GameWindowManager.cpp**: Manages window visibility via `winHide()`/`winEnable()`
- **GameClient/DisplayStringManager.cpp**: Uses `appendMessage()` for UI feedback
- **GameClient/TacticalView.cpp**: Calls `lookAt()` for camera centering on selected units

## Design Patterns
- **Singleton Pattern**: `TheInGameUI` provides global access to UI state and methods
- **Callback Pattern**: `IdleWorkerSystem()` handles window messages for idle worker interactions
- **Strategy Pattern**: `KindOfSelectionData` encapsulates selection criteria for unit filtering

*Not inferable*: Exact observer implementation for UI updates (likely tied to game logic events)
