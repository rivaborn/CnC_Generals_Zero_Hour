# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundBuffer.cpp

## Purpose
Manages audio buffer loading and memory handling for sound playback in the game.

## Responsibilities
- Loads audio data from files or memory into buffers
- Manages buffer memory allocation and deallocation
- Extracts audio statistics (duration, sample rate, etc.)
- Provides streaming sound buffer functionality

## Key Types
- **SoundBufferClass (Class)**: Main audio buffer class handling loading and stats
- **StreamSoundBufferClass (Class)**: Specialized buffer for streaming audio
- **FileMappingClass (Class)**: Tracks file mappings with reference counting
- **MappingList (DynamicVectorClass<FileMappingClass>)**: Global list of file mappings

## Key Functions
### SoundBufferClass::Load_From_File
- Purpose: Loads audio data from a file into the buffer
- Calls: FileFactory operations, Determine_Stats

### SoundBufferClass::Load_From_Memory
- Purpose: Loads audio data from memory into the buffer
- Calls: Determine_Stats

### SoundBufferClass::Determine_Stats
- Purpose: Extracts audio format information from buffer data
- Calls: AIL_WAV_info

### StreamSoundBufferClass::Load_From_File
- Purpose: Handles streaming audio file loading
- Calls: Determine_Stats

## Globals
- **MappingList (DynamicVectorClass<FileMappingClass>)**: Tracks active file mappings

## Dependencies
- soundbuffer.h, rawfile.h, wwdebug.h, utils.h, ffactory.h, win.h
- AIL sound library functions (AIL_WAV_info)
- FileFactory singleton (_TheFileFactory)
- Memory allocation utilities (W3DNEWARRAY)
