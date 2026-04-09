# Generals/Code/Libraries/Source/WWVegas/WWAudio/Sound3D.h

## Purpose
Defines the `Sound3DClass` for spatialized 3D audio in the SAGE engine, handling position, velocity, and attenuation for dynamic sound sources.

## Responsibilities
- Manages 3D sound properties (position, velocity, attenuation)
- Integrates with the sound scene for spatial playback
- Handles Miles audio system integration
- Supports serialization via `PersistClass`
- Provides culling and priority control

## Key Types
- **Sound3DClass (Class)**: Represents a 3D sound with spatial properties and playback control.

## Key Functions
### `Play`
- Purpose: Starts playback of the 3D sound.
- Calls: Not inferable.

### `Add_To_Scene`
- Purpose: Adds the sound to the scene for spatial processing.
- Calls: Not inferable.

### `Set_Position`
- Purpose: Updates the sound's position in 3D space.
- Calls: Not inferable.

### `Set_Velocity`
- Purpose: Sets the sound's velocity for Doppler effects.
- Calls: Not inferable.

### `Set_Max_Vol_Radius`
- Purpose: Configures the distance where sound reaches max volume.
- Calls: Not inferable.

### `Set_DropOff_Radius`
- Purpose: Sets the distance where sound becomes inaudible.
- Calls: Not inferable.

### `On_Frame_Update`
- Purpose: Updates sound state per frame (e.g., auto-calculated velocity).
- Calls: Not inferable.

### `Save` / `Load`
- Purpose: Serializes/deserializes sound state.
- Calls: Not inferable.

## Globals
- **None**

## Dependencies
- `AudibleSoundClass` (base class)
- `Vector3`, `Matrix3D` (math types)
- `SoundCullObjClass` (culling wrapper)
- `MILES_HANDLE` (Miles audio handle)
- `ChunkSaveClass`, `ChunkLoadClass` (serialization)
- `PersistFactoryClass` (factory pattern)
