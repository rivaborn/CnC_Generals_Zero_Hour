# Generals/Code/Libraries/Source/WWVegas/WWAudio/SoundPseudo3D.h

## Purpose
Defines the `SoundPseudo3DClass` for pseudo-3D audio effects without hardware 3D audio requirements.

## Responsibilities
- Manages pseudo-3D sound properties (volume, pan, position)
- Handles sound attenuation via max-volume and drop-off radii
- Updates sound volume and pan based on listener position
- Integrates with Miles Sound System for audio playback

## Key Types
- **SoundPseudo3DClass (Class)**: Manages pseudo-3D sound properties and playback.

## Key Functions
### `Update_Pseudo_Volume`
- Purpose: Updates sound volume based on distance from listener.
- Calls: Not inferable.

### `Update_Pseudo_Pan`
- Purpose: Updates sound pan based on position relative to listener.
- Calls: Not inferable.

### `On_Frame_Update`
- Purpose: Handles per-frame updates for the sound.
- Calls: Not inferable.

### `Set_Miles_Handle`
- Purpose: Sets the Miles Sound System handle for playback.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Sound3D.H` (base class)
- `Matrix3D`, `Vector3` (math types)
- `MILES_HANDLE` (Miles Sound System)
- `PersistClass` (for persistence support)
