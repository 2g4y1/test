![GitHub latest release](https://img.shields.io/github/v/release/dlt-green/node-installer-docker)
![GitHub release date](https://img.shields.io/github/release-date/dlt-green/node-installer-docker)
![GitHub contributors](https://img.shields.io/github/contributors/dlt-green/node-installer-docker)
![GitHub license](https://img.shields.io/github/license/dlt-green/node-installer-docker)

# DLT.GREEN INITIATIVE

Join us on a transformative journey in the IOTA community, as we at DLT.GREEN lead the charge to revolutionize how DNS — that's Dynamic Node Selection — operates within the IOTA/Shimmer ecosystem. Our mission is to elevate user interactions by transitioning from outdated static node configurations to an intelligent, situation-responsive framework. Imagine a future where wallets dynamically connect to the most optimal node without hesitation, freeing users from concerns about node reliability.

Envision IoT devices flawlessly navigating to nodes that are custom-selected for their unique requirements, whether it's processing speed, event compatibility, trust level, or workload capacity. At DLT.GREEN, we're committed to ensuring uninterrupted and direct data pathways between your wallet and the chosen node, effectively streamlining efficiency by eliminating reliance on intermediary node pools.

# DLT.GREEN NODE-INSTALLER VIA DOCKER

Discover the ease of setting up IOTA/Shimmer Nodes with our innovative DLT.GREEN Node-Installer-Docker tool. This intuitive script is your gateway to deploying Hornet and Wasp nodes with minimal effort. Backed by the power of Docker technology, this installer is crafted with all skill levels in mind — a boon for novices and experts alike. Quickly establish your own IOTA/Shimmer nodes on a variety of platforms including servers or virtual private servers (VPS), and join the forefront of distributed ledger technology today.

### Hardware Recommendations

#### For Standard Nodes
- **RAM:** 8 GB minimum
- **CPU Cores:** 4
- **Storage:** 160 GB SSD minimum
- **Operating System:** Ubuntu 22.04.03 LTS (Jammy Jellyfish) or Debian 12 (Bookworm)

#### For Event-Tracking Nodes or Additional Plugins
- **RAM:** 16 GB minimum
- **CPU Cores:** 4+
- **Storage:** 250 GB SSD minimum
- **Operating System:** Ubuntu 22.04.03 LTS (Jammy Jellyfish) or Debian 12 (Bookworm)

## Installation Guide

### Prerequisites
Before commencing with the installation:
- Ensure you have access to a server or VPS.
- Secure your own domain name.
Note: SSL certificates will be generated via Let's Encrypt automatically, but you can also use your own certificate.

### Installing NODE-INSTALLER

Execute the following command in your console:
```console
sudo wget https://github.com/dlt-green/node-installer-docker/releases/latest/download/node-installer.sh && sudo sh node-installer.sh
```

### NODE-INSTALLER with GUI

After running the installer for the first time, it creates an alias accessible at the user level:
```console
dlt.green
```

### NODE-INSTALLER Unattended Mode

To run the NODE-INSTALLER in unattended mode, use the following syntax with optional flags:
```console
dlt.green [-m mode/optional] [-t time/optional] [-r reboot/optional] [-c checks/optional] [-l logs/optional]
```

Each flag represents a different configuration option:

- `mode`: Sets the operation mode of the installer.
   - `s`: Start all Nodes.
   - `0`: Maintenance – Performs system updates, Docker cleanup, and certificate update. Installs Docker if not present.
   - `1`: Update – Updates IOTA-Hornet nodes.
   - `2`: Update – Updates IOTA-Wasp nodes.
   - `5`: Update – Updates Shimmer-Hornet nodes.
   - `6`: Update – Updates Shimmer-Wasp nodes.
   - `u`: Executes Mode 0 and performs unattended recursive Node Updates when possible. Supports the last 10 releases in the GitHub pipeline (older versions are not updated).
- `time`: Sets the delay in seconds before executing an action (0-20 seconds, default: 10).
- `reboot`:
   - `0`: No reboot after operations.
   - `1`: Executes a system reboot with automatic node shutdown prior to it (default: 0).
- `checks`:
   - `0`: Disables checks (not recommended).
   - `1`: Enforces UFW Firewall and Autostart setup (default: 1).
- `logs`:
   - `i`: Displays all logs.
   - `w`: Shows only warnings and errors in logs.
   - `e`: Shows only errors in logs (default: i).

Utilize these options according to your needs to automate node management tasks efficiently.

### Operation Tutorial

For a visual aid on installing IOTA/Shimmer Nodes using our script, visit our [video tutorials](https://www.youtube.com/channel/UCg1PgTJ1NzdoS1JYcnJtDUg).

[![Installation Video Tutorial](https://github.com/dlt-green/node-installer-docker/assets/89119285/e6bb308b-29a7-48e6-8eac-809e3069139a)](https://www.youtube.com/channel/UCg1PgTJ1NzdoS1JYcnJtDUg)

## Feedback and Support

Encounter an issue or have suggestions? Please create a Github issue or reach out to our team on Discord.

**Improvement Suggestions:** [Github Issues](https://github.com/dlt-green/node-installer-docker/issues)

**Contact Us:** [Discord](https://discord.gg/XaBnsE5NGb)

## Disclaimer

Use of this script is at your own risk. DLT.GREEN assumes no responsibility for any damages incurred.

## Disclosure

This is an independent installer not endorsed by the Iota Foundation; thus, IF support will not be available. However, our team and community offer support through our Discord.

## Donations

DLT.GREEN and its community proudly develop this project. Support us with donations:

**IOTA**: [`iota1qq7seed74mzvy9g6nj2nj88pm37gf2x5qv35jcun78n86hyzaqcaggy8ewa`](https://explorer.iota.org/mainnet/addr/iota1qq7seed74mzvy9g6nj2nj88pm37gf2x5qv35jcun78n86hyzaqcaggy8ewa)

**Shimmer**: [`smr1qzp87wkakd22ld6rvcjuwuvn5usevmvut565y6l32xhfucpemu0extkpws0`](https://explorer.shimmer.network/shimmer/addr/smr1qzp87wkakd22ld6rvcjuwuvn5usevmvut565y6l32xhfucpemu0extkpws0)

**Shimmer EVM**: [`0x6c5ab03b8e4b4f9ec591d211411082a7ab925c05`](https://explorer.evm.shimmer.network/address/0x6c5aB03b8E4b4F9ec591D211411082A7ab925C05)

**Soonaverse**: [`https://soonaverse.com/member/0x422bed2759f72e7d6ae1e100707ca45e26e9a12c`](https://soonaverse.com/member/0x422bed2759f72e7d6ae1e100707ca45e26e9a12c)
