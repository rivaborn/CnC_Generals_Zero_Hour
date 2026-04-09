# Generals/Code/Tools/wolSetup/WOLAPI/wolapi.h

## Purpose
This file defines COM interfaces for Westwood Online (WOL) API functionality, including chat, downloads, network utilities, and patching.

## Responsibilities
- Declares COM interfaces for WOL services (chat, downloads, network utils)
- Defines event callback interfaces
- Declares data structures for WOL entities (servers, channels, users)
- Provides GUIDs for COM objects and interfaces

## Key Types
- IRTPatcher (Class): Interface for applying runtime patches
- IChat (Class): Main chat interface for server/channel/user management
- IDownload (Class): Interface for file downloads
- INetUtil (Class): Network utility functions (ping, ladder, etc.)
- Locale (Enum): Country/region identifiers
- Server/Channel/User (Classes): Data structures for WOL entities

## Key Functions
### IRTPatcher::ApplyPatch
- Purpose: Apply a patch file to a destination path
- Calls: None visible

### IChat::RequestConnection
- Purpose: Establish connection to WOL server
- Calls: None visible

### IDownload::DownloadFile
- Purpose: Initiate file download
- Calls: None visible

### INetUtil::RequestPing
- Purpose: Ping a network host
- Calls: None visible

## Globals
- IID_IRTPatcher (GUID): Interface ID for IRTPatcher
- IID_IChat (GUID): Interface ID for IChat
- IID_IDownload (GUID): Interface ID for IDownload
- IID_INetUtil (GUID): Interface ID for INetUtil
- LIBID_WOLAPILib (GUID): Library ID for WOLAPI
- CLSID_RTPatcher (GUID): Class ID for RTPatcher
- CLSID_Chat (GUID): Class ID for Chat
- CLSID_Download (GUID): Class ID for Download
- CLSID_NetUtil (GUID): Class ID for NetUtil

## Dependencies
- windows.h, ole2.h: Windows COM headers
- rpc.h, rpcndr.h: RPC support headers
- oaidl.h, ocidl.h: COM interface definitions
- MIDL-generated stub functions for all interfaces
