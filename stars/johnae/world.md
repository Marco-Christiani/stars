---
repo: johnae/world
url: 'https://github.com/johnae/world'
homepage: null
starredAt: '2026-09-23T20:22:48Z'
createdAt: '2020-07-04T20:00:34Z'
updatedAt: '2026-09-26T11:41:58Z'
language: Nix
license: MIT
branch: main
stars: 133
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-09-27T00:41:21.411Z'
description: NixOS configuration
tags: []
---

My personal [NixOS](https://nixos.org) configuration managing all my machines and custom packages using [Nix flakes](https://nixos.wiki/wiki/Flakes). Provides declarative, reproducible system management across NixOS, nix-darwin (macOS), and home-manager only (non-NixOS Linux)—like Cargo.toml or package.json but language-agnostic.

This repo is my working environment—it's not a framework or template, but others might find ideas worth borrowing.

For modularity, [flake-parts](https://flake.parts) is used to keep [flake.nix](./flake.nix) clean and structured.

## ✨ Key Features

- Multi-platform: Manages NixOS, nix-darwin (macOS), and home-manager only (non-NixOS Linux) systems
- Stateless by default: Ephemeral root filesystems with persistent data management
- Automated updates: CI-driven updates with smart reboot coordination
- Encrypted secrets: Age-encrypted secrets with automatic deployment
- Remote unlock: SSH-based LUKS unlock for headless encrypted servers
- Modular design: Reusable profiles for different machine roles
- Comprehensive backups: Automated Restic backups to multiple destinations

## Repository Structure

```
world/
├── configurations/ # Machine-specific configurations
│   ├── nixos/      # NixOS systems (by architecture)
│   ├── darwin/     # nix-darwin (macOS) systems
│   ├── home/       # home-manager only (non-NixOS Linux)
│   └── microvms/   # MicroVM configurations
├── profiles/       # Reusable system profiles (server, desktop, laptop)
├── modules/        # Custom NixOS/nix-darwin/home-manager modules
├── users/          # User configurations (home-manager profiles)
├── packages/       # Custom packages not in nixpkgs
├── secrets/        # Encrypted configuration (agenix)
├── flake/          # Flake components (organized with flake-parts)
└── flake.nix       # Main flake definition
```

For detailed development guidelines, see [DEVELOPMENT.md](./DEVELOPMENT.md).

## 🚀 How I Use This

### The `world` CLI

I built a custom CLI wrapper (based on a Justfile) for common tasks:

```bash
# Search for packages
world search <package>

# Open shell with packages
world shell <packages>

# Update system
world upgrade

# Build without switching
world build

# Garbage collect
world gc

# Run linters
world lint

# Check flake
world check
```

### Setup Notes

Flakes must be enabled:
```bash
mkdir -p ~/.config/nix
echo "experimental-features = nix-command flakes" >> ~/.config/nix/nix.conf
```

## System Management

### Update Existing System

From GitHub using world cli:
```bash
world upgrade
```

From local clone using world cli:
```bash
world upgrade .
```

From GitHub using nix cli:
```bash
nixos-rebuild switch --flake github:johnae/world --use-remote-sudo
```

From local clone using nix cli:
```bash
nixos-rebuild switch --flake . --use-remote-sudo
```

### Installing on a New Machine

Notes for myself when provisioning a new host:

1. Create host configuration in `configurations/<type>/<arch>/<hostname>.nix`
2. Boot NixOS installer and enable flakes
3. Clone this repository
4. Install:

```bash
host=yourhostname
nix build .#"$host"-diskformat
./result/bin/diskformat
nixos-install --flake .#"$host" --no-root-passwd
```

## Architecture

The configuration follows a layered approach:

1. Base: Core packages and settings (`profiles/defaults.nix`)
2. Profile: Role-specific configs (server, desktop, workstation)
3. Host: Machine-specific settings and hardware
4. User: Personal configurations via home-manager

### Key Design Choices

- Impermanence: Root filesystem is tmpfs, only declared paths persist
- Declarative storage: Disk formatting is part of the configuration
- Profile inheritance: Hosts compose functionality from profiles
- Unified tooling: Same commands work across NixOS and macOS

## If You're Borrowing From This

This is highly specific to my setup, but if you want to adapt parts:

- Start with a single host as a reference
- Most reusable logic is in profiles/
- Secrets use agenix (you'll need your own keys)

### Common Modifications

- New machine: Copy similar configuration file under `configurations/<type>/<arch>/`, adjust hardware config
- New service: Add to appropriate profile or create new module
- User settings: Modify configurations under `users/profiles/`

## Security Features

- Encrypted disks: LUKS encryption with remote unlock capability
- Secrets management: Age-encrypted secrets, SSH key based
- Secure boot: Where supported by hardware
- Firewall: Enabled by default with explicit port management

## Automation

- CI/CD: Buildkite pipeline tests all configurations
- Dependency updates: Automated flake input updates
- Smart reboots: Coordinated reboots for kernel updates (in k8s clusters)
- Backup verification: Automated backup integrity checks

## Experimental Features

This repo includes some experimental work like MicroVM configurations for container workloads, but these aren't actively used and may not be fully functional.

## Resources

- [NixOS Manual](https://nixos.org/manual/nixos/stable/)
- [Nix Pills](https://nixos.org/guides/nix-pills/)
- [Home Manager](https://github.com/nix-community/home-manager)
- [Agenix](https://github.com/ryantm/agenix)

## License

[MIT](LICENSE)

---

*Note: This is a personal configuration that's highly customized to my workflow. Feel free to browse and borrow ideas, but you'll want to adapt it significantly for your own use.*
