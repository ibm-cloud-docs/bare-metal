---



copyright:
  years: 1994, 2017
lastupdated: "2017-11-24"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ハードウェア・モニタリングおよびセキュリティー管理

悪意のある脅威の増大と高度化のため、お客様は、より厳しいセキュリティー要件を課し、実行環境のあらゆる側面を精査するようになっています。ワークロードが既知の場所にある信頼できるハードウェアで実行されているかどうかを判別できるようにするハードウェア・モニタリングおよびセキュリティー管理を提供するように、クラウド・プロバイダーが期待されるようになっています。{{site.data.keyword.cloud}} は、Intel&reg; Trusted Execution Technology (Intel&reg; TXT) を使用して起動環境のセキュリティー検査を強化したハイブリッド環境およびクラウド環境をデプロイできるようにすることで、その道を開拓しています。{:shortdesc}

## 仕組み

Intel TXT は、{{site.data.keyword.cloud_notm}} インフラストラクチャーにデプロイまたはマイグレーションされるワークロードが、既知の場所にある信頼できるハードウェアで実行されていることを企業に保証できるようにするハードウェア・モニタリングおよびセキュリティー管理を提供します。{{site.data.keyword.cloud_notm}} は、各種 {{site.data.keyword.baremetal_short}} で、Intel TXT のサポートを提供します。完全なリストについては、http://www.softlayer.com/intel-txt を参照してください。

Intel TXT は、オペレーティング・システムやハイパーバイザーからコンピューティング・システムのブート・ファームウェアやハードウェアに至る、コンピューティング・システムのコンポーネントを分析して測定します。この分析には、システムの BIOS (Basic Input/Output System)、マスター・ブート・レコード (MBR)、ブート・ローダーが含まれます。測定値が標準ベースラインと比較され、システムが信頼できるのか信頼できないのかが判別されます。システム・ソフトウェアおよびローカルまたはリモートの管理ソフトウェアでは、信頼性の判断を使用して、当該コンピューティング・システムでのワークロードの実行を許可または拒否できます。Intel TXT はブート時に分析および測定を実行するため、セキュリティーの追加によってアプリケーションにパフォーマンスのオーバーヘッドが追加されることはありません。

ベースライン測定値は、Trusted Platform Module (TPM) ハードウェア・デバイスに保管されます。TPM デバイスは、サーバー・システム内に統合され、さまざまな Intel TXT セキュリティー関連機能を提供します。

## 実行機能

Intel TXT は、医療、金融サービス、政府組織など、コンプライアンスおよび監査の規制を受ける大規模エンタープライズの場合に特に利点をもたらします。関連するコンプライアンス団体 (HIPAA、PCI、FedRAMP、ISO、FISMA、SSAE 16) に対応して、すべての信頼できるリソースの追跡を確実に統合、管理、報告できるようになります。初めて、以下のようなワークロードについてクラウド・コンピューティング・システムが適切に保護されていると、これらの団体が認定できるようになります。

* ガバナンスおよびエンタープライズのリスク
* 情報およびライフサイクルの管理
* コンプライアンスおよび監査
* アプリケーション・セキュリティー
* ID およびアクセスの管理
* インシデント対応

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} での Intel TXT について詳しくは、http://www.softlayer.com/intel-txt を参照してください。

[IBM、VMware、HyTrust を使用した信頼できるセキュアなクラウド・ソリューション](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf)を使用したワークロードへのセキュリティーおよびコンプライアンスの追加について詳しくは、リンク先を参照してください。

**特別な技術的注意** Intel Trusted Execution Technology (Intel TXT) は、Intel&reg; によって提供され、サポートおよび管理のために特定の技術的知識を必要とする {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 上で動作します。
{{site.data.keyword.cloud_notm}} の現行デリバリー・モデルでは、Intel TXT をオンまたはオフにすることができます。**お客様の環境およびデータの機密性のため、{{site.data.keyword.cloud_notm}} では、Intel TXT 設定の構成を支援できません**。Intel の TXT テクノロジーについてスタッフをトレーニングするか、信頼の根幹 (Root of Trust) および MLE (Measured Launch Environment) アーキテクチャーにおける実績のある知識を持つコンサルティング会社と協議してください。
