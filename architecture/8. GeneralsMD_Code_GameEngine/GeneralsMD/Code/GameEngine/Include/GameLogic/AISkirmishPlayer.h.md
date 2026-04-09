# GeneralsMD/Code/GameEngine/Include/GameLogic/AISkirmishPlayer.h

## Purpose
Defines the AISkirmishPlayer class, representing the computer-controlled opponent in skirmish mode.

## Responsibilities
- Manages AI behavior for skirmish matches
- Handles base building and team management
- Computes superweapon targets
- Tracks enemy players and defense positions

## Key Types
- **AISkirmishPlayer (Class)**: Computer-controlled opponent logic
- **AISkirmishPlayerMagicEnum (Enum)**: Not inferable
- **AISkirmishPlayer_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### AISkirmishPlayer()
- Purpose: Constructor for AISkirmishPlayer
- Calls: Not inferable

### computeSuperweaponTarget()
- Purpose: Calculates best position for weapon given radius
- Calls: Not inferable

### update()
- Purpose: Simulates player behavior
- Calls: Not inferable

### doBaseBuilding()
- Purpose: Handles base-building behaviors
- Calls: Not inferable

### selectTeamToBuild()
- Purpose: Determines next team to build
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameMemory.h
- GameLogic/AIPlayer.h
- BuildListInfo (forward declaration)
- SpecialPowerTemplate (forward declaration)
