# GeneralsMD/Code/GameEngine/Include/Common/DynamicAudioEventInfo.h

## Purpose
Defines a class for customized audio events, extending `AudioEventInfo` to allow runtime overrides of audio properties.

## Responsibilities
- Manage overridden audio event properties (name, loop flags, volume, range, priority).
- Track which fields have been modified from their default INI values.
- Provide accessors for original and overridden values.
- Support memory pooling and serialization (via `Xfer`).

## Key Types
- **DynamicAudioEventInfo (Class)**: Extends `AudioEventInfo` to allow dynamic audio property overrides.
- **OverriddenFields (Enum)**: Flags for tracking which audio properties have been overridden.
- **AsciiString (Class)**: Used for storing audio event names.
- **Xfer (Class)**: Used for serialization/deserialization of non-name fields.

## Key Functions
### `overrideAudioName`, `overrideLoopFlag`, etc.
- **Purpose**: Override specific audio event properties (name, loop flags, volume, range, priority).
- **Calls**: Sets flags in `m_overriddenFields` and modifies base `AudioEventInfo` fields.

### `wasAudioNameOverriden`, `wasLoopFlagOverriden`, etc.
- **Purpose**: Check if a specific property was overridden.
- **Calls**: Tests flags in `m_overriddenFields`.

### `xferNoName`
- **Purpose**: Serialize/deserialize overridden fields except the name.
- **Calls**: Not inferable (implementation not shown).

## Globals
- **None**

## Dependencies
- `AudioEventInfo.h`: Base class for audio event data.
- `Bitflags.h`: For tracking overridden fields.
- `AsciiString`, `Xfer`: External classes for string handling and serialization.
