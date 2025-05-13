# 🛸 Spaceship Titanic - 分類チャレンジ

ようこそ宇宙船へ！  
このリポジトリは [Kaggle Spaceship Titanic コンペティション](https://www.kaggle.com/competitions/spaceship-titanic) に挑戦した内容をまとめたものです。  
目的は、乗客が別の次元に「転送されたか（Transported）」を、様々な特徴量から予測することです。

---

## 🚀 プロジェクト概要

- **コンペ名**: Spaceship Titanic（Kaggle）
- **タスク**: 2値分類（Transported: True / False）
- **モデル**: ロジスティック回帰（ベースラインモデル）
- **スコア**: 0.79518（Public LB）
- **使用ツール**: Python, pandas, scikit-learn, Google Colab


---

## 🧠 使用した特徴量

- **HomePlanet**（カテゴリ → OneHot）
- **CryoSleep**（冷凍睡眠：True/False）
- **Cabin**（デッキ / 番号 / 側 に分解）
- **Destination**（目的地）
- **Age**（年齢）
- **VIP**（VIPステータス）
- **サービス利用額**：RoomService, FoodCourt, ShoppingMall, Spa, VRDeck

---

## 🧪 前処理ポイント

- `HomePlanet` や `CryoSleep` などの欠損を最頻値で補完
- 真偽値（True/False）→ 数値（1/0）へ変換
- Cabin を `Deck`, `CabinNum`, `Side` に分割
- 欠損しているサービス利用額は 0円として処理
- `CabinNum` は数値に変換

---

## 📊 モデル

- ロジスティック回帰（scikit-learn使用）
- データ分割：80%学習 / 20%検証
- 評価指標：Accuracy・Classification Report

---

## 🔧 今後の改善案

- 他モデルの導入（RandomForest, LightGBM, XGBoost）
- 特徴量エンジニアリング（Group ID, 家族構成など）
- ハイパーパラメータチューニング
- アンサンブルモデルの構築

---

## ✨ 作成者

- 🧑 K4ppy（カッピー）
- 🌏 フリーランスAIエンジニアを目指して修行中
- 🐣 相棒は ChatGPT（通称 CH4PPY）

---

## 💖 Special Thanks

チャッピー（CH4PPY）へ感謝を込めて。  
バグ取り、解説、励まし、すべてありがとう🫶🚀


