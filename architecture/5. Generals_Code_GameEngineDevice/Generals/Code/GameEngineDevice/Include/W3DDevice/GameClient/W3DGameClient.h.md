# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGameClient.h

## Purpose
Defines the W3DGameClient class, the W3D implementation of the game interface responsible for managing drawables, GUI, and display.

## Responsibilities
- Manages game drawables and effects
- Handles GUI components (UI, windows, fonts)
- Controls display and rendering settings
- Initializes and updates game client state
- Creates input devices (keyboard, mouse)

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
- Purpose: Initializes game client resources.
- Calls: None.

### update
- Purpose: Per-frame update for the game client.
- Calls: None.

### reset
- Purpose: Resets the game client system.
- Calls: None.

### addScorch
- Purpose: Adds a scorch effect at a given position.
- Calls: None.

### createRayEffectByTemplate
- Purpose: Creates a ray effect between two points using a template.
- Calls: None.

### setTimeOfDay
- Purpose: Updates the time of day for all drawables.
- Calls: None.

### setTeamColor
- Purpose: Sets the team color (hack for demo).
- Calls: None.

### adjustLOD
- Purpose: Adjusts level of detail (hack for evaluation).
- Calls: None.
