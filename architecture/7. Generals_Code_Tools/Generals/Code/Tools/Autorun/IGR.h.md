# Generals/Code/Tools/Autorun/IGR.h

## Purpose
Defines a class for accessing Westwood Online (WOL) registry settings related to auto-login, nick storage, and registry app execution.

## Responsibilities
- Read/write WOL registry options
- Provide accessors for specific option flags
- Manage option validity state

## Key Types
- IGROptionsType (typedef): unsigned int for option bitflags
- IGROptionsClass (class): Wraps WOL registry option access

## Key Functions
### IGROptionsClass::Init
- Purpose: Reads options from registry
- Calls: Not inferable

### IGROptionsClass::Is_Auto_Login_Allowed
- Purpose: Checks if auto-login is permitted
- Calls: Not inferable

### IGROptionsClass::Is_Storing_Nicks_Allowed
- Purpose: Checks if storing nicks is permitted
- Calls: Not inferable

### IGROptionsClass::Is_Running_Reg_App_Allowed
- Purpose: Checks if running registry app is permitted
- Calls: Not inferable

### IGROptionsClass::Set_Options
- Purpose: Writes options to registry
- Calls: Not inferable

## Globals
- OnlineOptions (IGROptionsClass*): Global instance for WOL options

## Dependencies
- Windows registry constants (WOLAPI_REG_KEY_*)
- Option bitflag defines (IGR_NO_AUTO_LOGIN, etc.)
