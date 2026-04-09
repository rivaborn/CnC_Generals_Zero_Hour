# Generals/Code/Tools/WW3D/max2w3d/exportlog.h - Enhanced Analysis

## Architectural Role
This file defines the `ExportLog` class, which serves as a bridge between the 3D model export tool (max2w3d) and the user interface, providing progress feedback during the conversion process. It is part of the toolchain infrastructure for W3D asset pipeline.

## Cross-References
### Incoming
- Likely called by `max2w3d` tool's main export logic (not shown in file)
- Possibly referenced by other WW3D tools needing progress feedback

### Outgoing
- Interacts with Windows UI subsystem (via HWND)
- Uses Windows API for dialog management (implied by HWND usage)

## Design Patterns
- **Facade Pattern**: Hides complexity of Windows dialog management behind simple static interface
- **Singleton-like**: Static methods suggest single instance management (though not strictly a singleton)
- **Observer Pattern**: Progress updates imply notification mechanism (though implementation not visible here)

*Not inferable*: No clear use of other patterns without seeing implementation.
