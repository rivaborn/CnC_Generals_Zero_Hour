# Generals/Code/Tools/WorldBuilder/src/TeamGeneric.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for team-specific script hooks in WorldBuilder, bridging MFC dialog controls with the game's dictionary-based configuration system. It enables map editors to assign scripts to teams, critical for mission logic in the game.

## Cross-References
### Incoming
- `WorldBuilder` (parent tool) instantiates this property page
- `EditParameter` provides script loading functionality
- MFC framework calls `OnInitDialog` and message handlers

### Outgoing
- Calls into `Dict` class for configuration persistence
- Uses `EditParameter::loadScripts` for script enumeration
- Relies on `TheNameKeyGenerator` for key naming

## Design Patterns
- **Property Page Pattern**: Encapsulates UI and data synchronization for a specific configuration aspect
- **Observer Pattern**: UI controls notify via `ON_CBN_SELCHANGE` when selections change
- **Data Transfer Object**: Uses `Dict` as a configuration container, with this class as the adapter

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns in this file.
