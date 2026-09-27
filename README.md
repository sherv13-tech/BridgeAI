# BridgeAI

**BridgeAI v1** connects one approved Windows project folder to compatible remote AI/MCP clients without manual tunnels, port forwarding, or exposing your whole PC.

> **Free public beta.** BridgeAI is freeware: free to use, but the implementation source is privately maintained.

## Download

Open the **Releases** section of this repository.

Recommended:
- **BridgeAI-Setup-v1.exe** — normal Windows installer.

Alternative:
- **BridgeAI-v1-portable.zip** — extract it and run `BridgeAI.vbs`; no separate Node.js installation is required.

## Install

### Normal installer

1. Download `BridgeAI-Setup-v1.exe` from the latest release.
2. Double-click it.
3. Choose the local project folder BridgeAI may access.
4. Choose **Read only** or **Read + write**.
5. Open **Connections** and copy your private BridgeAI connection URL.
6. Add that URL to a supported MCP client.

The current public beta installer is unsigned. Windows may show an **Unknown Publisher** or reputation warning. Do not disable Windows security to install BridgeAI. If the installer is blocked, use the portable ZIP.

### Portable version

1. Download `BridgeAI-v1-portable.zip`.
2. Extract it to a normal local folder.
3. Double-click `BridgeAI.vbs`.
4. Complete the same workspace setup.

## What BridgeAI can access

BridgeAI is limited to the one workspace folder you approve.

Depending on your selected permission mode, BridgeAI can:
- show workspace information;
- list approved workspace folders/files;
- read UTF-8 text files;
- search text;
- create text files in **Read + write** mode;
- replace text-file contents in **Read + write** mode.

BridgeAI does **not** provide remote shell, PowerShell, CMD, arbitrary process execution, whole-PC filesystem access, remote desktop, package installation, or general-purpose remote file deletion.

## Private connection URL

Your BridgeAI connection URL is a credential. Treat it like a password.

If you believe it was exposed:
1. Open BridgeAI.
2. Go to **Settings**.
3. Rotate the connection credential.
4. Update the connection in your MCP client.

## Verify your download

Compare the downloaded file with the values in `SHA256SUMS.txt`.

Example:

```powershell
Get-FileHash .\BridgeAI-Setup-v1.exe -Algorithm SHA256
```

## License

BridgeAI v1 is distributed as **freeware** under the [BridgeAI Freeware License](LICENSE).

The official, unmodified BridgeAI binaries may be downloaded and used free of charge. The implementation source code is privately maintained and is not part of this public repository.

## Privacy and security

Please read [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) before testing.
