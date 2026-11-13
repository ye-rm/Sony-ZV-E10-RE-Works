# Sony ZV-E10 逆向项目索引

[English](README.md) | 简体中文

收集针对 **Sony ZV-E10 一代（ILCE-ZV-E10）** 的公开逆向研究、工具和兼容性补丁。ZV-E10 II 是不同机型；仅在项目明确涉及一代时列入。本仓库是链接索引，不分发固件或第三方代码，与 Sony 无关联。

> **初步审查稿 · 2026-11-13**：下列项目是候选项，并非已完成许可证合规审计。功能和验证状态来自项目自身说明，未在本仓库复现。欢迎先审查，再决定正式收录。

## 收录范围

- 相机固件和软件的逆向研究与修改，包括相关研究、备份和恢复工具。
- 修改原本不支持一代 ZV-E10 的软件以实现兼容的补丁。

要求公开实质性源码、文档或工具，并有项目自身的实际工作。重点审查内容及与机型的关系，许可证信息作为参考；公开源码不代表自动取得再分发许可。空仓库、伪开源和没有实质改动的 fork 不收录。具体审查方法见 [CONTRIBUTING.md](CONTRIBUTING.md)。

欢迎提出 issue 或 pull request，推荐更多逆向工作、修正条目或报告失效链接。

## 相机固件与软件的逆向修改

| 项目 | 可核查的工作与状态 | 许可及待审查 |
| --- | --- | --- |
| [qn06142/zv-e10-re](https://github.com/qn06142/zv-e10-re) | 基于 Sony-PMCA-RE 的 fork；新增 ZV-E10 服务模式、固件和资源格式研究，以及 `docs/`、`avcam_re/`、`retool/` 等内容。作者报告 USB 视频实验已在实机验证。 | MIT；需进一步核对新增内容及第三方材料的授权。 |
| [cokeenet/zve10-qemu](https://github.com/cokeenet/zve10-qemu) | 包含 QEMU 启动补丁、研究笔记和硬件恢复工具；新菜单移植据作者说明已在 QEMU 中运行，尚待相机验证。 | 项目含 [LICENSE](https://github.com/cokeenet/zve10-qemu/blob/main/LICENSE) 和 [NOTICE](https://github.com/cokeenet/zve10-qemu/blob/main/NOTICE.md)；需核对各部分许可。 |
| [ZV-E10-5GHz-WiFi-Unlock](https://github.com/dino2048/ZV-E10-5GHz-WiFi-Unlock) | 提供一代相机原生 5 GHz Wi-Fi 菜单解锁的技术笔记和工具；作者报告在固件 2.02、2.03 上验证，中国大陆配置完成连接测试。 | MIT；使用时参阅项目的地区及频段说明。 |
| [dino2048/zv-e10-toolkit](https://github.com/dino2048/zv-e10-toolkit) | 包含 USB 服务接口备份、BootROM 读取及 fastboot 分区恢复工具；作者报告 2.02、2.03 的实机验证记录。 | 仓库标注 MIT；作者注明部分移植代码的上游未声明再分发许可。 |
| [zve10-shutter-sound-tool](https://github.com/Mrliujunwen/zve10-shutter-sound-tool) | Windows 源码工具，管理已安装对应电子快门声音补丁的 2.02 相机的音效和音量；不安装该补丁。作者说明重构后的协议层尚未重新进行实机验证。 | 许可信息待核查；仅支持项目列明的补丁固件。 |

## 软件兼容性补丁

| 项目 | 可核查的工作与状态 | 许可及待审查 |
| --- | --- | --- |
| [zv-e10-creators-app-patcher](https://github.com/peiyuanix/zv-e10-creators-app-patcher) | 提供补丁程序和分析文档，使 Android 版 Creators' App 3.5.0 支持一代 ZV-E10；作者称原应用由用户自行提供并在本地修改。 | MIT；需核对依赖与补丁内容的授权。 |
| [zv-e10-monitor-control-patcher](https://github.com/peiyuanix/zv-e10-monitor-control-patcher) | 包含补丁程序和兼容性分析，针对 Android 版 Monitor & Control 3.0.1；作者报告测试了 USB 和 Wi-Fi 连接。 | MIT；需核对依赖与补丁内容的授权。 |

## 暂不收录：未授予开源许可

| 项目 | 原因 |
| --- | --- |
| [nolan2628/Sony-ZVE-10-Camtool](https://github.com/nolan2628/Sony-ZVE-10-Camtool) | 有服务模式和备份工具，但 README 明确表示未授予开源许可及再分发或复用权限，不符合当前收录标准。 |

## 风险提示

收录的项目可能未经独立验证。固件、分区或恢复操作可能造成数据丢失、损坏相机或导致设备无法启动，也可能影响保修。使用前请阅读各项目的适用固件版本、备份及恢复说明。

逆向及修改行为也可能存在合规风险。适用的法律法规、许可条款及无线电要求取决于具体行为和所在地区，请在操作前自行评估。

