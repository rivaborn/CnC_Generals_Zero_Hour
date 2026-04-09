# GeneralsMD/Code/GameEngine/Source/GameClient/System/Debug Displayers/AudioDebugDisplay.cpp

## Purpose
Handles audio-related debug display functionality in the game client.

## Responsibilities
- Provides debug output for audio system
- Interfaces with the global audio system
- Uses the debug display interface for printing

## Key Types
- None

## Key Functions
### printFunc
- Purpose: Prints debug text via the debug display interface
- Calls: debugDisplay->printf

### AudioDebugDisplay
- Purpose: Entry point for audio debug display, delegates to TheAudio
- Calls: TheAudio->audioDebugDisplay

## Globals
- debugDisplay (DebugDisplayInterface*): Stores the debug display interface pointer

## Dependencies
- DebugDisplay.h
- GameAudio.h
- PreRTS.h
- TheAudio (external audio system symbol)
