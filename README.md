<!--
  freedom-winds · GitHub Profile README（完整版 / 约 2 屏）
  基调：深色优先；深海军蓝 → 青，单色系；零 emoji；"主张 → 证据 → 数据" 三层结构。
  视觉全部由外链 SVG 生成，正文仅用 GFM + GitHub 白名单 HTML。
  README.md 存于 freedom-winds/freedom-winds 仓库。
-->

<div align="center">
<picture>
<source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&color=0:08131E,45:10506F,100:22D3EE&height=180&section=header&text=ZT%20Winds&fontSize=48&fontColor=E8FBFF&fontAlignY=38&desc=freedom-winds&descAlignY=66&descColor=8FD9EE">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:F2FBFF,45:A6DDEF,100:4CBBDD&height=180&section=header&text=ZT%20Winds&fontSize=48&fontColor=0A2233&fontAlignY=38&desc=freedom-winds&descAlignY=66&descColor=12557A" width="100%" alt="ZT Winds">
</picture>
<br>
<picture>
<source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=3600&pause=1500&color=22D3EE&center=true&vCenter=true&width=760&height=44&repeat=false&lines=%E5%86%99%E4%B8%80%E9%97%A8%E7%BC%96%E8%AF%91%E8%AF%AD%E8%A8%80%EF%BC%8C%E9%80%A0%E5%87%A0%E4%B8%AA%E4%BB%BF%E7%9C%9F%E5%99%A8%EF%BC%8C%E9%A1%BA%E4%BE%BF%E7%BB%99%E5%A4%A7%E5%9E%8B%E5%BC%80%E6%BA%90%E9%A1%B9%E7%9B%AE%E6%8A%93%E8%99%AB%E3%80%82">
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=3600&pause=1500&color=12557A&center=true&vCenter=true&width=760&height=44&repeat=false&lines=%E5%86%99%E4%B8%80%E9%97%A8%E7%BC%96%E8%AF%91%E8%AF%AD%E8%A8%80%EF%BC%8C%E9%80%A0%E5%87%A0%E4%B8%AA%E4%BB%BF%E7%9C%9F%E5%99%A8%EF%BC%8C%E9%A1%BA%E4%BE%BF%E7%BB%99%E5%A4%A7%E5%9E%8B%E5%BC%80%E6%BA%90%E9%A1%B9%E7%9B%AE%E6%8A%93%E8%99%AB%E3%80%82" alt="写一门编译语言，造几个仿真器，顺便给大型开源项目抓虫。">
</picture>
<br><br>
<b>写一门编译语言</b> — Rust 从零实现的原生编译语言 <a href="https://github.com/freedom-winds/talqor">talqor</a>，Cranelift + LLVM 双后端<br>
<b>造几个仿真器</b> — 物理运动跟踪 · 400 智能体垂直校园 · 三维热学工作台<br>
<b>抓上游的虫</b> — nginx · systemd · openssl · oxc · redis-rs 等 14+ 个项目，40+ PR / 16 merged
<br><br>
<img src="https://img.shields.io/badge/Rust-0F3350?style=flat-square&labelColor=0B1220&logo=rust&logoColor=DFF6FF" alt="Rust"> <img src="https://img.shields.io/badge/C-134A6B?style=flat-square&labelColor=0B1220&logo=c&logoColor=DFF6FF" alt="C"> <img src="https://img.shields.io/badge/Go-176285?style=flat-square&labelColor=0B1220&logo=go&logoColor=DFF6FF" alt="Go"> <img src="https://img.shields.io/badge/Python-1B7A9E?style=flat-square&labelColor=0B1220&logo=python&logoColor=DFF6FF" alt="Python"> <img src="https://img.shields.io/badge/TypeScript-1F93B6?style=flat-square&labelColor=0B1220&logo=typescript&logoColor=DFF6FF" alt="TypeScript">
</div>

## talqor — 自研编译语言

用 Rust 从零实现的**原生编译**高级语言：手写 `Lexer → AST → HIR → MIR` 管线，**Cranelift JIT/AOT 与 LLVM 双后端**；类 / 结构体 / 闭包 / 迭代器 / 异常，async-await 与任务调度器；C ABI 导入与嵌入式 CPython bridge；包管理器（`talqor.toml` / lock）配自托管 registry，带 numpy / scipy / pandas 起步包；Tree-sitter grammar、LSP，以及 `run / build / repl / test / fmt / doc` 全套 CLI。

