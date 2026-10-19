# OpenRouter - 费用趋势看板

与 `API-Cost-Dashboard` 同结构，数据来自飞书 **AI-平台消耗 → openrouter**（单位：美元，截至 **10/12**）。

**统计口径**：顶部 KPI、瀑布、占比、明细表合计仅含 **Flux + LLM-openrouter**。**LLM-novita 不计入**，仅在下方「LLM 日耗对比」图展示。

## 文件

- `OpenRouter-Cost-Dashboard.html`：看板本体。用浏览器打开，改数后 **Ctrl+F5** 强刷。

## 飞书列与看板费用项

| 看板费用项 | 飞书列 |
|-----------|--------|
| Flux | Flux |
| LLM · OpenRouter | LLM-openrouter（与 LLM 列一致） |
| LLM · Novita | LLM-novita |

- **余额**：第 2 行「账户余额」— Flux 列 / LLM 列（当前 Flux 67.35、LLM 1502.22）
- **10 月累计**：10/1–10/12（飞书 10 月「合计」行；10/13 起为空，不计入）
- **9 月同期**：9/1–9/12 逐日加总
- **9 月整月**：9 月「合计」行
- **整月预估**：`mtd ÷ 12 × 31`

## 更新

飞书改数 → 编辑 HTML 内 `platforms` → 保存 → 同步 `openrouter-看板.html`（若需要）→ 浏览器强刷。
