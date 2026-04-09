# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Listener.h

## Purpose
Defines the `Listener3DClass` for managing 3D audio listener position/velocity in the game world.

## Responsibilities
- Represents the 3D audio listener in the sound scene
- Manages listener position and velocity for spatial audio
- Provides attenuation settings for sound distance effects
- Handles scene lifecycle events (added/removed)

## Key Types
- **Listener3DClass (Class)**: Abstract base class for 3D audio listener functionality

## Key Functions
### Listener3DClass()
- Purpose: Default constructor
- Calls: None

### ~Listener3DClass()
- Purpose: Destructor
- Calls: None

### On_Added_To_Scene()
- Purpose: Called when listener is added to scene
- Calls: None

### On_Removed_From_Scene()
- Purpose: Called when listener is removed from scene
- Calls: None

### Set_Velocity()
- Purpose: Sets listener velocity for Doppler effect
- Calls: None

### Set_Max_Vol_Radius()
- Purpose: Sets maximum volume radius for sound attenuation
- Calls: None

### Set_DropOff_Radius()
- Purpose: Sets drop-off radius for sound attenuation
- Calls: None

## Globals
- None

## Dependencies
- `Sound3D.H` (base class)
- `Vector3` (for velocity)
- `SOUND_CLASSID`, `SOUND_STATE` (audio types)
