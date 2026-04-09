# GeneralsMD/Code/Libraries/Source/profile/test1/test1.cpp

## Purpose
Test file for profiling functionality in the SAGE engine, demonstrating basic profiling blocks and recursive function calls.

## Responsibilities
- Demonstrates profiling block usage (`ProfileHighLevel::Block`)
- Tests recursive function profiling
- Shows simple arithmetic operations for profiling
- Outputs profiling results via `printf`

## Key Types
- `ProfileHighLevel::Block`: RAII-style profiling block
- `ProfileHighLevel::Id`: Profiling identifier
- `ProfileHighLevel` (namespace): High-level profiling utilities

## Key Functions
### `DebugGetDefaultCommands`
- Purpose: Returns default debug commands for profiling.
- Calls: None

### `calcThis`
- Purpose: Increments global counter `q`.
- Calls: None

### `calcThat`
- Purpose: Calls `calcThis` then decrements `q`.
- Calls: `calcThis`

### `recursion`
- Purpose: Recursive function that increments `q` by level.
- Calls: `recursion2`

### `recursion2`
- Purpose: Recursive helper that calls `recursion`.
- Calls: `recursion`

### `recursionShell`
- Purpose: Wraps recursion in a profiling block.
- Calls: `recursion`, `ProfileHighLevel::Block` constructor

### `showResults`
- Purpose: Enumerates and prints profiling results.
- Calls: `ProfileHighLevel::EnumProfile`, `printf`

### `main`
- Purpose: Entry point that runs tests and shows results.
- Calls: `calcThis`, `calcThat`, `recursionShell`, `showResults`

## Globals
- `q` (int): Global counter for profiling tests

## Dependencies
- `"../profile.h"`: Profiling utilities
- `"../../debug/debug.h"`: Debug
