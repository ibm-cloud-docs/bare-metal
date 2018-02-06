---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} 中的 POWER8 - 常見問題

|1.|供應項目詳細資料||
|---|---|---|
|1.1|何時發生什麼情況？|<ul><li>SoftLayer 已擴充其供應項目，可包括 POWER8 型裸機系統。這些系統的建置是使用 IBM 的新 POWER8 處理器，以及針對 Linux 上雲端型資料部署、認知及 Web 工作負載特別調整的 OpenPOWER 型平台。</li><li>「虛擬機器即服務」將會進行測試版測試，而且應該會在不久的將來提供。</li></ul>|
|1.2|何謂 OpenPOWER 以及為何要注意它？|<ul><li>OpenPOWER 型伺服器是以 POWER8 架構所建置的全新開放式、強大且可自訂系統；針對資料密集工作負載從基礎設計的唯一處理器。</li><li>OpenPOWER Foundation (OPF) 在 2013 年 8 月時一開始很小，只是由擁有巨大構想的五家公司所形成的聯盟：藉由讓 POWER 軟硬體可用於進行開放式開發，來啟用新的技術及創新方式，以及建置整個產業聯盟來擴充平台上的創新者生態系統。在這麼短的時間內，OPF 已成長為超過 190 位參與者。這項快速成長反映出產業對這個「重新想像資料中心」的熱情。</li><li>OpenPOWER 平台會將 OpenPOWER 開放式協同作業所產生的 POWER8 及創新功能帶到 SoftLayer 公用雲端。</li></ul>|
|1.3|POWER8 平台在 SoftLayer 中的優點為何？|<ul><li>POWER8 針對架構最適用於資料工作負載的傳統雲端平台，帶來獨特的替代方案。相較於進行資料工作負載的類似 x86 系統，效能測試顯示平均 2 倍更好的效能。評比測試讓 SoftLayer 中顯示的 POWER8 可以提供：<ul><li>每小時 1.76x 倍以上的查詢，與 BLU 的 Db2 的每個查詢相較之下，少 20% 的成本。</li><li>在相同的時間量中，雲端中具有 BLU Acceleration on POWER8 的 Db2 提供認知見解的速度快 43%，並且提供多 65% 的見解。</li><li>用於進行資料分類及預測分析的 Spark Machine Learning 提高 64% 更好的效能。</li><li>廣泛用於 Big Data 叢集的 Spark SQL 處理快 66%。</li><li>根據 Spark 圖形工作負載，完整社交連線及產品建議快 83%。</li></ul></li></ul>|
|1.4|供應項目的詳細資料為何？|<ul><li>POWER8 系統的第一個階段適用於每月租賃，並且包括裸機部署的 4 個固定配置：小型、中型、大型，以及含 SSD 的大型（已安裝 Ubuntu OS）。</li><li>這些供應項目包括標準 SoftLayer API 支援，以及大部分的附屬項服務供應項目（例如儲存空間、網路及防火牆）。</li><li>POWER8 系統一開始位於 DAL09 資料中心內，並在 2016 年後期擴充到其他地理位置。</li></ul>|
|||![POWER8 C81](images/power8_fig1.png)<br /><br />![POWER8 圖 2](images/power8_fig2.png)|
||||
|1.5|命名的意義為何？|新的 POWER8 命名格式為 C812L，其中：<ul><li>"C" = 雲端</li><li>"8" = POWER8</li><li>"1" = 核心數</li><li>"2" = 2U</li><li>"L"= Linux</li></ul>|
|1.6|支援哪些作業系統？我可以執行 AIX 或 IBM i 嗎？|<ul><li>SoftLayer 一開始會提供 Ubuntu Linux 14.04 LTS 作業系統，而且稍後會新增其他 Linux 發行套件。</li><li>這些系統無法執行 AIX 或 IBM i。「AIX 即服務」可以從 IBM 的「雲端受管理服務」中取得，而且透過許多全球「商業夥伴」都可以取得受管理的 IBM i。</li></ul>|
||我可以租賃具有 AIX 或 IBM i 作業系統的系統嗎？|<ul<li>IBM 將繼續透過 IBM 的「雲端受管理服務」及其他夥伴在雲端中提供 AIX。IBM i 型雲端服務也可以透過許多 MSP 夥伴取得。</li></ul>|
|**2.**|**移至市場**||
|2.1|誰將從使用 POWER8 獲益？|<ul><li>如果現有 Power 客戶想要針對混合式雲端解決方案擴充其現有系統價值，則 SoftLayer 中 POWER8 供應項目的起始套組十分適合。</li><li>針對資料工作負載最佳化，這些系統可以輕鬆運用於雲端中的「開發/測試」，快速 POC 來證明 Power 的效能優點，或<a href="https://www.ibm.com/developerworks/library/l-port-linux-on-x86-application/">輕鬆地移植應用程式</a>到 Power 或 <a href="https://www-304.ibm.com/partnerworld/wps/servlet/ContentHandler/stg_com_sys_power-development-platform">Power Developer Cloud</a> 及 <a href="https://www-304.ibm.com/webapp/set2/sas/f/lopdiags/sdklop.html">SDK for Linux on Power</a>。</li><li>SoftLayer 雲端中的 POWER8 也可以用來支援運用專用及公用雲端資源的整合式應用程式。</li><li>POWER8 裸機系統也可以是新應用程式（例如基因體學、財務或認知服務）的絕佳管理平台。</li></ul>|
|2.2|最常見的使用案例為何？|<ul><li>在 Ubuntu OS（例如含 BLU 的 Db2、Cognos 或 WebSphere）上執行的資料及分析密集工作負載。</li><li>啟用 Apache Spark、MariaDB 及 LAMP 功能的應用程式（例如電子商務或「內容管理系統」）這類開放程式碼應用程式。</li><li>針對 Linux on Power 工作負載進行開發/測試、移轉及調整。</li><li>競爭 UNIX 工作負載及其他應用程式堆疊的「概念證明」。</li></ul>|
|2.3|我們的客戶有哪些優點？|<ul><li>POWER8 是唯一針對資料而設計的處理器，而且是 IBM 的 Power Systems 系列伺服器的龍頭。{{site.data.keywords_baremetal_short}} 很適合想要在雲端中執行需求、資料密集及認知工作負載的企業。</li><li>針對資料及分析工作負載，POWER8 增加的執行緒數目、記憶體頻寬及速度可以提供比類似 x86 型系統更高的傳輸量及效能。</li></ul>|
|2.4|如何訂購 POWER8 {{site.data.keywords_baremetal_short}}？|<ul><li>「POWER8 Bare Metal 即服務」可以從型錄（例如任何其他 SoftLayer 服務）取得及訂購。</li><li>POWER8 Bare Metal 也作為標準 IBM Cloud 供應項目，而 IBM 及企業夥伴賣方可以將其寫入至任何 IBM Cloud 合約。</li></ul>|
|2.5|POWER8 系統如何定價？|<ul><li>POWER8 裸機系統是根據所提供的效能，定出與 x86 系統類似的定價。</li><li><strong>小型：</strong>8 核心、64GB RAM、1x1TB SATA、10G Gbps、備用電源。</li><li><strong>中型：</strong>10 核心、256GB RAM、2x4TB SATA、10 Gbps、備用電源。</li><li><strong>大型：</strong>10 核心、512GB RAM、2x6TB SATA、10 Gbps、備用電源。</li><li><strong>大型/SSD：</strong>10 核心、256GB RAM、2x960 SSD、10 Gbps、備用電源。</li></ul>|
|**3.**|**在 SoftLayer 中實作 Power**|||
|3.1|我可以將這些新的 POWER8 系統連接至 SoftLayer 中的相鄰 x86 平台，以用於我的分層應用程式環境嗎？|<ul><li>是，針對需要 Power 及 x86 技術的分層應用程式環境，這些系統可以配置成接近其他 SoftLayer 供應項目及應用程式。</li></ul>|
|3.2|我可以在沒有作業系統的情況下佈建 POWER8 系統嗎？|<ul><li>目前無法使用「無 OS」執行的選項。</li></ul>|
|3.3|我可以使用自己的 Linux 作業系統（例如 RHEL 或 SUSE）嗎？|<ul><li>是，但不支援或驗證那些配置。客戶將負責與軟體供應商之間的授權管理、修補程式、版權及維護。SoftLayer 將繼續支援硬體，而且在發生硬體問題時，可能會要求客戶的存取權，以取得與硬體故障相關的 syslog 及錯誤訊息。</li></ul>|
|3.4|何時可以使用 Virtual Machines (VMaaS) on POWER8 架構？|<ul><li>VMs as a Service on POWER8 一般是在 2016 年後期提供。</li></ul>|
|3.5|POWER8 提供哪些自動化及佈建工具？|<ul><li>Canonical 的 JuJu Charms 可以自動部署至 Ubuntu OS。它們有許多預先建置的套件，可用來在 Ubuntu 上自動部署許多 IBM 及開放程式碼套件。在 Canonical 的 <a href="https://jujucharms.com/store">JuJu Charm Store</a> 中可以取得它們。</li></ul>|
|3.6|可以升級這些設計成進行快速佈建的系統，以及您未來將提供可配置的裸機嗎？|<ul><li>SoftLayer 將在未來新增配置選項、附加程式服務、作業系統選項以及每小時定價。</li></ul>|
|**4.**|**未來方向及進一步資訊**||
|4.1|這些新的 POWER8 系統將提供哪些額外的資料中心基礎架構及服務？|<ul><li>SoftLayer 將提供 POWER8 系統與現行 x86 供應項目相同的資料中心選項，但有一些異常狀況（eVault 及軟體型防火牆）。</li><li>SoftLayer 將繼續擴充 POWER8 配置及供應項目一段時間（包括其他配置及儲存空間選項、作業系統、擴充至其他資料中心、GPU 以及其他供應項目），以加強供應項目的選項及功能。</li></ul>|
