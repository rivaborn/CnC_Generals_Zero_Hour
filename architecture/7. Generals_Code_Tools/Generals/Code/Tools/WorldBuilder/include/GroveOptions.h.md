# Generals/Code/Tools/WorldBuilder/include/GroveOptions.h

## Purpose
Defines the `GroveOptions` class for configuring tree/grove placement options in WorldBuilder.

## Responsibilities
- Manages tree placement settings (count, types, placement rules)
- Provides UI for grove configuration
- Handles tree type display names and internal names
- Updates tree weights and counts dynamically

## Key Types
- `PairNameDisplayName` (struct): pairs internal name (AsciiString) with display name (UnicodeString)
- `VecPairNameDisplayName` (typedef): vector of name-display pairs
- `VecPairNameDisplayNameIt` (typedef): iterator for the vector
- `GroveOptions` (class): main configuration panel for grove options

## Key Functions
### `GetDisplayNameFromPair`
- Purpose: Retrieves display name from a name-display pair
- Calls: None

### `GroveOptions::makeMain`
- Purpose: Initializes the main grove options panel
- Calls: Not inferable

### `GroveOptions::OnInitDialog`
- Purpose: Initializes the dialog controls
- Calls: Not inferable

### `GroveOptions::_updateTreeWeights`
- Purpose: Updates tree distribution weights
- Calls: Not inferable

### `GroveOptions::_updateTreeCount`
- Purpose: Updates total tree count
- Calls: Not inferable

### `GroveOptions::_updateGroveMakeup`
- Purpose: Updates grove composition settings
- Calls: Not inferable

### `GroveOptions::_updatePlacementAllowed`
- Purpose: Updates placement restrictions (water/cliffs)
- Calls: Not inferable

## Globals
- `TheGroveOptions` (GroveOptions*): singleton instance of the grove options panel

## Dependencies
- `<map>`, `<vector>`
