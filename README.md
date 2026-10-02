# find-rental-in-japan

日本の賃貸物件を検索・絞り込み・検証するエージェント向けスキルです。予算、通勤、間取り、特別条件に合わせて候補を集め、重複排除、物件ごとの検証、独立した再確認を経て、出典付きの比較結果にまとめます。

## 使い方

インストール対象は **[find-japan-rentals/](find-japan-rentals/)** のみです。利用するエージェント環境のスキル導入手順に従い、このディレクトリ全体を配置してください。入口は [SKILL.md](find-japan-rentals/SKILL.md) です。参照資料とライセンスも同じディレクトリに含まれています。

スキルを読み込んだ後、例えば次のように依頼します。

> $find-japan-rentals を使って、日本の賃貸物件を探してください。希望エリア、予算、通勤先、間取り、必須条件を確認してから検索を始めてください。

並列エージェントに対応していない環境では、同じ役割を順番に実行し、独立した再確認を実施できていないことを明示します。物件情報や設備の対応状況は変わるため、利用時点の出典を確認してください。問い合わせ、個人情報の送信、予約、申し込み、契約は別途ユーザーの許可に従います。

## 構成

- [find-japan-rentals/SKILL.md](find-japan-rentals/SKILL.md)：日本語版の唯一のスキル入口
- [find-japan-rentals/contents.md](find-japan-rentals/contents.md)：文書マップ
- find-japan-rentals/references/：役割別の手順と必要に応じて読む付録
- find-japan-rentals/agents/openai.yaml：表示用メタデータ
- [docs/zh-CN/](docs/zh-CN/)：中国語の参考資料。インストール対象ではありません

中国語版は内容の参照用として同じリポジトリに置いています。別のスキルとして検出されないよう、入口のファイル名を `skill-reference.md` にしています。

## ライセンス

Copyright 2026 LUOXIAO92

このリポジトリのスキルと文書は **Apache License 2.0** で公開しています。全文は [LICENSE](LICENSE) を参照してください。インストール用ディレクトリにも同じライセンスと著作権表示を同梱しています。
