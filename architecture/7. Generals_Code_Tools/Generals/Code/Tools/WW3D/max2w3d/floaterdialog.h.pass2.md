# Generals/Code/Tools/WW3D/max2w3d/floaterdialog.h - Enhanced Analysis

## Architectural Role
This file defines a utility class for managing modeless dialog boxes within the Max2W3D tool, which is part of the WW3D (Westwood 3D) asset pipeline. It bridges Windows API dialog management with the tool's interface system, enabling floating UI elements for model editing/export workflows.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/w3dutil.cpp` (referenced in header comment as example usage)
- Likely called by Max2W3D's main tool interface for UI elements

### Outgoing
- Uses Windows API (`<windows.h>`) for dialog creation and message handling
- Depends on `Interface` class (tool-specific abstraction layer)

## Design Patterns
- **Facade Pattern**: Abstracts Windows dialog complexity behind a simple class interface
- **Observer Pattern**: Dialog_Proc acts as callback handler for Windows messages (implicit)
- **Dependency Injection**: `Interface` and child dialog proc are injected via `Create()`
