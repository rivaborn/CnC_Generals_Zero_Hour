# Generals/Code/Tools/WorldBuilder/src/EditAction.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for script action editing in WorldBuilder, bridging the MFC-based dialog system with the game's scripting engine. It handles parameter visualization and editing, leveraging the rich edit control for interactive text formatting.

## Cross-References
### Incoming
- **WorldBuilder main dialog**: Likely instantiates and shows this dialog when editing script actions
- **Script action system**: Passes `ScriptAction` objects for editing

### Outgoing
- **ScriptEngine**: Queries action templates via `TheScriptEngine->getActionTemplate()`
- **EditParameter**: Delegates parameter editing via `EditParameter::edit()`
- **MFC controls**: Uses `CRichEditCtrl` for formatted text display and interaction

## Design Patterns
- **Observer Pattern**: Handles rich edit control notifications (`EN_LINK`, `EN_SELCHANGE`) to update UI dynamically
- **Strategy Pattern**: Action type selection changes the behavior via `setActionType()`, with formatting adapted per type
- **Composite Pattern**: Combines static text and parameter placeholders in a single rich edit control for unified editing

*Not inferable*: No clear use of Visitor or Factory patterns despite scripting context.
