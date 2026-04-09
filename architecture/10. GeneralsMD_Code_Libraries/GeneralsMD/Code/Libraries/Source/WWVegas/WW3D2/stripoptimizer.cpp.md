# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/stripoptimizer.cpp

## Purpose
Implements triangle strip optimization algorithms for 3D rendering performance.

## Responsibilities
- Optimizes triangle strip ordering for vertex cache efficiency
- Combines multiple strips into single strips
- Generates triangle strips from raw triangle data
- Provides utility functions for strip manipulation

## Key Types
- **Tri (Class)**: Represents a triangle with three vertex indices
- **Vector3i (Class)**: 3D vector of integers (used for triangle vertices)
- **Edge (Class)**: Represents an edge between two vertices
- **Triangle (Class)**: Internal triangle structure with connectivity info
- **TriangleQueue (Class)**: Priority queue for triangle processing
- **Stripify (Class)**: Main strip generation class

## Key Functions
### Get_Strip_Similarity
- Purpose: Calculates similarity between two strips by counting shared indices
- Calls: None

### Optimize_Strip_Order
- Purpose: Reorders strips to maximize vertex reuse between consecutive strips
- Calls: Get_Strip_Similarity, Copy_Strip

### Optimize_Triangle_Order
- Purpose: Reorders triangles to maximize vertex reuse between consecutive triangles
- Calls: Get_Similarity

### Combine_Strips
- Purpose: Merges multiple strips into a single strip with minimal vertex duplication
- Calls: Get_Strip_Index_Count

### Stripify::stripify
- Purpose: Converts triangle list into optimized triangle strips
- Calls: generateTriangleList, TriangleQueue methods

## Globals
- None

## Dependencies
- stripoptimizer.h
- hashtemplate.h
- wwdebug.h
- W3D memory allocation functions (W3DNEWARRAY)
- HashTemplateClass template
- WWASSERT macro
