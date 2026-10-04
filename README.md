# Codex Usage HUD

Codexの利用枠残量と処理中のActivityを表示する、macOS用の小型常駐HUDです。アプリ自体はAIを使用しません。

![Codex Usage HUD](assets/hud-preview.png)

> [!WARNING]
> Codex Usage HUDはOpenAIおよびAppleの公式製品ではありません。現在の無料Preview版はApple Developer IDで署名・公証されていないため、初回起動時にAppleの警告が表示されます。配布元とSHA-256を確認し、信頼できる場合だけ使用してください。

## ダウンロード

右側の **Releases** から最新のPreview版を開き、Assetsにある次のファイルをダウンロードしてください。

- アプリ本体: `Codex-Usage-HUD-0.5.0-preview-mac.zip`
- 取扱説明書: `Codex-Usage-HUD-Manual-JA-0.5.0.pdf`

GitHubが自動表示する `Source code (zip)` はアプリ本体ではありません。

## 対応環境

- macOS 13以降
- Apple Silicon / Intel Mac
- Codexデスクトップアプリ、またはCodex CLI
- Windows非対応

## 表示内容

- **Activity LED**: 処理時間に応じて伸びる警告灯
- **LOAD**: 現在または直前の処理時間を、一つ前の処理時間と比較した倍率
- **PEAK**: 当日に到達した最大Activityレベル
- **REMAIN**: Codexが返した現在の利用枠残量

Activity LED、LOAD、PEAKは正確なトークン数ではありません。異常に長い処理を視覚的に察知するための目安です。

## インストール

1. ZIPを展開します。
2. `Codex Usage HUD.app` を「アプリケーション」フォルダへ移動します。
3. アプリを開きます。
4. Appleの警告が出た場合は、取扱説明書の手順を確認します。
5. HUDメニューから「Codex Hooksをインストール…」を選びます。
6. Codexを再起動し、`/hooks` でUsage HUDのHooksを確認して信頼します。

Appleによる未公証アプリの説明: https://support.apple.com/102445

## アンインストール

1. HUDメニューから「Codex Hooksを解除…」を選びます。
2. 「Macログイン時に起動」のチェックを外します。
3. HUDを終了します。
4. `Codex Usage HUD.app` をゴミ箱へ移動します。

## プライバシー

プロンプト本文、回答本文、ツール内容、ファイル内容、APIキー、ログイントークンは保存しません。詳細は [PRIVACY.md](PRIVACY.md) を参照してください。

## 技術的な制約

REMAINはCodex app-serverの内部的な利用枠情報に依存しています。将来のCodex更新で動作しなくなる可能性があります。

## 問題の報告

GitHub Issuesを利用してください。スクリーンショットやログを投稿する前に、個人情報、プロンプト、ファイルパス、認証情報が含まれていないことを確認してください。
