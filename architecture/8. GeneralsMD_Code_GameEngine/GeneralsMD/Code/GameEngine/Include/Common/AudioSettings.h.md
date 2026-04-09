# GeneralsMD/Code/GameEngine/Include/Common/AudioSettings.h

## Purpose
Defines the `AudioSettings` struct and related constants for configuring audio parameters in the game.

## Responsibilities
- Stores audio configuration paths (folders, extensions)
- Holds audio hardware and playback settings (sample counts, output rate, bits, channels)
- Manages volume and range settings for 2D/3D audio
- Defines microphone positioning and zoom-related audio adjustments

## Key Types
- `MAX_HW_PROVIDERS` (Enum): Maximum number of hardware audio providers (4).
- `AudioSettings` (Struct): Container for all audio-related configuration parameters.

## Key Functions
None.

## Globals
None.

## Dependencies
- `Common/AsciiString.h` (for string handling)
- Basic types: `Bool`, `Int`, `UnsignedInt`, `Real`
