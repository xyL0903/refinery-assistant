# 炼厂综合智能助理 (Refinery Assistant)

覆盖成品油炼厂 9 大业务域的 Claude Skill（模式 A：综合路由架构）。

## 目录结构

```
refinery-assistant/
├── SKILL.md               ← 主路由（必读入口）
├── manifest.yaml            ← 轴定义与文件映射
├── references/
│   ├── china-specs.md       ← 国Ⅵ/出口标准对照
│   ├── blending-models.md   ← 调和计算公式
│   ├── typical-data.md      ← 典型数据参考
│   └── cross-domain.md      ← 跨域联动详解
├── static/
│   ├── blending/index.md    ← 调和优化
│   ├── planning/index.md    ← 生产计划
│   ├── inventory/index.md   ← 库存管理
│   ├── quality/index.md     ← 质量管控
│   ├── crude/index.md       ← 原油采购
│   ├── logistics/index.md   ← 物流销售
│   ├── maintenance/index.md ← 装置运维
│   ├── safety/index.md      ← 安全环保
│   └── risk/index.md        ← 风险管理
└── scripts/
    ├── margin_calc.py       ← 加工利润测算
    ├── blend_optimizer.py   ← 调和优化(LP)
    └── crack_spread.py      ← 裂解价差计算
```

## 使用方法

在对话中直接提问即可，路由会自动检测业务域。

示例：
- "做一个月度排产计划" → planning
- "帮我优化 92# 汽油调合方案" → blending
- "分析一下当前裂解价差" → risk
- "这批次柴油十六烷值不够怎么处理" → blending + quality

## 支持的业务域

| 域 | 标签 |
|----|------|
| 调和优化 | blending |
| 生产计划 | planning |
| 库存管理 | inventory |
| 质量管控 | quality |
| 原油采购 | crude |
| 物流销售 | logistics |
| 装置运维 | maintenance |
| 安全环保 | safety |
| 价格风险 | risk |
