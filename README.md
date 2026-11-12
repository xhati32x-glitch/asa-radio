# 朝のまとめラジオ

ロランスの朝のまとめを、ティアとレンが読み上げるラジオ局です。
予定と進捗と、開いている件の現在地を毎朝届けます。

- 放送: https://xhati32x-glitch.github.io/asa-radio/
- 声: ティア／レン（AI音声）

## 仕組み

この局は [myradio](https://github.com/monoradio102/myradio)（ものラジオ）の仕組みを使っています。

- プレーヤーは `index.html` 1枚。`station.json`（局の設定）、`episodes.json`（回の一覧）、`episodes/<日付>-ja.json`（台本）を読んで再生します
- 台本の文は `{"say": 読み上げ用, "show": 字幕用}` の形で、`lines_timed` で音声と同期します
- 音声（`audio/`）は main ブランチに入れません。`tools/publish.sh` が「本体 ＋ 直近30日分の音声」を `gh-pages` ブランチに載せて GitHub Pages で配信します

## ライセンス

プレーヤー等のコードは myradio 由来で、MIT License です（`LICENSE` ファイルに原文と著作権表示があります）。
台本・音声・キャラクター画像の権利は局の運営者に帰属します。
