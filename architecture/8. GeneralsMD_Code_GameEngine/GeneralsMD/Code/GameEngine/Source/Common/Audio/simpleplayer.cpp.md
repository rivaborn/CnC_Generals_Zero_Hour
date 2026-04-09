# GeneralsMD/Code/GameEngine/Source/Common/Audio/simpleplayer.cpp

## Purpose
Implements a simple audio player using Windows Media Player SDK and WaveOut API.

## Responsibilities
- Manages audio playback from URLs or local files
- Handles streaming and buffering of audio data
- Interfaces with Windows Media Player SDK for media reading
- Manages wave output device for audio playback
- Handles completion events and cleanup

## Key Types
- CSimplePlayer (Class): Main audio player class implementing IWMReaderCallback
- WAVEHDR_LIST (Struct): Linked list node for tracking wave headers

## Key Functions
### CSimplePlayer::Play
- Purpose: Initiates playback of an audio file from a URL
- Calls: WMCreateReader, m_pReader->Open, m_pReader->QueryInterface, m_pReader->GetOutputCount, m_pReader->GetOutputProps, waveOutOpen, m_pReader->Start

### CSimplePlayer::OnSample
- Purpose: Handles incoming audio samples from the media reader
- Calls: pSample->GetBufferAndLength, waveOutPrepareHeader, waveOutWrite

### CSimplePlayer::OnStatus
- Purpose: Handles status notifications from the media reader
- Calls: MakeEscapedURL, LaunchURL

### CSimplePlayer::WaveProc
- Purpose: Static callback for wave output device messages
- Calls: OnWaveOutMsg

## Globals
- None

## Dependencies
- Common/SimplePlayer.h
- Common/URLLaunch.h
- Windows Media Player SDK (IWMReader, IWMHeaderInfo, etc.)
- Windows WaveOut API (waveOutOpen, waveOutWrite, etc.)
- COM interfaces (IUnknown, IWMReaderCallback)
