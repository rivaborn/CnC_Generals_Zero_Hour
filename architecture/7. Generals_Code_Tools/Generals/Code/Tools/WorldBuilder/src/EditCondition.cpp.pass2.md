# Generals/Code/Tools/WorldBuilder/src/EditCondition.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for editing script conditions in WorldBuilder, bridging the gap between the MFC-based dialog system and the game's scripting engine. It handles real-time formatting of condition text with interactive parameter links, demonstrating the engine's modular approach to tooling.

## Cross-References
### Incoming
- **WorldBuilder main dialog**: Likely instantiates and shows this dialog when editing conditions
- **Scripting system**: `TheScriptEngine` provides condition templates and validation

### Outgoing
- **EditParameter dialog**: Delegates parameter editing to `EditParameter::edit()`
- **Script engine**: Uses `Condition` class methods for UI text generation and validation
- **MFC controls**: Directly manipulates `CRichEditCtrl` for text formatting and link handling

## Design Patterns
- **Observer Pattern**: The dialog reacts to rich edit control notifications (EN_LINK, EN_SELCHANGE) to update formatting dynamically
- **Composite View**: Combines static text with interactive parameter links in a single rich edit control
- **Strategy Pattern**: Condition type changes trigger different formatting behaviors through `formatConditionText`

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns in this file.
