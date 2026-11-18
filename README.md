# Linux Server Administration

A hands-on Linux system administration portfolio focused on practical server operations, storage management, security, networking, service management, and troubleshooting.

> **Project status:** In progress  
> **Primary learning track:** Red Hat Enterprise Linux (RHEL) / RHCSA  
> **Environment:** Personal Linux virtual machine lab

## Purpose

This repository documents practical Linux administration work in a way that is useful for both RHCSA preparation and entry-level Linux Support / System Administrator roles.

The goal is not to collect commands. Each documented task should explain the requirement, implementation, verification, and troubleshooting approach.

## Lab environment

- Linux virtual machine used for administration practice
- Virtual disk currently observed as `/dev/vda` (40 GiB)
- LVM volume group currently observed as `rhel`
- Device names, sizes, IP addresses, and command output may differ between lab runs

## Project areas

| Area | Planned practical work | Status |
|---|---|---|
| Storage | Disk inspection, partitions, filesystems, mounts, persistent mounts | In progress |
| LVM | Physical volumes, volume groups, logical volumes, resizing | In progress |
| Users and groups | Account lifecycle, group membership, password policy | Planned |
| Permissions | Ownership, mode bits, special permissions, ACLs | Planned |
| Services | systemd service control, enablement, troubleshooting | Planned |
| Networking | Network configuration, DNS, connectivity diagnosis | Planned |
| Security | SELinux contexts and booleans, firewall rules | Planned |
| Package management | RPM/DNF, repositories, package troubleshooting | Planned |
| Scheduling | Cron and scheduled task verification | Planned |
| Backup and recovery | Archive-based backups and restore validation | Planned |
| Troubleshooting | Structured diagnosis using logs and system tools | Planned |

Statuses will be updated only after the relevant task has been performed and verified.

## Documentation standard

Each practical lab should include:

1. **Objective** — what needs to be configured or fixed.
2. **Environment** — relevant OS, devices, and assumptions.
3. **Implementation** — exact commands and configuration changes.
4. **Verification** — commands and output proving the result.
5. **Troubleshooting** — likely failure points and how to diagnose them.
6. **Lessons learned** — operational notes and safety considerations.

## Current checkpoint

The storage/LVM lab has started. The latest recorded checks showed:

- Physical volume: `/dev/vda3`
- Volume group: `rhel`
- Volume group size: approximately 39 GiB
- Free space in the volume group: 20 GiB
- Logical volumes reported by `vgs`: 2

These are observations from one lab checkpoint, not universal configuration values. The detailed task record will be added as the work is completed and verified.

## Repository structure

```text
linux-server-administration/
├── README.md
├── docs/
│   └── project-roadmap.md
└── labs/
    └── storage/
        └── lvm-checkpoint.md
```

## Safety notes

- Never commit passwords, private keys, tokens, or other credentials.
- Review command output and configuration files before publishing.
- Use disposable virtual machines or snapshots when practicing destructive storage operations.
- Redact public IPs and any personal or organization-specific information when necessary.

## Progress

This is an active learning project. Incomplete topics are explicitly marked as planned or in progress; they are not presented as completed production experience.
