# Generals/Code/Tools/Babylon/ExportDlg.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for Babylon's export tool, bridging user input with the export pipeline. It encapsulates dialog state and validation logic, serving as the primary interface for artists/designers to configure export parameters.

## Cross-References
### Incoming
- Likely called by Babylon's main tool window (not shown in cross-reference table)
- May be referenced by export pipeline initialization code

### Outgoing
- Uses MFC's CDialog framework (DoDataExchange, message handlers)
- Interfaces with TROPTIONS (export configuration struct) from expimp.h

## Design Patterns
- **MVC (Model-View-Controller)**: Dialog acts as the view/controller, with export options as the model
- **Observer**: Event handlers (OnSelchangeCombolang) react to UI changes
- **Facade**: Hides export complexity behind simple dialog interface

*Not inferable: No clear use of Strategy or Command patterns visible in header alone.*
