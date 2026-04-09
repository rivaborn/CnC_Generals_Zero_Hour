# GeneralsMD/Code/GameEngine/Include/GameClient/ShellHooks.h

## Purpose
Defines enumeration constants and function for UI interaction events in the game shell.

## Responsibilities
- Defines shell script hook event types for UI interactions
- Provides external array of hook names
- Declares function to signal UI interactions

## Key Types
- (anonymous enum) (Enum): UI interaction event types
- SHELL_SCRIPT_HOOK_MAIN_MENU_CAMPAIGN_SELECTED (Enum): Campaign menu selected event
- SHELL_SCRIPT_HOOK_MAIN_MENU_CAMPAIGN_HIGHLIGHTED (Enum): Campaign menu highlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_CAMPAIGN_UNHIGHLIGHTED (Enum): Campaign menu unhighlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_SKIRMISH_SELECTED (Enum): Skirmish menu selected event
- SHELL_SCRIPT_HOOK_MAIN_MENU_SKIRMISH_HIGHLIGHTED (Enum): Skirmish menu highlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_SKIRMISH_UNHIGHLIGHTED (Enum): Skirmish menu unhighlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_OPTIONS_SELECTED (Enum): Options menu selected event
- SHELL_SCRIPT_HOOK_MAIN_MENU_OPTIONS_HIGHLIGHTED (Enum): Options menu highlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_OPTIONS_UNHIGHLIGHTED (Enum): Options menu unhighlighted event
- SHELL_SCRIPT_HOOK_MAIN_MENU_ONLINE_SELECTED (Enum): Online menu selected event
- SHELL_SCRIPT_HOOK_MAIN_MENU_ONLINE_HIGHLIGHTED (Enum): Online menu highlighted
