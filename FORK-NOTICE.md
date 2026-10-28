# FORK-NOTICE — 本 fork 的来源、许可证基线与范围

本仓库是 [Ryder191/haloflux](https://github.com/Ryder191/haloflux) 的 fork。
除本文件外，仓库内容与上游提交 `225e2b2862b3d64ae9f6e0b012b27ccbe004e3d0` 完全一致，未做任何修改。

## 1. 为什么以该提交为基线

上游在 2026-10-26 将许可证从 MIT 更换为 PolyForm Noncommercial 1.0.0（提交 `5c1992a`，当前上游 `main`）。
上游 LICENSE 中明确记载：

> Earlier history: commits dated before 2026-10-26 were published under the MIT License.
> Starting 2026-10-26, this project and every later version are licensed only under the terms below.

因此 **2026-10-26 之前的提交仍按 MIT 授权**，可以完整地使用、修改、再分发。本 fork 固定在该日期前最后一个提交。

| 提交 | 日期 | 许可证 |
| --- | --- | --- |
| `5c1992a`（上游当前 `main`） | 2026-10-26 | PolyForm Noncommercial 1.0.0 |
| `225e2b2`（本 fork 基线） | 2026-10-23 | MIT |
| `7709cd2`（首个提交） | 2026-10-21 | MIT |

## 2. 覆盖范围

基线快照中的全部内容均处于 MIT 或更宽松条款下：

| 路径 | 内容 | 许可证 |
| --- | --- | --- |
| `LICENSE` | MIT 许可证全文 | MIT |
| `README.md` | 项目说明（MIT 时期版本） | MIT，随代码 |
| `index.html` | 入口页，按设备跳转 | MIT |
| `lab.html` | 桌面控制台版 | MIT |
| `mobile.html` | 移动端兼容版 | MIT |
| `wallpaper/` | Wallpaper Engine 网页壁纸版（`index.html`、`wp.js`、`project.json`、`preview.jpg`、`audio/`） | MIT |
| `audio/sw421k.mp3` | "Synthwave 421k" — The Cynic Project (cynicmusic) | CC0（作者以公共领域贡献发布，不受上游许可证条款约束） |
| `preview.png` | 预览图 | MIT，随代码 |

音乐为 CC0，比 MIT 更宽松，可自由使用、修改与再分发。

## 3. 本 fork 不包含的内容

上游 2026-10-26 及之后的版本（提交 `5c1992a` 起：LICENSE 更换、README 与源码中新增的 PolyForm 声明，以及任何后续提交）**不在本仓库中，也不在本 fork 的授权范围内**。如需这些内容，须另行取得版权持有人的授权。

## 4. MIT 义务的保留

MIT 许可证要求在所有副本或实质性部分中保留版权声明与许可声明。本仓库保留：

- `LICENSE`：原始 MIT 许可证全文，含版权行 `Copyright (c) 2026 RYDER CODE / Ms MAIKEBAIs CAT`。
- 各 HTML 文件与 `wallpaper/wp.js` 的原始内容未改动。

再分发或修改后发布时，请一并保留上述版权与许可声明。

## 5. 上游仓库跟踪

本 fork 保留了 `upstream` 远端，指向 `https://github.com/Ryder191/haloflux.git`，另存有本地分支 `upstream-polyform` 指向上游 PolyForm 版本的提交，便于对照查阅；该分支内容不在本 fork 的授权范围内。

```sh
git fetch upstream
git log --oneline upstream/main
```

## 6. 说明

本文件是本 fork 为记录基线来源与许可范围而新增，不改变上游代码的任何许可证状态，也不对上游作品作出超出其原作者授权范围的声明。
