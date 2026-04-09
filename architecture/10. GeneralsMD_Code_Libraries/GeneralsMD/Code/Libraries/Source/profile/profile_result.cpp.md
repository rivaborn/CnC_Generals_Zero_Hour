# GeneralsMD/Code/Libraries/Source/profile/profile_result.cpp

## Purpose
Handles writing profiling results to CSV and DOT files for performance analysis.

## Responsibilities
- Implements `ProfileResultFileCSV` for CSV output
- Implements `ProfileResultFileDOT` for DOT graph output
- Manages thread enumeration and profile data serialization
- Handles memory allocation/deallocation for profile results

## Key Types
- `ProfileResultFileCSV` (Class): CSV result writer
- `ProfileResultFileDOT` (Class): DOT graph result writer
- `FoldHelper` (Struct): Helper for folding functions in DOT output

## Key Functions
### `ProfileResultFileCSV::WriteThread`
- Purpose: Writes per-thread profiling data to CSV
- Calls: `ProfileFuncLevel::Thread::EnumProfile`, `ProfileFuncLevel::Id::GetCalls`, `ProfileFuncLevel::Id::GetFunctionTime`, etc.

### `ProfileResultFileCSV::WriteResults`
- Purpose: Writes high-level profiling results to CSV
- Calls: `ProfileHighLevel::EnumProfile`, `ProfileHighLevel::Id::GetName`, etc.

### `ProfileResultFileDOT::WriteResults`
- Purpose: Generates DOT graph visualization of call relationships
- Calls: `ProfileFuncLevel::EnumThreads`, `ProfileFuncLevel::Thread::EnumProfile`, `ProfileFuncLevel::Id::GetCaller`

## Globals
- None

## Dependencies
- `<stdio.h>`, `<stdlib.h>`
- `ProfileFuncLevel`, `ProfileHighLevel`, `ProfileAllocMemory`, `ProfileFreeMemory`
