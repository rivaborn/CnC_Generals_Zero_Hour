# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundSceneObj.h

## Purpose
Defines the abstract base class for sound objects in the audio system, handling positioning, culling, and scene integration.

## Responsibilities
- Provides interface for sound object management in 3D space
- Handles sound event callbacks and user data attachment
- Manages object attachment to render objects and scene integration
- Implements sound culling and identification mechanisms

## Key Types
- **SoundSceneObjClass (Class)**: Abstract base class for sound objects in the scene
- **SoundCullObjClass (Class)**: Wrapper for culling operations (forward declared)
- **SoundSceneClass (Class)**: Scene manager (forward declared)
- **RenderObjClass (Class)**: Renderable object (forward declared)
- **Vector3 (Class)**: 3D vector representation
- **Matrix3D (Class)**: 3D transformation matrix
- **LogicalListenerClass (Class)**: Listener interface
- **LogicalSoundClass (Class)**: Sound interface
- **Sound3DClass (Class)**: 3D sound implementation
- **SoundPseudo3DClass (Class)**: Pseudo-3D sound implementation
- **FilteredSoundClass (Class)**: Filtered sound implementation
- **Listener3DClass (Class)**: 3D listener implementation
- **AudibleSoundClass (Class)**: Audible sound interface

## Key Functions
### On_Event
- Purpose: Handles audio events and dispatches callbacks
- Calls: `On_Sound_Started`, `On_Sound_Ended`, `On_Logical_Heard`

### Register_Callback
- Purpose: Registers event callbacks for sound objects
- Calls: None

### Set_ID
- Purpose: Sets the unique identifier for the sound object
- Calls: None

### Attach_To_Object
- Purpose: Attaches sound to a render object with bone reference
- Calls: None

### Add_To_Scene
- Purpose: Adds sound object to the scene (pure virtual)
- Calls: None

## Globals
- **SOUND_OBJ_DEFAULT_ID (uint32)**: Default ID value (0)
- **SOUND_OBJ_START_ID (uint32)**: Starting ID value (1000000000)
- **m_GlobalSoundList (DynamicVectorClass)**: Static list of all sound objects
- **m_NextAvailableID (uint32)**: Next available sound object ID
- **m_IDListMutex (CriticalSectionClass)**: Mutex for ID list access

## Dependencies
- `Refcount.H`, `WWAudio.H`, `BitType.H`, `persist.h`, `multilist.h`, `mutex.h`
- `AudioCallbackClass::EVENTS
