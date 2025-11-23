# MammaMia
TPSによる制限や線路右クリックでのトロッコ召喚などを司るプラグインです。

- 重要: Paperのみでしか動作しません。
    - 1.21.10でのPaperの実装変更に伴い、TPS取得にPaperのみで使える機能を用いる仕様に変更したため
    - ただしEssentialsXとの依存関係の関係から、Paperプラグインとしては認識されずBukkitプラグインとして表示されるので注意

## 機能
- TPSによるエリトラ制限
- 氷右クリックで一時ボート召喚
- 線路右クリックでトロッコ召喚
- TPS低下時放置キック

## 依存プラグイン
- EssentialsX

## 開発環境
1. 直下に`gradle.properties`を作成
1. 依存プラグインであるEssentialsXのjarを任意のディレクトリにダウンロード
1. EssentialsXのjarのディレクトリを以下のように`gradle.properties`で指定
    ```
    pluginDir = path/to/jar_dependencies/dir/
    ```
1. ビルド時にはGradleタスクのうち`Tasks/shadow/shadowJar`を実行する(依存パッケージの実装をjarに含めるため)
