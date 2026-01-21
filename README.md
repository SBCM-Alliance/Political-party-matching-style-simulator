
# Political-party-matching-style-simulator
**🗳️ 2026 Japan General Election: Policy Simulator**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Engine: SBCM](https://img.shields.io/badge/Engine-SBCM_Logic-blue)](https://github.com/SBCM-Alliance)
[![Tech: JS](https://img.shields.io/badge/Tech-HTML5_%2F_Chart.js-orange)]()

> **"Don't vote on slogans. Vote on physics."**
> （スローガンで選ぶな。物理法則で選べ。）

## 📖 Overview

これは従来の「政党マッチング」ではありません。**「政策熱力学シミュレーター」**です。
ユーザーが入力した政策（税率、財政出動、社会保障など）が、5年後の日本経済にどのような物理的影響（手取り、インフレ、行政の歪み）を与えるかをリアルタイムで計算し、その結果が「どの政党のシナリオに近いか」を判定します。

**SBCM（Standard Block Comparison Method / 標準ブロック比較法）** の理論に基づき、財源の魔法を否定し、「痛み」と「恩恵」のトレードオフを可視化します。

## 🚀 Features

*   **物理法則ベースの計算:** 「痛みの保存則」「漏出の定理」などのSBCM理論を用いた簡易モデルにより、政策の副作用（インフレや将来負担）を計算。
*   **リアルタイム・シミュレーション:** スライダーを動かすだけで、5年後の「手取り年収」「インフレ率」「行政の歪み指数」がグラフに反映されます。
*   **2026年衆院選対応:** 最新の政党公約（自民・維新、国民民主、チームみらい等）のパラメータを搭載。
*   **インストール不要:** シングルHTMLファイル構成。ブラウザだけで即座に動作します（Python/PyScript不使用の軽量版）。

## ⚠️ Model limitations
計算に使っている「係数（数字）」は、あくまで仮定のモデルです。
*  **係数の恣意性:** 例えば「消費税を1%下げたら、インフレ率が0.2%上がる」という式を入れていますが、現実には0.1%かもしれないし、0.5%かもしれません。為替や原油価格にも左右されます。
*  **非線形性の欠如:** 現実は、ある一点を超えると急激に悪化する（ハイパーインフレなど）ことがありますが、この簡易プログラムではある程度リニア（直線的）に変化します。
*  **外部要因の無視:** 海外の戦争やパンデミックなどの外部要因は計算に入れていません。

## 🎛️ Simulation Logic (The Engine)

本シミュレーターは、以下の物理的制約を経済モデルに適用しています。

1.  **Conservation of Pain (痛みの保存則):**
    *   減税や社会保険料の軽減は「手取り」を増やしますが、適切な財源がない場合、「将来負担」または「インフレ」としてエネルギーが保存されます。
2.  **Theorem of Leakage (漏出の定理):**
    *   地域の供給能力（キャパシティ）を超える公共事業費の投入は、GDP成長には寄与せず、「行政の歪み（Distortion）」と「都心への資金流出（Leakage）」に変換されます。
3.  **System Optimization (システム最適化):**
    *   「チームみらい」が提唱するデジタルによる制度設計（なめらかな負担増など）は、「歪み係数」を低下させ、財政出動なしで実質手取りを向上させる効果として計算されます。

## 🗳️ Parties & Scenarios

2026年時点での主要な政治勢力の公約をパラメータ化しています。

| 政党/勢力 | 特徴 | SBCM的解釈 |
| :--- | :--- | :--- |
| **🔴 与党（自民・維新）** | 改革・成長・防衛 | 安定型だが、成長投資による格差拡大や歪みのリスクあり。 |
| **🔵 中道改革連合** | 人への投資・福祉 | 分配重視。低所得者には恩恵だが、現役世代の負担感は残る。 |
| **🟡 国民民主党** | 手取り最大化・積極財政 | 「年収の壁」撤廃による高圧経済。手取りは激増するが財政リスクも最大。 |
| **🚀 チームみらい** | テクノロジー・最適化 | デジタルによる「歪み」の除去。派手さはないが最も持続可能な成長。 |
| **🟣 野党共闘（共・れ）** | 消費税廃止・反緊縮 | 短期的な快楽（減税）と引き換えに、熱的死（ハイパーインフレ）を招く。 |

## 🛠️ Usage

### オンラインで試す
GitHub Pages等にホストして利用可能です（URL設定予定）。

### ローカルで動かす
1. リポジトリをクローン、または `index.html` をダウンロードします。
2. `index.html` をPCまたはスマートフォンのブラウザ（Chrome, Safari, Edge等）で開いてください。
3. インターネット接続が必要です（BootstrapやChart.jsをCDNから読み込むため）。

```bash
git clone https://github.com/YourName/Political-party-matching-style-simulator.git
open index.html
```

## 📂 File Structure

```
Political-party-matching-style-simulator/
│
├── index.html      # シミュレーター本体 (HTML/CSS/JS All-in-One)
└── README.md       # このドキュメント
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Acknowledgments

*   **SBCM Alliance:** For the foundational theory of Governance Engineering.
*   **Election 2026 Reports:** For the policy data sources.

---
*Disclaimer: このシミュレーターは物理モデルに基づく試算であり、特定の政党への投票を推奨または妨害するものではありません。投票はご自身の判断で行ってください。*
