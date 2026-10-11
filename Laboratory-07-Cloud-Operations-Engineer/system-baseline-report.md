# System Baseline Report

## Host System Baseline

Before deploying the client website, the Linux host was checked to determine its current resource condition.

### Memory Check

Command executed:

```bash
free -h
```

**Total RAM available:** `[ENTER THE EXACT TOTAL RAM SHOWN BY KILLERCODA]`

The memory check provides a baseline for determining whether the host has enough available RAM to support the application and additional traffic.

![Memory Check](screenshots/memory-check.png)

### Disk Check

Command executed:

```bash
df -h /
```

**Total storage capacity of the root (/) file system:** `[ENTER THE EXACT SIZE SHOWN BY KILLERCODA]`

Checking disk space before a massive traffic surge is critical because insufficient storage can prevent applications from writing logs or temporary data and can eventually cause services to fail.

![Disk Check](screenshots/disk-check.png)

### CPU and Process Check

Command executed:

```bash
top
```

The `top` command was used to observe active processes and changing CPU and memory utilization. The command was allowed to run for several seconds before exiting with `q`.

![CPU and Processes](screenshots/top.png)

## Baseline Summary

| Resource | Observed Value |
|---|---|
| Total RAM | `[ENTER VALUE FROM free -h]` |
| Root (/) Storage | `[ENTER VALUE FROM df -h /]` |
| CPU/Processes | Observed using `top` |

## Conclusion

The host baseline provides a reference point for comparing system health before and during application activity.
