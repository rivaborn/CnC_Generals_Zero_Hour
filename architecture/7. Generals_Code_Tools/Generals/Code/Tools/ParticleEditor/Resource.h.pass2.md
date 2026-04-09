# Generals/Code/Tools/ParticleEditor/Resource.h - Enhanced Analysis

## Architectural Role
This file serves as the resource header for the ParticleEditor tool, defining UI element IDs and dialog templates. It bridges the MFC-based editor UI with the underlying particle system logic, enabling runtime UI-to-data mapping.

## Cross-References
### Incoming
- `ParticleEditor.rc` (resource script) - includes this header for ID definitions
- `ParticleEditor.cpp` (editor implementation) - references these IDs for UI element access

### Outgoing
- None (header-only file with no function calls)

## Design Patterns
- **Resource ID Enumeration**: Uses sequential ID numbering to avoid collisions
- **Dialog Template Pattern**: Defines dialog layouts via resource IDs for MFC framework
- **UI-Data Separation**: IDs serve as contracts between UI and business logic layers

Key insight: The ID numbering scheme (e.g., 1000-1104 range) suggests this editor was developed alongside other tools using similar conventions, indicating a standardized toolchain architecture.
