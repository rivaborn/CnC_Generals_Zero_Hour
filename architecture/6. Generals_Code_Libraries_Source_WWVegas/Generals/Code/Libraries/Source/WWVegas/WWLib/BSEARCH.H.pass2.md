# Generals/Code/Libraries/Source/WWVegas/WWLib/BSEARCH.H - Enhanced Analysis

## Architectural Role
This file provides a low-level utility for efficient binary search operations, likely used throughout the engine for data structure traversal (e.g., unit lists, tech trees). Its inlined comparison optimization suggests it's critical for performance-sensitive lookups.

## Cross-References
### Incoming
- **Game Logic**: Unit/building lookup tables (e.g., `UnitType` searches)
- **AI**: Decision tree evaluations requiring sorted data access
- **Rendering**: W3D model/animation index searches

### Outgoing
- None (standalone utility)

## Design Patterns
- **Template Method**: Generic binary search with customizable comparison via operator overloads
- **Optimization Pattern**: Inlined comparison to reduce function call overhead
- **Early Exit**: Returns immediately on exact match to minimize comparisons

*Not inferable*: No other patterns evident from implementation.
