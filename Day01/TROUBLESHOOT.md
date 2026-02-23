
---

## 📄 Day 1 TROUBLESHOOT.md (example content)

```markdown
# Day 1 Troubleshooting

## Issue: Docker not found in PATH
- Fix: Added `C:\Program Files\Docker\Docker\resources\bin` to PATH via PowerShell.

## Issue: Docker Engine not running
- Fix: Waited for Docker Desktop to fully start, verified with `docker ps`.

## Issue: Minikube start failed
- Fix: Restarted Docker service, then ran `minikube start --driver=docker`.