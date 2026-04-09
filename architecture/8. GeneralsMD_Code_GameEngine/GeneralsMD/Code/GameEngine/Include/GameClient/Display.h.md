# GeneralsMD/Code/GameEngine/Include/GameClient/Display.h

## Purpose
Defines the Display class, a subsystem interface for graphics rendering and display management in the game engine.

## Responsibilities
- Manages display attributes (resolution, bit depth, windowed mode)
- Handles view management and rendering
- Provides 2D drawing primitives (lines, rectangles, images)
- Controls video playback and cinematic text
- Manages shroud/fog-of-war rendering

## Key Types
- **Display (Class)**: Main graphics display interface
- **ShroudLevel (Struct)**: Tracks shroud/fog-of-war state
- **DrawImageMode (Enum)**: Image rendering modes (solid, grayscale, alpha, additive)
- **DisplaySettings (Struct)**: Stores display resolution and mode settings
- **DebugDisplayCallback (Class)**: Callback interface for debug display updates

## Key Functions
### drawViews
- Purpose: Render all attached views
- Calls: Not inferable

### draw
- Purpose: Redraw the entire display
- Calls: Not inferable

### setDebugDisplayCallback
- Purpose: Register a debug display update callback
- Calls: Not inferable

### playLogoMovie
- Purpose: Play a logo movie with timing requirements
- Calls: Not inferable

## Globals
- **TheDisplay (Display*)**: Singleton instance of the Display class
- **StatDebugDisplay (Function)**: Debug display statistics function

## Dependencies
- View.h, Color.h, GameFont.h
- SubsystemInterface (base class)
- External classes: VideoBuffer, VideoStreamInterface, DebugDisplayInterface, Radar, Image, DisplayString
