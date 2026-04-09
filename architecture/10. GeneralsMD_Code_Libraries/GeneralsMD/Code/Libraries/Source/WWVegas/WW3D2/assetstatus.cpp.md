# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/assetstatus.cpp

## Purpose
Manages tracking and reporting of asset loading status (load-on-demand and missing assets) in the SAGE engine.

## Responsibilities
- Tracks load-on-demand and missing assets via hash tables
- Generates a report file on destruction (debug builds only)
- Provides methods to report different asset types
- Case-insensitive asset name handling

## Key Types
- **AssetStatusClass (Class)**: Singleton for asset status tracking and reporting
- **ReportCategoryNames (const char*)**: Array of category name strings

## Key Functions
### `Add_To_Report`
- Purpose: Records an asset name under a specific report category
- Calls: `HashTemplate::Get`, `HashTemplate::Set_Value`, `_strlwr`

### `Report_Load_On_Demand_RObj/Report_Load_On_Demand_HAnim/Report_Load_On_Demand_HTree`
- Purpose: Reports load-on-demand assets if enabled
- Calls: `Add_To_Report`

### `Report_Missing_RObj/Report_Missing_HAnim/Report_Missing_HTree`
- Purpose: Reports missing assets
- Calls: `Add_To_Report`

## Globals
- **ReportCategoryNames (const char*)**: Category name strings for reporting
- **AssetStatusClass::Instance (AssetStatusClass)**: Singleton instance

## Dependencies
- `assetstatus.h`, `hashtemplate.h`, `wwstring.h`, `rawfile.h`
- `HashTemplate`, `StringClass`, `RawFileClass`
