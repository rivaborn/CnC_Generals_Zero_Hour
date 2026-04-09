# GeneralsMD/Code/GameEngine/Include/GameClient/Gadget.h

## Purpose
Header file defining UI gadget controls for the Command & Conquer Generals game engine.

## Responsibilities
- Defines gadget types, message enums, and data structures
- Declares gadget input/system message handlers
- Provides constants for UI element dimensions
- Contains forward declarations for UI components

## Key Types
- GadgetGameMessage (Enum): UI event message types
- GWS_PUSH_BUTTON (Enum): Window style flags for different gadget types
- SliderData (Struct): Data for slider controls
- ListboxData (Struct): Data for listbox controls
- EntryData (Struct): Data for text entry fields
- PushButtonData (Struct): Data for push buttons
- TabControlData (Struct): Data for tab controls

## Key Functions
### GadgetPushButtonSystem
- Purpose: Handles system messages for push buttons
- Calls: Not inferable

### GadgetListBoxInput
- Purpose: Handles input messages for list boxes
- Calls: Not inferable

### InitializeEntryGadget
- Purpose: Initializes text entry gadget system
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameClient/GameWindow.h
- GameClient/Image.h
- WindowMsgHandledType (external type)
- DisplayString (external type)
- Color (external type)
- Image (external type)
