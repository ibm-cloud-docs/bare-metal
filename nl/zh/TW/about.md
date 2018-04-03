---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 開始使用 {{site.data.keyword.baremetal_short}}

{{site.data.keyword.baremetal_long}} 提供效能及控制權。{{site.data.keyword.baremetal_short}} 不會在 Hypervisor 中執行，而且您可以取得硬體資源的低階存取權。此外，其他客戶都不會與您共用伺服器 -- 全部都是您的！
{:shortdesc}

建立 {{site.data.keyword.baremetal_short}} 時，您可以自訂從處理器及地區到作業系統及硬碟的規格。

若要佈建 {{site.data.keyword.baremetal_short}}，請執行下列動作：
  1. 移至**運算 > {{site.data.keyword.baremetal_short}}**，然後按一下**新增**。
  2. 選取您要在其中佈建 {{site.data.keyword.baremetal_short}} 實例的位置。這是其中一個 {{site.data.keyword.Bluemix}} 地區中的資料中心。
  3. 選取伺服器的配置。此配置適用於針對此實例所建立的所有伺服器。
  4. 選取您要針對此實例而建立的伺服器數目。針對每一部伺服器，輸入唯一的主機名稱。
  5. **選用項目：**輸入您所定義用來配置伺服器的 Script 或文字檔的 URL。佈建 Script 必須使用 HTTPS 通訊協定。佈建實例之後，將會下載並執行 Script（可能的話）。如果 URL 未與可執行的 Script 相關聯，則只會下載 Script。
  6. 選取伺服器的作業系統。此作業系統適用於針對此實例所建立的所有伺服器。

在一個小時內，您的 {{site.data.keyword.baremetal_short}} 便會佈建且可供使用。
