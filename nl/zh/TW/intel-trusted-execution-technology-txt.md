---



copyright:
  years: 1994, 2017
lastupdated: "2017-11-24"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 硬體監視及安全控制

惡意威脅的增加及複雜可讓您運用更嚴格的安全需求，並詳細檢查執行環境的每個層面。您會希望雲端提供者提供硬體監視及安全控制，以判斷工作負載是否在已知位置的授信硬體上執行。{{site.data.keyword.cloud}} 可讓您使用 Intel&reg; Trusted Execution Technology (Intel&reg; TXT)，利用啟動環境的加強型安全驗證來部署混合式及雲端環境。
{:shortdesc}

## 運作方式

Intel TXT 提供硬體監視及安全控制，協助確認部署或移轉至 {{site.data.keyword.cloud_notm}} 基礎架構的工作負載是在已知位置的授信硬體上執行的業務。{{site.data.keyword.cloud_notm}} 支援 {{site.data.keyword.baremetal_short}} 範圍上的 Intel TXT。如需完整清單，請參閱 http://www.softlayer.com/intel-txt。

Intel TXT 會分析及測量從作業系統或 Hypervisor 到運算系統開機韌體及硬體的運算系統元件。分析包括系統的基本輸入/輸出系統 (BIOS)、主要開機記錄 (MBR) 及開機載入器。測量會與標準基準線進行比較，以判斷系統是受信任還是不受信任。系統軟體及本端或遠端管理軟體可以使用信任決策，來允許或拒絕工作負載在該運算系統上執行。因為 Intel TXT 會在開機期間執行分析並測量，所以新增的安全不會為應用程式新增任何效能額外負擔。

基準線測量儲存在「授信平台模組 (TPM)」硬體裝置上。TPM 裝置整合至伺服器系統內，並提供某範圍的 Intel TXT 安全相關功能。

## 它可執行的動作

Intel TXT 特別適用於具有規範及審核規定的大型企業，例如保健、金融服務及政府組織。它有助於確定追蹤可以整合、管理及報告相關規範組織（HIPAA、PCI、FedRAMP、ISO、FISMA 及 SSAE 16）上的所有授信資源。第一次時，這些組織將可以認證雲端運算系統可適當地保護工作負載的安全，例如：

* 控管及企業風險
* 資訊及生命週期管理
* 規範及審核
* 應用程式安全
* 身分及存取管理
* 突發事件回應

如需 {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 上 Intel TXT 的相關資訊，請造訪 http://www.softlayer.com/intel-txt。

下列鏈結的相關資訊是有關使用[含 IBM、VMware 及 HyTrust 的授信安全雲端解決方案](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf)來新增工作負載的額外安全及規範。

**特殊技術注意事項**：Intel Trusted Execution Technology (Intel TXT) 由 Intel&reg; 所提供，作用於需要有特定技術知識以進行支援及管理的 {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}。{{site.data.keyword.cloud_notm}} 現行遞送模型容許我們開啟或關閉 Intel TXT；**{{site.data.keyword.cloud_notm}} 因客戶環境及資料的靈敏度而無法協助配置 Intel TXT 設定**。建議您透過編排信任及已測量啟動環境 (MLE) 架構 root 的經過驗證的專門知識，來訓練人員的 Intel TXT 技術或與諮詢公司合作。
