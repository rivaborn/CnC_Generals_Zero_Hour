# Generals/Code/Tools/Autorun/DrawButton.cpp - Enhanced Analysis

## Architectural Role
This file implements a custom UI button control specifically for the Autorun tool, bridging the tool's UI layer with the game's localization and text rendering systems. It demonstrates the engine's modular design by supporting both standalone tool usage (LEAN_AND_MEAN) and integration with the full game engine.

## Cross-References
### Incoming
- Autorun tool UI system (likely Wnd_File.cpp) instantiates and manages DrawButton objects
- Localization system (Locale_API) provides string resources
- Font rendering system (TTFontClass) handles text display

### Outgoing
- GameText subsystem for localized string fetching (non-LEAN_AND_MEAN)
- Windows GDI for direct bitmap rendering
- UnicodeString for string manipulation

## Design Patterns
- **State Pattern**: Button state management (NORMAL/FOCUS/PRESSED) encapsulated within the class
- **Adapter Pattern**: Bridges between Windows RECT and custom Rect structures
- **Strategy Pattern**: Different rendering approaches based on LEAN_AND_MEAN compilation flag

Rules followed. Output under 400 tokens.
