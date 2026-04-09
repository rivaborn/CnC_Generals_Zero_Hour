# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Sound3D.h

## Purpose
Defines the `Sound3DClass` for 3D positional audio in the SAGE engine, handling spatial sound properties like position, velocity, and attenuation.

## Responsibilities
- Manages 3D sound properties (position, velocity, attenuation)
- Integrates with the sound scene for spatial audio processing
- Handles Miles Sound System (MSS) audio handle management
- Supports serialization via `PersistClass`
- Provides auto-calculation of velocity for moving sound sources

## Key Types
- **Sound3DClass (Class)**: Represents a 3D sound with spatial properties and attenuation settings.

## Key Functions
### `Play`
- Purpose: Plays the sound, optionally allocating a handle.
- Calls: Not inferable (implementation in .cpp).

### `Add_To_Scene`
- Purpose: Adds the sound to the sound scene for spatial processing.
- Calls: Not inferable.

### `Set_Position`
- Purpose: Updates the sound's position in 3D space.
- Calls: Not inferable.

### `Set_Velocity`
- Purpose: Sets the sound's velocity for Doppler effect calculations.
- Calls: Not inferable.

### `Auto_Calc_Velocity`
- Purpose: Enables/disables automatic velocity calculation based on position changes.
- Calls: Not inferable.

### `Set_Max_Vol_Radius`
- Purpose: Sets the distance at which the sound reaches maximum volume.
- Calls: Not inferable.

### `Set_DropOff_Radius`
- Purpose: Sets the distance at which the sound becomes inaudible.
- Calls: Not inferable.

### `On_Frame_Update`
- Purpose: Updates sound state per frame (e.g., velocity auto-calculation).
- Calls: Not inferable.

### `Save` / `Load`
- Purpose: Serializes/deserializes the sound object.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `AudibleSound.H` (base class)
- `mempool.h` (memory management)
- `Vector3`, `Matrix3D` (math types)
- `SoundCullObjClass` (culling wrapper)
- `MILES_HANDLE` (MSS audio handle)
- `ChunkSaveClass`, `ChunkLoadClass` (serialization)
- `PersistFactoryClass` (factory pattern)
