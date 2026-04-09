# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/SoundBuffer.cpp

## Purpose
Manages audio buffer loading and memory handling for sound playback in the SAGE engine.

## Responsibilities
- Loads audio data from files or memory into buffers
- Manages buffer memory allocation/deallocation
- Extracts audio metadata (rate, channels, bits, duration)
- Supports both static and streaming sound buffers

## Key Types
- **SoundBufferClass (Class)**: Core audio buffer class handling loading and metadata
- **StreamSoundBufferClass (Class)**: Subclass for streaming audio buffers
- **FileMappingClass (Class)**: Tracks file mappings with reference counting
- **MappingList (DynamicVectorClass<FileMappingClass>)**: Global list of file mappings

## Key Functions
### SoundBufferClass::Load_From_File
- Purpose: Loads audio data from a file into the buffer
- Calls: `Free_Buffer`, `Set_Filename`, `Determine_Stats`, `_TheFileFactory->Get_File`, `_TheFileFactory->Return_File`

### SoundBufferClass::Load_From_Memory
- Purpose: Loads audio data from a memory buffer
- Calls: `Free_Buffer`, `Set_Filename`, `Determine_Stats`

### SoundBufferClass::Determine_Stats
- Purpose: Extracts audio metadata from WAV data
- Calls: `AIL_WAV_info`

### StreamSoundBufferClass::Load_From_File
- Purpose: Placeholder for streaming buffer file loading
- Calls: None (empty implementation)

## Globals
- **MappingList (DynamicVectorClass<FileMappingClass>)**: Tracks active file mappings

## Dependencies
- `soundbuffer.h`, `rawfile.h`, `wwdebug.h`, `utils.h`, `ffactory.h`, `win.h`
- `AIL_WAV_info` (AIL sound library)
- `W3DNEWARRAY` (memory allocation)
- `MMSLockClass` (thread synchronization)
