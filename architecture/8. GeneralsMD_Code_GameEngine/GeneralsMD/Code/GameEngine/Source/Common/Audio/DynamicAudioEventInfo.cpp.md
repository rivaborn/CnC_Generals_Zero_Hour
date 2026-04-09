# GeneralsMD/Code/GameEngine/Source/Common/Audio/DynamicAudioEventInfo.cpp

## Purpose
Implements `DynamicAudioEventInfo`, a customizable audio event class for level-specific sounds in the SAGE engine.

## Responsibilities
- Provides override methods for audio event properties (name, loop, volume, range, priority).
- Manages serialization of overridden fields via `Xfer`.
- Supports dynamic casting for type-safe access.

## Key Types
- `DynamicAudioEventInfo` (Class): Extends `AudioEventInfo` to allow runtime customization of audio parameters.

## Key Functions
### `overrideAudioName`
- Purpose: Changes the audio event's name and tracks the original.
- Calls: `m_overriddenFields.set`

### `overrideLoopFlag`
- Purpose: Modifies the loop flag in the control bitfield.
- Calls: `BitSet`, `BitClear`

### `xferNoName`
- Purpose: Serializes overridden fields (except name) for save/load.
- Calls: `xfer->xferVersion`, `xfer->xferUnsignedByte`, `xfer->xferBool`, `xfer->xferInt`, `xfer->xferReal`

## Globals
- None

## Dependencies
- `Common/DynamicAudioEventInfo.h`
- `Common/Xfer.h`
- `PreRTS.h` (engine header)
- `BitSet`, `BitClear`, `BitTest` (bit manipulation macros)
