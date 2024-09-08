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

- Google Cloud を基盤としたクラウドアーキテクチャ設計、クラウドインフラ構築管理、基盤コード開発の経験が豊富です。
- 運用保守よりは新規開発の業務の経験の方が多く、上流下流問わずゼロからの設計／実装が可能です。
- 顧客との仕様調整等の折衝、またチーム全体を俯瞰したコミュニケーションも得意です。
- Computer Science の基本的な知識、技術への好奇心で未経験の技術でもすぐにキャッチアップできます。
- まだまだ様々な技術に興味があり、今後機会があれば機械学習系の領域にチャレンジしてみたいと思っています。

## 得意領域

- クラウドアーキテクチャ設計、クラウドインフラ構築管理／コスト最適化(Google Cloud)
- インフラのコード化(Terraform)
- GitOpsの導入
- CI/CDパイプライン構築、高速化
- ロードバランサーの導入
- コンテナ最適化
- IAM 最小権限設定
- セキュリティ対策
- Golang のサーバーサイド開発
- README/Wiki等ドキュメント作成

## スキル

### 言語（得意順）

Golang / TypeScript / Python / Java / Ruby

### フレームワーク（得意順）

Gin / Vue(Nuxt) / Django / Ruby on Rails

### AWS

Lambda / ECS / EC2 / Redshift / S3 / SNS / SES / Cloud Watch / Cloud9

### GCP

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
- Google Cloud - Professional Cloud Data Engineer
- Google Cloud - Professional Cloud Database Engineer
- Google Cloud - Professional Cloud Developer
- Google Cloud - Professional Cloud DevOps Engineer
- Google Cloud - Professional Cloud Network Engineer
- Google Cloud - Professional Cloud Security Engineer
- Java SE 8 Silver
- OSS-DB Silver
- 応用情報技術者
- TOEIC 900点

## 自然言語

- 日本語: ネイティブ
- 英語: かんたんな日常会話ができる

## 職務経歴

一定期間以上従事した、もしくは技術的難度の高かったプロジェクトのみ記載しています。

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
    GKE の Release channel を利用し、自動でバージョンアップを行う設定を導入。開発環境ではRegularチャンネル、本番環境ではStableチャンネルを採用し、事前に検証済みのバージョンを適用する仕組みを構築した。

1. Kubernetes 上での Web アプリケーションの基盤開発

    SPA(Vue.js)、REST API(Java)構成のWebアプリケーション kubernetes 基盤構築

    - Kuberenetes の Deployment, Service, Ingress 等のマニフェスト作成およびデプロイ
    - Helm によるパッケージ、テンプレート管理
    - Nginx によるリバースプロキシ、Basic 認証の設定

    【課題】
    当プロジェクトの他のシステムでは、各環境ごとに素の Kubernetesマニフェストファイルを管理していたが、ちょっとしたフィールドの有無など、意図しない環境間差異が発生していた。

    【解決策】
    環境間で共通の項目をテンプレート化できるツールを採用した。ここでは、Datadog Agent パッケージなどもインストールしやすい Helm を採用した。

1. Datadog を利用した監視設定

    Datadog を利用したGKE, Kubernetesメトリクスの監視設定、ログ収集設定

    - Datadog Agent インストール、GCP Integration 設定
    - Dataflow, Pub/Sub を利用した kubernetes アプリログ収集機構構築

1. CI/CDパイプライン構築

    kubernetes および VM 用 CI/CD パイプライン構築

    - GitHub, GitHub Container Registry, CircleCI を利用した Kubernetes 用 CI/CD パイプラインの構築
    - cron, systemd, Ansible を利用した VM への CD パイプラインの構築

#### 習得スキル

- GKE, Shared VPC
- Kuberenetes(Deployment, Service, Ingress, ConfigMap, Secret), Helm
- Nginx, Ansible
- Datadog

#### コメント

- 初めての Kubernetes 上での Webアプリケーション構築であったが、公式ドキュメントやLLMを活用して、デファクトスタンダードから逸脱しない（作業を引き継いだが苦労しない）アプリケーション基盤を構築できた

