# Salesforce SFDX テンプレート

よく使う設定を一元管理することで、初期のプロジェクト作成の手間を軽減するとともに、
プロジェクト標準の設定とすることでコード品質を高めることを目的として作成。

## 使用するにあたっての前提条件

-   [Node.js](https://nodejs.org/ja/) のインストール
-   [Salesforce CLI](https://developer.salesforce.com/ja/tools/sfdxcli) のインストール
-   git クライアントのインストール　例）[git for windows](https://gitforwindows.org/)

## Salesforce CLI を npm でインストールする場合

```cmd
npm install -g sfdx-cli
```

## `.vscode/setting.json`：VSCode の設定を記述するファイル

-   ファイルを保存するときにフォーマットする
-   エディターで制御文字を表示する
-   エディターで空白文字を表示する
-   ブラケットペアのガイドを有効にする
-   ブラケットペアの彩色を有効にする
-   ファイルの保存時に末尾の空白をトリミングする
-   ファイルの保存時に最新の行を末尾に挿入する
-   ファイルの保存時に最終行以降の新しい行をトリミングする
-   起動時に SObject の定義を更新する
-   ローカルのソースファイル保存時にデプロイしない
-   Apex テスト実行時にコードカバレッジの結果を取得する
-   Salesforce による利用状況データの収集を有効化しない
-   Salesforce CLI コマンドのステータスメッセージをポップアップしない

## `.vscode/launch.json`：Apex Replay Debugger の設定を記述するファイル

[Apex Replay Debugger](https://developer.salesforce.com/tools/vscode/ja/apex/replay-debugger)は VSCode の拡張機能として使える Apex のデバッグ機能です。

> 参考：https://dackdive.hateblo.jp/entry/2018/10/31/100000

## `.eslintignore`：任意のディレクトリ、ファイルをチェック対象から除外する

dreamhouse に準拠

## `.forceignore`：Salesforce DX ソース形式に同期または変換時のソースの除外

dreamhouse に準拠

## `.gitignore`：Git の管理に含めないファイルを指定する

dreamhouse に準拠

## `.prettierignore`：Prettier の管理に含めないファイルを指定する

dreamhouse に準拠

## `.prettierrc`：Prettier の設定ファイル

dreamhouse をベースに以下を追記

-   ダブルクォートをシングルクォートに揃える
-   タブサイズ：4

## `jest.config.js`：Jest の構成ファイル

SFDX プロジェクト作成時のまま

## `package.json`：npm パッケージを定義する JSON ファイル

dreamhouse をベースに以下を追記

-   apex:local:start：Apex コードを prettier で整形する速度を高速化するサーバを起動
-   apex:local:stop：Apex コードを prettier で整形する速度を高速化するサーバを終了

### 以下コマンドを用いて npm パッケージをインストールする

```cmd
npm install
```

もしくは

```cmd
npm install --legacy-peer-deps
```

### スタンドアローンサーバ起動

```cmd
npm run apex:local:start
```

### スタンドアローンサーバ終了

```cmd
npm run apex:local:stop
```

## `sfdx-project.json`：SFDX プロジェクト設定ファイル

SFDX プロジェクト作成時のまま

## 必須拡張機能

-   [Salesforce Extension Pack](https://marketplace.visualstudio.com/items?itemName=salesforce.salesforcedx-vscode)

## [推奨拡張機能](https://developer.salesforce.com/tools/vscode/ja/getting-started/recommended-extensions)

-   [Apex PMD](https://marketplace.visualstudio.com/items?itemName=chuckjonas.apex-pmd)
-   [Apex Log Analyzer](https://marketplace.visualstudio.com/items?itemName=financialforce.lana)
-   [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
-   [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
-   [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml)

## 便利拡張機能

-   Live Server
-   Trailing Spaces
-   Material Icon Theme
-   Git Graph
-   Codey Midnight
-   lwc-builder

## サンプルコード

-   [dreamhouse-lwc](https://github.com/trailheadapps/dreamhouse-lwc)
-   [lwc-recipes](https://github.com/trailheadapps/lwc-recipes)
-   [ebikes-lwc](https://github.com/trailheadapps/ebikes-lwc)
-   [apex-recipes](https://github.com/trailheadapps/apex-recipes)

## Read All About It

-   [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/ja)
-   [Salesforce CLI 設定ガイド](https://developer.salesforce.com/docs/atlas.ja-jp.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
-   [Salesforce DX 開発者ガイド](https://developer.salesforce.com/docs/atlas.ja-jp.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
-   [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.ja-jp.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
