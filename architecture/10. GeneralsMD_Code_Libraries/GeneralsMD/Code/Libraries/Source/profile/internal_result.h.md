# GeneralsMD/Code/Libraries/Source/profile/internal_result.h

## Purpose
Defines internal profiling result interfaces for CSV and DOT file output.

## Responsibilities
- Declares `ProfileResultFileCSV` for flat CSV profiling data.
- Declares `ProfileResultFileDOT` for DOT graph visualization.
- Provides factory methods (`Create`) for both result types.
- Manages thread-specific and hierarchical profiling data.

## Key Types
- **ProfileResultFileCSV (Class)**: CSV flat file profiler.
- **ProfileResultFileDOT (Class)**: DOT graph profiler.
- **(anonymous enum) (Enum)**: Placeholder for `MAX_FUNCTIONS_PER_FILE`.
- **MAX_FUNCTIONS_PER_FILE (Enum)**: Limits functions per DOT file.
- **FoldHelper (Class)**: Helper for folding functions in DOT output.

## Key Functions
### ProfileResultFileCSV::Create
- Purpose: Factory for CSV profiler.
- Calls: Not inferable.

### ProfileResultFileDOT::Create
- Purpose: Factory for DOT profiler.
- Calls: Not inferable.

### ProfileResultFileDOT::WriteResults
- Purpose: Writes DOT graph data.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `ProfileResultInterface` (base class).
- `ProfileFuncLevel` (for thread/function data).
- `ProfileResultFileCSV`/`ProfileResultFileDOT` inherit from `ProfileResultInterface`.
