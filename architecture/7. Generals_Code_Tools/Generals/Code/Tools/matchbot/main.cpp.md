# Generals/Code/Tools/matchbot/main.cpp

## Purpose
Main entry point for the matchbot tool, handling configuration, logging, and game matching logic.

## Responsibilities
- Initialize logging and output devices
- Load configuration and set up signal handlers
- Spawn matching threads based on game type
- Manage log rotation for normal and paranoid logs

## Key Types
- `GeneralsMatcher` (Class): Handles Generals game matching logic
- `GeneralsClientMatcher` (Class): Handles Generals client matching logic
- `OutputDevice` (Class): Base class for output devices (file/stdout)

## Key Functions
### `main`
- Purpose: Main entry point that initializes the matchbot
- Calls: `Global.ReadFile`, `MsgManager::setAllStreams`, `MyMsgManager::setParanoidStream`, `GeneralsMatcher::connectAndLoop`, `GeneralsClientMatcher::connectAndLoop`

### `logMonitor`
- Purpose: Background thread for rotating normal log files
- Calls: `MsgManager::ReplaceAllStreams`, `rename`

### `paranoidLogMonitor`
- Purpose: Background thread for rotating paranoid log files
- Calls: `MyMsgManager::ReplaceAllStreams`, `rename`

### `Signal_Quit`
- Purpose: Signal handler for graceful shutdown
- Calls: `exit`

## Globals
- `Program_Usage` (char*): Usage message string
- `output_device` (OutputDevice*): Normal log output device
- `paranoid_output_device` (OutputDevice*): Paranoid log output device
- `s_generalsMatcher` (GeneralsMatcher*): Generals matcher instance
- `s_generalsClientMatcher` (GeneralsClientMatcher*): Client matcher instance

## Dependencies
- `<csignal>`, `<iostream>`, `<wstring.h>`, `<wdebug.h>`, `<filed.h>`, `<stdoutd.h>`, `<wstypes.h>`, `<xtime.h>`, `"global.h"`, `"generals.h"`, `"timezone.h"`, `<threadfac.h>`, `<tcp.h>`, `"mydebug.h"`
- `Global`, `MsgManager`, `MyMsgManager`, `GeneralsMatcher`, `GeneralsClientMatcher`
