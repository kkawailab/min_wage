# 最低賃金マップ 2024

[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-blue)](https://kkawailab.github.io/min_wage/min_wage_leaflet.html)

2024年度の都道府県別最低賃金を地図上に可視化するWebアプリケーションです。

## デモ

**[アプリを起動する](https://kkawailab.github.io/min_wage/min_wage_leaflet.html)**

ブラウザで上記リンクにアクセスすると、すぐに地図を閲覧できます。

## 概要

このアプリケーションは、日本全国47都道府県の最低賃金（時給）をインタラクティブな地図上で確認できます。

### 主な機能

- **色分け表示**: 最低賃金の金額に応じて都道府県を色分け表示
- **インタラクティブ**: 都道府県にマウスをホバーすると詳細情報を表示
- **ポップアップ**: クリックすると各都道府県の最低賃金を表示
- **全国平均表示**: 全国加重平均（1,055円）を表示
- **レスポンシブデザイン**: PCやスマートフォンで閲覧可能

### 技術スタック

- **Leaflet.js**: インタラクティブ地図ライブラリ
- **OpenStreetMap**: 背景地図データ
- **Geolonia/japanese-admin-boundaries**: 都道府県境界データ（GeoJSON）

## クイックスタート

このアプリケーションは純粋なHTML/CSS/JavaScriptで作成されており、特別なインストールや依存関係は不要です。

### オンラインで使用

**[GitHub Pages版](https://kkawailab.github.io/min_wage/min_wage_leaflet.html)** にアクセスするだけで、すぐに利用できます。

### ローカルで使用

```bash
# リポジトリをクローン
git clone https://github.com/kkawailab/min_wage.git
cd min_wage

# ブラウザで開く
open min_wage_leaflet.html  # macOS
xdg-open min_wage_leaflet.html  # Linux
start min_wage_leaflet.html  # Windows
```

または、`min_wage_leaflet.html`をブラウザにドラッグ&ドロップしてください。

#### ローカルサーバーで起動（推奨）

より安定した動作のために、ローカルサーバーで起動することをお勧めします。

```bash
# Pythonを使用する場合
python -m http.server 8000

# Node.jsのhttp-serverを使用する場合
npx http-server
```

ブラウザで `http://localhost:8000/min_wage_leaflet.html` にアクセスしてください。

## 使い方

1. 地図が表示されたら、任意の都道府県にマウスカーソルを合わせます
2. 右上のパネルに選択した都道府県の最低賃金が表示されます
3. 都道府県をクリックすると、ポップアップで詳細情報が表示されます
4. 左下の凡例で色と金額の対応関係を確認できます

## データ出典

- **最低賃金データ**: 厚生労働省（2024年度）
- **境界データ**: Geolonia/japanese-admin-boundaries（MIT License）、OpenStreetMap

## トラブルシューティング

### 地図が表示されない場合

- インターネット接続を確認してください（外部CDNやGeoJSONデータの取得に必要）
- ブラウザの開発者コンソール（F12）でエラーメッセージを確認してください

### 色分けが正しく表示されない場合

- ブラウザの開発者コンソール（F12）を開いて、各都道府県のデータが正しく読み込まれているか確認してください
- `Prefecture:` と `Value:` のログが表示されます

## ライセンス

このプロジェクトは個人利用・学習目的で作成されています。
