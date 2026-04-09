# Generals/Code/Libraries/Source/WWVegas/WWLib/Surface.h

## Purpose
Abstract interface class for graphic surfaces, defining core rendering operations.

## Responsibilities
- Declares virtual methods for blitting, filling, drawing primitives
- Provides pixel access and surface metadata queries
- Supports surface locking/unlocking for direct memory access
- Maintains logical dimensions (width/height)

## Key Types
- **Surface (Class)**: Abstract base class for graphic surfaces

## Key Functions
### Surface::Blit_From
- Purpose: Copies regions between surfaces with optional transparency
- Calls: None (pure virtual)

### Surface::Fill_Rect
- Purpose: Fills rectangular regions with a color
- Calls: None (pure virtual)

### Surface::Draw_Line
- Purpose: Draws lines between points
- Calls: None (pure virtual)

### Surface::Lock/Unlock
- Purpose: Manages direct access to video memory
- Calls: None (pure virtual)

### Surface::Is_Direct_Draw
- Purpose: Identifies DirectDraw surfaces (RTTI workaround)
- Calls: None

## Globals
- None

## Dependencies
- `Point.h`, `TRect.h`
- `Point2D`, `Rect` types
