# 箱入り娘パズル

Webブラウザ上で動作する「箱入り娘パズル」のサンプル実装です。  
プレイヤーは盤面上の駒を操作し、娘駒（2×2）を目標の位置（下段中央）に移動させることを目的としています。

---

## 概要

「箱入り娘パズル」はスライディングブロックパズルの一種で、指定された駒を盤面から脱出させる、もしくは所定の位置に移動させるパズルです。  
本実装では以下の特徴があります。

- **盤面構成**：  
  5行×4列のグリッドで構成された盤面を用意。  
  各セルのサイズは100px×100pxです。

- **駒の種類**：  
  - 娘（2×2、脱出目標）  
  - 父親、母親、下男、下女（1×2、縦向き）  
  - 番頭（2×1、横向き）  
  - 小僧（1×1）×4

- **初期配置**：  
  盤面上に各駒が配置され、娘駒は盤面の中央上部に位置しています。

- **操作方法**：  
  1. **駒の選択**：  
     任意の駒をクリックすると、その駒が選択状態になり、赤枠でハイライトされます。  
  2. **移動操作**：  
     選択した駒をドラッグして、上下左右の隣接する空きセルへ移動します。  
     ドラッグの移動距離がセルサイズの半分（50px）以上であれば、その方向へ1マスの移動を試みます。  
     移動先に障害物がなければ盤面の状態と駒の位置が更新されます。

- **勝利条件**：  
  娘駒（2×2）が下段中央に配置されると、クリアのアラートが表示されます。

---

## ファイル構成

- `index.html`  
  HTML、CSS、JavaScript を1つのファイルにまとめたシンプルな実装です。  
  ※ コード内に詳細なコメントを記述しており、各処理（盤面描画、駒の移動、ドラッグ操作、勝利判定など）の実装内容が分かりやすくなっています。

---

## 使い方

1. **実行方法**  
   - 本ファイルを `index.html` などの名前で保存してください。  
   - ブラウザ（Chrome, Firefox, Edgeなど）でファイルを開くとゲームが起動します。

2. **ゲーム操作**  
   - **駒の選択**：  
     任意の駒をクリックすると、赤い枠が表示され、駒が選択状態となります。  
   - **移動操作**：  
     選択した駒をクリックしたままドラッグし、上下左右の隣接セルに移動します。  
     ドラッグの移動距離が一定以上であれば、1マス分の移動が試みられます。  
   - **勝利判定**：  
     娘駒が下段中央に配置されると、クリアのメッセージが表示されます。


---

## 技術スタック

- **HTML5/CSS3**  
  基本的な構造とスタイルの設定に使用しています。

- **JavaScript**  
  ゲームロジック、イベントハンドリング、盤面描画、駒の移動制御などを実装しています。

