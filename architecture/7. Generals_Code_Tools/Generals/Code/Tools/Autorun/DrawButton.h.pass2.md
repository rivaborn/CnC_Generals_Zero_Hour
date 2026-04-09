# Generals/Code/Tools/Autorun/DrawButton.h - Enhanced Analysis

## Architectural Role
This header defines a lightweight UI button component used in the Autorun tool, likely for pre-game configuration or launch options. It abstracts button state management and rendering, decoupling visual representation from game logic.

## Cross-References
### Incoming
- Autorun tool UI systems (e.g., main menu, options screens)
- Event handlers for mouse input (calls `Is_Mouse_In_Region`)

### Outgoing
- `TTFontClass` for text rendering (calls `Draw_Text`)
- Windows GDI (`HDC`) for bitmap drawing

## Design Patterns
- **State Pattern**: Encapsulates button states (normal/pressed/focus) with behavior tied to each state.
- **Facade Pattern**: Hides complex rendering logic behind simple methods like `Draw_Text`.
- **Data Transfer Object**: Primarily holds button state/data, with minimal behavior.

*Not inferable*: No clear use of Observer or Strategy patterns.
