# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/soundlibrarybridge.h

## Purpose
Defines an abstract interface for bridging between the 3D engine and the sound library.

## Responsibilities
- Declares pure virtual methods for playing 2D/3D audio and stopping audio playback.
- Provides a forward declaration for Matrix3D.
- Serves as a base class for concrete sound library implementations.

## Key Types
- **SoundLibraryBridgeClass (Class)**: Abstract interface for sound library operations.
- **Matrix3D (Class)**: Forward-declared 3D transformation matrix (used for 3D audio positioning).

## Key Functions
### Play_3D_Audio
- Purpose: Plays 3D positional audio.
- Calls: None (pure virtual).

### Play_2D_Audio
- Purpose: Plays 2D audio (non-positional).
- Calls: None (pure virtual).

### Stop_Playing_Audio
- Purpose: Stops playback of a named audio clip.
- Calls: None (pure virtual).

## Globals
None.

## Dependencies
- Forward declaration of `Matrix3D`.
- No external symbols used.
