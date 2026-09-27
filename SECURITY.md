# BridgeAI Security

## Approved workspace only

BridgeAI is designed to limit file operations to the one workspace folder selected by the user.

BridgeAI rejects or contains common path-escape cases including:
- parent-directory traversal;
- absolute paths;
- UNC/network paths;
- Windows device namespaces;
- alternate data-stream syntax;
- NUL bytes;
- resolved symlink/junction escapes outside the approved root.

## Restricted remote capability

BridgeAI v1 does not provide a remote shell, arbitrary process execution, whole-PC access, remote desktop, package installation, or general-purpose remote file deletion.

## Private connection credential

Your private BridgeAI MCP URL is a credential. Do not post it publicly or include it in screenshots.

If it is exposed:
1. Open BridgeAI.
2. Go to **Settings**.
3. Rotate the connection credential.
4. Replace the old connection URL in your MCP client.

## Service availability

The BridgeAI service operator may temporarily suspend relay access for maintenance, abuse prevention, capacity management, or security reasons. These service controls do not provide general remote-control access to a user's PC.

## Unsigned beta installer

The current public beta installer may be unsigned. A Windows reputation warning does not by itself prove that a file is malicious, but only download BridgeAI from the official release page and verify the published SHA-256 checksum.

Do not disable Windows security just to install BridgeAI.
