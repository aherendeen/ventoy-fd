# Ventoy Configuration

A curated **Ventoy configuration** featuring a clean, responsive layout, dedicated directory structures for multi-OS bootable environments, and custom theme overrides. This repository helps you turn any USB flash drive into the ultimate multi-ISO booting powerhouse.

---

## 🚀 Introduction

[Ventoy](https://ventoy.net) is an open-source tool to create bootable USB drives for ISO/WIM/IMG/VHD(x)/EFI files. With Ventoy, you don't need to format the disk over and over; you just need to copy the files to the USB drive and boot them directly.

This repository provides an optimized `ventoy.json` setup that structures your distribution images, enhances the menu with custom branding, and integrates a streamlined GRUB theme.

### Directory Structure

To use this configuration effectively, organize your bootable USB flash drive according to the following tree layout:

```text
💾 Ventoy USB Root
 ├─ 📂 drivers/
 ├─ 📂 iso/
 │   ├─ 📂 linux/
 │   └─ 📂 windows/
 ├─ 📂 theme/
 ├─ 📂 ventoy/
 │   └─ 📄 ventoy.json
 └─ 📄 README.md
```

---

## 💿 Supported OS & Distributions

This configuration is optimized and visually tailored to support a wide array of operating systems. Click any distribution below to visit its official homepage and download the latest ISO:

* **[Arch Linux](https://archlinux.org)** — A lightweight and flexible Linux® distribution that tries to Keep It Simple.
* **[Bodhi Linux](https://bodhilinux.com)** — The Enlightened Linux Distribution featuring the lightweight Moksha desktop.
* **[CachyOS](https://cachyos.org)** — An ultra-fast, performance-first distribution based on Arch Linux.
* **[EndeavourOS](https://endeavouros.com)** — A terminal-centric distro with a vibrant and helpful community at its core.
* **[Fedora Linux](https://fedoraproject.org)** — An innovative, open-source platform for hardware, clouds, and containers.
* **[Garuda Linux](https://garudalinux.org)** — A rolling distribution based on Arch Linux focused on performance and vibrant aesthetics.
* **[Gentoo Linux](https://gentoo.org)** — A highly versatile, performance-oriented rolling distribution built from source.
* **[Manjaro](https://manjaro.org)** — A professionally designed, user-friendly operating system based on Arch.
* **[Linux Mint](https://linuxmint.com)** — A modern, elegant, and comfortable operating system that is both powerful and easy to use.
* **[NixOS](https://nixos.org)** — A reproducible and declarative Linux distribution built on top of the Nix package manager.
* **[System Rescue](https://system-rescue.org)** — A Linux system rescue disk available as a bootable CD-ROM or USB stick for administration tasks.
* **[Tails](https://tails.net)** — A live operating system that protects against surveillance and censorship.
* **[Ubuntu](https://ubuntu.com)** — The world's most popular open-source desktop operating system and cloud platform.
* **[VMware ESXi](https://bravura.com)** — A bare-metal hypervisor that installs directly onto your physical server.
* **[Void Linux](https://voidlinux.org)** — An independent, general-purpose operating system developed from scratch.
* **[Windows](https://microsoft.com)** — Official installation and recovery media for Microsoft Windows environments.

---

## 🎨 Theme Customization

This environment utilizes a customized variation of the sleek **[Dark Matter GRUB Theme](https://github.com)**. 

### Installation Instructions

To install and align the assets with the structural overrides defined in `ventoy.json`, mount your Ventoy drive and run the following placement commands:

```bash
# Move the core theme directory to Ventoy's asset path
mv darkmatter-grub2-theme/dark-matter /mnt/ventoy/theme/

# Apply specific progress bar configuration overrides
mv darkmatter-grub2-theme/assests/progressbar/linux_pb.png /mnt/ventoy/theme/dark-matter/progress_highlight_c.png

# Swap in the default system background canvas
mv darkmatter-grub2-theme/assests/backgrounds/linux.png /mnt/ventoy/theme/dark-matter/background.png

# Deploy the high-resolution color icon pack
mv darkmatter-grub2-theme/assests/icons/color /mnt/ventoy/theme/dark-matter/icons
```

---

## ⚙️ Configuration File (`ventoy.json`)

Ensure that the repository's `ventoy.json` is accurately placed inside the `ventoy/` directory on your primary partition. This file controls global behaviors, sets directory aliases, assigns custom menu icons based on regex pattern-matching rules, and registers the Dark Matter theme parameters.
