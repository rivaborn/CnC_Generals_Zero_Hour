# GeneralsMD/Code/GameEngine/Source/Common/System/Radar.cpp

## Purpose
Implements radar logic for the game, including object tracking, event handling, and terrain visualization.

## Responsibilities
- Manages radar object lists and their visibility
- Handles radar events (attacks, infiltrations)
- Updates radar display based on game state
- Serializes radar data for save/load
- Manages terrain sampling for radar visualization

## Key Types
- **Radar (Class)**: Main radar system manager
- **RadarObject (Class)**: Represents objects on radar with position/color data
- **RadarColorLookup (Class)**: Color lookup table for radar display
- **RadarEvent (Struct)**: Stores radar event data (position, type, timing)

## Key Functions
### `xferRadarObjectList`
- Purpose: Serializes/deserializes radar object lists
- Calls: `xfer->xferSnapshot`, `xfer->xferUnsignedShort`

### `tryUnderAttackEvent`
- Purpose: Creates radar event when object is under attack
- Calls: `tryEvent`, `TheControlBar->triggerRadarAttackGlow`, `TheInGameUI->message`

### `tryInfiltrationEvent`
- Purpose: Creates radar event for infiltration warnings
- Calls: `createEvent`, `TheInGameUI->message`, `TheAudio->addAudioEvent`

### `refreshTerrain`
- Purpose: Updates radar terrain visualization
- Calls: None directly (clears refresh queue)

## Globals
- **TheRadar (Radar*)**: Global radar system singleton
- **radarColorLookupTable (RadarColorLookup)**: Color lookup table for radar display

## Dependencies
- GameAudio, GameState, Player, TerrainLogic
- Xfer (serialization), Drawable, Eva
- GameLogic, PartitionManager, ContainModule
- W3D rendering system (implied by Drawable usage)
