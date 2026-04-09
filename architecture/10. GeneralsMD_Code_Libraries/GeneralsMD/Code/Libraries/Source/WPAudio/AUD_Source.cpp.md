# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Source.cpp

## Purpose
Handles audio sample creation, management, and format operations for the game's audio system.

## Responsibilities
- Manages audio sample creation and destruction
- Handles audio format initialization and updates
- Supports MP3 file reading and seeking
- Manages audio frame operations
- Provides utility functions for audio format calculations

## Key Types
- AudioSample (struct): Represents an audio sample with data and format information
- AudioFormat (struct): Describes audio format parameters (compression, channels, rate, etc.)
- AudioFrame (struct): Represents a frame of audio data within a sample

## Key Functions
### AudioCreateSample
- Purpose: Creates a new audio sample with allocated memory
- Calls: AudioSampleInit, AudioMemAlloc

### AudioFormatReadMP3File
- Purpose: Reads MP3 file header to determine format parameters
- Calls: file->read, file->position, file->size, file->seek, AudioFormatUpdate

### AudioFormatSeekToPos
- Purpose: Seeks to a specific position in an audio file based on format
- Calls: AudioFormatInit, AudioFormatReadMP3File, AudioFormatSame, file->seek

### AudioFormatUpdate
- Purpose: Updates format's bytes-per-second calculation based on compression type
- Calls: None

## Globals
- sample_rate (const int[2][2][4]): Lookup table for MP3 sample rates
- bit_rate (const int[2][15]): Lookup table for MP3 bit rates
- MSADPCM_StdCoef (const short[7][2]): Standard coefficients for MS-ADPCM compression

## Dependencies
- wpaudio/altypes.h, wpaudio/memory.h, wpaudio/time.h, wpaudio/source.h
- wsys/file.h
- Uses DBG_* macros for debugging
- Uses List* functions for linked list management
