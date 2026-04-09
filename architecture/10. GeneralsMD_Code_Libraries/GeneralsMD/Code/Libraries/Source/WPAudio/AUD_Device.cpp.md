# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Device.cpp

## Purpose
Manages audio device creation, destruction, and service routines in the WPAudio library.

## Responsibilities
- Creates and destroys audio devices and systems
- Manages audio channels and their attributes
- Handles audio service scheduling and performance tracking
- Provides device enumeration and debugging utilities

## Key Types
- AudioData (Struct): Global audio system state container
- AudioAttribsNode (Class): Node for managing audio attribute lists
- AudioServiceInfoStruct (Class): Tracks service intervals and performance metrics

## Key Functions
### audioCreateDevice
- Purpose: Creates and initializes an audio device for a given system and unit
- Calls: AudioAttribsInit, AudioServiceInfoInit, master->open

### AudioDeviceService
- Purpose: Services an audio device (handles playback, mixing, etc.)
- Calls: dev->deviceHandler

### AudioServicePerform
- Purpose: Updates service timing statistics for performance tracking
- Calls: None

### AudioDeviceDump
- Purpose: Generates diagnostic output for an audio device's state
- Calls: AudioServiceInfoDump, AudioDeviceFirstChannel, AudioDeviceNextChannel

## Globals
- audioData (AudioData*): Global audio system state pointer
- audioStdChannelAttribs (AudioAttribs*): Default channel attributes
- audioInitialized (int): Tracks if audio system is initialized

## Dependencies
- WPAudio internal headers (altypes.h, memory.h, list.h, etc.)
- Audio system/device/channel management interfaces
- Debugging macros (DBG_DECLARE_TYPE, etc.)
