# Week 0: Terraform 開発環境セットアップ（2025/04/27 – 2025/05/02）

この週では Terraform の基礎操作（`terraform init` / `terraform plan`）を実際に動かせる開発環境を用意し、HashiCorp Learn のチュートリアルを通じてワークフローを体験する。アウトプットとしては **plan 実行結果のスクリーンショット** と **手順メモ** を残し、次週以降の学習土台を整える。

## 2025/04/27 (Sun)

**タスク**
1. macOS へ Terraform 1.7.x をインストール (`brew install terraform`)
2. AWS CLI v2 インストール＆ `sandbox` プロファイル設定
3. VSCode + Terraform Language Server (tf-ls) 拡張を導入

**参照テキスト & URL**
- Terraform インストール（HashiCorp Learn 日本語版）: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli?hl=ja
- Qiita: Mac に Terraform を Homebrew で入れてみる: https://qiita.com/fukubaka0825/items/0c9d56e2e3c1d8939e81
- AWS CLI インストール（日本語公式）: https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/getting-started-install.html

**アウトプット課題**
- `terraform -v` と `aws sts get-caller-identity` の実行ログをスクリーンショット

---

## 2025/04/28 (Mon)

**タスク**
1. HashiCorp Learn 「Your First Terraform Configuration」実施
2. ローカルで S3 バケットを作成する `main.tf` を記述

**参照テキスト & URL**
- HashiCorp Learn 初めての Terraform 構成（日本語）: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build?hl=ja
- Qiita: Terraform で S3 バケットを作成する手順: https://qiita.com/kenmatsu4/items/1877c604b4177b46137a
- Terraform S3 Resource Docs: https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket

**アウトプット課題**
- `main.tf` に S3 バケットリソースを定義 & コミット

---

## 2025/04/29 (Tue)

**タスク**
1. `terraform init` の実行フローを理解し、`.terraform` ディレクトリを確認
2. Backend なしの local state の存在を確認

**参照テキスト & URL**
- Command `terraform init` （日本語ガイド）: https://developer.hashicorp.com/terraform/cli/commands/init?hl=ja

**アウトプット課題**
- `terraform init` 実行ログを Markdown に貼付け

---

## 2025/04/30 (Wed)

**タスク**
1. `terraform plan` の出力を読み解く
2. `terraform apply -auto-approve` で実リソースを作成し、AWS Console で確認

**参照テキスト & URL**
- Command `terraform plan` （日本語ガイド）: https://developer.hashicorp.com/terraform/cli/commands/plan?hl=ja
- Command `terraform apply` （日本語ガイド）: https://developer.hashicorp.com/terraform/cli/commands/apply?hl=ja

**アウトプット課題**
- `terraform plan` 出力全文のスクリーンショット (CLI)
- AWS Console の S3 バケット画面キャプチャ

---

## 2025/05/01 (Thu)

**タスク**
1. `terraform destroy` を実行し、削除フローを把握
2. Learn ページの「Clean up」節を実践

**参照テキスト & URL**
- Command `terraform destroy` （日本語ガイド）: https://developer.hashicorp.com/terraform/cli/commands/destroy?hl=ja

**アウトプット課題**
- `terraform destroy` 出力スクリーンショット

---

## 2025/05/02 (Fri)

**タスク**
1. 今週の手順・学びを `week0_report.md` にまとめる
2. GitHub に `week0_setup` ブランチを Push し PR 作成

**参照テキスト & URL**
- Markdown 基本文法（Qiita 日本語記事）: https://qiita.com/kamorits/items/6f342da395ad57468ae3

**アウトプット課題**
- `week0_report.md` (手順・知見・課題) 作成
- PR URL を Slack に共有

---

### 追加メモ
- **VSCode 拡張**: HashiCorp Terraform (official) / Terraform fmt & validate on save を有効化
- **AWS リソース課金**: S3 バケットは無料枠内だが、作成リソース数を最小限に抑えること
- **GitHub Actions**: 時間に余裕があれば `terraform fmt` チェックのみの CI を設定しても良い 