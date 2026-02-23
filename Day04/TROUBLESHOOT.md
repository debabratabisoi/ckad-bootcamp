
---

## 📄 Day 4 TROUBLESHOOT.md (example content)

```markdown
# Day 4 Troubleshooting

## Issue: ConfigMap not mounted
- Fix: Verified `mountPath` matches nginx config directory (`/etc/nginx/conf.d`).

## Issue: Secret values not visible
- Fix: Used `kubectl exec` to confirm environment variables are injected.
