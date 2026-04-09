# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/editable.h - Enhanced Analysis

## Architectural Role
This file defines the core interface for the SAGE engine's parameter-based editing system, enabling runtime modification of game object properties through a standardized macro-based API. It bridges the gap between game data serialization and the editor/debug tools.

## Cross-References
### Incoming
- Editor tools (e.g., `WWEdit`) - uses `DECLARE_EDITABLE` and parameter macros
- Game object classes (e.g., units, buildings) - inherit `EditableClass`
- Save/load system - leverages parameter serialization

### Outgoing
- `ParameterClass` hierarchy (int, float, string, etc.) - creates parameter instances
- `ParameterListClass` - manages parameter collections
- `W3DNEW` - memory allocation for parameter objects

## Design Patterns
- **Template Method**: `EditableClass` defines parameter access hooks (`Get_Parameter_Count`, `Lock_Parameter`) with default no-op implementations
- **Macro-Based DSL**: Parameter registration uses domain-specific macros (e.g., `INT_EDITABLE_PARAM`) to hide boilerplate
- **Conditional Compilation**: `#ifdef PARAM_EDITING_ON` gates editor-specific functionality, enabling stripped builds

*Not inferable*: Exact usage of `W3DNEW` (custom allocator?) and parameter persistence mechanism.
