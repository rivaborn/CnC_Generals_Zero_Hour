# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwprofile.cpp

## Purpose
This file implements a hierarchical profiling system for performance measurement in the game engine.

## Responsibilities
- Manages profiling nodes in a tree structure
- Tracks execution time and call counts for profiled sections
- Provides iterators for traversing profile data
- Handles loading/saving profile logs
- Supports memory and time logging

## Key Types
- `WWProfileHierachyNodeClass` (Class): Represents a node in the profiling hierarchy
- `WWProfileManager` (Class): Manages the profiling system and root node
- `WWProfileIterator` (Class): Iterates through profile nodes
- `WWProfileInOrderIterator` (Class): Performs in-order traversal of profile nodes
- `WWProfileHierachyInfoClass` (Class): Stores profile information for loading/saving
- `WWTimeItClass` (Class): RAII timer for measuring execution time
- `WWMeasureItClass` (Class): RAII timer that stores result in a float
- `WWMemoryAndTimeLog` (Class): Logs memory allocations and time

## Key Functions
### `WWProfile_Get_Ticks`
- Purpose: Retrieves CPU performance counter
- Calls: None

### `WWProfileHierachyNodeClass::Call`
- Purpose: Starts timing for a profile node
- Calls: `WWProfile_Get_Ticks`

### `WWProfileHierachyNodeClass::Return`
- Purpose: Stops timing and records results
- Calls: `WWProfile_Get_Ticks`, `WWProfile_Get_Inv_Processor_Ticks_Per_Second`

### `WWProfileManager::Start_Profile`
- Purpose: Begins a named profile section
- Calls: `Get_Sub_Node`

### `WWProfileManager::Stop_Profile`
- Purpose: Ends a profile section and records results
- Calls: `Return`

### `Read_Frame`
- Purpose: Parses frame data from profile log
- Calls: `Read_Int`, `Read_Float`, `Read_String`, `Read_Line`

### `WWMemoryAndTimeLog::Log_Intermediate`
- Purpose: Logs intermediate memory and time measurements
- Calls: `WWProfile_Get_System_Time`, `FastAllocatorGeneral::Get_Allocator`

## Globals
- `ProfileCollectVector` (SimpleDynVecClass): Collects profile nodes
- `TotalFrameTimes` (double): Accumulates total frame times
- `ProfileCollecting` (bool): Flag for profile collection state
- `ProfileStringHash` (HashTemplateClass): Maps profile names to IDs
- `ProfileStringCount` (unsigned): Count of profile strings
- `ThreadID` (unsigned int): Current thread ID for profiling

## Dependencies
- `wwprofile.h`, `fastallocator.h`, `wwdebug.h`, `windows.h`, `systimer.h`, `rawfile.h`, `ffactory.h`, `simplevec.h`, `cpudetect.h`, `hashtemplate.h`, `<stdio.h>`
- `TIMEGETTIME()`, `CPUDetectClass::Get_Inv_Processor_Ticks_Per_Second()`
- `W3DNEW`, `WWASSERT`, `WWDEBUG_SAY`, `WWRELEASE_SAY` macros
