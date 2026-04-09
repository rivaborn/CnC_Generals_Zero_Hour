# Generals/Code/Tools/WorldBuilder/include/DrawObject.h

## Purpose
Defines the `DrawObject` class for rendering 3D feedback in the WorldBuilder tool.

## Responsibilities
- Manages vertex/index buffers for rendering feedback (brush, mesh, ramp, waypoints).
- Handles static feedback state (brush width, square/round feedback).
- Provides methods to update and render different types of feedback.
- Implements `RenderObjClass` interface for collision and rendering.

## Key Types
- **DrawObject (Class)**: Base class for rendering feedback objects.
- **MeshClass (Class)**: Reference to W3D mesh model.
- **PolygonTrigger (Class)**: Reference to polygon trigger.
- **WaterRenderObjClass (Class)**: Reference to water rendering object.
- **(anonymous enum) (Enum)**: Defines constants (`MAX_RADIUS`, `NUM_FEEDBACK_VERTEX`, `NUM_FEEDBACK_INDEX`).

## Key Functions
### `BuildRectFromSegmentAndWidth`
- Purpose: Constructs a rectangular prism from a segment and width.
- Calls: None visible.

### `DrawObject::Render`
- Purpose: Renders the feedback object.
- Calls: `updateFeedbackVB`, `updateMeshVB`, `updateRampVB`, `updateWaypointVB`, `updateForWater`, `updateBoundaryVB`, `updateAmbientSoundVB`.

### `DrawObject::Cast_Ray`
- Purpose: Tests ray collision with the object.
- Calls: Not inferable.

## Globals
- **m_squareFeedback (Bool)**: Controls square/round brush feedback.
- **m_brushWidth (Int)**: Width of brush feedback.
- **m_brushFeatherWidth (Int)**: Width of brush feathered feedback.
- **m_toolWantsFeedback (Bool)**: Enables/disables brush feedback.
- **m_disableFeedback (Bool)**: Globally dis
