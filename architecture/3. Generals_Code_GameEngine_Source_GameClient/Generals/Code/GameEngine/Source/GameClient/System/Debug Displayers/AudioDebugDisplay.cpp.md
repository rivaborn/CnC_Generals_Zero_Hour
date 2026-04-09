# Generals/Code/GameEngine/Source/GameClient/System/Debug Displayers/AudioDebugDisplay.cpp

## Purpose
Handles audio-related debug display functionality in the game client.

## Responsibilities
- Provides debug output for audio system
- Integrates with the debug display interface
- Exposes audio debug information via `TheAudio` interface

## Key Types
- None

## Key Functions
### printFunc
- Purpose: Outputs debug text via the debug display interface
- Calls: `debugDisplay->printf`

### AudioDebugDisplay
- Purpose: Entry point for audio debug display functionality
- Calls: `TheAudio->audioDebugDisplay`

## Globals
- debugDisplay (DebugDisplayInterface*): Stores reference to the debug display interface

## Dependencies
- `DebugDisplay.h` - Debug display interface
- `GameAudio.h` - Audio system interface
- `TheAudio` - Global audio system instance
- `PreRTS.h` - Required header for GameEngine files
