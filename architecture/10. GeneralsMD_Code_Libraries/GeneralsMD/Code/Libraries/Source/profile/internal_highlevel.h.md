# GeneralsMD/Code/Libraries/Source/profile/internal_highlevel.h

## Purpose
Defines the `ProfileId` class for high-level profiling in the game engine.

## Responsibilities
- Manages profiling IDs with names, descriptions, and units
- Tracks incremental and maximum values across frames
- Provides frame-based recording and value retrieval
- Handles string conversion for display
- Maintains a linked list of all profile IDs

## Key Types
- **ProfileId (Class)**: Core profiling identifier with value tracking
- **ValueMode (Enum)**: Mode flags (Unknown, ModeIncrement, ModeMaximum)
- **MAX_FRAME_RECORDS (Enum)**: Constant for max simultaneous frame recordings (4)
- **STRING_BUFFER_SIZE (Enum)**: Constant for internal string buffer size (1024)

## Key Functions
### ProfileId::Increment
- Purpose: Adds a value to the current profile counter
- Calls: None visible

### ProfileId::Maximum
- Purpose: Sets a new maximum value for the profile
- Calls: None visible

### ProfileId::GetCurrentValue
- Purpose: Returns and resets the current value
- Calls: None visible

### ProfileId::GetFrameValue
- Purpose: Retrieves a recorded frame value
- Calls: None visible

### ProfileId::AsString
- Purpose: Converts a numeric value to a formatted string
- Calls: None visible

### ProfileId::FrameStart
- Purpose: Starts a new profiling frame
- Calls: None visible

### ProfileId::FrameEnd
- Purpose: Ends the current profiling frame
- Calls: None visible

## Globals
- **first (ProfileId*)**: Head of the linked list of profile IDs
- **curFrame (int)**: Current frame number
- **frameRecordMask (unsigned)**: Bitmask of active frame recordings
- **stringBuf (char[STRING_BUFFER_SIZE])**: Shared string buffer
- **stringBufUnused (unsigned)**: Next unused position in string buffer

## Dependencies
- None explicitly listed; appears to be a standalone header
- Uses basic C++ types (char*, double, int, etc.)
