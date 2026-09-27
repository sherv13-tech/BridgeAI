# BridgeAI Privacy Notes

BridgeAI is designed around a local workspace boundary.

## Local workspace

Your selected workspace remains on your PC. BridgeAI does not continuously synchronize or upload your whole project.

When a remote MCP client explicitly calls a BridgeAI tool, the tool request and its result travel through the BridgeAI relay so the remote client can communicate with your local agent. Requested file content can therefore pass through the relay **in transit** for that tool call.

## Local activity

The dashboard activity log is stored locally. It records tool metadata such as action, relative target path, outcome, duration, and byte counts. It is not intended to store file contents.

The animated bridge uses short-lived in-memory activity events on your local agent. Those events are not added to the developer installation registry.

## Shared relay control plane

For operating the free tester relay, BridgeAI keeps a small pseudonymous installation record that can include:
- random installation ID
- derived connector identifier
- BridgeAI version
- first-seen / last-connected timestamps
- revoked/allowed state

BridgeAI's application-level control plane does not intentionally persist Windows usernames, machine names, workspace paths, workspace names, file names, source files, private MCP URLs, or local activity logs.

The relay runs on Cloudflare infrastructure. Like other Internet services, the infrastructure provider may process ordinary network metadata such as IP addresses while delivering the service. BridgeAI does not claim network-level anonymity or "untraceability."

## Private connection URL

Your BridgeAI connection URL contains a capability credential. Treat it like a password. Do not post it publicly or include it in screenshots. Rotate it from Settings if you believe it was exposed.
