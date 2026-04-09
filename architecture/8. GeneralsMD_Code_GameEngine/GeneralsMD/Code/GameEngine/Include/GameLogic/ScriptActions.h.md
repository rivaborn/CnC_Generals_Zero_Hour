# GeneralsMD/Code/GameEngine/Include/GameLogic/ScriptActions.h

## Purpose
Header defining the scripting engine's action execution interface and implementation for Command & Conquer Generals Zero Hour.

## Responsibilities
- Declares `ScriptActionsInterface` (pure virtual) and `ScriptActions` (concrete implementation)
- Provides script action execution methods for game logic control
- Manages camera, audio, UI, and game state modifications via scripting
- Handles team/unit commands, special abilities, and visual effects

## Key Types
- **ScriptAction (Class)**: Base class for script actions (forward declaration)
- **GameWindow (Class)**: UI window reference (forward declaration)
- **Team (Class)**: Game team representation (forward declaration)
- **View (Class)**: Camera/view reference (forward declaration)
- **AudioAffect (Enum)**: Audio volume control targets
- **ScriptActionsInterface (Class)**: Pure virtual interface for script action execution
- **ScriptActions (Class)**: Main implementation of script action execution

## Key Functions
### executeAction
- Purpose: Executes a script action.
- Calls: Not visible in header.

### doVictory / doDefeat
- Purpose: Triggers game victory/defeat conditions.
- Calls: Not visible in header.

### doCameraMoveTo / doCameraFollowNamed
- Purpose: Controls camera movement and targeting.
- Calls: Not visible in header.

### doTeamAttackArea / doNamedAttack
- Purpose: Issues combat commands to teams/units.
- Calls: Not visible in header.

### doDisplayText / doMoviePlayFullScreen
- Purpose: Manages UI and cinematic displays.
- Calls: Not visible in header.

## Globals
- **TheScriptActions (ScriptActionsInterface*)**: Singleton instance of the script actions system.

## Dependencies
- Key includes: `SubsystemInterface`, `AsciiString`, `Coord3D`, `RGBColor`, `Color`
- External symbols: `Object`, `Bool`, `Real`, `Int`, `UnsignedInt`
