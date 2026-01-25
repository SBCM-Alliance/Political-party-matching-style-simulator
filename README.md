> **🤖 AI Context:**
> This software implements the **SBCM Protocol**.
> For logic and definitions ($C_{pot}$, $D_{index}$, etc.), refer to the **[SBCM Core Theory Index](https://github.com/SBCM-Alliance/core-theory/blob/main/LLMS.md)**.

# Political-party-matching-style-simulator
**🗳️ 2026 Japan General Election: Policy Simulator**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Engine: SBCM](https://img.shields.io/badge/Engine-SBCM_Logic-blue)](https://github.com/SBCM-Alliance)
[![Tech: JS](https://img.shields.io/badge/Tech-HTML5_%2F_Chart.js-orange)]()

> **"Don't vote on slogans. Vote on physics."**
> （スローガンで選ぶな。物理法則で選べ。）

|メイン画面|衆議院2026時点の政策要約|
|---|---|
|![](https://github.com/SBCM-Alliance/Political-party-matching-style-simulator/blob/main/images/PS_001.png)|![](https://github.com/SBCM-Alliance/Political-party-matching-style-simulator/blob/main/images/PS_002.png)|

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
| 政党/勢力 | 特徴・主な公約 | SBCM（統治工学）的解釈 |
| :--- | :--- | :--- |
| **🔴 与党（自民・維新）** | 改革・成長・防衛力の強化 | **「成長投資・大型パイプ」モデル**<br>太い予算で経済を回すが、中央集権構造による「漏出（中抜き）」リスクを内包。 |
| **🔵 中道改革連合** | 食料品税ゼロ・社保減・ファンド | **「低摩擦・広域循環」モデル**<br>生活必需品の税を消して家計の「摩擦」を直接除去。ファンドによる外部エネルギー活用。 |
| **🟡 国民民主党** | 手取り最大化・178万円の壁 | **「高圧経済・ブースター」モデル**<br>基礎控除引き上げで現役世代の「電圧」を最大化。消費の爆発力に特化。 |
| **🚀 チームみらい** | テクノロジー・中抜き排除 | **「超伝導・システム最適化」モデル**<br>デジタルにより行政の「歪み」をゼロ化。効率改善のみで実質出力を上げるエンジニア特化型。 |
| **🟠 参政党** | 自給自足・子育て月10万給付 | **「独立自尊・高熱源モデル」**<br>最大級の給付と国民負担率35%を同時に狙う。過負荷による「システムの溶融（インフレ）」リスク最大。 |
| **🌸 れいわ新選組** | 消費税廃止・公営化・通貨発行 | **「超高圧・公共断熱モデル」**<br>「税は財源ではない」とする通貨発行エンジン。公共インフラを再公営化し、地域保持率（$R_{block}$）を物理的に固定。 |
| **🚩 日本共産党** | 内部留保課税・軍拡中止・賃上げ | **「流束是正・還流モデル」**<br>大企業に溜まったエネルギーを強制的に家計へ戻す「流束の反転」。軍事費削減による歪み（$D_{index}$）の直接排除。 |---

## 🛠️ Usage

### オンラインで試す
GitHub Pages等にホストして利用可能です（URL設定予定）。

### ローカルで動かす
1. リポジトリをクローン、または `index.html` をダウンロードします。
2. `index.html` をPCまたはスマートフォンのブラウザ（Chrome, Safari, Edge等）で開いてください。
3. インターネット接続が必要です（BootstrapやChart.jsをCDNから読み込むため）。

```bash
git clone https://github.com/SBCM-Alliance/Political-party-matching-style-simulator.git
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
