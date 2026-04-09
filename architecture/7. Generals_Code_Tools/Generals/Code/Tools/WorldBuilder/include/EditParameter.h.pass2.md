# Generals/Code/Tools/WorldBuilder/include/EditParameter.h - Enhanced Analysis

## Architectural Role
This header defines the `EditParameter` dialog class, a critical component of WorldBuilder's parameter editing system. It bridges the gap between the game's scripting system and the editor's UI, allowing modders to configure game parameters through a structured interface.

## Cross-References
### Incoming
- **WorldBuilder UI modules**: Likely called by various editor panels that need to edit parameters (e.g., script triggers, unit properties).
- **Scripting system**: Used when editing script parameters in the editor.

### Outgoing
- **GameLogic/Scripts.h**: Directly interacts with the scripting system to load and validate parameters.
- **Common/SubsystemInterface.h**: Likely uses common utilities for string/parameter handling.
- **MFC UI components**: Relies on MFC's `CDialog`, `CComboBox`, etc., for the actual UI rendering.

## Design Patterns
- **Factory Method**: The `load*` methods act as factory methods for populating combo boxes with game data.
- **Strategy Pattern**: Different `load*` methods implement different strategies for loading specific parameter types (scripts, units, etc.).
- **Singleton-like Static Methods**: Many methods are static, suggesting a utility-class pattern for parameter editing operations.

**Note**: The heavy use of static methods and global-like static members (`m_sidesListP`, `m_unitName`) indicates a design optimized for the editor's workflow rather than strict OOP principles. This is typical for tooling code where state management is less critical than rapid development.
