---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 建置自訂裸機伺服器
{: #ordering-baremetal-server}

使用下列步驟來建置自訂 {{site.data.keyword.baremetal_short}}。

1. 開啟 [{{site.data.keyword.cloud_notm}} 型錄](https://console.bluemix.net/catalog/){:target="_blank"}。   
2. 選取 Bare Metal Server。
3. 按一下「建立」。
4. 在伺服器清單下，尋找陳述：**對其他配置選項感興趣嗎？請按一下這裡**。選取此選項。這時會顯示自訂伺服器表單。
1. 選取伺服器的資料中心位置。
* 按一下**開始價格根據**鏈結，從三個伺服器種類選取伺服器。
  * SAP 認證伺服器（如需佈建 SAP 認證伺服器的相關資訊，請參閱 [{{site.data.keyword.cloud_notm}} SAP 認證基礎架構](/docs/bare-metal/bare-metal-sap-applications.html)）
  * 單一處理器多核心伺服器
  * 雙重處理器多核心伺服器

* 從您的配置選項選取。**資料中心**、**RAM** 和**作業系統**是必要欄位。所有其他欄位都是選用欄位。如需選用欄位的相關資訊，請參閱**[其他伺服器配置選項](#addl-server-options)**。

    **附註**：伺服器和作業系統之間存在衝突時，會顯示錯誤訊息。例如，在 Microsoft SQL Server 上選取 Linux。
* 按一下**新增至訂單**。即會顯示「結帳」頁面。

  從「結帳」頁面中，您可以按一下其中一個重新配置選項，回到配置頁面。
* 在「進階系統配置」區段中，指定其他配置選項。如需相關資訊，請參閱**[進階系統配置](#adv-system-config)**。

*   按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
*   確認或輸入您的付款資訊，然後按一下**提交訂單**。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

  您也可以按一下**另存為報價**，儲存此訂單而不採購。

 將一系列的電子郵件傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。在您登入 {{site.data.keyword.cloud_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

 ## 其他伺服器配置選項
 {: #addl-server-options}

 當您佈建裸機伺服器時，可以使用其他選項，例如公用頻寬、上行鏈路埠速度、公用次要 IP 位址等等。表 1 說明您的其他選項。


 |**欄位** |**說明** |
 |-------------------|---------------|
 |伺服器安全|例如 Trusted Execution Technology (Intel TXT)|
 |Software Guard Extensions|提高機密程式碼和資料的安全 (Intel SGX)。<br><br>請參閱[使用 Intel SGX 佈建裸機伺服器](../bare-metal/bare-metal-provision-SGX.html)。|
 |RAM|選擇符合您伺服器需要的 RAM 層次。|
 |作業系統 |從 CentOS、FreeBSD、Microsoft、Red Hat、Ubuntu 或「其他」中進行選取。|
 |硬碟 |利用使用者介面中的工具，根據您選取的 OS 預先填入欄位，來設定硬碟。<br><br> 您也可以選取使用 Intel Optane SSD 磁碟機。請參閱[佈建 Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html)。
 |公用頻寬 |決定在一個月的期間，可以透過公用介面傳送的資料量。針對需要透過此介面所傳送之安裝資料的測試環境，需要調整超過一開始所傳送資料量的值。請考慮 [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn)，以將起始資料負載傳送至其中一個 {{site.data.keyword.cloud_notm}} 資料中心。可以升級任何 {{site.data.keyword.baremetal_short}}，以包括未計量（無限制）頻寬。所有未計量的裝置都位在專用的專用埠上。|
 |上行鏈路埠速度 |判定內部及外部介面的速度。|
 |公用次要 IP 位址 |將其他 IP 位址指派給伺服器。根據您的情境，您可能需要進一步指派給伺服器的 IP 位址。可額外使用的數量為 1、2、4、8、16 或 32 的 IPv4 位址。|
 |主要 IPv6 位址 |指派給伺服器的內部及外部介面。|
 |公用靜態 IPv6 位址 |從 /64 區塊指派其他 IPv6 位址。|
 |作業系統附加程式|選取諸如 VMware、備份解決方案、控制台、資料庫、硬體 & 軟體防火牆、防毒軟體、間諜軟體保護、侵入偵測 & 保護等選項。<br><br>強烈建議您讓公司安全部門符合 {{site.data.keyword.cloud_notm}} 支援中心的標準，以討論這些選項的詳細資料。
 |Evault |代理程式型備份工具，可以安裝在伺服器上，以抄寫伺服器之間的備份。|
 |服務附加程式|選取任何服務附加程式，例如監視、自動回應和保險。|
 {: caption="表 1. 其他伺服器選項" caption-side="top"}

## 進階系統配置
{: #adv-system-config}

**進階系統配置**下的欄位會完成您的佈建程序。

|**欄位** |**說明** |
|---|---|
|主機名稱 |伺服器的永久或暫時名稱，例如，_server1_。**附註**：如果您要佈建 SAP 認證伺服器，您的 SAP 主機名稱必須由最多 13 個英數字元組成。如需 SAP 主機名稱的相關資訊，請參閱 [SAP Notes 611361](https://launchpad.support.sap.com/#/notes/2611361) 和 [129997](https://launchpad.support.sap.com/#/notes/129997)。需要 SAP S 使用者 ID。|
|網域 |不應該與網際網路網域名稱衝突的子網域名稱，例如，_test.acme.com_。|
|VLAN 選擇 |如果您的帳戶下有 VLAN，因為您已訂購至少一部伺服器，則可以將新伺服器新增至該 VLAN。|
|佈建 Script |您可以提供 Script，以容許您在佈建之後自動執行某些步驟。|
|SSH 金鑰 |您可以提供 SSH 金鑰的公開金鑰，以容許您在佈建之後登入伺服器。|
{: caption="表 2. 進階系統配置" caption-side="top"}

 如需進一步資訊，請洽詢 {{site.data.keyword.cloud_notm}} 支援中心。

 **附註：**您可以使用運算裝置來訂購次要子網路。不過，如果您訂購次要子網路，則在收回運算裝置時會收回它們。如果您獨立訂購次要子網路（而不是作為運算訂購的附加選項），則可以保留子網路，直到您明確取消它為止。請務必記住這項區別，如此才不會在收回運算裝置時，意外地遺失部分 IP 位址。

## 後續步驟
佈建 {{site.data.keyword.baremetal_short}} 之後，即可開始進行管理。如需相關資訊，請參閱[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
