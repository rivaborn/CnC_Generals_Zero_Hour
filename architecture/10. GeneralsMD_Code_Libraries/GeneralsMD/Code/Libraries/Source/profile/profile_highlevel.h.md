# GeneralsMD/Code/Libraries/Source/profile/profile_highlevel.h

## Purpose
High-level profiling interface for performance metrics in the game engine.

## Responsibilities
- Manages profile IDs and their associated data
- Provides timer-based function block profiling
- Enumerates and searches registered profiles
- Tracks incremental values and maximums

## Key Types
- **ProfileId (Class)**: Internal ID representation (not fully exposed)
- **ProfileHighLevel::Id (Class)**: High-level profile ID with value accessors
- **ProfileHighLevel::Block (Class)**: Timer-based function block profiler
- **ProfileHighLevel (Class)**: Singleton profiler manager

## Key Functions
### ProfileHighLevel::AddProfile
- Purpose: Registers a new high-level profile value
- Calls: Not inferable (implementation in .cpp)

### ProfileHighLevel::EnumProfile
- Purpose: Enumerates registered profiles by index
- Calls: Not inferable

### ProfileHighLevel::FindProfile
- Purpose: Searches for a profile by name
- Calls: Not inferable

### ProfileHighLevel::Id::Increment
- Purpose: Increments the internal profile value
- Calls: Not inferable

### ProfileHighLevel::Id::SetMax
- Purpose: Sets a new maximum value if larger than current
- Calls: Not inferable

### ProfileHighLevel::Block::Block
- Purpose: Starts a timer-based function block
- Calls: Not inferable

## Globals
- **ProfileHighLevel::Instance (ProfileHighLevel)**: Singleton instance

## Dependencies
- Key includes: None visible in header
- External symbols: `_int64` (likely from Windows SDK)
