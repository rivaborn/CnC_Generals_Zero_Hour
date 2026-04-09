# Generals/Code/Tools/WorldBuilder/include/MapPreview.h

## Purpose
Header for the MapPreview class, which generates and saves a preview image of a map's height data.

## Responsibilities
- Define dimensions for map preview (128x128).
- Provide methods to generate and save preview textures.
- Convert between preview coordinates and world coordinates.
- Color interpolation based on height data.

## Key Types
- (anonymous enum) (Enum): Contains MAP_PREVIEW_HEIGHT and MAP_PREVIEW_WIDTH constants.
- MAP_PREVIEW_HEIGHT (Enum): Height dimension of preview (128).
- MAP_PREVIEW_WIDTH (Enum): Width dimension of preview (128).
- MapPreview (Class): Manages map preview generation and saving.

## Key Functions
### MapPreview()
- Purpose: Constructor for MapPreview class.
- Calls: None.

### save()
- Purpose: Saves the map preview as an image file.
- Calls: Not inferable.

### interpolateColorForHeight()
- Purpose: Interpolates color based on height value.
- Calls: None.

### mapPreviewToWorld()
- Purpose: Converts preview coordinates to world coordinates.
- Calls: None.

### buildMapPreviewTexture()
- Purpose: Builds the preview texture from height data.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- CString (assumed from user includes).
- RGBColor (assumed from user includes).
- Real (assumed from user includes).
- Bool (assumed from user includes).
- UnsignedInt (assumed from user includes).
- ICoord2D (assumed from user includes).
- Coord3D (assumed from user includes).
