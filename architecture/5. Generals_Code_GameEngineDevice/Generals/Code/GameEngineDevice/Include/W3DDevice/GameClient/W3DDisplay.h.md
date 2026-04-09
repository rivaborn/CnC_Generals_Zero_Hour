# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDisplay.h

## Purpose
Header defining the W3DDisplay class, the main display interface for the W3D rendering system in Command & Conquer Generals.

## Responsibilities
- Manages 2D/3D rendering and display initialization
- Handles screen drawing operations (lines, rectangles, images)
- Controls display modes, gamma, and video settings
- Provides debug statistics and asset management
- Manages light environments and scene rendering

## Key Types
- **W3DDisplay (Class)**: Main display interface for W3D rendering
- **VideoBuffer (Class)**: Video buffer management
- **W3DDebugDisplay (Class)**: Debug display interface
- **DisplayString (Class)**: Display string handling
- **W3DAssetManager (Class)**: Asset management
- **LightClass (Class)**: Light environment management
- **Render2DClass (Class)**: 2D rendering interface
- **RTS3DScene (Class)**: 3D scene representation
- **RTS2DScene (Class)**: 2D scene representation
- **RTS3DInterfaceScene (Class)**: 3D interface scene
- **DisplayStringCount (Enum)**: Debug display string types

## Key Functions
### W3DDisplay::init
- Purpose: Initialize or re-initialize the display system
- Calls: initAssets, init3DScene, init2DScene

### W3DDisplay::draw
- Purpose: Redraw the entire display
- Calls: drawFPSStats, drawDebugStats, drawCurrentDebugDisplay

### W3DDisplay::drawLine
- Purpose: Draw a line on the display in screen coordinates
- Calls: None (direct rendering call)

### W3DDisplay::drawImage
- Purpose: Draw an image within specified screen coordinates
- Calls: None (direct rendering call)

### W3DDisplay::setClipRegion
- Purpose: Set clip rectangle for 2D draw operations
- Calls: None

## Globals
- **m_3DScene (RTS3DScene*)**: Static 3D scene representation
- **m_2DScene (RTS2DScene*)**: Static 2D scene representation
- **m_3DInterfaceScene (RTS3DInterfaceScene*)**: Static 3D interface scene
- **m_assetManager (W3DAssetManager*)**: Static asset manager
- **m_displayStrings (DisplayString*)**: Array of debug display strings
- **m_benchmarkDisplayString (DisplayString*)**: Benchmark display string
- **m_nativeDebugDisplay (W3DDebugDisplay*)**: W3D-specific debug display interface

## Dependencies
- **GameClient/Display.h**: Base Display class
