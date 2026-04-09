# Generals/Code/Tools/WorldBuilder/include/FeatherOptions.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for brush feathering controls in WorldBuilder, bridging MFC dialog patterns with custom slider behavior. It exposes static methods for external tools to update feathering parameters, making it a key integration point for terrain editing workflows.

## Cross-References
### Incoming
- **WorldBuilder main UI**: Likely instantiates `FeatherOptions` and calls static methods (`setFeather`, `setRate`, `setRadius`) to update feathering during brush operations.
- **PopupSlider system**: Uses `PopupSliderOwner` interface for slider behavior, implying calls from slider UI components.

### Outgoing
- **MFC framework**: Inherits from `COptionsPanel` and `CWnd`, using MFCâs DDX/DDV system for data binding.
- **Custom slider controls**: Interacts with `WBPopupSliderButton` instances for slider UI rendering.

## Design Patterns
- **Singleton-like static access**: Uses `m_staticThis` to allow global access to the dialog instance, enabling external updates without direct object references.
- **Observer pattern**: Implements slider callbacks (`PopSliderChanged`, `PopSliderFinished`) to react to user input, decoupling UI events from business logic.
- **Model-View separation**: Internal state (`m_currentFeather`, `m_currentRadius`, `m_currentRate`) is distinct from UI controls, though tightly coupled via MFCâs DDX.
