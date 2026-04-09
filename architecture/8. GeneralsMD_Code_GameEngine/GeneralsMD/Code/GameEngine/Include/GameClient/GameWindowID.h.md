# GeneralsMD/Code/GameEngine/Include/GameClient/GameWindowID.h

## Purpose
Defines unique identifiers for game windows to enable message passing between UI components.

## Responsibilities
- Defines window ID constants for sidebar elements
- Provides invalid window ID marker
- Enables cross-component communication via window IDs

## Key Types
None

## Key Functions
None

## Globals
- GWID_INVALID (int): Invalid window ID marker
- GWID_SIDEBAR (int): Main sidebar window ID
- GWID_SIDEBAR_1-12 (int): Individual sidebar slot IDs
- GWID_SIDEBAR_TAB_1-4 (int): Sidebar tab IDs
- GWID_SIDEBAR_RADAR (int): Sidebar radar window ID

## Dependencies
- None (header-only file)
