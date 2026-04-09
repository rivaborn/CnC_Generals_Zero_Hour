# GeneralsMD/Code/Libraries/Source/profile/internal_result.h - Enhanced Analysis

## Architectural Role
This file defines concrete implementations of the profiling result interface, enabling runtime profiling data export in two formats: CSV for flat data and DOT for hierarchical visualization. It bridges the profiling subsystem with external tools (like GraphViz) for performance analysis.

## Cross-References
### Incoming
- Likely called by the main profiling manager (e.g., `profile_manager.cpp`) to instantiate result handlers
- Used by the profiling initialization code to register available result formats

### Outgoing
- Inherits from `ProfileResultInterface`, implementing its virtual methods
- Uses `ProfileFuncLevel` for thread/function data access
- Depends on `ProfileResultFileCSV`/`ProfileResultFileDOT` implementations in corresponding `.cpp` files

## Design Patterns
- **Factory Pattern**: `Create` methods abstract object instantiation
- **Strategy Pattern**: Different result formats implement the same interface
- **Visitor Pattern**: `WriteResults` acts as a visitor for profiling data structures

*Not inferable: Exact caller relationships or template usage*
