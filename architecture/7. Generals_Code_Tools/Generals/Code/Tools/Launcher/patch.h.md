# Generals/Code/Tools/Launcher/patch.h

## Purpose
Header file declaring the patch application function for the game launcher.

## Responsibilities
- Declares the `Apply_Patch` function interface
- Includes necessary headers for patching functionality
- Defines the patch header guard

## Key Types
- None

## Key Functions
### Apply_Patch
- Purpose: Applies a patch file to the game configuration
- Calls: Not inferable (implementation in separate file)

## Globals
- None

## Dependencies
- `winblows.h`: Windows API wrappers
- `dialog.h`: Dialog box utilities
- `resource.h`: Resource IDs
- `wdebug.h`: Debugging utilities
- `process.h`: Process management
- `ConfigFile`: Class for configuration file handling
