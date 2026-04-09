# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwprofile.h

## Purpose
Header file defining profiling utilities for performance measurement in the game engine.

## Responsibilities
- Declares profiling hierarchy node and iterator classes
- Provides timing macros for code instrumentation
- Manages global profiling state and statistics

## Key Types
- **WWProfileHierachyNodeClass (Class)**: Represents a node in the profiling hierarchy tree, tracking call counts and execution time.
- **WWProfileIterator (Class)**: Iterator for navigating the profiling hierarchy tree.
- **WWProfileInOrderIterator (Class)**: Depth-first iterator for the profiling tree.
- **WWProfileManager (Class)**: Singleton manager for the profiling system.
- **WWProfileSampleClass (Class)**: RAII wrapper for profiling scoped sections.
- **WWTimeItClass (Class)**: Simple timer for measuring execution time.
- **WWMeasureItClass (Class)**: Timer that stores results in a float pointer.

## Key Functions
### WWProfileManager::Start_Profile
- Purpose: Starts profiling a named section.
- Calls: Not inferable.

### WWProfileManager::Stop_Profile
- Purpose: Stops the current profiling section.
- Calls: Not inferable.

### WWProfileManager::Reset
- Purpose: Resets all profiling statistics.
- Calls: Not inferable.

## Globals
- **Root (WWProfileHierachyNodeClass)**: The root node of the profiling hierarchy.
- **CurrentNode (WWProfileHierachyNodeClass*)**: Pointer to the currently active profiling node.
- **FrameCounter (int)**: Counts frames since last reset.
- **ResetTime (__int64)**: Timestamp of the last reset.

## Dependencies
- Uses `__int64` for timing (defined for UNIX compatibility)
- Conditionally includes `WWDEBUG` macro for debug builds
- No external symbols used beyond standard types
