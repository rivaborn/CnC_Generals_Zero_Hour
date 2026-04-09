# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudioEvents.h

## Purpose
Defines audio event callback mechanisms for the WWAudio system, including C-style and C++-style callbacks.

## Responsibilities
- Declares forward classes for audio objects (SoundSceneObjClass, LogicalListenerClass, etc.)
- Defines callback function pointers for sound events (started, ended, heard)
- Provides C++-style callback class (AudioCallbackClass) with virtual methods
- Implements callback list management (AudioCallbackListClass) for tracking callbacks

## Key Types
- **SoundSceneObjClass (Class)**: Base class for sound objects in the scene.
- **LogicalListenerClass (Class)**: Represents audio listeners.
- **LogicalSoundClass (Class)**: Represents logical sound sources.
- **AudibleSoundClass (Class)**: Represents audible sound instances.
- **StringClass (Class)**: String handling class.
- **LPFNSOSCALLBACK (Type)**: Callback for sound started events.
- **LPFNEOSCALLBACK (Type)**: Callback for sound ended events.
- **LPFNHEARDCALLBACK (Type)**: Callback for sound heard events.
- **LPFNTEXTCALLBACK (Type)**: Callback for text audio events.
- **AudioCallbackClass (Class)**: Base class for C++-style audio callbacks.
- **EVENTS (Enum)**: Defines audio event types (started, ended, heard).
- **AUDIO_CALLBACK_STRUCT (Struct)**: Template struct for storing callback pointers and user data.
- **AudioCallbackListClass (Class)**: Manages a list of audio callbacks.

## Key Functions
### AudioCallbackListClass<T>::Add_Callback
- Purpose: Adds a callback to the list with associated user data.
- Calls: `Add` (from parent SimpleDynVecClass)

### AudioCallbackListClass<T>::Get_Callback
- Purpose: Retrieves a callback and its user data by index.
- Calls: None

### AudioCallbackListClass<T>::Remove_Callback
- Purpose: Removes a callback from the list by pointer.
- Calls: `Delete` (from parent SimpleDynVecClass)

## Globals
None

## Dependencies
- `simplevec.h`: For `SimpleDynVecClass` inheritance.
- `bittype.h`: For `uint32` type definition.
