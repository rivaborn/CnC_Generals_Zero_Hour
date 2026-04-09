# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/stripoptimizer.h

## Purpose
Header defining the `StripOptimizerClass` for optimizing 3D mesh rendering strips and triangle order.

## Responsibilities
- Provides static methods for stripifying triangles, combining strips, and optimizing strip/triangle order.
- Calculates strip index counts for memory management.
- Supports efficient vertex access patterns for rendering performance.

## Key Types
- **StripOptimizerClass (Class)**: Utility class for mesh strip optimization.

## Key Functions
### Stripify
- Purpose: Converts a list of triangles into vertex strips.
- Calls: Not inferable.

### Combine_Strips
- Purpose: Merges multiple strips into a single optimized strip.
- Calls: Not inferable.

### Optimize_Strip_Order
- Purpose: Sorts strips to minimize GPU cache misses.
- Calls: Not inferable.

### Optimize_Triangle_Order
- Purpose: Reorders triangles for near-optimal rendering performance.
- Calls: Not inferable.

### Get_Strip_Index_Count
- Purpose: Returns the total number of indices in a strip set.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `always.h` (included header).
- External symbols: `int*` (return types), `const int*` (input parameters).
