# Generals/Code/GameEngine/Source/Common/System/Radar.cpp

## Purpose
This file implements radar logic for the Command & Conquer Generals game, handling radar object management, events, and UI updates.

## Responsibilities
- Manages radar objects and their display.
- Handles radar events such as "under attack" and "infiltration".
- Updates radar data per frame.
- Manages radar window and terrain refresh.

## Key Types
- **RadarColorLookup (Class)**: Manages color lookup for radar rendering.
- **RadarObject (Class)**: Represents objects visible on the radar.
- **Radar (Class)**: Main radar logic, managing radar state and events.

## Key Functions
### xferRadarObjectList
- Purpose: Transfers radar object list data during save/load operations.
- Calls:
  - `xfer->xferVersion`
  - `xfer->xferUnsignedShort`
  - `xfer->xferSnapshot`

### Radar::tryUnderAttackEvent
- Purpose: Creates a "we're under attack" radar event with UI feedback.
- Calls:
  - `tryEvent`
  - `TheControlBar->triggerRadarAttackGlow`
  - `TheInGameUI->message`
  - `TheAudio->addAudioEvent`

### Radar::tryInfiltrationEvent
- Purpose: Creates an "infiltration" radar event with UI feedback.
- Calls:
  - `createEvent`
  - `TheInGameUI->message`
  - `TheAudio->addAudioEvent`

## Globals
- **TheRadar (Radar \*)**: Global singleton instance of the Radar class.
- **radarColorLookupTable (RadarColorLookup)**: Lookup table for radar colors.

## Dependencies
- Key includes:
  - "Common/GameAudio.h"
  - "Common/GameState.h"
  - "Common/Radar.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Object.h"
  - "GameLogic/TerrainLogic.h"
