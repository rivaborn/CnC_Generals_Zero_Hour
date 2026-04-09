# Generals/Code/Tools/Babylon/GenerateDlg.h

## Purpose
Header file for a dialog class used in the Babylon tool for generating localized game strings.

## Responsibilities
- Defines the `CGenerateDlg` class for managing string generation options
- Handles UI interactions for file prefix, language selection, and output formats
- Manages dialog data exchange and message handling

## Key Types
- **CGenerateDlg (Class)**: Main dialog class for string generation UI
- **(anonymous enum) (Enum)**: Contains dialog resource ID
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### CGenerateDlg::OnInitDialog
- Purpose: Initializes the dialog controls
- Calls: Not inferable

### CGenerateDlg::OnSelectall
- Purpose: Handles selection of all languages
- Calls: Not inferable

### CGenerateDlg::OnInvert
- Purpose: Inverts the selection of languages
- Calls: Not inferable

### CGenerateDlg::OnChangePrefix
- Purpose: Handles changes to the file prefix
- Calls: Not inferable

### CGenerateDlg::OnNoxstr
- Purpose: Toggles XSTR format option
- Calls: Not inferable

### CGenerateDlg::OnUnicode
- Purpose: Toggles Unicode output option
- Calls: Not inferable

### CGenerateDlg::OnOK
- Purpose: Processes dialog confirmation
- Calls: Not inferable

## Globals
- **filename (char[200])**: Stores the output file prefix
- **options (GNOPTIONS)**: Holds generation options
- **langids (LangID[200])**: Array of supported language IDs
- **langindices (int[200])**: Array of language indices
- **num_langs (int)**: Number of languages selected

## Dependencies
-
