# ナレーション音声（ナナミ ja-JP-NanamiNeural）

この `audio/` に `01.mp3`〜`07.mp3` を置くと、提案書（`../index.html`）の
「音声でのご説明」セクションで再生されます。

## 生成方法（ネット接続が必要）
```bash
pip install edge-tts
python3 engine/mp3gen.py lp/hamano-kessai/narration.json --out lp/hamano-kessai/audio
```
- 声: ja-JP-NanamiNeural（ナナミ）。`--voice` で変更可。
- 原稿: `../narration.json` の `narration[]`（読み間違い防止のため一部を読み下し・分かち書きにしています）。

## 注意
- 本リポジトリの実行環境はネットワーク遮断中（GitHubアカウント停止に伴う egress 制限）のため、
  この環境では mp3 を生成できません。ネット接続のある環境／復旧後に上記コマンドで生成してください。
- mp3 未生成でも、提案書には原稿テキストが表示されるため内容は伝わります。
