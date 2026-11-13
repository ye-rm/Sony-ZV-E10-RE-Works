# Sony ZV-E10 Reverse Engineering Index

English | [简体中文](README.zh-CN.md)

An index of public reverse engineering research, tools and compatibility patches for the **first-generation Sony ZV-E10 (ILCE-ZV-E10)**. The ZV-E10 II is a different model; projects are listed only when they explicitly cover the original. This repository links to external work, does not distribute firmware or third-party code, and is not affiliated with Sony.

> **Preliminary review · 2026-11-13:** These are candidates, not projects that have passed a license compliance audit. Features and validation status are reported by the authors and have not been independently reproduced here. The list is open for review before final inclusion.

## Scope

- Reverse engineering research or documentation on ZV-E10 firmware, hardware, protocols and runtime environments.
- Tools specifically for ZV-E10 research, backup, analysis or recovery.
- Patches that adapt software which did not originally support the first-generation ZV-E10.

Projects should publicly provide substantial source code, documentation or tools and include work of their own. Review focuses on substance and relevance; license information is provided for reference. Public source code does not automatically grant redistribution rights. Empty projects, pseudo-open-source projects and forks without substantial changes are excluded. See [CONTRIBUTING.md](CONTRIBUTING.md) for review guidance.

## Firmware reverse engineering and research

| Project | Work and status | License and notes |
| --- | --- | --- |
| [qn06142/zv-e10-re](https://github.com/qn06142/zv-e10-re) | A Sony-PMCA-RE fork adding ZV-E10 service-mode, firmware and resource-format research, including `docs/`, `avcam_re/` and `retool/`. The author reports hardware validation of a USB video experiment. | MIT; licensing of additions and third-party material needs further review. |
| [cokeenet/zve10-qemu](https://github.com/cokeenet/zve10-qemu) | QEMU boot patches, research notes and hardware recovery tools. The author reports that the new-menu port works in QEMU but awaits camera validation. | See [LICENSE](https://github.com/cokeenet/zve10-qemu/blob/main/LICENSE) and [NOTICE](https://github.com/cokeenet/zve10-qemu/blob/main/NOTICE.md); individual components need review. |
| [ZV-E10-5GHz-WiFi-Unlock](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock) | Technical notes and tools for unlocking the original camera's native 5 GHz Wi-Fi menu. The author reports validation on firmware 2.02 and 2.03 and connection tests with the mainland China configuration. | MIT; consult the project's regional and frequency-band guidance. |

## Reverse engineering and recovery tools

| Project | Work and status | License and notes |
| --- | --- | --- |
| [dino2048/zv-e10-toolkit](https://github.com/dino2048/zv-e10-toolkit) | USB service-interface backup, BootROM reading and fastboot partition recovery tools. The author reports hardware validation records for 2.02 and 2.03. | Repository marked MIT; the author notes that upstream code used for some ports does not state a redistribution license. |
| [zve10-shutter-sound-tool](https://github.com/Mrliujunwen/zve10-shutter-sound-tool) | Windows source tool for managing sounds and volume on 2.02 cameras with a specified electronic shutter sound patch already installed; it does not install the patch. The author says the refactored protocol layer has not yet been revalidated on hardware. | License information pending; supports only the patched firmware identified by the project. |

## Software compatibility patches

| Project | Work and status | License and notes |
| --- | --- | --- |
| [zv-e10-creators-app-patcher](https://github.com/peiyuanix/zv-e10-creators-app-patcher) | Patcher and analysis enabling the original ZV-E10 in Creators' App 3.5.0 for Android. The author says users supply the original app and patch it locally. | MIT; dependencies and patch content need license review. |
| [zv-e10-monitor-control-patcher](https://github.com/peiyuanix/zv-e10-monitor-control-patcher) | Patcher and compatibility analysis for Monitor & Control 3.0.1 for Android. The author reports testing USB and Wi-Fi connections. | MIT; dependencies and patch content need license review. |

## Not included: no open-source license

| Project | Reason |
| --- | --- |
| [nolan2628/Sony-ZVE-10-Camtool](https://github.com/nolan2628/Sony-ZVE-10-Camtool) | Contains service-mode and backup tools, but its README explicitly grants no open-source license or permission for redistribution or reuse. |

Firmware, partition and recovery operations can cause data loss or render a camera unbootable. Consult each project's supported firmware versions, backup instructions and recovery procedures.
