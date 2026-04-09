# GeneralsMD/Code/GameEngine/Include/Common/SkirmishBattleHonors.h

## Purpose
Defines the `SkirmishBattleHonors` class for tracking player achievements and statistics in skirmish mode.

## Responsibilities
- Track wins, losses, win streaks, and best win streaks
- Manage campaign completion statuses for USA, China, and GLA
- Store challenge medals and special achievements (SCUD, Particle Cannon, Nuke)
- Provide tooltip and UI insertion utilities for displaying honors

## Key Types
- **SkirmishBattleHonors (Class)**: Tracks skirmish battle statistics and achievements
- **Image (Class)**: Used for UI display (external)
- **GameWindow (Class)**: UI container (external)
- **WinInstanceData (Class)**: Window instance data (external)

## Key Functions
### ResetBattleHonorInsertion
- Purpose: Resets battle honor insertion state
- Calls: Not inferable

### InsertBattleHonor
- Purpose: Inserts a battle honor item into a UI list
- Calls: Not inferable

### BattleHonorTooltip
- Purpose: Generates tooltip for battle honor items
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/UnicodeString.h`
- `Common/UserPreferences.h`
- `Image`, `GameWindow`, `WinInstanceData` (forward declarations)