<br>

### 専門医による医療健康情報安心化サービス開発(2022/2 ~ 2023/1)

概要: メディアなどのクライアントが執筆した記事を本サービスに登録した医師が妥当性を担保する Webアプリの新規リプレイス開発

#### 担当業務

1. GCP プロダクト選定およびアーキテクチャ設計

    フロントエンド、バックエンド、データベース等に利用するプロダクト設計

    - フロントエンド: Firebase Hosting、バックエンド: Cloud Run、データベース: Firestore
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

    - 上記各プロダクトに対して Pull Requset 作成、マージ時に実行される config ファイルの記述

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
    - 他のメンバーの実装レビュー

    【課題】
    フロントエンドは全くの未経験領域であった。

    【解決策】
    基礎をじっくり学習する時間もなかったので、他のフロントエンドエンジニアに相談する、他機能の既存コードをフル活用しながら、応用→基本という流れで知見をつけた。

#### 習得スキル

- Vue, Nuxt, TypeScript
- Cloud Run、Cloud Build、Eventarc、Cloud Load Balancing、Cloud Armor、Cloud CDN
- Firebase Authentication、Hosting、Firestore、Remote Config

#### コメント

- 初めての新規Webアプリ開発であったが、技術力の高いメンバーに協力を仰いで、作業を進められた。適切で簡潔な質問で知見のあるメンバーから意見を引き出すというのも大切なスキルだと感じた。

- Terraform が書けるようになったこともあり、プロジェクト中盤以降は インフラ周りを完全に任せてもらえるようになった。そこでこれまで断片的になっていた GCP の知見が実務を通して、体系的に整理されたのは非常によかった。

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

#### 習得スキル

- 基本的なWebアプリ開発フロー
- GKE、Docker Compose、Circle CI
- Golang、Gin、Gorm での開発

#### コメント

- 初めての Webアプリ開発であったが、Google Chrome の開発ツールの使い方、クライアントサイドとサーバーサイドの構成、エンドポイントの概念等の理解を、最低限のレベルに早急に引き上げることですぐにバリューを発揮できるようになった。

- 決められたタスクだけでなく、インフラ周りを中心に積極的に自ら課題を見つけ取り組めたことは良かった。意識の問題だけでなく、埋もれている課題を発見するだけの技術力が身についてきたと感じる。

<br>

### スマホゲームの開発・運営支援業務(2020/11 ~ 2021/03)

概要: スマホゲームのサーバーサイド開発、および運用監視

#### 担当業務

1. サーバーサイドAPI設計・実装・単体/結合テスト

    - ゲーム新規イベント用のクライアント用API作成
    - ユーザーデータの Datastore Entity の作成/更新処理
    - ゲーム内のロジック実装
    - ゲーム内のガチャ抽選処理
    - マスタデータの作成

    【課題】
    諸々のドキュメントが皆無で、ゲームの仕様が理解できていないと実装が進められない部分が多々あった。「ソースコードを読んで理解して」という状態であった。

    【解決策】
    ゲームを実際にプレーして仕様を把握した。IDEの機能やオリジナルのメモを作成し、ソースコードの全体像理解に努めた。

1. 他メンバーのソースコードレビュー

    - Golang のコードとして問題/改善点はないか
    - ゲーム仕様を満たすコードが実装できているかどうか
    - テストコードのテストケースは充分かどうか

#### 習得スキル

- 大規模人数での Git/GitHub 開発フロー
- GAE、Datastore、Circle CI
- Golangでのプログラミング、テスト実装

#### コメント

- ビッグタイトルのスマホゲームということもあり、私がいたサーバーサイド担当だけでも10人程、クライアントサイドやテスターも含めると3、40人ほどの大規模案件であった。

- 形態としてはフルリモートのSESであった。参画初期の方は特に良好な人間関係を構築するために積極的にSlackで雑談もするよう心がけた。

<br>

### 携帯端末データのGCP取込(2020/08 ~ 2020/10)

概要: Cloud Storage にアップロードされた特殊な形式のファイルをCSVに変換し、BigQuery にインポートする機能開発。

