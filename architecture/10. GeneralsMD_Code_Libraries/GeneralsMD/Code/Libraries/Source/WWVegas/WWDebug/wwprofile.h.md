# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwprofile.h

## Purpose
Header file for the WWProfile profiling system, providing runtime performance measurement and hierarchical profiling capabilities.

## Responsibilities
- Defines profiling classes and macros for timing code execution
- Manages hierarchical profiling nodes and iteration
- Provides time and memory logging utilities
- Handles profile data collection and serialization

## Key Types
- **WWProfileHierachyNodeClass (Class)**: Represents a node in the profiling hierarchy tree
- **WWProfileManager (Class)**: Central manager for profiling system
- **WWProfileSampleClass (Class)**: RAII wrapper for profiling scoped sections
- **WWTimeItClass (Class)**: Simple timing utility without data storage
- **WWMemoryAndTimeLog (Struct)**: Tracks memory allocations and time for logging

## Key Functions
### WWProfile_Get_System_Time
- Purpose: Wrapper for timeGetTime() to get current system time
- Calls: None

### WWProfileManager::Start_Profile
- Purpose: Starts profiling a named section
- Calls: Internal node management

### WWProfileManager::Stop_Profile
- Purpose: Stops current profiling section
- Calls: Internal node management

## Globals
- **WWProfileManager::Root (WWProfileHierachyNodeClass)**: Root node of profiling hierarchy
- **WWProfileManager::CurrentNode (WWProfileHierachyNodeClass**)**: Currently active profiling node
- **WWProfileManager::IsProfileEnabled (bool)**: Global enable flag for profiling

## Dependencies
- "wwstring.h" for StringClass
- FileClass for file I/O operations
- timeGetTime() system call
- WWDEBUG and ENABLE_WWPROFILE compilation flags
