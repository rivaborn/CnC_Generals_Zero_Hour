# Generals/Code/Libraries/Source/WWVegas/WW3D2/stripoptimizer.h

## Purpose
Header for the `StripOptimizerClass`, which provides static methods for optimizing 3D mesh rendering by converting triangles into vertex strips and ordering them for better GPU performance.

## Responsibilities
- Converting triangle lists into vertex strips
- Combining multiple strips into a single optimized strip
- Optimizing strip and triangle order for rendering efficiency
- Calculating strip index counts

## Key Types
- **StripOptimizerClass (Class)**: Provides static methods for mesh strip optimization.

## Key Functions
### Stripify
- Purpose: Converts a triangle list into vertex strips.
- Calls: Not inferable.

### Combine_Strips
- Purpose: Combines multiple vertex strips into a single optimized strip.
- Calls: Not inferable.

### Optimize_Strip_Order
- Purpose: Sorts strips to optimize rendering access order.
- Calls: Not inferable.

### Optimize_Triangle_Order
- Purpose: Sorts triangles into a near-optimal access order for rendering.
- Calls: Not inferable.

### Get_Strip_Index_Count
- Purpose: Returns the total number of indices in a set of strips.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `always.h` (included header)
