# GeneralsMD/Code/Libraries/Source/profile/profile_highlevel.cpp

## Purpose
High-level profiling system for performance measurement in the game engine.

## Responsibilities
- Manages profile IDs for tracking metrics (time, calls, etc.)
- Provides scoped timing blocks (`Block`) for measuring execution time
- Handles frame-based recording of profile data
- Supports string formatting for profile values
- Thread-safe access via fast critical section

## Key Types
- `ProfileHighLevel::Id` (Class): Wrapper for a profile ID, provides accessors for values and metadata
- `ProfileHighLevel::Block` (Class): RAII-style scoped timer for measuring code block execution time
- `ProfileId` (Class): Core profile ID implementation, stores values, metadata, and frame history
- `ProfileFastCS` (Class): Custom fast critical section for thread synchronization

## Key Functions
### `ProfileHighLevel::AddProfile`
- Purpose: Creates or retrieves a profile ID by name
- Calls: `FindProfile`, `ProfileAllocMemory`, `new`

### `ProfileHighLevel::Block::Block`
- Purpose: Starts a timed block, increments call counter
- Calls: `AddProfile`, `ProfileGetTime`

### `ProfileHighLevel::Block::~Block`
- Purpose: Ends timed block, calculates and records elapsed time
- Calls: `ProfileGetTime`

### `ProfileId::FrameStart`
- Purpose: Begins recording for a new frame
- Calls: `ProfileAllocMemory`, `ProfileReAllocMemory`

### `ProfileId::FrameEnd`
- Purpose: Ends frame recording, stores or mixes frame data
- Calls: `ProfileReAllocMemory`

## Globals
- `cs` (`ProfileFastCS`): Global critical section for thread synchronization
- `ProfileHighLevel::Instance` (`ProfileHighLevel`): Singleton instance of the high-level profiler

## Dependencies
- `_pch.h`: Precompiled header
- `<new>`: For placement `new`
- `<stdio.h>`: For string formatting
- `ProfileAllocMemory`, `ProfileReAllocMemory`: Memory allocation functions
- `ProfileGetTime`: Time measurement function
- `DFAIL_IF`: Debug assertion macro
