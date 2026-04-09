# GeneralsMD/Code/GameEngine/Include/GameClient/ShellMenuScheme.h - Enhanced Analysis

## Architectural Role
This file defines the UI shell menu system, which handles the rendering of static menu backgrounds and decorative elements (lines/images) in the SAGE engine. It bridges the INI-based configuration system with the rendering pipeline, allowing modders to customize menu appearances without touching core code.

## Cross-References
### Incoming
- Likely called by UI managers (e.g., `MenuSystem`) for menu rendering
- Used by INI parsing infrastructure (via `FieldParse` callbacks)
- Potentially referenced by `GameClient` initialization code

### Outgoing
- Depends on `Image` class for texture rendering
- Uses `Color` for line drawing
- Interacts with INI parsing system (`INI` class, `FieldParse`)

## Design Patterns
- **Composite**: `ShellMenuScheme` aggregates `ShellMenuSchemeImage` and `ShellMenuSchemeLine` objects
- **Singleton-like**: `ShellMenuSchemeManager` appears to be the sole manager for menu schemes (though no explicit singleton pattern)
- **Strategy**: Parse functions (`parseImagePart`, `parseLinePart`) act as strategy objects for INI parsing

*Not inferable*: No clear use of Observer, Factory, or other patterns from header alone.
