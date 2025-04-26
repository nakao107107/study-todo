# goal.md

## 現状の問題点
- Terraform state 運用手順が未確立 (state mv / import 等が未習得)
- Module 構成とベストプラクティスの理解不足
- AWS ネットワーク (VPC, Subnet, NAT, VPC Endpoint) の詳細知識不足
- ALB / NLB の機能差・用途未整理
- ECS Fargate AutoScaling の設定経験不足
- データストア (RDS Multi-AZ / Read Replica, ElastiCache) 詳細理解不足
- CloudFront OAC, WAF Bot Control / Rate-based Rule の理解不足
- 監視 (CloudWatch Alarm → Slack)・コスト最適化のベストプラクティス未整備

## 2ヶ月間で達成する目標
1. プロジェクトのインフラ構成を 100% 図解・口頭説明できる
2. Terraform の state 操作・Module 設計・リファクタを自走できる
3. ネットワーク／コンピュート／データ／セキュリティ／運用の各領域でベストプラクティスを理解し、改善案を 10 件以上提示
4. Terraform 変更 PR を最低 2 本マージし、レビューを通過
5. 最終週に「学習レポート＋最新構成図」をドキュメントとして整備し、オンボーディング資料化 