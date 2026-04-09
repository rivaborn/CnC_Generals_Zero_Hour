# Generals/Code/Tools/WW3D/max2w3d/logdlg.cpp - Enhanced Analysis

## Architectural Role
This file implements a threaded logging dialog for the W3D export tool, bridging the export process with user feedback. It runs in a separate thread to avoid blocking the main export workflow while providing real-time progress updates.

## Cross-References
### Incoming
- **w3dexp.cpp**: Likely calls `LogDataDialogClass::printf`/`updatebar` during export to log progress
- **max2w3d.exe**: Main tool entry point probably instantiates `LogDataDialogClass`

### Outgoing
- **Windows API**: Uses `SendMessage` for RichEdit control updates, `DialogBoxParam` for UI creation
- **util.h**: May use utility functions for string formatting or path handling

## Design Patterns
- **Active Object**: Uses a dedicated thread (`_logdata_thread_function`) to decouple logging UI from export logic
- **Facade**: `LogDataDialogClass` abstracts Windows dialog complexity behind simple methods like `printf`
- **Observer (light)**: Progress updates push to UI via `updatebar`, though not a full observer pattern

*Not inferable*: No clear use of Strategy, Factory, or other patterns in this file.
