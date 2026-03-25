# GLB Video Maker
Geminiでつくった。
GLBをくるくるさせる動画と一緒にコメントを表示したいときにどうぞｗ

### ✨ 特徴<br>
* 手動で微調整する「Single」と、CSVで全自動一括生成＆ZIP保存する「Batch」を搭載<br>
* 各種アスペクト比のプリセット対応<br>
* カクつかない5秒/1回転の完全ループ対応<br>

### 🚀 使い方<br>
* Singleモード: GLB読込 → 配置・テキスト・解像度を調整 → 「Record」で保存。<br>
* Batchモード: GLB複数ファイルとCSV指示書をアップロード → 「Start」で一括処理（ZIP保存）。<br>
### 📄 CSV仕様 (Batch Mode)<br>
 1行目をヘッダーにしてください（Shift-JIS/UTF-8対応）<br>

| カラム名 | 必須 | 説明 | 初期値 |
|-----|-----|-----|-----|
|filename|必須|対象GLBファイル名|-|
|comment|任意|合成テキスト（\nで改行可）	(空)|
|text_color|任意|文字色（HEX形式）|#ffffff|
|bg_color|任意|背景色（HEX形式）|#000000
|scale|任意|モデルの拡大縮小倍率|1.0|
|height|任意|高さ(Y軸)の微調整|0.0|
|align|任意|配置基準 (center, bottom, origin)|center|

# 🛠 構成 & ⚠️ 注意事項<br>
技術スタック: Three.js, Tailwind CSS, JSZip, PapaParse, Chart.js<br>
注意: 動画エンコードはPCスペックに依存します。大量処理時はブラウザのメモリ枯渇を防ぐため、50〜100件程度に分割して実行してください。<br>
