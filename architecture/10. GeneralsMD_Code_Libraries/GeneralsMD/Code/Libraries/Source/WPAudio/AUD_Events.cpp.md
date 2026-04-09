# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Events.cpp

## Purpose
Manages audio event classes, instances, and playback in the SAGE engine's audio system.

## Responsibilities
- Audio event lifecycle management (creation, playback, destruction)
- Event scheduling and prioritization
- Volume and pan adjustments
- Time-of-day and compression handling
- Global audio state control (pause/resume/flush)

## Key Types
- AudioEventClassTag (Class): Defines audio event class properties (priority, volume, limits)
- AudioEventTag (Class): Represents an individual audio event instance
- EClassBucketTag (Class): Manages event buckets for prioritization
- AudioEventState (Enum): Tracks event state (NEW, START_PLAYING, WAITING, PLAYING, DONE)

## Key Functions
### AudioEventClassCreate
- Purpose: Creates a new audio event class
- Calls: audioInitEventClass, ListAddToTail

### AudioEventCreate
- Purpose: Creates an audio event instance from a class
- Calls: AudioMemoryPoolAlloc, eventAddLocalSort

### AudioEventService
- Purpose: Services all audio events (playback, state transitions)
- Calls: AudioEventHandleInit, audioEventPrep, audioEventStart, audioEventDestroy

### AudioEventKill
- Purpose: Kills an audio event
- Calls: AudioEventHandleDeinit, audioEventDestroy

### AudioEventSetVolume
- Purpose: Adjusts event volume
- Calls: AudioAttribsSetVolume

## Globals
- audioEventClasses (ListHead): Global list of audio event classes
- audioCache (AudioCache*): Reference to audio cache system
- audioDevice (AudioDevice*): Reference to audio device
- eventsOn (int): Global audio events enabled flag
- AudioEventsCount (int): Current active event count
- audioEventPool (AudioMemoryPool*): Pool for event memory allocation

## Dependencies
- wpaudio/altypes.h, cache.h, events.h, level.h, profiler.h, channel.h, device.h, attributes.h, handle.h
- AudioCache, AudioDevice, AudioChannel, AudioAttribs, AudioMemoryPool, ListHead/Node
- DBG_TYPE macro for debugging
