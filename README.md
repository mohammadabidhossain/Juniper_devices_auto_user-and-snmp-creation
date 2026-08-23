# Junos Multi-Hop Automation Scripts

A set of automated Expect scripts designed for managing Juniper Networks (Junos OS) devices through a bastion jump host. These scripts assist network administrators in streamlining user provisioning and system monitoring parameters without interactive manual intervention.

## Features

- **Multi-Hop Traversal:** Handles nested SSH authentication through a jump host before targeting network switches.
- **Automated Privilege Provisioning:** Creates new administrative users (`super-user` class) with configured authentication.
- **SNMP Configuration:** Sets up read-only community strings, restricted NMS subnets, and location metadata dynamically.
- **Safe Execution:** Automates Junos syntax application along with `show | compare` visibility and atomic `commit and-quit` commands.

## Requirements

- **OS:** Linux, macOS, or Windows Subsystem for Linux (WSL)
- **Tooling:** `expect` utility installed (`sudo apt install expect` on Ubuntu/Debian)
- **Network Connectivity:** SSH access to the intermediate Jump Host, with valid routing to target Junos devices.

## Script Overview

| Script Name | Target Task | Usage |
|---|---|---|
| `add_user.exp` | Adds a new super-user account | `./add_user.exp <switch_ip>` |
| `configure_snmp.exp` | Provisions SNMP v2c community & subnets | `./configure_snmp.exp` |

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/junos-expect-automation.git](https://github.com/your-username/junos-expect-automation.git)
   cd junos-expect-automation
