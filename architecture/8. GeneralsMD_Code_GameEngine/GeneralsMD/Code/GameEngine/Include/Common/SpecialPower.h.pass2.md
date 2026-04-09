# GeneralsMD/Code/GameEngine/Include/Common/SpecialPower.h - Enhanced Analysis

## Architectural Role
This file defines the core data structures and utility functions for the game's special power system, serving as the central interface between power definitions and their runtime usage. It bridges the gap between INI-based power configurations and the game logic modules that implement specific powers.

## Cross-References
### Incoming
- Game logic modules (CashHackSpecialPower, DefectorSpecialPower, etc.) use the bitmask utility functions (TEST_SPECIALPOWERMASK, etc.) for power type checking
- Power modules likely query SpecialPowerStore for template data during initialization

### Outgoing
- Calls into BitFlags.h for mask operations
- Uses Overridable system for template inheritance
- References AudioEventRTS for sound playback
- Depends on INI parsing infrastructure for data loading

## Design Patterns
- **Template Method**: SpecialPowerTemplate uses Overridable for data-driven behavior
- **Singleton**: TheSpecialPowerStore provides global access to power definitions
- **Bitmask Flags**: SpecialPowerMaskType enables efficient power type combinations

Rules followed. Output under 400 tokens.
