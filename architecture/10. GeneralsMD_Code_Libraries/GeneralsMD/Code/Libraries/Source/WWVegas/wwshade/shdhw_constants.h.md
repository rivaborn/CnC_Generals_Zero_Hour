# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdhw_constants.h

## Purpose
Defines constant register indices for shader parameters in the SAGE engine's hardware shader system.

## Responsibilities
- Declares constant register IDs for generic shader parameters
- Defines lighting-related constant register indices
- Provides register IDs for ambient, diffuse, and specular lighting components

## Key Types
None

## Key Functions
None

## Globals
- `CV_CONST` (int): Generic constant register index
- `CV_LIGHT_DIRECTION_0-3` (int): Register indices for light direction vectors
- `CV_LIGHT_COLOR_0-3` (int): Register indices for light color values
- `CV_AMBIENT` (int): Register index for ambient lighting
- `CV_DIFFUSE` (int): Register index for diffuse lighting
- `CV_SPECULAR` (int): Register index for specular lighting

## Dependencies
- None (header-only file with no external dependencies)