![Rust](https://img.shields.io/badge/Rust-0F3350?style=flat-square&labelColor=0B1220&logo=rust&logoColor=DFF6FF) ![Cranelift](https://img.shields.io/badge/Cranelift-134A6B?style=flat-square&labelColor=0B1220) ![LLVM](https://img.shields.io/badge/LLVM-155580?style=flat-square&labelColor=0B1220) ![JIT + AOT](https://img.shields.io/badge/JIT%20%2B%20AOT-176285?style=flat-square&labelColor=0B1220) ![CPython bridge](https://img.shields.io/badge/CPython%20bridge-1B7A9E?style=flat-square&labelColor=0B1220) ![Tree-sitter + LSP](https://img.shields.io/badge/Tree--sitter%20%2B%20LSP-1F93B6?style=flat-square&labelColor=0B1220)

> **基准** · 对 GCC 16.1.0 `-O2`：43 类基准 / 129 个工作量点 / 9675 次计时；96 个语义等价点的几何均值 **0.8451**，剔除 6 类由字符串构造与数学库主导的项后 **≈0.98**。LLVM 路径的构建时间与峰值内存为 Cranelift 路径的 **2.0× / 1.7×**。

## 上游贡献

| 上游 | 修复 | 状态 |
| --- | --- | --- |
| **lz4**<br><sub>GB/s 级实时压缩事实标准 · Linux 内核 / Android / ZFS 内置，数十亿设备在跑</sub> | HC `continue_destSize` 部分消费后的流状态损坏——官方 changelog 单独致谢 | ![](https://img.shields.io/badge/credited-1F7A54?style=flat-square&labelColor=0B1220) |
| **redis-rs**<br><sub>Rust 生态事实标准的 Redis 客户端</sub> | cluster-async ASKING 失败传播与重定向路由重置 #2305 / #2306 | ![](https://img.shields.io/badge/merged-1F7A54?style=flat-square&labelColor=0B1220) |
| **libcoap**<br><sub>IoT 通信协议 CoAP（RFC 7252）的主流 C 实现</sub> | OSCORE CBOR 大计数导致的无限循环 #2109 | ![](https://img.shields.io/badge/merged-1F7A54?style=flat-square&labelColor=0B1220) |
| **openmls**<br><sub>IETF 端到端加密群聊标准 MLS（RFC 9420）主流 Rust 实现</sub> | MemoryStorage 提案队列残留 #2163（#2165 / #2166 因上游裁撤 DS crate 关闭） | ![](https://img.shields.io/badge/merged-1F7A54?style=flat-square&labelColor=0B1220) |
| **nginx**<br><sub>全球三分之一的网站跑在它上面</sub> | 空 `X-Forwarded-For` 读越界 · slice 滤镜 `Content-Range` 有符号溢出（UBSan 复现） | ![](https://img.shields.io/badge/open-1E5B82?style=flat-square&labelColor=0B1220) |
| **systemd**<br><sub>主流 Linux 发行版的 1 号进程</sub> | journal-remote 大文件上传边界与断点续传健壮性（多轮 review） | ![](https://img.shields.io/badge/open-1E5B82?style=flat-square&labelColor=0B1220) |
| **esp-idf**<br><sub>乐鑫 ESP32 系列官方开发框架</sub> | 边界校验 #19381–#19383：UART 队列长度 · OTA 分区数上界 · flash 读取越界 | ![](https://img.shields.io/badge/open-1E5B82?style=flat-square&labelColor=0B1220) |
| **oxc**<br><sub>高性能 JS 工具链（Rust 实现）</sub> | minifier / parser / regex / checker 共 22 个修复 | ![](https://img.shields.io/badge/open-1E5B82?style=flat-square&labelColor=0B1220) |
| openssl · micropython · libsql · hyper · nghttp3 | 安全审计、边界与并发修复 | ![](https://img.shields.io/badge/partial-3F5A6E?style=flat-square&labelColor=0B1220) |

## 项目

<table>
<tr>
<td width="50%" valign="top">
<b>NandRX Tracker</b><br>
<sub>物理教学视频运动分析 · 本地优先</sub><br><br>
旋转感知自动跟踪 <b>ORB + Affine RANSAC + Rotated ZNCC</b>；导入 → 坐标标定 → 自动跟踪 → 运动分析 → CSV/JSON，自有 <code>.mtrk</code> 工程格式。FastAPI + OpenCV 后端，React + TypeScript 前端。
</td>
<td width="50%" valign="top">
<b>Building Zero</b><br>
<sub>400 智能体的垂直校园仿真</sub><br><br>
10 层综合楼、400 名日程驱动智能体；双楼梯 + 三电梯跨层 A*；<b>LLM 驱动决策</b>（优先级 / 并发 / 超时 fallback / IndexedDB 回放）；昼夜、雨天与程序化环境声；Tauri 2 桌面版（NSIS / MSI）。
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b>lexy-simlab</b><br>
<sub>中文本地三维仿真工作台</sub><br><br>
基本体 / 草图拉伸 / STEP 导入建模；内置 <b>2D 稳态导热</b>与<b>二维静电场</b>求解器及原生热学 CLI；场分布可视化，工程可保存重开。Three.js 画布，纯本地运行。
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/freedom-winds/CodexMux">CodexMux</a></b><br>
<sub>OpenAI Codex 运行时模型路由</sub><br><br>
Codex 与 NewAPI 之间的本地控制平面：逻辑模型名保持稳定，按健康状态为每次请求挑选物理模型，<b>输出开始前完成故障转移</b>，跨不兼容模型 API 适配推理参数；带可视化路由编辑器，单文件 EXE 免安装运行。
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/freedom-winds/newapi-antiAnti">newapi-antiAnti</a></b><br>
<sub>new-api 内容审核管理面板</sub><br><br>
Go 单二进制<b>独立服务</b>，直连 new-api 的 PostgreSQL，为内容审核补丁提供 Web 面板：抽检配置与记录、违规检出统计、被标记对话的人工复核；<b>不修改 new-api 任何代码</b>，脚本一键部署。
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/freedom-winds/typeFlow">typeFlow</a></b><br>
<sub>键盘行为记录与统计</sub><br><br>
Windows 托盘应用，后台记录键盘输入：SQLite 本地存储，完整历史 <b>AES-GCM 加密</b>；仪表盘展示按键频次、打字速率与活跃时段统计。
</td>
</tr>
</table>

## 统计

<p align="center">
<img width="100%" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=freedom-winds&theme=github_dark" alt="Profile details">
</p>
<p align="center">
<img height="150" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=freedom-winds&theme=github_dark" alt="Languages by repo">
<img height="150" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=freedom-winds&theme=github_dark" alt="Languages by commit">
<img height="150" src="https://streak-stats.demolab.com?user=freedom-winds&hide_border=true&border_radius=6&background=0D1117&border=30363D&stroke=30363D&ring=22D3EE&fire=2FA8C9&currStreakNum=E8FBFF&currStreakLabel=7FD8EE&sideNums=E8FBFF&sideLabels=7FD8EE&dates=5C8BA1" alt="Streak">
</p>

<!-- 备选：github-readme-stats 官方实例当前返回 DEPLOYMENT_PAUSED，恢复后可用：
<img height="160" src="https://github-readme-stats.vercel.app/api?username=freedom-winds&show_icons=true&hide_border=true&bg_color=0D1117&title_color=22D3EE&text_color=C9E7F5">
-->

<details>
<summary>全部上游 PR</summary>

<br>

| 仓库 | PR |
| --- | --- |
| [nginx](https://github.com/nginx/nginx) | #1942 slice `Content-Range` 有符号溢出 · #1946 空 `X-Forwarded-For` 读越界（open） |
| [systemd](https://github.com/systemd/systemd) | #44702 journal-remote 大文件上传边界与断点续传（open，多轮 review） |
| [esp-idf](https://github.com/espressif/esp-idf) | #19381–#19383 UART / OTA / flash 边界校验修复（open） |
| [openmls](https://github.com/openmls/openmls) | #2163 **merged** · #2165 / #2166 MLS 协议修复（closed，上游裁撤 DS/CLI crate）· #2164 closed |
| [redis-rs](https://github.com/redis-rs/redis-rs) | #2305 / #2306 **merged** · #2307 closed |
| [libcoap](https://github.com/obgm/libcoap) | #2109 **merged** |
| [oxc](https://github.com/oxc-project/oxc) | minifier / parser / regex / checker 共 22 个修复 PR |
| [gopcua/opcua](https://github.com/gopcua/opcua) | #892 Variant 负长度校验 · #893 Variant 维度分配上界（open）· #891 closed |
| [hyper](https://github.com/hyperium/hyper) | #4160 FFI 替换值时的头顺序 · #4161 拒绝禁用 trailer 字段（open） |
| [nghttp3](https://github.com/ngtcp2/nghttp3) | #549 QPACK Required Insert Count 除零（open）· #547 / #548 closed |
| [micropython](https://github.com/micropython/micropython) | #19812 IOBase write 传 memoryview（open）· #19811 closed |
| [libsql](https://github.com/tursodatabase/libsql) | #2303 legacy HTTP savepoint 检查 · #2304 cursor step_end 反序列化（open） |
| [lz4](https://github.com/lz4/lz4) | #1935 `continue_destSize` 流状态损坏（维护者确认并以独立补丁修复，随 v1.11.0 发布，changelog 致谢 @freedom-winds）· #1936 closed |
| rust-sdk · modrinth/code · openssl | 边界、生命周期与解压路径修复（closed / 部分合并） |

</details>

<!-- 论文展示块：决定公开后取消注释
## 论文

**talqor：面向原生编译高级语言的编译器开销消除研究**（2026-11）
43 类基准 / 129 个工作量点 / 9675 次有效计时 vs GCC 16.1.0 -O2，96 个语义等价点几何均值 0.8451。
-->
