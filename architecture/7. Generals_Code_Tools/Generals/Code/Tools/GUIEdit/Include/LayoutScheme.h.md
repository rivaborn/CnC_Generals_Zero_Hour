# Generals/Code/Tools/GUIEdit/Include/LayoutScheme.h

## Purpose
Defines the `LayoutScheme` class for managing default UI control appearances in the GUI editor.

## Responsibilities
- Stores default colors, images, and fonts for UI controls
- Provides methods to load/save schemes and apply them to windows
- Manages text drawing properties for enabled/disabled/highlighted states

## Key Types
- **LayoutScheme (Class)**: Manages default UI control appearances and schemes
- **ImageAndColorInfo (Struct)**: Not inferable (external type)
- **TextDrawData (Struct)**: Not inferable (external type)
- **StateIdentifier (Enum)**: Not inferable (external type)

## Key Functions
### `LayoutScheme::init`
- Purpose: Initializes the layout scheme
- Calls: Not inferable

### `LayoutScheme::openDialog`
- Purpose: Opens the scheme editing dialog
- Calls: Not inferable

### `LayoutScheme::saveScheme`
- Purpose: Saves the current scheme to a file
- Calls: Not inferable

### `LayoutScheme::loadScheme`
- Purpose: Loads a scheme from a file
- Calls: Not inferable

### `LayoutScheme::applyPropertyTablesToWindow`
- Purpose: Applies stored properties to all windows in the editor
- Calls: Not inferable

## Globals
- **TheDefaultScheme (LayoutScheme*)**: Global instance of the default layout scheme

## Dependencies
- `windows.h`, `BaseType.h`, `Properties.h`
- `Image`, `Color`, `GameFont`, `GameWindow`, `StateIdentifier` (external types)
