# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpecialPowerModule.cpp

## Purpose
Manages special power abilities for game objects, handling timing, activation, and UI integration.

## Responsibilities
- Tracks cooldown timers for special powers
- Handles activation logic and sound effects
- Manages paused states and percentage readiness
- Integrates with UI for superweapon timers
- Supports scripted special powers

## Key Types
- **SpecialPowerModuleData (struct)**: Holds configuration for special power modules
- **SpecialPowerModule (class)**: Core class managing special power behavior
- **None**: No other major types defined

## Key Functions
### `startPowerRecharge`
- Purpose: Initiates cooldown timer after power use
- Calls: None directly visible

### `doSpecialPower`
- Purpose: Triggers special power execution
- Calls: `initiateIntentToDoSpecialPower`, `triggerSpecialPower`

### `pauseCountdown`
- Purpose: Pauses/unpauses special power cooldown
- Calls: None directly visible

### `getPercentReady`
- Purpose: Calculates readiness percentage (0.0-1.0)
- Calls: `isReady`, `getSpecialPowerTemplate`

## Globals
- **None**: No global/static variables

## Dependencies
- Key includes: `SpecialPower.h`, `Player.h`, `GameLogic.h`, `ScriptEngine.h`
- External symbols: `TheGameLogic`, `TheInGameUI`, `TheAudio`, `TheScriptEngine`, `TheGlobalData`
