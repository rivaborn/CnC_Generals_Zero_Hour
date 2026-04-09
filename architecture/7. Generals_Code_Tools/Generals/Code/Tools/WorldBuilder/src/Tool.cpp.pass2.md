# Generals/Code/Tools/WorldBuilder/src/Tool.cpp - Enhanced Analysis

## Architectural Role
This file defines the base `Tool` class for WorldBuilder's editing tools, serving as the foundation for all brush-based operations. It abstracts common functionality like cursor management, blend calculations, and coordinate conversions, which are reused across specialized tools (e.g., terrain, object placement).

## Cross-References
### Incoming
- **Tool subclasses**: `BrushTool`, `MoundTool`, `RampTool`, etc., inherit and extend this base class.
- **UI Framework**: `CMainFrame` calls `activate()` to manage tool activation dialogs.
- **Rendering**: `DrawObject` interacts via `setDoBrushFeedback` for visual feedback control.

### Outgoing
- **Document System**: Calls `CWorldBuilderDoc` methods for coordinate-cell conversions.
- **Win32 API**: Directly uses `::SetCursor` and `::DestroyCursor` for cursor handling.

## Design Patterns
- **Template Method**: `activate()` provides a default implementation (no-options dialog) for subclasses to override.
- **Strategy**: Blend factor calculations (`calcRoundBlendFactor`, `calcSquareBlendFactor`) encapsulate different brush behaviors.
- **Dependency Injection**: `CWorldBuilderDoc` is passed as a parameter, decoupling tools from the document system.
