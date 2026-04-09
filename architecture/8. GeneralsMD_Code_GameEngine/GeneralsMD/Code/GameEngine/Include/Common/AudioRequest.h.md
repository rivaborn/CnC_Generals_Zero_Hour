# GeneralsMD/Code/GameEngine/Include/Common/AudioRequest.h

## Purpose
Defines the `AudioRequest` structure and related types for audio control operations in the game.

## Responsibilities
- Declares the `AudioRequest` structure for audio command requests.
- Defines request types (`AR_Play`, `AR_Pause`, `AR_Stop`).
- Uses memory pooling for object management.
- Provides a union for handling different audio interaction targets.

## Key Types
- **AudioEventRTS (Class)**: Not inferable.
- **RequestType (Enum)**: Audio request types (play, pause, stop).
- **AudioRequest (Struct)**: Container for audio requests with type and target.
- **AudioRequestMagicEnum (Enum)**: Not inferable.
- **(anonymous union) (Union)**: Holds either an `AudioEventRTS*` or `AudioHandle`.

## Key Functions
### MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE
- Purpose: Memory management macros for `AudioRequest`.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/GameAudio.h` (for `AudioHandle`, `AudioEventRTS`)
- `Common/GameMemory.h` (for `MemoryPoolObject`)
