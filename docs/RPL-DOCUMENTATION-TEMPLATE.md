# RPL Peptide — Technical Documentation Template & Standards

> 基于 Tirzepatide 文档制作经验固化，适用于所有产品

## 文档结构

### 目录树

```
[product-name]/
├── Technical Data Sheets/
│   └── [product]-technical-data-sheet.md
├── Certificates of Analysis/
│   └── [product]-coa-template.md
├── Product Specifications/
│   └── [product]-product-specifications.md
├── Safety Data Sheets/
│   └── [product]-safety-data-sheet.md
├── HPLC Library/
│   └── [product]-hplc-analysis.md
├── Mass Spectra Library/
│   └── [product]-mass-spectrometry.md
├── Storage Guides/
│   └── [product]-storage-guide.md
├── Solubility Guides/
│   └── [product]-solubility-guide.md
├── Reconstitution Guides/
│   └── [product]-reconstitution-guide.md
├── Stability Guides/
│   └── [product]-stability-guide.md
├── Analytical Methods/
│   └── [product]-analytical-methods.md
├── Quality Standards/
│   └── [product]-quality-standards.md
├── White Papers/
│   └── [product]-white-paper.md
├── Technical Bulletins/
│   └── [product]-technical-bulletin.md
├── Application Notes/
│   └── [product]-application-note.md
├── FAQ Library/
│   └── [product]-faq.md
├── Peptide Glossary/
│   └── [product]-peptide-glossary.md
├── Documentation Policy/
│   └── [product]-documentation-policy.md
├── README.md
└── [product]-complete-documentation.md    ← 合成文档
```

### 合成文档结构（单文件手册）

#### 1. 首页元信息

```
RPL Peptide

Official Technical Documentation

---

## [Product Name] Technical Manual

| Field | Value |
|-------|-------|
| **Document Title** | [Product] — Complete Technical Documentation |
| **Document ID** | RPL-TM-[PRODUCT-CODE]-001 |
| **Document Type** | Complete Technical Documentation Manual |
| **Publisher** | RPL Peptide (Qingdao RPL Biotechnology Co., Ltd.) |
| **Version** | 1.0 |
| **Revision Date** | July 2026 |
| **Status** | Current |
| **Intended Audience** | Research laboratories, procurement professionals, quality assurance teams, biotechnology organizations, and scientific researchers |
| **Scope** | [产品特定的范围描述] |
| **Keywords** | [产品关键词，逗号分隔] |
| **How to Cite This Document** | RPL Peptide. (2026). *[Product] Technical Manual* (Version 1.0). RPL Peptide Official Technical Documentation. https://rplpeptides.com |

---

## Table of Contents

| Chapter | Title |
|:-------:|-------|
| 1 | Technical Data Sheet |
| 2 | Certificates of Analysis |
| 3 | Product Specifications |
| 4 | Safety Data Sheet |
| 5 | HPLC Library |
| 6 | Mass Spectra Library |
| 7 | Storage Guide |
| 8 | Solubility Guide |
| 9 | Reconstitution Guide |
| 10 | Stability Guide |
| 11 | Analytical Methods |
| 12 | Quality Standards |
| 13 | White Paper |
| 14 | Technical Bulletin |
| 15 | Application Notes |
| 16 | FAQ Library |
| 17 | Peptide Glossary |
| 18 | Documentation Policy |
```

#### 2. 正文组织方式（Chapter 1–18）

每个 Chapter 以 `# Chapter N: Title` 开头，去掉原始单文件中的 H1 标题（避免重复）。内容完整保留。

#### 3. 页尾

```
---

© 2026 RPL Peptide

Official Technical Documentation

rplpeptides.com
```

### 每份单文件标准

**Top (every individual doc):**
```
RPL Peptide

Official Technical Documentation

[Document Type]
```

**Bottom (every individual doc):**
```
© 2026 RPL Peptide

Official Technical Documentation

rplpeptides.com
```

## 关键规范

### ✅ 内容规范

| 文档类型 | 必须包含 |
|----------|---------|
| **Technical Data Sheet** | 产品概述、规格表、分子特征、QA方法、复溶协议、免责声明 |
| **COA (模版)** | 批号信息、分析结果表、QC审核、签名栏 + ⚠️ 提示「此为展示模版，具体批次COA请联系RPL工作人员」 |
| **Product Specs** | 通用信息、物化性质、纯度规格、包装规格、储存/运输条件 |
| **SDS** | GHS 16 节标准格式 |
| **HPLC / Mass Spec** | 方法参数、验收标准、批次数据占位符 |
| **Storage / Solubility / Reconstitution / Stability** | 步骤化流程、数据表、故障排查、注意事项 |
| **White Paper** | 摘要、引言、技术正文（含子节）、参考文献 |
| **Application Note** | 实验方案、材料清单、预期结果、数据分析 |
| **FAQ** | 产品信息、质量文档、操作存储、采购供应、研究应用 |
| **Glossary** | A–Z 术语表，每个词条含定义 |
| **Documentation Policy** | 政策声明、范围、结构标准、版本控制、审批流程、分发、保留 |

### ❌ 禁止项（GitHub 提交前检查清单）

- [ ] 无 `[source: N]` 或类似 AI 引用标记
- [ ] 无 `as an AI` / `I am an AI` / `AI-generated` 字眼
- [ ] 无未被解析的模版占位符（COA 中 `[Batch Number]` 类占位符允许保留，因为是模板）
- [ ] 合成文档中无重复 H1 标题（每个 Chapter 一个 H1）
- [ ] 合成文档中无残留的节标题如 `---` `---` 空分隔块
- [ ] 合成文档头尾品牌标识各仅一次（非每节重复）
- [ ] COA 模板中必须标注「此为展示模板」提示
- [ ] 文件命名统一小写 + 连字符
- [ ] 全英文

## 后续产品执行步骤

1. 读取产品链接/资料，提取规格数据
2. 生成 18 份独立文档（按目录树存放）
3. 运行脚本合成单文件手册（带首页元信息 + 18 Chapter + 页尾）
4. 执行清理检查（AI 标记、重复 H1、残留品牌头尾）
5. 发送确认
