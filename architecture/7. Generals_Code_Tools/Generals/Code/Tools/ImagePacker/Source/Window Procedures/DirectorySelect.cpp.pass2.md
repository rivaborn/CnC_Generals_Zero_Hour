# Generals/Code/Tools/ImagePacker/Source/Window Procedures/DirectorySelect.cpp - Enhanced Analysis

## Architectural Role
This file implements the directory selection UI for the ImagePacker tool, bridging the tool's core functionality with Windows dialog management. It handles user-driven file system navigation, which is critical for the tool's primary purpose of packing image assets.

## Cross-References
### Incoming
- Called by the main ImagePacker window procedure when the "Add Directory" button is clicked (not shown in file)
- Likely invoked from the main tool's menu system for directory selection

### Outgoing
- Interacts with Windows API for dialog management (DialogBox, SendDlgItemMessage)
- Uses Windows file system APIs (GetCurrentDirectory, SetCurrentDirectory)
- Accesses TheImagePacker global for main window handle

## Design Patterns
- **Dialog Controller**: The DirectorySelectProc function acts as a controller for the directory selection dialog, handling all messages and coordinating between UI elements and file system operations
- **State Management**: Maintains directory state through the startDir global and current directory tracking
- **Event-Driven Architecture**: Follows Windows message loop pattern for UI event handling

Rules followed. Analysis limited to 400 tokens.
