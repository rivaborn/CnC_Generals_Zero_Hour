# GeneralsMD/Code/GameEngine/Include/Common/DisabledTypes.h - Enhanced Analysis

## Architectural Role
This header defines the core disable state system used across the game engine to track various disabled conditions for game objects. It serves as the central type definition for all disable-related logic, ensuring consistent state management for units, buildings, and other entities.

## Cross-References
### Incoming
- Game object classes (e.g., units, buildings) that maintain disable state
- AI systems that check/manipulate disable states
- Damage/weapon systems that apply disable effects
- Power management systems (for DISABLED_UNDERPOWERED)

### Outgoing
- Uses `BitFlags` template from Common/BitFlags.h for mask operations
- Uses `BitFlagsIO` for serialization (implied by naming)
- Relies on `BaseType.h` for fundamental types

## Design Patterns
- **Type Object Pattern**: The `DisabledType` enum acts as a type object defining all possible disable states
- **Bitmask Pattern**: Uses `BitFlags` template to efficiently track multiple disable states
- **Utility Function Pattern**: Provides inline helper functions for common mask operations

*Not inferable*: No clear use of other patterns like Factory, Observer, etc. in this header.
