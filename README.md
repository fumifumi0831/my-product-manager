# MyProductManager

## 概要
MyProductManagerは、プロジェクト開発における様々な課題を事前に検出し、より効率的な開発をサポートするための個人用アシスタントツールです。API実装、インフラ構築、ライブラリ管理などの側面から、過去の反省点を踏まえたアドバイスを提供します。

## 主な機能
1. **API仕様チェック**: 最新のAPI仕様書に基づいた実装アドバイス
2. **ライブラリ互換性管理**: バージョン指定の徹底とライブラリ依存関係の監視
3. **インフラ最適化提案**: 現状のインフラ構成を記録し、新要件に対する最適な構成を提案
4. **API制約確認**: レート制限やリクエスト制限などの制約を事前に確認

## 使用方法
このリポジトリを活用して以下のようにプロジェクト管理を行います：

1. `api-specs/` ディレクトリに最新のAPI仕様書を保存する
2. `infrastructure/` ディレクトリに現在のインフラ構成情報を記録する
3. `libraries/` ディレクトリにプロジェクトで使用しているライブラリとバージョン情報を管理する
4. `projects/` ディレクトリに各プロジェクトの概要情報を記録する
5. `advisor.md` でプロジェクト進行中に得られたアドバイスを記録・参照する

## 活用のためのTips（反省点から学んだこと）

### API実装に関するTips
- ✅ 新機能を実装する前に、必ず `api-specs/` に最新の仕様書を更新・参照する
- ✅ 実装するAPIの制約（レート制限、データ上限など）を事前に確認し `api-constraints.md` に記録する
- ✅ 作業開始前に「このAPIにはどのような制約がありますか？」と自問する習慣をつける
- ✅ コード実装前に必要な機能だけをリスト化し、不要な機能を追加しないよう計画する

### ライブラリ管理に関するTips
- ✅ すべてのライブラリは `requirements.txt` や `package.json` などでバージョンを明示的に固定する
- ✅ 新しいライブラリを導入する際は、互換性テストを実施してから本番環境に反映する
- ✅ 標準ライブラリであっても、バージョン管理を徹底する（特にHTTP関連ライブラリ）
- ✅ 定期的にライブラリの脆弱性スキャンを実施し、必要に応じて更新を行う

### インフラ構築に関するTips
- ✅ インフラの選択理由と構成図を `infrastructure/` ディレクトリで常に最新化する
- ✅ 新規要件ごとに「現インフラで対応可能か？」の検証を行い、結果を記録する
- ✅ インフラコストとパフォーマンスのバランスを定期的に見直す
- ✅ スケーラビリティを考慮した設計を心がけ、将来の拡張に備える

### 全般的なプロジェクト管理Tips
- ✅ 週に一度は「反省点の改善状況」を確認する時間を設ける
- ✅ 問題が発生したら、すぐに `lessons-learned.md` に記録し、再発防止策を考える
- ✅ 新機能開発前に MyProductManager を使って事前チェックリストを作成する
- ✅ チーム内での知識共有のため、得られた知見を定期的に共有する

## ディレクトリ構造
```
my-product-manager/
├── api-specs/             # API仕様書保存ディレクトリ
├── infrastructure/        # インフラ構成情報
├── libraries/             # ライブラリ管理情報
├── projects/              # プロジェクト概要情報
├── advisor.md             # アドバイス記録
├── api-constraints.md     # API制約情報
└── lessons-learned.md     # 学んだ教訓の記録
```

## 貢献方法
個人用ツールとして作成していますが、同様の課題を持つ方のフィードバックや提案は歓迎します。IssueやPull Requestでぜひご意見をお寄せください。
