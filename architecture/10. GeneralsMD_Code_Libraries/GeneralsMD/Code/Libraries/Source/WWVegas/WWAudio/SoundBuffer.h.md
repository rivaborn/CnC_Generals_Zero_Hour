# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundBuffer.h

## Purpose
Defines sound buffer classes for managing raw audio data in the game's audio system.

## Responsibilities
- Manages raw sound data for non-streaming and streaming audio
- Provides loading from files and memory
- Exposes audio buffer properties (duration, rate, channels, etc.)
- Handles buffer memory allocation/deallocation

## Key Types
- **SoundBufferClass (Class)**: Base class for managing non-streaming sound buffers
- **StreamSoundBufferClass (Class)**: Derived class for managing streaming sound buffers
- **FileClass (Class)**: Forward-declared file handling class

## Key Functions
### SoundBufferClass::Load_From_File
- Purpose: Loads sound data from a file
- Calls: Not inferable

### SoundBufferClass::Load_From_Memory
- Purpose: Loads sound data from memory buffer
- Calls: Not inferable

### SoundBufferClass::Determine_Stats
- Purpose: Analyzes sound buffer to determine audio properties
- Calls: Not inferable

### StreamSoundBufferClass::Load_From_File
- Purpose: Loads streaming sound data from a file
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Mss.H` (included)
- `RefCount.H` (included)
- `FileClass` (forward-declared)
