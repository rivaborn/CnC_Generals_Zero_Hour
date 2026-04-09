# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGameClient.h

## Purpose
Defines the W3DGameClient class, the W3D implementation of the game interface responsible for managing drawables, GUI, and display systems.

## Responsibilities
- Manages game drawables and effects
- Handles GUI and display creation
- Controls time-of-day and team colors
- Manages input devices (keyboard/mouse)
- Initializes and updates game state

## Key Types
- **ThingTemplate (Class)**: Not inferable.
- **W3DGameClient (Class)**: Main game client interface for W3D rendering.

## Key Functions
### W3DGameClient()
- Purpose: Constructor for W3DGameClient.
- Calls: None.

### ~W3DGameClient()
- Purpose: Destructor for W3DGameClient.
- Calls: None.

### friend_createDrawable
- Purpose: Creates a drawable from a ThingTemplate.
- Calls: None.

### init
- Purpose: Initializes game resources.
- Calls: None.

### update
- Purpose: Per-frame game update.
- Calls: None.

### reset
- Purpose: Resets the game system.
- Calls: None.

### addScorch
- Purpose: Adds a scorch mark effect.
- Calls: None.

### createRayEffectByTemplate
- Purpose: Creates a ray effect between two points.
- Calls: None.

### setTimeOfDay
- Purpose: Updates time-of-day for all drawables.
- Calls: None.

### setTeamColor
- Purpose: Sets team color (hack for demo).
- Calls: None.

### adjustLOD
- Purpose: Adjusts level-of-detail (hack for evaluation).
- Calls: None.

### notifyTerrainObjectMoved
- Purpose: Notifies
