Proxmox: VFIO
=============

An Ansible role that loads the vfio modules on a Proxmox VE host. 

Requirements
------------

N/A.

Role Variables
--------------

|        Variable        |  Type  |                      Default                      |                       Description                       |
| :--------------------: | :----: | :-----------------------------------------------: | :-----------------------------------------------------: |
| `proxmox_vfio_modules` | string | `[vfio, vfio_iommu_type1, vfio_pci, vfio_virqfd]` | Override the auto-generated cmdline with this variable. |

For more details about the **default** variables, take a look at the [defaults/main.yml](defaults/main.yml).

Dependencies
------------

N/A.

Example Playbook
----------------

``` yml
---
- name: Load the VFIO modules on all PVE hosts
  hosts: pve
  remote_user: root

  roles:
    - role: mirceanton.proxmox_vfio
```

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
