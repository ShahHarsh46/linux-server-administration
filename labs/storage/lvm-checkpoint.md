# LVM Lab — Current Checkpoint

**Status:** In progress  
**Purpose:** Record the observed LVM state before continuing storage administration practice.

## Latest recorded observations

Commands used:

```bash
pvs
vgs
```

Recorded output:

```text
PV         VG   Fmt  Attr  PSize   PFree
/dev/vda3  rhel lvm2 a--   <39.00g 20.00g

VG   #PV #LV #SN Attr   VSize   VFree
rhel   1   2   0 wz--n- <39.00g 20.00g
```

## What this confirms

- `/dev/vda3` is registered as an LVM physical volume.
- The physical volume belongs to the `rhel` volume group.
- The volume group contains one physical volume and two logical volumes.
- Approximately 20 GiB is free in the volume group at this checkpoint.

## Next verification

Before making changes, inspect the current layout:

```bash
lsblk -f
pvs
vgs
lvs -a -o +devices
findmnt
df -hT
```

Compare the outputs and identify which logical volumes and filesystems exist. Do not assume device names or sizes are unchanged between lab sessions.

## Safety

LVM and partition operations can make data inaccessible if applied to the wrong device. Confirm the target disk and take a VM snapshot before destructive changes. Do not run resize, format, or partition commands until the target and intended result are clear.

## Documentation status

This file records a checkpoint only. The full LVM procedure, filesystem creation, mount configuration, resizing, and final verification will be documented after those tasks are completed.
