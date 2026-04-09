# Generals/Code/Tools/mangler/wlib/mboxd.h

## Purpose
Defines a debug output device that displays messages in a Windows message box.

## Responsibilities
- Inherits from `OutputDevice` to provide debug output.
- Displays debug strings in a Windows message box.
- Manages memory allocation/deallocation for message strings.

## Key Types
- **MboxD (Class)**: Debug output device that shows messages in a Windows message box.

## Key Functions
### MboxD::print
- Purpose: Displays the input string in a Windows message box.
- Calls: `new`, `memset`, `memcpy`, `MessageBox`, `delete[]`.

## Globals
- None

## Dependencies
- `odevice.h` (for `OutputDevice` base class)
- Windows API (`MessageBox`)
