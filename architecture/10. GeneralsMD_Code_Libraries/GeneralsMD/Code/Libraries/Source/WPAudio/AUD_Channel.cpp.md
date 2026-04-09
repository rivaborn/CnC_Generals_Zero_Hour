# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Channel.cpp

## Purpose
Manages audio channels, including creation, destruction, playback control, and attribute management.

## Responsibilities
- Audio channel lifecycle management (create/destroy)
- Playback control (start/stop/pause/resume)
- Channel state tracking and attribute recalculation
- Sample handling and format management

## Key Types
- **AudioChannel (struct)**: Represents an audio playback channel with control, attributes, and sample data.
- **AudioControl (struct)**: Manages channel state (playing/paused/looping).
- **AudioAttribs (struct)**: Handles audio attributes (volume, pan, etc.).
- **AudioFormat (struct)**: Describes audio format parameters.

## Key Functions
### audioChannelCreate
- Purpose: Creates and initializes a new audio channel.
- Calls: `AudioControlInit`, `AudioAttribsInit`, `audioChannelMakeStandard`, `dev->driver->openChannel`

### AudioChannelStart
- Purpose: Starts playback on an audio channel.
- Calls: `AudioAttribsUpdate`, `audioChannelRecalcAttribs`, `chan->driver->lock`, `chan->driver->start`, `chan->driver->unlock`

### audioChannelRecalcAttribs
- Purpose: Recalculates channel attributes by applying various attribute sets.
- Calls: `AudioAttribsInit`, `AudioAttribsApply`, `AudioAttribsUsed`

### AudioChannelSetSample
- Purpose: Assigns an audio sample to a channel for playback.
- Calls: `AudioSampleFirstFrame`

### AudioChannelIsAudible
- Purpose: Checks if a channel is currently playing audio.
- Calls: None

## Globals
- **AudioChannel (struct)**: Core audio channel structure.
- **audioInitialized (bool)**: Tracks if audio system is initialized.
- **audioStdChannelAttribs (AudioAttribs)**: Default channel attributes.

## Dependencies
- `<wpaudio/altypes.h>`, `<wpaudio/memory.h>`, `<wpaudio/list.h>`, `<wpaudio/channel.h>`, `<wpaudio/device.h>`
- `AudioSample`, `AudioFrame`, `AudioDriver` (external types)
- `AudioMemFree`, `audioRemoveChannel`, `AudioAttribsUpdate` (external functions)
