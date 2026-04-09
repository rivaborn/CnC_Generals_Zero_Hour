# Generals/Code/Tools/WorldBuilder/include/propedit.h

## Purpose
Defines the `PropEdit` dialog class for editing properties in the WorldBuilder tool.

## Responsibilities
- Manages property editing UI for key-value pairs
- Validates input data types and values
- Handles UI events for property modification
- Supports different data types (bool, string, etc.)

## Key Types
- **PropEdit (Class)**: Dialog for editing dictionary properties
- **(anonymous enum) (Enum)**: Contains `IDD` constant for dialog ID
- **IDD (Enum)**: Dialog resource identifier

## Key Functions
### PropEdit::validate
- Purpose: Validates the current property value against its type
- Calls: Not inferable

### PropEdit::OnChangeKeyname
- Purpose: Handles key name change events
- Calls: Not inferable

### PropEdit::OnChangeValue
- Purpose: Handles value change events
- Calls: Not inferable

### PropEdit::OnInitDialog
- Purpose: Initializes the dialog UI
- Calls: Not inferable

### PropEdit::OnPropbool
- Purpose: Handles boolean property editing
- Calls: Not inferable

## Globals
- **m_key (AsciiString*)**: Stores the property key
- **m_type (Dict::DataType*)**: Stores the property data type
- **m_value (AsciiString*)**: Stores the property value
- **m_valueOnly (Bool)**: Flag for value-only editing mode
- **m_updating (int)**: Tracks UI update state

## Dependencies
- `CDialog`, `CWnd` (MFC classes)
- `AsciiString`, `Dict::DataType` (custom types)
- `CDataExchange` (MFC DDX/DDV support)
- `DECLARE_MESSAGE_MAP()` (MFC macro)
