# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDisplay.h

## Purpose
Header file defining the W3DDisplay class, responsible for managing the game's visual display and rendering operations.

## Responsibilities
- Manages display initialization and configuration
- Handles 2D/3D rendering operations
- Controls debug display and performance statistics
- Manages video buffers and screenshots
- Handles light environments and time-of-day effects

## Key Types
- W3DDisplay (Class): Main display management class
- VideoBuffer (Class): Video buffer handling
- W3DDebugDisplay (Class): Debug display interface
- DisplayString (Class): Display text handling
- W3DAssetManager (Class): Asset management
- LightClass (Class): Light environment management
- Render2DClass (Class): 2D rendering interface
- RTS3DScene (Class): 3D scene representation
- RTS2DScene (Class): 2D scene representation
- RTS3DInterfaceScene (Class): 3D interface scene
- (anonymous enum): Debug display string types

## Key Functions
### W3DDisplay::init
- Purpose: Initialize or re-initialize the display system
- Calls: initAssets, init3DScene, init2DScene

### W3DDisplay::draw
- Purpose: Redraw the entire display
- Calls: drawFPSStats, drawDebugStats, drawCurrentDebugDisplay

### W3DDisplay::drawFPSStats
- Purpose: Draw the FPS counter on screen
- Calls: Not inferable

### W3DDisplay::updateAverageFPS
- Purpose: Calculate average FPS over last 30 frames
- Calls: Not inferable

### W3DDisplay::createLightPulse
- Purpose: Create a light pulse effect
- Calls: Not inferable

### W3DDisplay::setTimeOfDay
- Purpose: Set the time of day for lighting
- Calls: Not inferable

## Globals
- m_3DScene (RTS3DScene*): Static 3D scene representation
- m_2DScene (RTS2DScene*): Static 2D scene representation
- m_3DInterfaceScene (RTS3DInterfaceScene*): Static 3D interface scene
- m_assetManager (W3DAssetManager*): Static asset manager
- m_initialized (Byte): Initialization flag
- m_myLight (LightClass*): Array of light objects
- m_2DRender (Render2DClass*): 2D rendering interface
- m_clipRegion (IRegion2D): Clipping region
- m_isClippedEnabled (Bool): Clipping enabled flag
- m_averageFPS (Real): Average FPS counter
