# Day 6 Troubleshooting

## Issue: StatefulSet pods not starting
- Cause: Missing or incorrect environment variable for MySQL root password.
- Fix: Added `MYSQL_ROOT_PASSWORD` env variable in the StatefulSet manifest.

## Issue: PVCs not binding for StatefulSet
- Cause: No matching PersistentVolume available.
- Fix: Verified `volumeClaimTemplates` in StatefulSet and created PVs with matching size and accessModes.

## Issue: Headless Service not resolving pod DNS
- Cause: Service selector labels didn’t match StatefulSet pod labels.
- Fix: Ensured both Service and StatefulSet use `app: mysql` label consistently.

## Issue: Lens not showing StatefulSet pods in order
- Cause: Misunderstanding of how StatefulSets create pods sequentially.
- Fix: Waited for pods to initialize one by one (`mysql-0`, then `mysql-1`, then `mysql-2`) before checking Lens.

## Issue: Pod logs showing MySQL initialization errors
- Cause: PVC mount path didn’t match MySQL’s expected data directory.
- Fix: Corrected `mountPath` to `/var/lib/mysql` in the StatefulSet manifest.
