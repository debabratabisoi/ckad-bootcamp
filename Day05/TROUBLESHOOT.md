# Day 5 Troubleshooting

## Issue: PVC stuck in Pending
- Fix: Verified PV and PVC accessModes and storage size match.

## Issue: Pod not starting
- Fix: Ensured PVC was bound before applying Pod manifest.

## Issue: Data not persisting
- Fix: Confirmed mountPath matches nginx default directory (`/usr/share/nginx/html`).

## Issue: kubectl exec failed with Git Bash
- Error: `OCI runtime exec failed: exec failed: unable to start container process: exec: "C:/Program Files/Git/usr/bin/bash": no such file or directory`
- Cause: Git Bash rewrote `/bin/bash` to a Windows path that doesn’t exist inside the container.
- Fix: Used `sh` instead of `bash`:
  ```bash
  kubectl exec -it nginx-pv-pod -- sh

or ran from PowerShell/Command Prompt to avoid Git Bash path substitution.