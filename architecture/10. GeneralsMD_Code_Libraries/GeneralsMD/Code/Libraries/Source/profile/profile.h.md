# GeneralsMD/Code/Libraries/Source/profile/profile.h

## Purpose
Header file defining the `Profile` class for performance profiling in the game engine.

## Responsibilities
- Manages range-based profiling (start/stop/append ranges)
- Tracks recorded frames and their names
- Provides access to profiling data (frame count, names, totals)
- Supports pattern matching for filtering profiles
- Handles CPU clock cycle measurements

## Key Types
- **Profile (Class)**: Core profiling interface with static methods for range management and data access.
- **FrameName (Struct)**: Stores metadata for recorded frames (name, count, recording state, etc.).
- **PatternListEntry (Struct)**: Linked list node for storing active/inactive pattern filters.

## Key Functions
### `StartRange(const char *range)`
- Purpose: Begins recording a named range or the current frame.
- Calls: Not inferable (implementation in .cpp).

### `StopRange(const char *range)`
- Purpose: Ends recording a range, making data available as a new frame.
- Calls: Not inferable.

### `SimpleMatch(const char *str, const char *pattern)`
- Purpose: Recursively matches strings against patterns (wildcard `*` only).
- Calls: Not inferable.

### `AddResultFunction(...)`
- Purpose: Registers a factory function for creating result interfaces.
- Calls: Not inferable.

## Globals
- **firstPatternEntry (PatternListEntry*)**: Head of the pattern filter linked list.
- **lastPatternEntry (PatternListEntry*)**: Tail of the pattern filter list for O(1) appends.
- **m_rec (unsigned)**: Count of recorded frames.
- **m_recNames (char**)**: Array of recorded frame names.
- **m_names (unsigned)**: Count of known frame names.
- **m_frameNames (FrameName*)**: Array of `FrameName` structs.
- **m_clockCycles (_int64)**: Cached CPU clock cycles per second.

## Dependencies
- **Includes**: `profile_doc.h`, `profile_highlevel.h`, `profile_funclevel.h`, `profile_result.h`
- **External Symbols**: `ProfileResultInterface` (from `profile_result.h`), `_int64` (Windows type).
