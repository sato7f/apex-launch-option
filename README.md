# Apex Legends 起動オプション ジェネレーター

[English version](./README.en.md)

🔗 **公開ページ: <https://sato7f.github.io/apex-launch-option/>**

Apex Legends の起動オプション (launch options) をチェックボックスで選んで生成・コピーできるシンプルな単一HTMLツールです。日本語と英語の表示切り替えに対応しています。

選択内容と入力値はブラウザの `localStorage` に自動保存されるので、次回開いたときも同じ設定が復元されます。

## 機能

- カテゴリ別 (起動 / パフォーマンス / 解像度 / 入力 / 視野 / ゲームプレイ / 上級) に整理されたオプション一覧
- フラグ型 (`-novid` など) はチェックだけ、値指定型 (`+fps_max 0` など) はチェック + 入力欄
- 各オプションに**説明・注意事項・出典リンク**を併記。出典は EA 公式ヘルプ・Valve Developer Wiki・PCGamingWiki などをクリックで参照可能
- 既存の起動オプション文字列を貼り付けると、認識可能なオプションを自動でチェック・値反映
- 生成された文字列をワンクリックでクリップボードにコピー
- 選択状態と入力値・言語設定を `localStorage` に自動保存
- カテゴリ見出しクリックで折り畳み、各オプションの詳細（注意・出典）も折り畳み可能
- ヘッダー右上のボタンで日本語 / English を切り替え（初回はブラウザ言語に応じて自動選択）
- レスポンシブ対応（PC・タブレット・スマートフォン）

## 使い方

`index.html` をブラウザで開くだけです。ビルドや依存パッケージはありません。

```bash
# 例: WSL / Linux
xdg-open index.html

# macOS
open index.html
```

生成された文字列をコピーして、Steam の「ライブラリ → Apex Legends を右クリック → プロパティ → 起動オプション」または、EA アプリの「ライブラリ → Apex の "..." → プロパティ → 詳細起動オプション」に貼り付けてください。

## GitHub Pages で公開する場合

このリポジトリをそのまま GitHub Pages で配信できます。リポジトリの **Settings → Pages** で **Source** を `main` ブランチのルートに設定すれば、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

## リファレンス

オプションの一次情報は `index.html` 下部の「起動オプション リファレンス」セクションを参照してください。EA 公式ヘルプ、Valve Developer Wiki、PCGamingWiki、Apex Movement Wiki、ProSettings、Steam 公式コミュニティガイドへのリンクを掲載しています。

## ファイル構成

- `index.html` — ツール本体（HTML/CSS/JS 一体）
- `README.md` — 本ファイル（日本語）
- `README.en.md` — 英語版 README
- `.gitignore`
