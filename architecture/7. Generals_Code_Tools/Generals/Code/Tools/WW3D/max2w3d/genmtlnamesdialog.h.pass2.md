# Generals/Code/Tools/WW3D/max2w3d/genmtlnamesdialog.h - Enhanced Analysis

## Architectural Role
This file defines the UI layer for material naming configuration in the Max2W3d asset conversion tool, bridging between the 3DS Max plugin interface and the W3D export pipeline. It encapsulates dialog management for artist-facing material naming parameters.

## Cross-References
### Incoming
- `max2w3d.cpp` (likely calls `GenMtlNamesDialogClass` constructor and `Get_Options()`)
- 3DS Max SDK (via `Interface` parameter in constructor)
- Windows message loop (calls `Dialog_Proc()`)

### Outgoing
- Windows API (`HWND`, `WPARAM`, `LPARAM` usage)
- `ISpinnerControl` for numeric input handling
- Likely calls into `OptionsStruct` validation logic in `Ok_To_Exit()`

## Design Patterns
- **Mediator**: The dialog class mediates between UI controls and the underlying naming options
- **Facade**: Presents a simplified interface (`Get_Options()`) to the complex Windows dialog system
- **Not inferable**: No clear use of other patterns (e.g., no observable Singleton, Observer, or Factory patterns)

*Token count: 198*
