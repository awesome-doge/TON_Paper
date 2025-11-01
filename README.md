# The Open Network Whitepaper Translation Project
# The Open Network 白皮書翻譯專案

[![Build and Release PDFs](https://github.com/awesome-doge/TON_Paper/actions/workflows/build_and_release.yml/badge.svg)](https://github.com/awesome-doge/TON_Paper/actions/workflows/build_and_release.yml)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/awesome-doge/TON_Paper)
![GitHub contributors](https://img.shields.io/github/contributors/awesome-doge/TON_Paper)
![GitHub issues](https://img.shields.io/github/issues/awesome-doge/TON_Paper)
![GitHub pull requests](https://img.shields.io/github/issues-pr/awesome-doge/TON_Paper)
![GitHub license](https://img.shields.io/github/license/awesome-doge/TON_Paper)

[English](#english) | [繁體中文](#繁體中文)

---

## English

This repository provides high-quality Traditional Chinese (Taiwan) translations of The Open Network (TON) whitepapers and technical documentation, making these essential blockchain resources accessible to the Chinese-speaking community worldwide.

### What is TON?

The Open Network (TON) is a decentralized blockchain platform designed for fast, secure, and scalable applications. Originally developed by Telegram, TON features a unique multi-blockchain architecture with infinite sharding capability.

### Translation Status

All five main technical documents have been successfully translated to Traditional Chinese (Taiwan):

- ✅ **TON** (133 pages PDF) - Main whitepaper describing the Telegram Open Network architecture
- ✅ **TVM** (144 pages PDF) - TON Virtual Machine specification and instruction set
- ✅ **Tblkch** (2,329 lines) - TON blockchain specification and protocol details
- ✅ **Catchain** - Byzantine Fault Tolerant consensus protocol documentation
- ✅ **Fiftbase** (2,205 lines) - Fift programming language documentation

### Available Documents

All documents are available in both English and Traditional Chinese (Taiwan):

| Document | Description | English | 繁體中文 |
|----------|-------------|---------|---------|
| **TON** | Main TON whitepaper | [TEX](en_ton.tex) • [PDF](en_ton.pdf) | [TEX](tw_ton.tex) • [PDF](tw_ton.pdf) |
| **TVM** | TON Virtual Machine specification | [TEX](en_tvm.tex) • [PDF](en_tvm.pdf) | [TEX](tw_tvm.tex) • [PDF](tw_tvm.pdf) |
| **Tblkch** | TON blockchain specification | [TEX](en_tblkch.tex) • [PDF](en_tblkch.pdf) | [TEX](tw_tblkch.tex) • [PDF](tw_tblkch.pdf) |
| **Catchain** | Byzantine Fault Tolerant consensus | [TEX](en_catchain.tex) • [PDF](en_catchain.pdf) | [TEX](tw_catchain.tex) • [PDF](tw_catchain.pdf) |
| **Fiftbase** | Fift language documentation | [TEX](en_fiftbase.tex) • [PDF](en_fiftbase.pdf) | [TEX](tw_fiftbase.tex) • [PDF](tw_fiftbase.pdf) |

### Download Compiled PDFs

Pre-compiled PDF versions of all documents are available in the [Releases](https://github.com/awesome-doge/TON_Paper/releases) section. PDFs are automatically generated and published whenever changes are pushed to the main branch.

### Building PDFs Locally

#### Prerequisites

You'll need XeLaTeX with Chinese font support. On Ubuntu/Debian:

```bash
sudo apt-get update -qq
sudo apt-get install -y texlive-latex-base texlive-fonts-recommended \
    texlive-fonts-extra texlive-latex-extra texlive-science \
    texlive-xetex texlive-lang-chinese fonts-wqy-microhei
```

#### Compile Individual Document

Run XeLaTeX three times to properly generate the table of contents and references:

```bash
xelatex tw_ton.tex
xelatex tw_ton.tex
xelatex tw_ton.tex
```

#### Compile All Documents

```bash
for file in en_ton en_tvm en_tblkch en_catchain en_fiftbase \
            tw_ton tw_tvm tw_tblkch tw_catchain tw_fiftbase; do
  xelatex "$file.tex"
  xelatex "$file.tex"
  xelatex "$file.tex"
done
```

#### Clean Build Artifacts

```bash
rm -f *.aux *.log *.out *.toc *.gz *.xdv *.fls *.fdb_latexmk
```

### Project Structure

```
TON_Paper/
├── en_*.tex              # English LaTeX source files
├── tw_*.tex              # Traditional Chinese LaTeX source files
├── *.pdf                 # Generated PDFs (auto-compiled by CI)
├── .github/workflows/    # GitHub Actions CI/CD configuration
└── README.md             # This file
```

### CI/CD Automation

This repository uses GitHub Actions to automatically:

1. Compile all `.tex` files to PDFs when pushed to the `main` branch
2. Commit generated PDFs back to the repository
3. Create timestamped releases with all PDF artifacts

See [`.github/workflows/build_and_release.yml`](.github/workflows/build_and_release.yml) for details.

### Additional Documentation

The repository includes supplementary technical guides:

- Node Operation: `Validator-HOWTO`, `FullNode-HOWTO`, `LiteClient-HOWTO`
- Services: `DNS-HOWTO`, `TonSites-HOWTO`
- Configuration: `ConfigParam-HOWTO`, `TestGrams-HOWTO`
- Development: `smc-guidelines.txt`, `catchain-dos.md`

### Contributing

We welcome contributions of all kinds! Whether improving translations, fixing formatting, or enhancing documentation, your help is valuable. Please see our [Contributing Guidelines](CONTRIBUTING.md) before getting started.

Translation improvements are especially welcome to ensure technical accuracy and readability.

### License

This project is licensed under the [MIT License](LICENSE).

---

## 繁體中文

此專案旨在為 The Open Network (TON) 白皮書及技術文件提供高品質的繁體中文（台灣）翻譯版本，使全球華語社群能夠更容易理解這些重要的區塊鏈技術資源。

### TON 是什麼？

The Open Network (TON) 是一個為快速、安全且可擴展的應用程式而設計的去中心化區塊鏈平台。TON 最初由 Telegram 開發，具有獨特的多區塊鏈架構和無限分片能力。

### 翻譯進度

所有五份主要技術文件均已完成繁體中文（台灣）翻譯：

- ✅ **TON**（133 頁 PDF）- 描述 Telegram Open Network 架構的主白皮書
- ✅ **TVM**（144 頁 PDF）- TON 虛擬機規範與指令集
- ✅ **Tblkch**（2,329 行）- TON 區塊鏈規範與協定細節
- ✅ **Catchain** - 拜占庭容錯共識協定文件
- ✅ **Fiftbase**（2,205 行）- Fift 程式語言文件

### 可用文件

所有文件均提供英文及繁體中文（台灣）版本：

| 文件 | 說明 | English | 繁體中文 |
|------|------|---------|---------|
| **TON** | TON 主白皮書 | [TEX](en_ton.tex) • [PDF](en_ton.pdf) | [TEX](tw_ton.tex) • [PDF](tw_ton.pdf) |
| **TVM** | TON 虛擬機規範 | [TEX](en_tvm.tex) • [PDF](en_tvm.pdf) | [TEX](tw_tvm.tex) • [PDF](tw_tvm.pdf) |
| **Tblkch** | TON 區塊鏈規範 | [TEX](en_tblkch.tex) • [PDF](en_tblkch.pdf) | [TEX](tw_tblkch.tex) • [PDF](tw_tblkch.pdf) |
| **Catchain** | 拜占庭容錯共識 | [TEX](en_catchain.tex) • [PDF](en_catchain.pdf) | [TEX](tw_catchain.tex) • [PDF](tw_catchain.pdf) |
| **Fiftbase** | Fift 語言文件 | [TEX](en_fiftbase.tex) • [PDF](en_fiftbase.pdf) | [TEX](tw_fiftbase.tex) • [PDF](tw_fiftbase.pdf) |

### 下載已編譯的 PDF

所有文件的預編譯 PDF 版本可在[發布區域](https://github.com/awesome-doge/TON_Paper/releases)下載。當變更推送至主分支時，PDF 會自動生成並發布。

### 本地編譯 PDF

#### 必備條件

您需要安裝支援中文字型的 XeLaTeX。在 Ubuntu/Debian 上：

```bash
sudo apt-get update -qq
sudo apt-get install -y texlive-latex-base texlive-fonts-recommended \
    texlive-fonts-extra texlive-latex-extra texlive-science \
    texlive-xetex texlive-lang-chinese fonts-wqy-microhei
```

#### 編譯單一文件

執行 XeLaTeX 三次以正確產生目錄和參考文獻：

```bash
xelatex tw_ton.tex
xelatex tw_ton.tex
xelatex tw_ton.tex
```

#### 編譯所有文件

```bash
for file in en_ton en_tvm en_tblkch en_catchain en_fiftbase \
            tw_ton tw_tvm tw_tblkch tw_catchain tw_fiftbase; do
  xelatex "$file.tex"
  xelatex "$file.tex"
  xelatex "$file.tex"
done
```

#### 清理建置檔案

```bash
rm -f *.aux *.log *.out *.toc *.gz *.xdv *.fls *.fdb_latexmk
```

### 專案結構

```
TON_Paper/
├── en_*.tex              # 英文 LaTeX 原始檔
├── tw_*.tex              # 繁體中文 LaTeX 原始檔
├── *.pdf                 # 生成的 PDF（由 CI 自動編譯）
├── .github/workflows/    # GitHub Actions CI/CD 設定
└── README.md             # 本文件
```

### CI/CD 自動化

本專案使用 GitHub Actions 自動化：

1. 當推送至 `main` 分支時，編譯所有 `.tex` 檔案為 PDF
2. 將生成的 PDF 提交回儲存庫
3. 建立包含所有 PDF 檔案的時間戳記發布版本

詳情請見 [`.github/workflows/build_and_release.yml`](.github/workflows/build_and_release.yml)。

### 其他文件

本儲存庫包含補充技術指南：

- 節點操作：`Validator-HOWTO`、`FullNode-HOWTO`、`LiteClient-HOWTO`
- 服務：`DNS-HOWTO`、`TonSites-HOWTO`
- 設定：`ConfigParam-HOWTO`、`TestGrams-HOWTO`
- 開發：`smc-guidelines.txt`、`catchain-dos.md`

### 如何貢獻

我們歡迎各種形式的貢獻！無論是改進翻譯、修正格式或增強文件，您的協助都非常寶貴。開始之前，請先參閱我們的[貢獻指南](CONTRIBUTING.md)。

特別歡迎翻譯改進，以確保技術準確性和可讀性。

### 授權條款

本專案採用 [MIT 授權條款](LICENSE)。