#### 担当業務

1. GCPアーキテクチャ設計

    【課題】
    通常ならばワークロードとしては Cloud Functions を選択したいところだが、処理対象のファイルサイズが大きく、最大タイムアウト時間の9分を超える可能性があったため、Cloud Functions は使用できなかった。

    【解決策】
    このシステムは別の機能ですでに GKE を利用していたため、ワークロードとしては GKE、なおかつリトライ処理を自前でやってくれる Kubernetes Job を利用することにした。

1. バッチ処理設計・実装・単体/結合テスト

    - Firestore のエンティティ作成/更新処理
    - CSV 変換処理
    - Cloud Storage Compose 処理

1. ストリーミング処理設計・実装・単体/結合テスト

    - PubSubメッセージ受信処理
    - Kubernetes Job 起動処理
    - Kubernetes マニフェストファイル作成
    - Workload Identity の設定

    【課題】
    開発 / 検証 / 本番 環境 でそれぞれ yamlファイルを定義していたが、何か変更がある度に全ファイルを書き換えるのが面倒であった。

    【解決策】
    Kustomize と Skaffold という技術の組み合わせで yamlファイルを環境に応じて上書きするという方法を用いた。他にも Helm という選択肢はあったが扱いにくいという印象を受けたので採用しなかった。

#### 習得スキル

- GCPの基本的なサービス
- GKE、Datastore、Big Query、Cloud Functions、Terraform、Cloud Build
- Golangでのプログラミング、テスト実装

#### コメント

- 初めての Kubernetes (GKE) で最初はどこから理解していったら分からないといった状態であったが、Pod、Node、Deployment、Config などの概念を一つ一つ整理し紐づけることで、「なんとなくはわかる」という状態に素早く持ち込むことに成功し、実装着手まで素早く移行することができた。

<br>

### スマートフォン中古端末買取システム(2020/04 ~ 2020/07)

概要: Cloud SQL にあるデータを BigQuery に取り込み、 Data Portal で可視化。

#### 担当業務

1. データ分析項目の要件定義

    - 顧客の分析したい要望に沿って、KPIを定義した。

1. GCPアーキテクチャ設計

    - Cloud SQL (asia-northeast1) の データを BigQuery (US) にインポートするアーキテクチャの設計。

    【課題】
    BigQuery には外部テーブルとして、Cloud SQLのテーブルを参照する機能があるが、ベータ版の機能で使用が認められなかった。

    【解決策】
    Cloud SQLからCloud Storage にデータを CSV 出力、その CSV を BigQuery に取り込むアーキテクチャを採用した。

1. バッチ処理設計・実装・単体/結合テスト

    - Cloud Storage に 出力された CSV を BigQueryに取込む部分を Cloud Functions (Golang) で実装。

    【課題】
    冪等性の考慮。Cloud Functions は PubSub 通知のメッセージから発火されるが、PubSubは at-least-once配信なので、Cloud Functions が同じCSVファイルに対して複数回起動した場合でも BigQueryには 同じデータが重複しない必要があった。

    【解決策】
    日付型の パーティションテーブルを活用して BigQuery への 書き込みモード  `WRITE_TRUNCATE` (毎回データを上書く) 採用した。

1. BIツールを用いたデータの可視化

    - BigQuery を参照し、定義したKPIを表として出力する。

#### 習得スキル

- GCPの基本的なサービス(IAM、VPC等)
- BigQuery、Cloud Functions、GCS、Cloud SQL
- Data Portal(Data Studio)
- Golangでのプログラミング、テスト実装

#### コメント

- 初めてのGCPであったが、直近のプロジェクトで培ったAWSの知識を用いてかなりはやく慣れることができた。アーキテクチャ設計に関してもAWSで得たノウハウを存分にGCPに適用することができた。

