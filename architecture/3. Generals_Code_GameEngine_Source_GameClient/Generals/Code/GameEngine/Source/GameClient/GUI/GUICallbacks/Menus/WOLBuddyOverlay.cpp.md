# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLBuddyOverlay.cpp

## Purpose
Manages the Westwood Online (WOL) buddy overlay system, including buddy lists, chat, and right-click menus.

## Responsibilities
- Handles buddy list updates and chat messages
- Manages buddy requests (add/remove/accept/deny)
- Controls right-click context menus for buddies
- Displays notifications for buddy events
- Manages ignore lists

## Key Types
- BuddyControls (Class): Container for buddy UI controls
- (anonymous enum): Buddy window types (BUDDY_WINDOW_BUDDIES, etc.)
- (anonymous enum): Notification expiration timer

## Key Functions
### BuddyControlSystem
- Purpose: Handles buddy control messages (right-click, chat input)
- Calls: GadgetListBoxGetItemData, TheGameSpyBuddyMessageQueue->addRequest, insertChat

### WOLBuddyOverlaySystem
- Purpose: Main overlay system for buddy management
- Calls: TheGameSpyBuddyMessageQueue->addRequest, updateBuddyInfo, showNotificationBox

### WOLBuddyOverlayRCMenuSystem
- Purpose: Handles right-click menu actions (add/delete/ignore)
- Calls: RequestBuddyAdd, TheGameSpyBuddyMessageQueue->addRequest, updateBuddyInfo

### insertChat
- Purpose: Adds chat messages to the buddy chat listbox
- Calls: GadgetListBoxAddEntryText

### updateBuddyInfo
- Purpose: Refreshes buddy list and chat display
- Calls: GadgetListBoxReset, TheGameSpyInfo->getBuddyMap

## Globals
- parentID (NameKeyType): ID for main buddy overlay window
- isOverlayActive (Bool): Tracks if overlay is active
- buddyControls (BuddyControls): Contains buddy UI controls
- rcMenu (GameWindow*): Right-click menu window
- noticeLayout (WindowLayout*): Notification popup layout

## Dependencies
- GameSpy overlay systems (BuddyThread, LobbyUtils)
- UI components (WindowLayout, GadgetListBox)
- GameText for localization
- AudioEventRTS for notifications
