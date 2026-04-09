# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwprofile.cpp

## Purpose
Provides CPU profiling functionality for performance measurement in the game engine.

## Responsibilities
- Manages hierarchical profiling nodes for timing code sections
- Tracks CPU ticks and clock frequency for accurate timing
- Provides iterators for traversing profiling data
- Handles thread-safe profiling operations
- Supports recursive function profiling

## Key Types
- `WWProfileHierachyNodeClass` (Class): Represents a node in the profiling hierarchy with timing data
- `WWProfileManager` (Class): Manages the profiling system and root node
- `WWProfileIterator` (Class): Iterates through profiling nodes
- `WWProfileInOrderIterator` (Class): Performs in-order traversal of profiling nodes
- `WWTimeItClass` (Class): RAII-style timer for measuring code block execution time
- `WWMeasureItClass` (Class): RAII-style timer that stores results in a float pointer

## Key Functions
### `WWProfile_Get_Ticks`
- Purpose: Retrieves the CPU performance counter value
- Calls: None (inline assembly)

### `WWProfile_Get_Tick_Rate`
- Purpose: Returns the CPU clock frequency
- Calls: `QueryPerformanceFrequency`

### `WWProfileHierachyNodeClass::Call`
- Purpose: Starts timing for a profiling node
- Calls: `WWProfile_Get_Ticks`

### `WWProfileHierachyNodeClass::Return`
- Purpose: Stops timing and records results
- Calls: `WWProfile_Get_Ticks`, `WWProfile_Get_Tick_Rate`

### `WWProfileManager::Start_Profile`
- Purpose: Begins profiling a named code section
- Calls: `GetCurrentThreadId`, `Get_Sub_Node`, `Call`

### `WWProfileManager::Stop_Profile`
- Purpose: Ends profiling and records results
- Calls: `GetCurrentThreadId`, `Return`, `Get_Parent`

## Globals
- `ThreadID` (unsigned int): Stores the thread ID for thread-safe profiling
- `WWProfileManager::Root` (WWProfileHierachyNodeClass): Root node of the profiling hierarchy
- `WWProfileManager::CurrentNode` (WWProfileHierachyNodeClass*): Currently active profiling node
- `WWProfileManager::FrameCounter` (int): Counts frames for profiling
- `WWProfileManager::ResetTime` (__int64): Stores time when profiling was reset

## Dependencies
- `wwprofile.h`, `wwdebug.h`, `always.h`
- Windows API: `GetCurrentThreadId`, `QueryPerformanceFrequency`
- `W3DNEW` for memory allocation
