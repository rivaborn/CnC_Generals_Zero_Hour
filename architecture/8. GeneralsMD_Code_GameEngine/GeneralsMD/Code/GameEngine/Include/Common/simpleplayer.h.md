# GeneralsMD/Code/GameEngine/Include/Common/simpleplayer.h

## Purpose
Defines a simple audio player class using Windows Media SDK for playing audio streams.

## Responsibilities
- Manages audio playback via IWMReaderCallback
- Handles wave headers and audio buffers
- Provides COM interface for reference counting
- Manages playback state and completion events

## Key Types
- **WAVEHDR_LIST (struct)**: Linked list node for wave headers
- **CSimplePlayer (class)**: Main audio player class implementing IWMReaderCallback
- **(anonymous union)**: Stores WAVEFORMATEX or raw buffer

## Key Functions
### CSimplePlayer::Play
- Purpose: Starts playback of an audio stream
- Calls: Not inferable (implementation in .cpp)

### CSimplePlayer::OnSample
- Purpose: Handles incoming audio samples from the media reader
- Calls: AddWaveHeader

### CSimplePlayer::WaveProc
- Purpose: WaveOut callback procedure for audio device messages
- Calls: OnWaveOutMsg

### CSimplePlayer::AddWaveHeader
- Purpose: Adds a wave header to the playback queue
- Calls: Not inferable

## Globals
- **SIMPLE_PLAYER_OPEN_EVENT (string)**: GUID for open event
- **SIMPLE_PLAYER_CLOSE_EVENT (string)**: GUID for close event
- **WMAPLAY_EVENT (string)**: GUID for play event

## Dependencies
- **wmsdk.h**: Windows Media SDK headers
- **IWMReaderCallback**: Media reader callback interface
- **WAVEHDR**: Windows wave header structure
- **CRITICAL_SECTION**: Thread synchronization primitive