- 新型コロナの影響でリモートワークなので、ビデオ会議が増えた。対面でのコミュニケーションに比べるとインプットされる情報(ジェスチャーや、顔の細かい表情)が少ないので、情報伝達の効率は落ちる。対策として、あらかじめ説明のための補足資料を用意してから会議等に臨むようにした。
結果、いつも30分程度かかっていたMTGが10分程度早く終わるようになった。プロジェクト全体からすると、一人の準備(15分 × 1人)で、全体の(10分 × 4人)の時間を削減できるというのは大きなことだと感じた。習慣として継続したい。

<br>

### 製薬会社向け既存システム統合(2019/01 ~ 2020/01)

概要: 顧客が利用している様々な外部サービスに蓄積されているデータをAWS上で管理分析するための基盤構築。

#### 担当業務

1. AWSアーキテクチャ設計構築

    外部サービスから取得したデータを Amazon Redshift にインポートするアーキテクチャの設計および構築。データフローとしては、EC2 → S3 →  CloudWatch → Lambda → Redshift となった。下記を特に担当。

    - EC2、Lambda の AZ 設計

    - CloudWatch Alarm、SNS通知の設定

    - S3のフォルダ (オブジェクトキーのプレフィックス)の設計

    【課題】
    客先の独自監視システムでバッチ処理のエラー検知を行うことになった。当初は「正規表現を用いた特定の文字列検知」を想定していたが、実装完成後にそのシステムが正規表現は使用できないことが発覚した。

    【解決策】
    一番修正の手間を短縮できる方法を検討した結果、使用していたログパッケージに対するラッパー関数を用意し、「エラーレベルログの場合は特定の文字列とともにログを出力する」という機能を用意することで解決に至った。

1. システム連携バッチ処理の設計・実装・テスト

    外部サービスに保存されているデータを Web API を叩いて取得し、CSV を作成し、S3へアップロードする機能の設計・実装・テスト (Python)。EC2へのデプロイ。

    【課題】
    CSV ファイル作成に際し、仕様上「Web API のレスポンスを CSV にそのまま Parse すれば よい」というものでもなかったので、複雑なデータ操作（文字列操作、分割等）を要求された。

    【解決策】
    スマートな実装方法のようなものはなかったのでトライアンドエラーで複雑なデータ操作を実装した。
    想定されるテストデータを用意し、正常系・準正常系・異常系のインプットに対して適切なアウトプットができているか確認することで、そのデータ操作の確かさを確認した。

1. メンバー間の作業割り振り

    プロジェクト新規参入メンバーへのタスクの割り振り

1. IAM権限のベンダー間調整

    IAM、S3への読み込み書き込み権限の整理

#### 習得スキル

- AWSの基本的なサービス(IAM、VPC等)
- Lambda、S3、CloudWatch、Redshift、EC2
- Pythonでのプログラミング、テスト実装
- Bash Scriptでのプログラミング
- REST APIの知見

#### コメント

- 仕様ドキュメントが英語のみのWebAPIを理解する必要があった。これは英語力が高い人にしかできない作業で私に割り当てられることになった。結果一機能の設計/実装/テストを全て個人で行うことができたので自信につながった。

- Pythonでのプログラミングは初めてであったが、文法的には以前学習していたRuby等と似ていることもあってあまり苦労しなかった。学習には公式チュートリアルやProgateを利用した。

- パブリッククラウド(AWS)も初めてで、こちらは全体を把握するのにかなり時間を要した。一つ一つのサービスについてはドキュメントを読めばそのまま理解できるが、それぞれのサービスの結びつきは基本的なVPCやリージョン、IAMの概念を把握していないと理解できないためである。これらを理解することは目先のタスクを消化するのには寄与しないということもあったが、長期的な時間短縮、何より技術への好奇心から遠回りして基本サービスを把握することに努めた。

<br>

### 携帯キャリア向けデータ移行(2018/09 ~ 2018/12)

概要: SQLServerで稼働している既存のデータベースをOracleに移行。

#### 担当業務

1. バッチ処理設計
1. データ移行マッピングの設計・実装・テスト
1. 新規開発メンバーのサポート

#### 習得スキル

- DBに関する知見（テーブル設計、正規化等）
- Stored Procedureに関する知見
- Oracle PL/SQLでのプログラミング
