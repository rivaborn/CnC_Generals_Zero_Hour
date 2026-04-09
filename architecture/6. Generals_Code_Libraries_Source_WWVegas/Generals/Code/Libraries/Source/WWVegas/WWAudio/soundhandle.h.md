# Generals/Code/Libraries/Source/WWVegas/WWAudio/soundhandle.h

## Purpose
Defines the base `SoundHandleClass` and related handle classes for audio management in the SAGE engine.

## Responsibilities
- Provides abstract interface for sound handles (3D, 2D, stream, buffer, listener).
- Manages sound sample control (playback, volume, pan, loops, etc.).
- Handles Miles Sound System (MSS) integration via virtual methods.
- Supports runtime type identification (RTTI) for derived handle types.

## Key Types
- **SoundHandleClass (Class)**: Base class for all sound handles.
- **Sound3DHandleClass (Class)**: Handle for 3D positional audio.
- **Sound2DHandleClass (Class)**: Handle for 2D audio.
- **SoundStreamHandleClass (Class)**: Handle for audio streams.
- **SoundBufferClass (Class)**: Handle for sound buffers.
- **ListenerHandleClass (Class)**: Handle for audio listeners.

## Key Functions
### `SoundHandleClass()`
- Purpose: Default constructor.
- Calls: None.

### `~SoundHandleClass()`
- Purpose: Virtual destructor.
- Calls: None.

### `As_Sound3DHandleClass()`
- Purpose: RTTI cast to `Sound3DHandleClass`.
- Calls: None.

### `Initialize(SoundBufferClass *buffer)`
- Purpose: Initializes the sound handle with a buffer.
- Calls: None.

### `Start_Sample()`
- Purpose: Starts playback of the sound sample.
- Calls: None.

### `Stop_Sample()`
- Purpose: Stops playback of the sound sample.
- Calls: None.

### `Set_Sample_Volume(S32 volume)`
- Purpose: Sets the volume of the sound sample.
- Calls: None.

### `Get_Sample_V
