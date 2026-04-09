# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectDefectionHelper.cpp

## Purpose
Handles the logic for objects that have defected (e.g., turned into undetected enemies) in the game.

## Responsibilities
- Manages the defection timer for objects.
- Controls visual/audio effects for defected objects.
- Updates object status based on defection state.
- Handles network serialization (Xfer) for defection data.

## Key Types
- `ObjectDefectionHelper` (Class): Manages defection behavior for game objects.
- `UpdateSleepTime` (Enum): Defines update sleep intervals.

## Key Functions
### `update()`
- Purpose: Updates defection state and triggers effects if timer expires.
- Calls: `getObject()`, `getDrawable()`, `friend_setUndetectedDefector()`, `flashAsSelected()`, `addAudioEvent()`.

### `startDefectionTimer(UnsignedInt numFrames, Bool withDefectorFX)`
- Purpose: Starts the defection timer for an object.
- Calls: `getObject()`, `setWakeFrame()`.

### `crc(Xfer *xfer)`
- Purpose: Computes CRC for network synchronization.
- Calls: `ObjectHelper::crc()`.

### `xfer(Xfer *xfer)`
- Purpose: Serializes/deserializes defection helper data.
- Calls: `ObjectHelper::xfer()`.

### `loadPostProcess()`
- Purpose: Post-processing after loading.
- Calls: `ObjectHelper::loadPostProcess()`.

## Globals
- `m_defectionDetectionStart` (UnsignedInt): Start frame of defection timer.
- `m_defectionDetectionEnd` (UnsignedInt): End frame of defection timer.
- `m_defectionDetectionFlashPhase` (Real): Tracks flashing phase for visual effects.
- `m_doDefectorFX`
