# Sony ZV-E10 Reverse Engineering Index

English | [简体中文](README.zh-CN.md)

**Last updated:** 2026-11-20

A curated index of public reverse engineering research, tools, and compatibility patches for the **first-generation Sony ZV-E10 (ILCE-ZV-E10)**. The ZV-E10 II is a different model; projects are listed only when they explicitly cover the original ZV-E10. This repository links to external projects only—it does not distribute firmware or third-party code and is not affiliated with Sony.

> **Preliminary review · 2026-11-18:** Entries below are candidates and have not undergone a full license compliance audit. Unless noted otherwise, features and validation status are reported by the project authors. [ye-rm](https://github.com/ye-rm) has preliminarily tested the software compatibility patches and the 5 GHz Wi-Fi unlock. Feedback is welcome before final inclusion.

## Scope and review criteria

**Included:**
- Reverse engineering and modifications of camera firmware and software, including related research, backup, and recovery tools.
- Patches adapting software that did not originally support the first-generation ZV-E10.

**Review criteria:**
- Projects must publicly provide substantial source code, documentation, or tools with original work of their own.
- Empty repositories, pseudo-open-source projects, and forks without substantial changes are excluded.
- Review focuses on technical substance and relevance to the original ZV-E10. License details are provided for reference; public source code does not automatically grant redistribution rights.

See [CONTRIBUTING.md](CONTRIBUTING.md) for review guidance. Contributions are welcome—open an issue or pull request to suggest a project, correct an entry, or report a broken link.

## Camera firmware and software reverse engineering

| Project | Summary & target | Validation & limitations | License & notes |
| --- | --- | --- | --- |
| [qn06142/zv-e10-re](https://github.com/qn06142/zv-e10-re) | Sony-PMCA-RE fork adding ZV-E10 service-mode, firmware, and resource-format research (`docs/`, `avcam_re/`, `retool/`). | **Author-reported:** Hardware validation of a USB video experiment. | MIT. Licensing of additions and third-party material needs further review. |
| [cokeenet/zve10-qemu](https://github.com/cokeenet/zve10-qemu) | QEMU boot patches, research notes, and hardware recovery tools. | **Author-reported:** New-menu port runs in QEMU.<br>**Limitations:** Awaits validation on camera hardware. | See [LICENSE](https://github.com/cokeenet/zve10-qemu/blob/main/LICENSE) and [NOTICE](https://github.com/cokeenet/zve10-qemu/blob/main/NOTICE.md). Individual components need review. |
| [dino2048/ZV-E10-5GHz-WiFi-Unlock](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock) | Technical notes and tools to unlock the native 5 GHz Wi-Fi menu.<br>**Firmware:** 2.02, 2.03. | **Author-reported:** Validated on 2.02 and 2.03; connection tested with the mainland China configuration.<br>**Preliminary test:** On Windows with one 2.03 camera (mainland China config), [ye-rm](https://github.com/ye-rm) confirmed the band menu opened and a phone connected to the 5 GHz hotspot ([Test report #4](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock/issues/4)). | MIT. Review the project's regional and frequency-band guidance before use. |
| [dino2048/zv-e10-toolkit](https://github.com/dino2048/zv-e10-toolkit) | Tools for USB service-interface backup, BootROM reading, and fastboot partition recovery.<br>**Firmware:** 2.02, 2.03. | **Author-reported:** Hardware validation records for 2.02 and 2.03. | Marked MIT. Author notes that upstream code used in some ports does not state a redistribution license. |
| [Mrliujunwen/zve10-shutter-sound-tool](https://github.com/Mrliujunwen/zve10-shutter-sound-tool) | Windows source tool to manage sounds and volume on cameras that already have a specified electronic shutter-sound patch installed (does not install the patch).<br>**Firmware:** 2.02 (project-specified patched firmware only). | **Limitations:** Author notes the refactored protocol layer has not yet been revalidated on hardware. | License pending. |
| [adeveloper79/sony-a6400-research (`zv-e10`)](https://github.com/adeveloper79/sony-a6400-research/tree/zv-e10) | RAM-only port of the α6400 MTF2 menu touch mod to the original ZV-E10.<br>**Firmware:** 2.02, 2.03. | **Author-reported:** Hardware-tested on 2.02 and 2.03; touch works across much of the main menu.<br>**Limitations:** Some submenus and action items cannot be opened by touch; My Menu does not respond; inconsistent touch response on Fn tiles. | [MIT](https://github.com/adeveloper79/sony-a6400-research/blob/zv-e10/LICENSE). Credits [ivica00/bionz-x-research](https://github.com/ivica00/bionz-x-research) for the original work. |
| [ivica00/bionz-x-research](https://github.com/ivica00/bionz-x-research) | Shared BIONZ X (CXD90045) platform research: QEMU and Unicorn emulation, firmware mapping covering the original ZV-E10, and the upstream α6400 MTF2 touch mod. | **Author-reported:** Documents α6400 emulation and hardware results. | MIT. See the [platform model](https://github.com/ivica00/bionz-x-research/blob/main/docs/PLATFORM_MODEL.md) for the ZV-E10 mapping. |
| [XiaoQAQ10086/ZV-E10-Firmware-Research](https://github.com/XiaoQAQ10086/ZV-E10-Firmware-Research) | Windows installer framework with pre-write checks, backup, and rollback.<br>**Firmware:** 2.02, 2.03. | **Author-reported:** Restored the 5 GHz menu on one 2.03 camera after a cold boot; verified writes and rollback on hardware in the shutter-sound experiment.<br>**Limitations:** RF connectivity is untested in this project; the camera did not play the replacement shutter audio. | MIT. See [NOTICE](https://github.com/XiaoQAQ10086/ZV-E10-Firmware-Research/blob/main/NOTICE.md) for upstream attribution and component licenses. |
| [nolan2628/ZVE10-Astra-Public](https://github.com/nolan2628/ZVE10-Astra-Public) | Experimental port of the ZV-1M2 ASTRA touch UI to the original ZV-E10, with a [runtime shim](https://raw.githubusercontent.com/nolan2628/ZVE10-Astra-Public/main/src/appFwBoot_g4host.c), QEMU Web touch controls, and build and recovery tools.<br>**Firmware baseline:** ZV-E10 2.03. | **Author-reported:** Shows the new shooting UI and vertical menu on camera hardware, and separately demonstrates touch interaction in QEMU.<br>**Limitations:** Developer-only; requires user-supplied firmware. FL/VV Creative Look processing is incomplete, and custom LUTs require an external solution. | Repository marked MIT. See [THIRD_PARTY_NOTICES.md](https://github.com/nolan2628/ZVE10-Astra-Public/blob/main/THIRD_PARTY_NOTICES.md) for third-party components. |

## Software compatibility patches

| Project | Summary & target | Validation & limitations | License & notes |
| --- | --- | --- | --- |
| [peiyuanix/zv-e10-creators-app-patcher](https://github.com/peiyuanix/zv-e10-creators-app-patcher) | Patcher and analysis enabling the original ZV-E10. Per the author, users supply the original app and patch it locally.<br>**Target:** Creators' App 3.5.0 (Android). | **Preliminary test:** [ye-rm](https://github.com/ye-rm) reports that the patch and PRs [#1](https://github.com/peiyuanix/zv-e10-creators-app-patcher/pull/1) and [#2](https://github.com/peiyuanix/zv-e10-creators-app-patcher/pull/2) worked; basic functions of PR #2 worked on their phone. | MIT. Dependencies and patch content need license review. |
| [peiyuanix/zv-e10-monitor-control-patcher](https://github.com/peiyuanix/zv-e10-monitor-control-patcher) | Patcher and compatibility analysis enabling the original ZV-E10.<br>**Target:** Monitor & Control 3.0.1 (Android). | **Author-reported:** Tested over USB and Wi-Fi.<br>**Preliminary test:** [ye-rm](https://github.com/ye-rm) reports that the patch worked. | MIT. Dependencies and patch content need license review. |

## Projects without an open-source license

| Project | Reason |
| --- | --- |
| [nolan2628/Sony-ZVE-10-Camtool](https://github.com/nolan2628/Sony-ZVE-10-Camtool) | Contains service-mode and backup tools, but its README explicitly grants no open-source license and permits no redistribution or reuse. |

## Risks

- **Hardware and warranty risks:** Listed projects may not have been independently verified. Firmware, partition, and recovery operations can cause data loss, damage the camera, render it unbootable, or affect warranty coverage. Always check each project's supported firmware versions, backup steps, and recovery procedures before use.
- **Legal and compliance risks:** Reverse engineering and modifications may carry legal, licensing, or regulatory risks (including wireless and radio rules) depending on the activity and jurisdiction. Assess applicable requirements before proceeding.
