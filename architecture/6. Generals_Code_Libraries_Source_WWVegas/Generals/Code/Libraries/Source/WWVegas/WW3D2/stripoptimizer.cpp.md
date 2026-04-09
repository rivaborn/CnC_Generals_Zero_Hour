# Generals/Code/Libraries/Source/WWVegas/WW3D2/stripoptimizer.cpp

## Purpose
Implements triangle strip optimization algorithms for 3D rendering performance.

## Responsibilities
- Optimizes triangle strip ordering for vertex cache efficiency
- Combines multiple strips into single strips
- Implements strip generation from triangle lists
- Provides sorting utilities for optimization

## Key Types
- **Tri (Class)**: Represents a triangle with vertex indices
- **Vector3i (Class)**: 3D vector of integers for vertex data
- **Edge (Class)**: Represents an edge between two vertices
- **Triangle (Class)**: Triangle with connectivity information
- **TriangleQueue (Class)**: Priority queue for triangle processing
- **Stripify (Class)**: Main strip generation class

## Key Functions
### `Get_Strip_Similarity`
- Purpose: Calculates similarity between two strips by counting shared indices
- Calls: None

### `Optimize_Strip_Order`
- Purpose: Reorders strips to maximize vertex reuse
- Calls: `Get_Strip_Similarity`, `Copy_Strip`

### `Optimize_Triangle_Order`
- Purpose: Reorders triangles to maximize vertex reuse
- Calls: `Get_Similarity`

### `Combine_Strips`
- Purpose: Merges multiple strips into a single strip
- Calls: None

### `Stripify::stripify`
- Purpose: Generates triangle strips from input triangles
- Calls: `generateTriangleList`, `getTriangleNodeConnectivityWeights`

## Globals
- None

## Dependencies
- `stripoptimizer.h`
- `hashtemplate.h`
- `wwdebug.h`
- Uses `W3DNEWARRAY` for memory allocation
- Uses `WWASSERT` for debugging
