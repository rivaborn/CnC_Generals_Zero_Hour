# Generals/Code/Tools/Babylon/excel8.cpp

## Purpose
This file contains COM wrapper classes for Excel 8.0 automation, providing C++ interfaces to Excel objects like Workbooks, Application, Range, and formatting elements.

## Responsibilities
- Wraps Excel COM interfaces for workbook operations
- Provides access to Excel application properties and methods
- Handles range manipulation and formatting (borders, interior)
- Exposes Excel's calculation and evaluation capabilities
- Manages workbook opening/closing and sheet operations

## Key Types
- `Workbooks` (Class): Excel workbook collection interface
- `_Application` (Class): Excel application object wrapper
- `Range` (Class): Excel cell/range manipulation interface
- `Border` (Class): Cell border formatting
- `Borders` (Class): Collection of border objects
- `Interior` (Class): Cell interior formatting

## Key Functions
### `Workbooks::Open`
- Purpose: Opens an Excel workbook file
- Calls: `InvokeHelper` with DISPATCH_METHOD

### `_Application::GetRange`
- Purpose: Retrieves a range object from cell references
- Calls: `InvokeHelper` with DISPATCH_PROPERTYGET

### `Range::GetNumberFormat`
- Purpose: Gets the number format of a range
- Calls: `InvokeHelper` with DISPATCH_PROPERTYGET

## Globals
- `THIS_FILE` (char[]): Debug file tracking variable

## Dependencies
- `stdafx.h` for precompiled headers
- COM automation interfaces (IDispatch)
- MFC classes (CString, VARIANT)
- Excel 8.0 type library (implied by method signatures)
