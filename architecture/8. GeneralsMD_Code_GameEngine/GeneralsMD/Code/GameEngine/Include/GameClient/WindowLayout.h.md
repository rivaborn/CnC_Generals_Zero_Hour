# GeneralsMD/Code/GameEngine/Include/GameClient/WindowLayout.h

## Purpose
Defines the `WindowLayout` class for managing UI window layouts loaded from `.wnd` files.

## Responsibilities
- Load and manage windows from `.wnd` files
- Control visibility and ordering of windows
- Provide callbacks for initialization, update, and shutdown
- Maintain a list of windows in the layout

## Key Types
- **WindowLayout (Class)**: Manages a collection of windows for a UI layout.
- **WindowLayoutInitFunc (typedef)**: Callback for layout initialization.
- **WindowLayoutUpdateFunc (typedef)**: Callback for layout updates.
- **WindowLayoutShutdownFunc (typedef)**: Callback for layout shutdown.

## Key Functions
### `load`
- Purpose: Loads windows from a `.wnd` file.
- Calls: Not inferable.

### `hide`
- Purpose: Hides or un-hides all windows in the layout.
- Calls: Not inferable.

### `runInit`
- Purpose: Executes the initialization callback if set.
- Calls: `m_init(this, userData)`

### `runUpdate`
- Purpose: Executes the update callback if set.
- Calls: `m_update(this, userData)`

### `runShutdown`
- Purpose: Executes the shutdown callback if set.
- Calls: `m_shutdown(this, userData)`

### `addWindow`
- Purpose: Adds a window to the layout.
- Calls: Not inferable.

### `removeWindow`
- Purpose: Removes a window from the layout.
- Calls: Not inferable.

### `findWindow`
- Purpose: Finds a window in the layout.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/GameMemory.h`
- `GameClient/GameWindow.h`
- `GameWindow` class (forward
