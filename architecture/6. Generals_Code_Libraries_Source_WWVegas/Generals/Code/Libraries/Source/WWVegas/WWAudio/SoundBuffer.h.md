# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundBuffer.h

## Purpose
Defines sound buffer classes for managing raw audio data in the game's audio system.

## Responsibilities
- Manages in-memory sound buffers for non-streaming audio
- Handles streaming audio buffers for large files
- Provides access to audio data and metadata
- Supports loading from files and memory
- Reference-counted resource management

## Key Types
- **SoundBufferClass (Class)**: Base class for managing raw sound data (non-streaming)
- **StreamSoundBufferClass (Class)**: Derived class for managing streaming audio buffers
- **FileClass (Class)**: Forward-declared file handling class

## Key Functions
### SoundBufferClass::Load_From_File
- Purpose: Loads sound data from a file
- Calls: Not inferable

### SoundBufferClass::Load_From_Memory
- Purpose: Loads sound data from a memory buffer
- Calls: Not inferable

### StreamSoundBufferClass::Load_From_File
- Purpose: Loads streaming sound data from a file
- Calls: Not inferable

### SoundBufferClass::Determine_Stats
- Purpose: Analyzes sound data to extract metadata
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Mss.H` (Windows multimedia API)
- `RefCount.H` (reference counting base class)
- `FileClass` (file handling)
