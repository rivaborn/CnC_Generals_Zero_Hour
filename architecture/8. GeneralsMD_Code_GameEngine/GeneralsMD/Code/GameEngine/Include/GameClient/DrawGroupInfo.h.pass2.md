# GeneralsMD/Code/GameEngine/Include/GameClient/DrawGroupInfo.h - Enhanced Analysis

## Architectural Role
This file defines the configuration structure for text rendering in the game's UI system, bridging the gap between INI-based configuration and the rendering pipeline. It encapsulates all visual properties needed for consistent text display across the game's HUD and menus.

## Cross-References
### Incoming
- UI rendering systems (e.g., HUD, menu drawing)
- INI parsing infrastructure (uses `FieldParse` table)
- Localization systems (font name configuration)

### Outgoing
- Core rendering subsystem (W3D) for text drawing
- Color management utilities
- String/INI parsing utilities

## Design Patterns
- **Data Transfer Object (DTO)**: Pure data container for text rendering configuration
- **Union for Type Switching**: Allows runtime selection between pixel/percentage offsets
- **Singleton-like Global**: `TheDrawGroupInfo` suggests a global configuration pattern (though actual singleton implementation may be elsewhere)
