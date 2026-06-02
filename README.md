# きずなコン リモート設定

このリポジトリは「きずなコン」アプリのリモート設定ファイルを管理します。

## config.json の使い方

| フィールド | 説明 |
|---|---|
| `notice` | アプリ起動時にダイアログで表示するお知らせ。空欄で非表示 |
| `known_bad_ps_versions` | 問題が確認されたPS Remote Playのバージョン名リスト |
| `force_update_message` | アプリの強制アップデートを促すメッセージ。空欄で非表示 |
| `min_app_version` | 最低限必要なアプリのversionCode |
| `ps_remote_play_package` | PS Remote PlayのAndroidパッケージ名 |

## Sony更新時の対応手順

1. PS Remote Playがアップデートされたら動作確認を行う
2. 問題あれば `known_bad_ps_versions` にバージョン名を追加してコミット
3. ユーザーのアプリが次回起動時に自動で警告を表示する

## 設定例

```json
{
  "known_bad_ps_versions": ["8.0.0"],
  "notice": "PS Remote Play 8.0.0 で一部ボタンが効かない問題を確認中です。アップデートをお待ちください。"
}
```
