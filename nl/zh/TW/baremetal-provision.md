---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# 建置自訂裸機伺服器
{: #ordering-baremetal-server}

使用下列步驟來建置自訂 {{site.data.keyword.baremetal_long}}。

## 透過 {{site.data.keyword.cloud_notm}} 型錄來佈建
{: #provision-through-the-catalog}

請使用下列步驟，透過 {{site.data.keyword.cloud_notm}} 來佈建 {{site.data.keyword.baremetal_short}}。

1. 開啟 [{{site.data.keyword.cloud_notm}} 型錄](https://cloud.ibm.com/catalog/){: external}。   
2. 在**運算**下選取 {{site.data.keyword.baremetal_short}}。
3. 按一下「繼續」。如果您沒有看到「繼續」按鈕，可能需要登入。
4. 輸入要佈建之**相同**伺服器的**數量**。預設值為 1。如果您想要佈建具有_不同_ 規格的多部伺服器，則需要個別佈建伺服器。
5. **主機名稱**是伺服器的永久或暫時名稱，例如 baremetal01。按一下**資訊**可取得格式化特性。
6. **網域**是識別字串，用來定義網際網路中的管理控制，例如 Customer-123456.cloud。按一下**資訊**可取得格式化特性。
7. **計費**是**按小時**或**按月**。
8. 選取您的伺服器所在的**位置**、地區和資料中心。
9. 按一下**所有伺服器**，以查看處理器清單（單一、雙重及四）及認證伺服器（SAP 和 VMware）。選取最符合您工作負載的伺服器。
10. 選取 **RAM**。對於部分伺服器，RAM 預設值是以「CPU 模型」為基礎，無法變更。 

對於 SAP 認證伺服器，RAM 和「作業系統」預設值是以您選取的伺服器為基礎。您的本端儲存空間選項預設值也會以您選取的伺服器為基礎。
{: note}

11. 為您的 **SSH 金鑰**輸入選用性的公開金鑰，您可以在佈建伺服器之後，使用它來登入伺服器。
12. 選取伺服器的**映像檔**（作業系統）。您的選項是以所選取的伺服器為基礎。
13. 展開**附加程式**以選取與伺服器配置相關的選項。
14. **儲存空間磁碟**是根據您選取的伺服器而預先配置。佈建 {{site.data.keyword.baremetal_short}} 之後，展開**附加程式**以新增檔案或區塊儲存空間磁區。 
15. 在**網路介面**下，選取「上行鏈路埠速度」及「專用 VLAN」選項。展開**附加程式**區段以選取適當的選項，或使用預設值。
16. 在「訂單摘要」中檢閱您的訂單。
17. 在**套用促銷代碼**下，輸入您有的任何促銷代碼。
18. 按一下任何所列出合約的協力廠商服務合約。
19. 按一下**建立**來佈建伺服器。即會將您重新導向至具有佈建訂單號碼的畫面，您可以列印該畫面，因為它也是您的收據。

將一系列的電子郵件傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。

_佈建完成_ 電子郵件會包含*裝置詳細資料* 頁面的鏈結，以便您可以登入 {{site.data.keyword.cloud_notm}}。您也可以直接登入 {{site.data.keyword.slportal}}。

您也可以選擇將訂單儲存為報價，或將其新增至預估。當您儲存報價時，會將鏈結傳送至與您帳戶相關聯的電子郵件位址。請開啟鏈結以查看已儲存的報價資訊。另一個選項是移至「管理」>「計費及用量」，然後選取「銷售」>「裝置報價」。如果您有存取權，則可以按一下報價並確認訂單，以購買所報價的供應項目。新增至預估會將配置所提議成本放在定價計算機中。如需定價計算機的詳細資料，請按一下**資訊**。

## 透過客戶入口網站進行佈建
請使用下列步驟，透過 {{site.data.keyword.slportal}} 來佈建 {{site.data.keyword.baremetal_short}}。

1. 使用您的唯一認證登入 [{{site.data.keyword.slportal}}](control.softlayer.com){: external}。
2. 移至**帳戶** > **下訂單**。
3. 選擇**按小時**或**按月**。
3. 從清單選取您的 {{site.data.keyword.baremetal_short}} 所在的資料中心，然後按一下**開始價格**來選取認證伺服器（SAP 或 VMware）或處理器（單一、雙重及四）。
4. 輸入要佈建之**相同**伺服器的_數量_。預設值為 1。如果您想要佈建具有_不同_ 規格的多部伺服器，則需要個別佈建伺服器。
5. 選取 **RAM**。對於部分伺服器，RAM 預設值是以「CPU 模型」為基礎，無法變更。 

對於 SAP 認證伺服器，RAM 和「作業系統」預設值是以您選取的伺服器為基礎。您的本端儲存空間選項預設值也會以您選取的伺服器為基礎。
{: note}

6. 選取您的作業系統。
7. 選取硬碟和其他系統附加程式。
8. 按一下**新增至訂單**，在這裡您會被重新導向以確認您的訂單。
9. 確認或編輯伺服器的網域資訊。**主機名稱**是伺服器的永久或暫時名稱，例如 baremetal01。 
10. 選取**雲端服務條款**及**協力廠商服務合約**。
11. 在**促銷代碼**下，輸入您有的任何促銷代碼，然後按一下**套用**。
12. 確認或輸入您的付款資訊，然後按一下**提交訂單**。即會將您重新導向至具有佈建訂單號碼的畫面，您可以列印該畫面，因為它也是您的收據。 

將一系列的電子郵件傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。在您登入 {{site.data.keyword.Bluemix_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

## 後續步驟
佈建 {{site.data.keyword.baremetal_short}} 之後，即可開始進行管理。如需相關資訊，請參閱[管理 {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers)。
