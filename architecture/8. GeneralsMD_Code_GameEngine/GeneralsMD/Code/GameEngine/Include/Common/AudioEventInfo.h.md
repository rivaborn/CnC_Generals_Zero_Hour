# GeneralsMD/Code/GameEngine/Include/Common/AudioEventInfo.h

## Purpose
Defines data structures and enums for audio event management in the game engine.

## Responsibilities
- Declares enums for audio types, priorities, sound types, and controls
- Defines the `AudioEventInfo` struct for storing audio event properties
- Provides memory pool management for `AudioEventInfo` objects
- Declares global arrays for enum string representations

## Key Types
- `AudioType` (Enum): categorizes audio as music, streaming, or sound effect
- `AudioPriority` (Enum): defines priority levels for audio playback
- `SoundType` (Enum): specifies sound context (UI, world, voice, etc.)
- `AudioControl` (Enum): controls sound behavior (looping, randomness, etc.)
- `AudioEventInfo` (Struct): container for all audio event properties and settings

## Key Functions
### `isPermanentSound`
- Purpose: Determines if a sound will loop indefinitely
- Calls: `BitTest` (bitwise check on control flags)

### `getFieldParse`
- Purpose: Returns the parse table for INI definition
- Calls: None

## Globals
- `theAudioPriorityNames` (char*): Array of priority level names
- `theSoundTypeNames` (char*): Array of sound type names
- `theAudioControlNames` (char*): Array of audio control names

## Dependencies
- `Common/AsciiString.h`
- `Common/GameMemory.h`
- `Common/STLTypedefs.h`
- `FieldParse` (forward declaration)
