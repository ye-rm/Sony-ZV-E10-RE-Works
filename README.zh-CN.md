# Sony ZV-E10 逆向项目索引

[English](README.md) | 简体中文

**更新日期**：2026-11-20

本仓库收录针对 **Sony ZV-E10 一代（ILCE-ZV-E10）** 的公开逆向研究、工具与兼容性补丁。ZV-E10 II 属于不同机型，仅当项目明确覆盖一代时才会收录。本仓库仅提供外部项目索引，不分发任何固件或第三方代码，亦与 Sony 无关。

> **初步审查稿 · 2026-11-18**：下列项目为候选项，尚未完成完整的许可证合规审计。除特别注明外，功能与验证状态均来自项目作者说明。[ye-rm](https://github.com/ye-rm) 已初步测试软件兼容性补丁与 5 GHz Wi-Fi 解锁功能。欢迎在正式收录前参与审查与反馈。

## 收录范围与审查标准

**收录内容：**
- 相机固件与软件的逆向研究及修改，包括相关研究文档、备份与恢复工具。
- 面向原本不支持一代 ZV-E10 的软件所做的兼容性补丁。

**审查标准：**
- 项目须公开实质性的源码、文档或工具，并包含自身原创工作。
- 不收录空仓库、伪开源项目以及无实质改动的 fork。
- 审查重点在于实际技术内容与一代机型的相关性；许可证信息仅供参考，公开源码并不等同于授予再分发许可。

详细审查要求见 [CONTRIBUTING.md](CONTRIBUTING.md)。欢迎通过 issue 或 pull request 推荐项目、修正信息或报告失效链接。

## 相机固件与软件的逆向修改

| 项目 | 内容与适用范围 | 验证状态与限制 | 许可证与备注 |
| --- | --- | --- | --- |
| [qn06142/zv-e10-re](https://github.com/qn06142/zv-e10-re) | 基于 Sony-PMCA-RE 的 fork，新增 ZV-E10 服务模式、固件及资源格式研究（包含 `docs/`、`avcam_re/`、`retool/`）。 | **作者报告**：USB 视频实验已在实机验证。 | MIT。新增内容及第三方材料的授权待进一步核对。 |
| [cokeenet/zve10-qemu](https://github.com/cokeenet/zve10-qemu) | QEMU 启动补丁、研究笔记与硬件恢复工具。 | **作者报告**：新菜单移植已在 QEMU 中运行。<br>**已知限制**：尚待实机验证。 | 见 [LICENSE](https://github.com/cokeenet/zve10-qemu/blob/main/LICENSE) 与 [NOTICE](https://github.com/cokeenet/zve10-qemu/blob/main/NOTICE.md)。各组件许可待核对。 |
| [dino2048/ZV-E10-5GHz-WiFi-Unlock](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock) | 解锁一代相机原生 5 GHz Wi-Fi 菜单的技术笔记与工具。<br>**适用固件**：2.02、2.03。 | **作者报告**：已在 2.02 与 2.03 上验证，并基于中国大陆配置完成连接测试。<br>**初步测试**：[ye-rm](https://github.com/ye-rm) 在 Windows 上使用一台中国大陆配置、运行 2.03 固件的实机确认可打开频段菜单，且手机成功连入 5 GHz 热点（[测试记录 #4](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock/issues/4)）。 | MIT。使用前请参阅项目的地区与频段说明。 |
| [dino2048/zv-e10-toolkit](https://github.com/dino2048/zv-e10-toolkit) | USB 服务接口备份、BootROM 读取及 fastboot 分区恢复工具。<br>**适用固件**：2.02、2.03。 | **作者报告**：记录有 2.02 与 2.03 的实机验证结果。 | 仓库标注 MIT。作者注明部分移植代码的上游未声明再分发许可。 |
| [Mrliujunwen/zve10-shutter-sound-tool](https://github.com/Mrliujunwen/zve10-shutter-sound-tool) | Windows 源码工具，用于管理已安装对应电子快门音效补丁的相机音效与音量（工具本身不安装补丁）。<br>**适用固件**：仅限项目指定的 2.02 补丁固件。 | **已知限制**：作者说明重构后的协议层尚未重新在实机上验证。 | 许可信息待核查。 |
| [adeveloper79/sony-a6400-research (`zv-e10`)](https://github.com/adeveloper79/sony-a6400-research/tree/zv-e10) | 将 α6400 的 MTF2 菜单触控修改移植到一代 ZV-E10，仅在 RAM 中运行。<br>**适用固件**：2.02、2.03。 | **作者报告**：已在 2.02 与 2.03 上实机测试，主菜单大部分区域支持触控。<br>**已知限制**：部分子菜单与操作项无法触控打开；「我的菜单」无触控响应；Fn 菜单磁贴触控响应不稳定。 | [MIT](https://github.com/adeveloper79/sony-a6400-research/blob/zv-e10/LICENSE)。原始工作归功于 [ivica00/bionz-x-research](https://github.com/ivica00/bionz-x-research)。 |
| [ivica00/bionz-x-research](https://github.com/ivica00/bionz-x-research) | BIONZ X（CXD90045）同平台研究，涵盖 QEMU 与 Unicorn 仿真、一代 ZV-E10 固件映射及 α6400 上游 MTF2 触控修改。 | **作者报告**：记录了 α6400 的仿真与实机结果。 | MIT。一代 ZV-E10 映射见[平台文档](https://github.com/ivica00/bionz-x-research/blob/main/docs/PLATFORM_MODEL.md)。 |
| [XiaoQAQ10086/ZV-E10-Firmware-Research](https://github.com/XiaoQAQ10086/ZV-E10-Firmware-Research) | Windows 安装框架，提供写入前检查、备份与回滚功能。<br>**适用固件**：2.02、2.03。 | **作者报告**：在一台 2.03 相机上冷启动后恢复了 5 GHz 菜单；快门音实验已在实机验证写入与回滚。<br>**已知限制**：本项目尚未测试无线连接；相机未播放替换的快门音频。 | MIT。上游署名及组件许可见 [NOTICE](https://github.com/XiaoQAQ10086/ZV-E10-Firmware-Research/blob/main/NOTICE.md)。 |
| [nolan2628/ZVE10-Astra-Public](https://github.com/nolan2628/ZVE10-Astra-Public) | 将 ZV-1M2 的 ASTRA 触控界面实验性移植到一代 ZV-E10，提供[运行时适配层](https://raw.githubusercontent.com/nolan2628/ZVE10-Astra-Public/main/src/appFwBoot_g4host.c)、QEMU 网页触控界面以及构建与恢复工具。<br>**固件基线**：ZV-E10 2.03。 | **作者报告**：展示了实机上的新版拍摄界面和竖向菜单，并另行演示了 QEMU 中的触控交互。<br>**已知限制**：仅面向开发者，需自备固件。FL/VV 创意外观的底层处理尚未打通，自定义 LUT 需要外部方案。 | 仓库标注 MIT。第三方组件见 [THIRD_PARTY_NOTICES.md](https://github.com/nolan2628/ZVE10-Astra-Public/blob/main/THIRD_PARTY_NOTICES.md)。 |

## 软件兼容性补丁

| 项目 | 内容与适用范围 | 验证状态与限制 | 许可证与备注 |
| --- | --- | --- | --- |
| [peiyuanix/zv-e10-creators-app-patcher](https://github.com/peiyuanix/zv-e10-creators-app-patcher) | 补丁程序与分析文档，使应用支持一代 ZV-E10（作者说明需由用户自行提供原版应用并在本地修补）。<br>**适用版本**：Android 版 Creators' App 3.5.0。 | **初步测试**：[ye-rm](https://github.com/ye-rm) 初步测试认为该补丁及 PR [#1](https://github.com/peiyuanix/zv-e10-creators-app-patcher/pull/1)、[#2](https://github.com/peiyuanix/zv-e10-creators-app-patcher/pull/2) 可用，其中 PR #2 的基本功能已在其手机上测试通过。 | MIT。依赖项与补丁内容的授权待核对。 |
| [peiyuanix/zv-e10-monitor-control-patcher](https://github.com/peiyuanix/zv-e10-monitor-control-patcher) | 补丁程序与兼容性分析，使应用支持一代 ZV-E10。<br>**适用版本**：Android 版 Monitor & Control 3.0.1。 | **作者报告**：已测试 USB 与 Wi-Fi 连接。<br>**初步测试**：[ye-rm](https://github.com/ye-rm) 初步测试认为该补丁可用。 | MIT。依赖项与补丁内容的授权待核对。 |

## 无开源许可证的项目

| 项目 | 原因 |
| --- | --- |
| [nolan2628/Sony-ZVE-10-Camtool](https://github.com/nolan2628/Sony-ZVE-10-Camtool) | 包含服务模式与备份工具，但其 README 明确声明未授予开源许可，也不允许再分发或复用。 |

## 风险提示

- **设备与保修风险**：本索引收录的项目可能未经独立验证。涉及固件、分区或恢复的操作可能导致数据丢失、相机损坏或无法启动，并可能影响保修。操作前请务必核对各项目的适用固件版本、备份步骤及恢复方案。
- **法律与合规风险**：逆向与修改行为可能涉及法律法规、软件许可条款及无线电管理等方面的合规风险，具体要求因操作内容与所在地区而异，请在操作前自行评估。
