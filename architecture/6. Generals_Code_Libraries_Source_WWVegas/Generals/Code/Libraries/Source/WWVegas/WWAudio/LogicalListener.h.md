# Generals/Code/Libraries/Source/WWVegas/WWAudio/LogicalListener.h

## Purpose
Defines the `LogicalListenerClass` for handling audio listeners in the game world that react to logical sounds.

## Responsibilities
- Manages listener position and transformation
- Controls sound type filtering via type mask
- Handles scene integration and timestamping for audio objects
- Provides attenuation scaling for sound distance effects

## Key Types
- **LogicalListenerClass (Class)**: Represents a listener entity that hears logical sounds in the game world.

## Key Functions
### `Set_Type_Mask`
- Purpose: Sets the sound type mask for filtering.
- Calls: None

### `Set_Position`
- Purpose: Updates the listener's position in 3D space.
- Calls: None

### `Set_Transform`
- Purpose: Sets the listener's position from a transformation matrix.
- Calls: `Get_Translation`

### `Add_To_Scene`
- Purpose: Adds the listener to the active sound scene.
- Calls: None

### `Set_Scale`
- Purpose: Adjusts the listener's attenuation scale.
- Calls: None

### `Get_New_Timestamp`
- Purpose: Generates a new timestamp for audio synchronization.
- Calls: None

## Globals
- **m_GlobalScale (float)**: Static scale factor applied to all listeners.
- **m_OldestTimestamp (uint32)**: Tracks the oldest active timestamp.
- **m_NewestTimestamp (uint32)**: Tracks the newest active timestamp.

## Dependencies
- `SoundSceneObj.H`, `BitType.H`, `Vector3.H`, `Matrix3D.H`
- Inherits from `SoundSceneObjClass`
- Uses `ChunkSaveClass` and `ChunkLoadClass` for persistence
