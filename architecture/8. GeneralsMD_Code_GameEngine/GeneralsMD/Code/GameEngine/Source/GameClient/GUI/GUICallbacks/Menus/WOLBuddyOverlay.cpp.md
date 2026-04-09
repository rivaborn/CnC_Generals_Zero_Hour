# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLBuddyOverlay.cpp

## Purpose
Manages the Westwood Online (WOL) buddy overlay UI, including buddy lists, chat, and right-click menus.

## Responsibilities
- Handles buddy list updates and chat messages
- Manages buddy requests (add/remove/accept/deny)
- Controls right-click context menus for buddies
- Displays notifications for buddy events
- Manages ignore lists

## Key Types
- BuddyControls (Class): Holds references to buddy list and chat UI controls
- (anonymous enum): Defines buddy window types (BUDDY_WINDOW_BUDDIES, etc.)
- NOTIFICATION_EXPIRES (Enum): Notification timeout constant

## Key Functions
### BuddyControlSystem
- Purpose: Handles buddy control messages (right-clicks, chat input)
- Calls: GadgetListBoxGetItemData, TheGameSpyBuddyMessageQueue->addRequest, insertChat

### WOLBuddyOverlaySystem
- Purpose: Main overlay system handling buddy list updates and chat
- Calls: TheGameSpyInfo->getBuddyMap, updateBuddyInfo, insertChat

### WOLBuddyOverlayRCMenuSystem
- Purpose: Handles right-click menu actions (add/delete/ignore buddies)
- Calls: TheGameSpyBuddyMessageQueue->addRequest, updateBuddyInfo, refreshIgnoreList

### showNotificationBox
- Purpose: Displays buddy notifications
- Calls: TheWindowManager->winCreateLayout, TheWindowManager->winSetLoneWindow

## Globals
- parentID (NameKeyType): ID for main overlay window
- isOverlayActive (Bool): Tracks overlay visibility state
- buddyControls (BuddyControls): Manages buddy UI controls
- rcMenu (GameWindow*): Right-click menu window pointer
- noticeLayout (WindowLayout*): Notification popup layout

## Dependencies
- GameSpy overlay systems (BuddyThread, LobbyUtils)
- UI components (WindowLayout, GadgetListBox)
- Game text and audio systems
- Player/Profile management systems
