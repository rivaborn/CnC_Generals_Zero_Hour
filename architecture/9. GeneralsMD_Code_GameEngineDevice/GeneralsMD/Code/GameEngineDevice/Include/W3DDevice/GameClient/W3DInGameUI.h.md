# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DInGameUI.h

## Purpose
Header for the W3D implementation of the in-game user interface, managing user interaction and feedback during gameplay.

## Responsibilities
- Rendering in-game UI elements
- Handling selection regions and movement/attack hints
- Managing building placement visuals
- Updating UI state per frame
- Creating W3D-specific views

## Key Types
- **HAnimClass (Class)**: Not inferable.
- **W3DInGameUI (Class)**: Singleton class for W3D in-game UI rendering and interaction.

## Key Functions
### W3DInGameUI()
- Purpose: Constructor for W3DInGameUI.
- Calls: None.

### ~W3DInGameUI()
- Purpose: Destructor for W3DInGameUI.
- Calls: None.

### init()
- Purpose: Initialize the in-game user interface.
- Calls: None.

### update()
- Purpose: Update the UI by calling preDraw(), draw(), and postDraw().
- Calls: None.

### reset()
- Purpose: Reset the UI state.
- Calls: None.

### draw()
- Purpose: Render the in-game user interface.
- Calls: None.

### createView()
- Purpose: Factory method for creating W3D views.
- Calls: None.

### drawSelectionRegion()
- Purpose: Draw the selection region on screen.
- Calls: None.

### drawMoveHints(View *view)
- Purpose: Draw move hint visual feedback.
- Calls: None.

### drawAttackHints(View *view)
- Purpose: Draw attack hint visual feedback.
- Calls: None.

### drawPlaceAngle(View *view)
- Purpose: Draw place building angle if needed.
- Calls: None.

## Globals
- **m_moveHintRenderObj
