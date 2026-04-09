# Generals/Code/Tools/WorldBuilder/include/ScorchOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for scorch effect configuration in WorldBuilder, bridging the gap between user input and map object property manipulation. It extends the `COptionsPanel` and `PopupSliderOwner` frameworks to provide a modeless dialog for adjusting scorch parameters.

## Cross-References
### Incoming
- **WorldBuilder UI controllers**: Likely called by main WorldBuilder window when scorch tools are activated
- **Map object selection system**: Uses `getSingleSelectedScorch()` to access currently selected objects
- **Property dictionary system**: Interacts with `Dict` objects for storing/retrieving scorch parameters

### Outgoing
- **Popup slider system**: Implements `PopupSliderOwner` interface for radius adjustment
- **Map object modification**: Applies changes to selected objects via `Dict` manipulation
- **Game type system**: Uses `Scorches` enum from `Common/GameType.h`

## Design Patterns
- **Observer Pattern**: Static `update()` method suggests external components register for UI state changes
- **Strategy Pattern**: Different scorch types likely implemented as separate strategies (inferred from `Scorches` enum usage)
- **Mediator Pattern**: Coordinates between UI controls and underlying map object properties without direct coupling

*Not inferable*: Exact implementation of `Dict` property manipulation or how scorch effects are rendered in-game.
