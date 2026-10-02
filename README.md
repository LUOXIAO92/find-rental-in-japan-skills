# find-rental-in-japan

日本の賃貸物件を探し、条件に合うか調べるエージェント向けスキルです。予算、通勤、間取り、特別条件に合わせて候補を集めます。重複する掲載を整理し、物件ごとの検証と別のエージェントによる再確認を経て、出典付きの比較結果にまとめます。

## 使い方

インストールするのは[find-japan-rentals/](find-japan-rentals/)だけです。利用するエージェント環境の導入手順に従い、このディレクトリを丸ごと配置してください。[SKILL.md](find-japan-rentals/SKILL.md)がスキルの入口です。参照資料とライセンスも同じディレクトリに含まれています。

スキルを読み込んだら、例えば次のように依頼します。

> $find-japan-rentalsを使って、日本の賃貸物件を探してください。希望エリア、予算、通勤先、間取り、必須条件を確認してから検索を始めてください。

## ファイル構成

- [find-japan-rentals/SKILL.md](find-japan-rentals/SKILL.md)：日本語版スキルの入口
- [find-japan-rentals/contents.md](find-japan-rentals/contents.md)：文書一覧と参照先の案内
- find-japan-rentals/references/：役割別の手順と、必要なときに読む付録
- find-japan-rentals/agents/openai.yaml：表示用メタデータ
- [docs/zh-CN/](docs/zh-CN/)：中国語の参考資料。インストールは不要です

中国語版は内容を参照するために置いています。別のスキルとして検出されないよう、入口のファイル名を`skill-reference.md`にしています。スキルとして読み込む入口は日本語版の1つだけです。

## ライセンス

Copyright 2026 LUOXIAO92

このリポジトリのスキルと文書はApache License 2.0で公開しています。全文は[LICENSE](LICENSE)を参照してください。インストール用ディレクトリにも同じライセンスと著作権表示を同梱しています。
