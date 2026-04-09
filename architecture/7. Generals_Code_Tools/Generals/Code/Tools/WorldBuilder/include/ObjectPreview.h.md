# Generals/Code/Tools/WorldBuilder/include/ObjectPreview.h

## Purpose
Header for the ObjectPreview class, which handles rendering previews of game objects in the WorldBuilder tool.

## Responsibilities
- Rendering object previews in a window
- Managing texture drawing for previews
- Storing and updating the current object template

## Key Types
- **ThingTemplate (Class)**: Reference to the object template being previewed
- **ObjectPreview (Class)**: Window class for displaying object previews

## Key Functions
### ObjectPreview()
- Purpose: Default constructor for ObjectPreview.
- Calls: None

### ~ObjectPreview()
- Purpose: Destructor for ObjectPreview.
- Calls: None

### SetThingTemplate()
- Purpose: Sets the ThingTemplate to preview.
- Calls: None

### OnPaint()
- Purpose: Handles window painting, likely calls DrawMyTexture.
- Calls: Not inferable (implementation not shown)

### DrawMyTexture()
- Purpose: Renders texture data to the preview window.
- Calls: None

## Globals
- **m_tTempl (const ThingTemplate*)**: Stores the current object template for preview.

## Dependencies
- `lib/BaseType.h` (for Int, UnsignedByte types)
- MFC classes (CWnd, CDC, afx_msg)
- `ThingTemplate` class (forward-declared)
