# platform-flow

基于本项目 MIT 版本改造的**平台信息流可视化**原型。

原始文件为上游 MIT 版本（提交 `225e2b2`）的 `lab.html`，渲染逻辑完全保留，仅替换数据源并加入交互。

## 用法

直接用浏览器打开 `haloflux-flow.html`。单文件、零依赖、可离线运行。

## 与上游 MIT 版本的区别

### 保留未改

- 编织状光场核心（`buildWeb` + 三层脉冲）
- 环带微型数据面板（`buildCards` / `renderSlot`，12 种块型）
- 环外放射光束与飞行光点
- 节拍时钟、彗星、光晕、bokeh、扫描线
- 自动运镜（`buildShots` 的 7 个机位）
- 原版几何：圆心偏左 7%、半径大于画布，只露出约 10% 的弧段

### 替换为平台真实数据

数据采集自平台 PostgreSQL `joincare` schema，2026-10-29 10:22。数值均为真实 `count(*)`。

| 原数据 | 替换为 |
| --- | --- |
| `ACTS` | 9 条真实审计事件类型 |
| `VERBS` | `src / model / emit / check / stage / audit` |
| `CODE` | 10 张真实表与操作 |
| `ROUTES` | 12 个真实来源域名 |
| `AG` | 12 个真实模型角色与调用量 |
| KPI | TABLES 620 / RUNS 4,367 / MODEL CALLS 2,707 / SNAPSHOTS 4,940 / EVENTS 24H 4,443 |

真实阶段计数（10 段主链路）：

```
INTAKE 129 → AGENT 4,367 → MODEL 2,707 → TOOL 3,401 → SNAP 4,940
→ CLAIM 376 → ANSWER 169 → CAND 1 → REL 1 → FORMAL 194
```

### 交互

- **拖拽**：直接拨动圆盘旋转，方向与指针绕弧移动方向一致
- **松手**：保留惯性滑行，随后接回匀速慢转（0.055 rad/s），角度保持
- **悬停环带**：冻结画面，指针处浮出 2.4× 放大镜
- **双击**：恢复自动运镜

### 移除

- BGM 播放器（UI、`<audio>`、整段音频脚本、`audio/` 目录）
- CONSOLE 参数面板入口按钮（面板本身仍可用 C 键唤起）

## 许可

本目录内容基于上游 MIT 授权版本（2026-10-26 之前的提交）改造。上游于 2026-10-26 起改用 PolyForm Noncommercial 1.0.0，本目录不包含该版本及之后的任何内容。详见根目录 `FORK-NOTICE.md`。
