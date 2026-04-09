# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthUpdate.h

## Purpose
Defines the StealthUpdate module for handling object stealth behavior in the game.

## Responsibilities
- Manages stealth states and transitions for game objects
- Handles disguise mechanics and visual effects
- Processes stealth-related updates and conditions
- Provides stealth status queries and detection logic

## Key Types
- **StealthUpdateModuleData (Class)**: Configuration data for stealth behavior
- **StealthUpdate (Class)**: Main stealth update module implementation
- **StealthLookType (Enum)**: Not inferable (forward reference)
- **EvaMessage (Enum)**: Not inferable (forward reference)
- **FXList (Class)**: Not inferable (forward reference)

## Key Functions
### StealthUpdate::update
- Purpose: Main update loop for stealth behavior
- Calls: calcSleepTime, calcStealthedStatusForPlayer, hintDetectableWhileUnstealthed, changeVisualDisguise

### StealthUpdate::disguiseAsObject
- Purpose: Applies disguise to the object
- Calls: Not inferable

### StealthUpdate::calcStealthedStatusForPlayer
- Purpose: Determines stealth status for a specific player
- Calls: Not inferable

## Globals
- **TheStealthLevelNames (const char**)**: Array of stealth level names (conditional)

## Dependencies
- UpdateModule.h
- Thing, StealthLookType, EvaMessage, FXList (forward references)
- MultiIniFieldParse, ObjectStatusMaskType, Real, UnsignedInt, Bool, Object, ThingTemplate (external types)
