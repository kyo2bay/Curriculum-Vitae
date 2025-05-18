# 職務経歴書

## 基本情報

|key|value|
|---|-----|
|Name|小崎 勇周 (Kozaki Yushu)|
|Address|東京都|
|Education|京都大学 総合人間学部 卒業 <br> Foothill College Computer Science 中退|
|Zenn|[@kyo2bay](https://zenn.dev/kyo2bay)
|Qiita|[@kyo2bay](https://qiita.com/kyo2bay)
|LinkedIn|[@kyo2bay](https://www.linkedin.com/in/kyo2bay)

## 概要

- アーキテクトとしてクラウドインフラの設計・構築・運用の経験が豊富です。
- バックエンドからフロントエンドまで開発経験があり、フルスタックエンジニアとしても対応可能です。
- 運用監視および SRE 業務の経験を通じ、既存システムの信頼性向上と開発生産性の改善に貢献できます。
- 顧客との仕様調整などの折衝、チーム全体を俯瞰したコミュニケーションを得意とします。
- コンピューターサイエンスの基礎と強い技術好奇心により、未経験技術でも短期間でキャッチアップできます。
- 本当に好きなプロダクトにエンジニアリングスキルを注ぎ込みたいと考えています。

## 得意領域

- Google Cloud クラウドアーキテクチャ設計・構築・コスト最適化
- Terraform による Infrastructure as Code の実践・運用
- コンテナ基盤の最適化およびロードバランサー設計・導入
- IAM 最小権限設計とセキュリティベストプラクティス適用
- GitOps ワークフローの導入・整備
- CI/CD パイプラインの設計・構築・高速化
- オブザーバビリティツールの導入
- トイル削減、自動化ツール開発
- Golang によるスケーラブルなサーバサイド開発
- ドキュメント整備とナレッジマネジメント

## スキル

### 言語（得意順）

Golang / TypeScript / Python / Java / Ruby

### フレームワーク（得意順）

Gin / Vue(Nuxt) / Django / Ruby on Rails

### AWS

Lambda / ECS / EC2 / Redshift / S3 / SNS / SES / CloudWatch / Cloud9

### Google Cloud

#### Compute

Cloud Run / Cloud Functions / GKE / GAE / Firebase

#### Databases

Cloud SQL / Cloud Spanner / Firestore / BigQuery

### CI/CD

GitHub Actions / GitLab CI/CD / CircleCI / Google Cloud Build

### その他

Terraform / Docker / Kubernetes / Nginx / Ansible / Datadog / New Relic

## 受賞

[Google Cloud Partner Top Engineer 2023](https://cloud.google.com/blog/ja/topics/partners/partner-top-engineer-2023-award-winners?hl=ja)

## 資格

- AWS Certified Solutions Architect – Associate
- Google Cloud - Associate Cloud Engineer
- Google Cloud - Professional Cloud Architect
- Google Cloud - Professional Data Engineer
- Google Cloud - Professional Cloud Database Engineer
- Google Cloud - Professional Cloud Developer
- Google Cloud - Professional Cloud DevOps Engineer
- Google Cloud - Professional Cloud Network Engineer
- Google Cloud - Professional Cloud Security Engineer
- Google Cloud - Professional Machine Learning Engineer
- Java SE 8 Silver
- OSS-DB Silver
- 応用情報技術者
- TOEIC 900点

## 自然言語

- 日本語: ネイティブ
- 英語: かんたんな日常会話ができる

## 職務経歴

一定期間以上従事した、もしくは技術的難度の高かったプロジェクトのみ記載しています。

### デジタルバンク運用支援(2024/6 ~ 現在)

概要: 口座数100万のデジタルバンクの運用監視、SRE業務支援

#### 担当業務

1. アラート・インシデント対応

    アプリケーションログ、インフラメトリクスなどの起因によるアラート対応・原因調査

    - 高重要度のインシデントへのオンコール対応
    - 障害根本原因切り分け（クラウドインフラ障害、アプリケーションバグなど）
    - 各スクラム(マイクロサービス)チームとの連携

    【課題】
    アプリ保守・運用チームと、このアラート対応チームが分離していたためか、アプリケーション起因の「頻発のアラート」へのバグ修正の優先度はアプリ保守・運用で後回しにされがちであった。

    【解決策】
    典型的な DevOps の課題であり、本来はマイクロサービス単位で一気通貫してアプリ保守・運用からアラート対応まで行うべきであったと思うが、個人としてそういった組織体制に変革を与えられる状況ではなかったため、SRE として、「アラートが過剰に発生すると Site Reliability の低下を招く」などを啓発することで、バグ修正などの優先度を高めてもらうようにした。

1. 監視設計・実装・運用

    New Relic を活用したオブザーバビリティの実現

    - アプリケーションの仕様に応じたアラート条件の設計・実装
    - 実態に即したアラート条件・レベルの見直し・削除
    - 日々のダッシュボード確認

1. 高セキュリティ要件の VM 設計・構築

   CISポリシーに準拠したアドホックなコマンド実行環境の VM 設計・構築

   - CISポリシーを基本としたプロジェクトセキュリティポリシー設計
   - OS 設定用 Ansible Playbook 作成

<br>

### 製造業向け社内システム刷新(2023/10 ~ 2024/5)

概要: 在庫、生産、受発注、経理などの業務を管理する社内 Web アプリケーションの新規開発

#### 担当業務

1. GKE クラスタ構築

    GKE Autopilot モードクラスタ構築

    - クラスタとの認証認可など各項目の設計
    - Pod, Service 用共有VPCのIPアドレス範囲設計

    【課題】
    当プロジェクトの他のシステムでは、GKE バージョンアップデートの検証に毎回時間を要していた。

    【解決策】
    GKE の Release Channel を利用し、自動でバージョンアップを行う設定を導入。開発環境ではRegularチャンネル、本番環境ではStableチャンネルを採用し、事前に検証済みのバージョンを適用する仕組みを構築した。

1. Kubernetes 上での Web アプリケーションの基盤開発

    SPA(Vue.js)、REST API(Java)構成のWebアプリケーション Kubernetes 基盤構築

    - Kubernetes の Deployment, Service, Ingress 等のマニフェスト作成およびデプロイ
    - Helm によるパッケージ、テンプレート管理
    - Nginx によるリバースプロキシ、Basic 認証の設定

    【課題】
    当プロジェクトの他のシステムでは、各環境ごとに素の Kubernetes マニフェストファイルを管理していたが、ちょっとしたフィールドの有無など、意図しない環境間差異が発生していた。

    【解決策】
    環境間で共通の項目をテンプレート化できるツールを採用した。ここでは、Datadog Agent パッケージなどもインストールしやすい Helm を採用した。

1. Datadog を利用した監視設定

    Datadog を利用したGKE, Kubernetesメトリクスの監視設定、ログ収集設定

    - Datadog Agent インストール、GCP Integration 設定
    - Dataflow, Pub/Sub を利用した Kubernetes アプリログ収集機構構築

1. CI/CDパイプライン構築

    Kubernetes および VM 用 CI/CD パイプライン構築

    - GitHub, GitHub Container Registry, CircleCI を利用した Kubernetes 用 CI/CD パイプラインの構築
    - cron, systemd, Ansible を利用した VM への CD パイプラインの構築

<br>

### 専門医による医療健康情報安心化サービス開発(2022/2 ~ 2023/1)

概要: メディアなどのクライアントが執筆した記事を本サービスに登録した医師が妥当性を担保する Webアプリの新規リプレイス開発

#### 担当業務

1. GCP プロダクト選定およびアーキテクチャ設計

    フロントエンド、バックエンド、データベース等に利用するプロダクト設計

    - フロントエンド: Firebase Hosting、バックエンド: Cloud Run、データベース: Firestore
    - 認証: Firebase Authentication
    - 非同期処理: Cloud Tasks、イベントトリガー: Eventarc

    【課題】
    参画当時のメンバーが GCP に疎く、バックエンドにレガシープロダクトの Google App Engine を採用しようしていた。

    【解決策】
    現在の GCP におけるコンピュートプロダクトのファーストチョイスは Cloud Run であることを、その特徴を示しつつ説明し、GAE から Cloud Run に変更した。

1. インフラのコード化、および GitOps の実装

    Terraform を利用した GCP プロダクトのコード化、および GitHub Pull Request ベースの 適用戦略の実装

    - dev, stage, prod プロジェクトで生じる差分に対して対応できるようなモジュール／ディレクトリ構成で HCL を記述
    - ローカルなどで手動実行するのではなく、CI/CD パイプラインを通して実行させる設定をし、GitOps を実現させた

    【課題】
    社内に Terraform に詳しい人がおらず、また特に GitOps スタイルは完全に前例がないため、独自で実装を進める必要があった。

    【解決策】
    Terraform および GCP の公式ドキュメントを愚直に読みつつ、サンドボックスの GCP プロジェクトで試行錯誤を繰り返した。

1. CI/CD パイプライン構築

    Cloud Build を利用した Firebase Hosting、Cloud Run(PR プレビュー含む)、Terraform のパイプライン構築

    【課題】
    CI/CD にかかる時間は開発効率に直結するので、1分でも速くしたかった。

    【解決策】
    下記の手段によって、それぞれの CD が最大でも4分で完了するようにした。

    - step の実行順序最適化
    - コンテナイメージの最小化
    - kaniko キャッシュの活用
    - Cloud Build 実行マシンのアップグレード

1. ネットワーク関連設定実装

    ロードバランサーの設定、DNSのレコード作成等

    - Firebase Hosting と カスタムドメインのマッピング
    - Cloud Run とカスタムドメインのマッピング
    - Load Balancing / CDN / Cloud Armor の設定

1. フロントエンドの実装

    Vue、Vuetify、Nuxt、TypeScript でのフロントエンド機能開発

    - Vue テンプレートの記述
    - Component (Composition API)の実装

<br>

### カーシェアリング Web アプリ開発(2021/05 ~ 2021/9)

概要: カーシェアリング Web アプリの機能追加開発

#### 担当業務

1. サーバーサイドAPI実装

    Golang、Gin、Gorm、クリーンアーキテクチャ で構成されたサーバーサイドの機能追加/修正

    - クライアント用APIエンドポイント新規追加/修正
    - 新卒メンバーの実装ヘルプ

    【課題】
    新卒メンバーの実装のヘルプ度合いの難しさ。あまり関与しすぎても成長に繋がらないが、放置しすぎても作業が進まない。

    【解決策】
    作業における目標を新卒メンバーのスキル向上にフォーカスし、現在のスキルをヒアリングして正確に把握し、逐一コミュニケーションをとって一番スキル向上に寄与するヘルプ度合いを探りながら進めていった。

1. クライアントサイドコードレビュー

    React、Redux で構成されたクライアントサイドのコードレビュー

    - 既存コードとの一貫性を保てているかどうか
    - Figma でデザインされたビューが再現されているかどうか

1. CI/CDリファクタ

    本案件の必須タスクではなかったが、開発途中で気になった部分をリファクタし、開発サイクルの向上を図った。

    - CircleCIの `config.yml` の可読性向上(`executors`, `commands`, `parameters` の活用)

    【課題】
    Dockerイメージのビルドにかなり時間がかかっていた。特にクライアントサイドは3分近くかかっていた。

    【解決策】
    `Dockerfile` を確認したところ、Docker Layer Cache を利用しておらず、毎回のビルドでモジュールのインストールを行っていることが分かった。`package.json`、`go.mod` 等のパッケージファイルを先に `COPY` し、パッケージファイルに変更がない場合は、モジュールのインストールが行われないようにした。

<br>

### スマホゲームの開発・運営支援業務(2020/11 ~ 2021/03)

概要: スマホゲームのサーバーサイド開発、および運用監視

#### 担当業務

1. Golang によるサーバーサイドAPI設計・実装・単体/結合テスト

    - ゲーム新規イベント向けAPI
    - ユーザーデータの Datastore Entity の作成/更新処理
    - ゲーム内のロジック・ガチャ抽選処理
    - マスタデータの作成
<br>

### 携帯端末データのGCP取込(2020/08 ~ 2020/10)

概要: Cloud Storage にアップロードされた独自フォーマットのファイルをCSVに変換し、BigQuery にインポートする機能開発。

#### 担当業務

1. GCPアーキテクチャ設計

    【課題】
    標準的な設計として、ワークロードは Cloud Functions を選択したいところだったが、処理対象のファイルサイズが大きく、最大タイムアウト時間の9分を超える可能性があったため、Cloud Functions は使用できなかった。

    【解決策】
    このシステムでは別の機能ですでに GKE を利用していたこともあり、ワークロードとしては GKE、なおかつリトライ処理を自前でやってくれる Kubernetes Job を利用することにした。

1. Kubernetes Job バッチ処理設計・実装・単体/結合テスト

    - Firestore のエンティティ作成/更新処理
    - CSV 変換処理
    - Cloud Storage Compose 処理

1. Golang によるストリーミング処理設計・実装・単体/結合テスト

    - PubSubメッセージ受信処理
    - BigQuery テーブルへのデータ書き込み処理
    - Kubernetes Job 起動処理
    - Kubernetes マニフェストファイル作成
    - Workload Identity の設定

    【課題】
    開発 / 検証 / 本番 環境 でそれぞれ yamlファイルを定義していたが、何か変更がある度に全ファイルを書き換えるのが面倒であった。

    【解決策】
    Kustomize と Skaffold という技術の組み合わせで yamlファイルを環境に応じて上書きするという方法を用いた。他にも Helm という選択肢はあったが扱いにくいという印象を受けたので採用しなかった。

<br>

### スマートフォン中古端末買取システム(2020/04 ~ 2020/07)

概要: Cloud SQL のデータを BigQuery に取り込み、 Data Portal で可視化。

#### 担当業務

1. データ分析項目の要件定義

    - 顧客の分析したい要望に沿って、KPIを定義した。

1. GCPアーキテクチャ設計

    - Cloud SQL (asia-northeast1) の データを BigQuery (US) にインポートするアーキテクチャの設計。

    【課題】
    BigQuery には外部テーブルとして、Cloud SQLのテーブルを参照する機能があるが、ベータ版の機能で使用が認められなかった。

    【解決策】
    Cloud SQLからCloud Storage にデータを CSV 出力、その CSV を BigQuery に取り込むアーキテクチャを採用した。

1. Golang によるバッチ処理設計・実装・単体/結合テスト

    - Cloud Storage に 出力された CSV を BigQueryに取込む部分を Cloud Functions (Golang) で実装。

    【課題】
    冪等性の考慮。Cloud Functions は PubSub 通知のメッセージから発火されるが、PubSub は at-least-once 配信なので、Cloud Functions が同じCSVファイルに対して複数回起動した場合でも BigQueryには 同じデータが重複しない必要があった。

    【解決策】
    日付型の パーティションテーブルを活用して BigQuery への 書き込みモード  `WRITE_TRUNCATE` (毎回データを上書く) 採用した。

1. BIツールを用いたデータの可視化

    - BigQuery をソースとして Data Portal でダッシュボードを作成。

<br>

### 製薬会社向け既存システム統合(2019/01 ~ 2020/01)

概要: 顧客が利用している様々な外部サービスに蓄積されているデータをAWS上で管理分析するためのDWH基盤構築。

#### 担当業務

1. AWSアーキテクチャ設計構築

    - EC2 (データ取得) -> S3 (生データ保存) -> CloudWatch (イベント通知) -> Lambda (生データ加工) -> Amazon Redshift (DWH)

1. Python / Bash によるシステム連携バッチ処理の設計・実装・テスト

<br>

### 携帯キャリア向けデータ移行(2018/09 ~ 2018/12)

概要: SQLServerのデータベースをOracleに移行。

#### 担当業務

1. Stored Procedure バッチ処理設計
1. Oracle PL/SQL によるデータ移行マッピングの設計・実装・テスト
1. 新規開発メンバーのサポート
