# Generals/Code/Libraries/Source/WWVegas/WWAudio/AudioEvents.h

## Purpose
Defines audio event callback mechanisms for the game's sound system.

## Responsibilities
- Declares callback types for sound events (started, ended, heard)
- Provides C-style and C++-style callback interfaces
- Manages lists of registered callbacks
- Forward declares core audio classes

## Key Types
- **SoundSceneObjClass (Class)**: Base sound object.
- **LogicalListenerClass (Class)**: Listener entity.
- **LogicalSoundClass (Class)**: Logical sound representation.
- **AudibleSoundClass (Class)**: Audible sound instance.
- **StringClass (Class)**: String wrapper.
- **LPFNSOSCALLBACK (Type)**: Callback for sound started events.
- **LPFNEOSCALLBACK (Type)**: Callback for sound ended events.
- **LPFNHEARDCALLBACK (Type)**: Callback for sound heard events.
- **LPFNTEXTCALLBACK (Type)**: Callback for text audio events.
- **AudioCallbackClass (Class)**: Base class for C++-style callbacks.
- **EVENTS (Enum)**: Event type identifiers.
- **AUDIO_CALLBACK_STRUCT (Struct)**: Template struct holding callback pointer and user data.
- **AudioCallbackListClass (Class)**: Manages a list of callbacks.

## Key Functions
### AudioCallbackListClass<T>::Add_Callback
- Purpose: Adds a callback to the list.
- Calls: `SimpleDynVecClass<>::Add`

### AudioCallbackListClass<T>::Get_Callback
- Purpose: Retrieves a callback by index.
- Calls: None.

### AudioCallbackListClass<T>::Remove_Callback
- Purpose: Removes a callback from the list.
- Calls: `SimpleDynVecClass<>::Delete`

## Globals
None.

## Dependencies
- `simplevec.h`: For `SimpleDynVecClass`.
- `bittype.h`: For `uint32`.
