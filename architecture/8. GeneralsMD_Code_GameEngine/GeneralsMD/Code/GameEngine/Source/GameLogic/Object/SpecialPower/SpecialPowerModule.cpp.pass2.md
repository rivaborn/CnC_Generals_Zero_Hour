# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpecialPowerModule.cpp - Enhanced Analysis

## Architectural Role
This file implements the core logic for special powers (superweapons) in the game, bridging between object behavior, player state, and UI presentation. It manages cooldown timers, activation conditions, and synchronization across networked players.

## Cross-References
### Incoming
- **GameLogic/Object.cpp**: Calls `doSpecialPower` when objects receive special power commands
- **GameClient/ControlBar.cpp**: Uses `getPercentReady` for UI progress bars
- **ScriptEngine.cpp**: Invokes `pauseCountdown` for script-controlled power pauses
- **Player.cpp**: Calls `startPowerRecharge` during player initialization

### Outgoing
- **GameLogic/Module/SpecialPowerUpdateModule.cpp**: Delegates frame-by-frame power execution
- **GameClient/InGameUI.cpp**: Updates superweapon timers via `addSuperweapon`
- **Common/SpecialPower.cpp**: Uses template methods for power type checks
- **Common/GameAudio.cpp**: Plays initiation sounds through `TheAudio`

## Design Patterns
- **Module Pattern**: SpecialPowerModule inherits from BehaviorModule, following the engine's component-based architecture
- **State Machine**: Implicit state tracking (ready/paused/disabled) via frame counters and flags
- **Observer Pattern**: Notifies UI of power readiness changes without direct coupling

Rules followed. Output under 400 tokens.
