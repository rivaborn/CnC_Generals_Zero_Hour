# Generals/Code/Tools/WorldBuilder/include/WBPopupSlider.h - Enhanced Analysis

## Architectural Role
This file defines the UI control infrastructure for WorldBuilder's popup slider, a specialized input widget for adjusting numeric values. It bridges MFC's windowing system with WorldBuilder's tooling needs, providing a reusable component for parameter tuning in the editor.

## Cross-References
### Incoming
- **WorldBuilder tool windows**: Likely call `PopupSlider::New` to spawn sliders for property editing.
- **MFC framework**: Handles message routing via `DECLARE_MESSAGE_MAP()`.

### Outgoing
- **MFC classes**: Inherits from `CButton` and `CWnd`, uses `CBrush` for rendering.
- **`PopupSliderOwner`**: Delegates slider events to implementing classes (e.g., property editors).

## Design Patterns
- **Singleton**: `gPopupSlider` ensures only one popup slider exists at a time.
- **Observer**: `PopupSliderOwner` interface decouples slider behavior from UI logic.
- **Factory Method**: `PopupSlider::New` abstracts object creation and initialization.

*Not inferable*: No clear use of Strategy or Composite patterns.
