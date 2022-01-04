# 概要
IaCを導入することでインフラ構築の自動化とコスト削減を行う

## CloudFormationのYAMLを分割管理
機能ごとにyamlが分割してあり、ビルドを行うことで一つのyamlに統括されるフレームワーク

### 使い方
#### インストール
通常は、CloudFormation を使うプロジェクト内にインストールすれば OK です。

`npm install -D @u-minor/cftemplate`
> global に入れても OK 

#### CloudFormation テンプレートのビルド
cftemplate コマンドで src フォルダを指定すると、ビルドされたテンプレートが標準出力にアウトプットされるので、以下のようにリダイレクトでファイルに向けます。

`npx cftemplate src > stack.yml`
