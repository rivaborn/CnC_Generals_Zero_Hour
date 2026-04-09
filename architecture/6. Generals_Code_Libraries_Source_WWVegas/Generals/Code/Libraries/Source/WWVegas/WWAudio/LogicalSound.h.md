# Generals/Code/Libraries/Source/WWVegas/WWAudio/LogicalSound.h

## Purpose
Defines the `LogicalSoundClass`, representing in-game sounds that affect gameplay without producing audible output.

## Responsibilities
- Manages logical sound properties (position, type mask, notification delays).
- Handles scene integration and culling.
- Provides persistence (save/load) for sound state.
- Tracks listener timestamps for notification logic.

## Key Types
- **LogicalSoundClass (Class)**: Represents non-audible sounds affecting gameplay.

## Key Functions
### `Allow_Notify`
- Purpose: Checks if notification is allowed based on timestamp.
- Calls: None visible.

### `On_Frame_Update`
- Purpose: Updates sound state per frame.
- Calls: None visible.

### `Add_To_Scene`
- Purpose: Adds sound to the active scene.
- Calls: None visible.

### `Remove_From_Scene`
- Purpose: Removes sound from the active scene.
- Calls: None visible.

## Globals
- None.

## Dependencies
- `SoundSceneObj.H`, `BitType.H`, `Vector3.H`, `Matrix3D.H`
- Inherits from `SoundSceneObjClass`
- Uses `ChunkSaveClass`, `ChunkLoadClass`, `PersistFactoryClass`
