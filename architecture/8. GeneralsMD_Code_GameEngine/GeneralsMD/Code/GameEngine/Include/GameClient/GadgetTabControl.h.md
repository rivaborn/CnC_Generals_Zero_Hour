# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetTabControl.h

## Purpose
Header file providing helper functions for managing tab controls in the game UI.

## Responsibilities
- Defines tab control indices (background + 8 tabs)
- Provides wrapper functions for tab control properties
- Manages sub-pane creation, sizing, and visibility
- Handles tab region computation and resizing

## Key Types
- (anonymous enum): Tab control indices (background + 8 tabs)

## Key Functions
### GadgetTabControlComputeTabRegion
- Purpose: Recalculate tab positions based on user data
- Calls: Not inferable

### GadgetTabControlCreateSubPanes
- Purpose: Create/destroy windows attached to user data as panes
- Calls: Not inferable

### GadgetTabControlComputeSubPaneSize
- Purpose: Calculate dependent size for sub-panes
- Calls: Not inferable

### GadgetTabControlShowSubPane
- Purpose: Show specified sub-pane
- Calls: Not inferable

### GadgetTabControlResizeSubPanes
- Purpose: Resize panes when parent size changes
- Calls: Not inferable

### GadgetTabControlFixupSubPaneList
- Purpose: Hook up children to sub-pane array after game creation
- Calls: Not inferable

## Globals
None

## Dependencies
- GameClient/GameWindow.h
- GameWindow class methods (winSetEnabledImage, winSetEnabledColor, etc.)
