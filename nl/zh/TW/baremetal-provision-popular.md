---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 從最熱門伺服器中選取
「最熱門伺服器」清單中的伺服器已預先配置為符合大部分用戶端使用案例的需求，而且在訂購它們之後，它們在 30 到 40 分鐘內即可執行。
1. 開啟 [{{site.data.keyword.cloud_notm}} 型錄](https://console.bluemix.net/catalog/){:target="_blank"}。   
2. 選取 Bare Metal Server。
3. 按一下「建立」。
2. 選取下列資訊：
    <table>
    <CAPTION>表 1. 裸機伺服器選擇</CAPTION>
    <THEAD>
    <TR>
    <th>欄位</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>數量</td>
    <td>使用 + 和 - 圖示來指定要佈建的相同伺服器數目。<br>如果您要佈建具有不同規格的多部伺服器，則需要個別佈建它們。
    <tr>
    <td>位置</td>
    <td>選取您想要伺服器所在的地區和資料中心。</td>
    </tr>
    <tr>
    <tr>
    <td>主機名稱及網域</td>
    <td>這些欄位會移入預設值。您可以變更它們。</td>
    </tr>
    <tr>
    <td>選取伺服器</td>
    <td>在**熱門伺服器**下，選取符合您需求的伺服器。這些伺服器已預先配置，在 30 到 40 分鐘內即可使用。
    </tr>
    <tr>
    <td>RAM</td>
    <td>根據您所選伺服器的預設值。</td>
    </tr>
    <tr>
    <td>SSH 金鑰 </td>
    <td>提供 SSH 金鑰的公開金鑰，您可以在佈建伺服器之後，使用它來登入伺服器。</td>
    </tr>
    <tr>
    <td>映像檔<br>（作業系統）</td>
    <td>選取實例的作業系統。**附註**：伺服器和作業系統之間存在衝突時，會顯示錯誤訊息。例如，在 Microsoft SQL Server 上選取 Linux。</td>
    </tr>
    <td>上行鏈路埠速度 </td>
    <td>判定內部及外部介面的速度。</td>
    </tr>
    <tr>
    <td>附加程式</td>
    <td> 選取適當的選項，或使用預設值。</td>
    </tr>
    </TBODY>
    </table>

3.  在「訂單摘要」區段中，選取**按小時**或**按月**計費。
4.  檢閱您的訂單。
5.  檢閱任何列出的協力廠商服務合約，然後按一下**協力廠商服務合約**勾選框。
6.  按一下**佈建**。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

 一系列的電子郵件會傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。佈建完成電子郵件會包含*裝置詳細資料* 頁面的鏈結，以便您可以登入 {{site.data.keyword.cloud_notm}}。您也可以直接登入 {{site.data.keyword.slportal}}。


## 後續步驟
佈建 {{site.data.keyword.baremetal_short}} 之後，即可開始進行管理。如需相關資訊，請參閱[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
