# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3dtrig.h

## Purpose
Defines trigger IDs for debugging features in the WW3D rendering library.

## Responsibilities
- Declares debug trigger constants for render stats, surface cache stats, and process stats.
- Provides IDs for external trigger handlers to monitor and activate debug features.
- Used by WWDebug library to check for debugging triggers.

## Key Types
- (anonymous enum) (Enum): Contains WW3D debug trigger IDs.
- WW3D_TRIGGER_RENDER_STATS (Enum): ID for displaying render stats in debug window.
- WW3D_TRIGGER_SURFACE_CACHE_STATS (Enum): ID for displaying surface cache info.
- WW3D_TRIGGER_PROCESS_STATS (Enum): ID for rendering stats of the last frame only.

## Key Functions
None.

## Globals
None.

## Dependencies
- None (header-only file).
