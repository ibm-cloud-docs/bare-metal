---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 佈建裸機伺服器

## 開始之前
您有兩個選項可以佈建公用 {{site.data.keyword.baremetal_long}}。第一個是透過 {{site.data.keyword.cloud}} 型錄，第二個則是透過 {{site.data.keyword.slportal_full}}。型錄及 {{site.data.keyword.slportal}} 需要唯一的登入 ID。您的型錄使用者名稱及密碼無法用於登入入口網站，反之亦然。
{:shortdesc}

開始之前，請確定您已設定 {{site.data.keyword.cloud_notm}} 型錄或 {{site.data.keyword.slportal}} 認證。 
  
**附註：**針對 {{site.data.keyword.cloud_notm}} 型錄，您必須具有已升級的帳戶，才能訂購 {{site.data.keyword.baremetal_short}}。如需升級帳戶的相關資訊，請參閱[切換至 IBM ID](https://console.ng.bluemix.net/docs/admin/softlayerlink.html)。
  
## 登入 
請確定您已透過 {{site.data.keyword.cloud_notm}} 型錄或 {{site.data.keyword.slportal}} 進行登入： 

  <table>
   <CAPTION>表 1. 選擇登入位置</CAPTION>
   <THEAD>
   <TR>
   <th>如果您要使用下列項目登入...</th>
   <th>則...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud 型錄</td>
   <td>
   <ol>
   <li>開啟新的瀏覽器視窗，並輸入 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>。</li>
   <li>按一下<b>登入</b>鏈結。</li>
   <li>輸入電子郵件或 IBM ID，然後按一下<b>繼續</b>。</li>
   <li>輸入密碼，然後按一下<b>登入</b>。</li>
   <li>選取<b>基礎架構</b> > <b>運算</b>。</li>
   <li>按一下 <b>{{site.data.keyword.baremetal_short}}</b> 磚。</li>
   <li>按一下<b>建立</b>。即會開啟 {{site.data.keyword.slportal}} 的主頁面。</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>客戶入口網站</td>
   <td>
   <ol>
   <li>開啟新的瀏覽器視窗，並輸入 <a href="https://control.softlayer.com">https://control.softlayer.com</a>。</li>
   <li>輸入「使用者名稱」及「密碼」，然後按一下<b>登入</b>。或者，按一下<b>使用 IBM ID 登入</b>。然後，輸入電子郵件或 IBM ID，然後按一下<b>繼續</b>。輸入密碼，然後按一下<b>登入</b>。即會開啟 {{site.data.keyword.slportal}} 的主頁面。</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 佈建裸機伺服器
{: #ordering-baremetal-server}
登入之後，即可開始佈建 {{site.data.keyword.baremetal_short}}。您可以透過**裝置**功能表或**裝置**圖示來佈建 {{site.data.keyword.baremetal_short}}。

### 透過裝置圖示佈建裸機伺服器
若要透過*裝置* 圖示來佈建 {{site.data.keyword.baremetal_short}}，請完成下列步驟：

1.  從 {{site.data.keyword.slportal}}，找出**訂購**區段，然後按一下**裝置**。
2.  在「裝置」頁面上，按一下 {{site.data.keyword.baremetal_short}} 下方的**每小時**或**每月**。
3.  選取**資料中心**、捲動瀏覽頁面，然後按一下**開始價格根據**鏈結以選取伺服器。 
4.  在**配置 {{site.data.keyword.baremetal_short}}** 頁面上填寫資訊，然後按一下**新增至訂單**按鈕以繼續。如需如何配置伺服器的相關資訊，請參閱[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md)。驗證訂單之後，即會重新導向至**結帳**頁面。
5.  輸入伺服器的**進階系統配置**。如需如何設定此作業的相關資訊，請參閱[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md)。
6.  按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
7.  確認或輸入付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

 一系列的電子郵件會傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.cloud_notm}} 之後，佈建完成的電子郵件裡會包含*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

### 透過裝置功能表佈建裸機伺服器
{: #ordering-baremetal-devices-menu}

您也可以透過主要 {{site.data.keyword.slportal}} 頁面上的*裝置* 功能表來佈建 {{site.data.keyword.baremetal_short}}。 

1. 按一下**裝置 > 裝置清單**。「裝置」頁面會顯示您帳戶內的所有裝置類型：專用主機、虛擬伺服器、裸機伺服器及 NetScaler 應用程式遞送控制器。
2. 按一下右上角的**訂購裝置**鏈結。
3. 在「訂購 SoftLayer 產品及服務」頁面上，按一下 {{site.data.keyword.baremetal_short}} 下方的**每小時**或**每月**。
4. 選取**資料中心**，捲動瀏覽頁面，然後按一下**開始價格根據**鏈結以選取伺服器。 
5.  在**配置 {{site.data.keyword.baremetal_short}}** 頁面上填寫資訊，然後按一下**新增至訂單**按鈕以繼續。如需如何配置伺服器的相關資訊，請參閱[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md)。驗證訂單之後，即會重新導向至**結帳**頁面。
6.  輸入伺服器的**進階系統配置**。如需如何設定此作業的相關資訊，請參閱[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md)。
7. 按一下**雲端服務條款**及**協力廠商服務合約**勾選框。
8. 確認或輸入付款資訊，然後按一下**提交訂單**按鈕。即會將您重新導向至包含佈建訂單號碼的畫面。您可以列印畫面，因為它也是您的佈建訂單收據。

將一系列的電子郵件傳送給管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。登入 {{site.data.keyword.cloud_notm}} 之後，佈建完成電子郵件會包括*裝置詳細資料* 頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

### 後續步驟
佈建 {{site.data.keyword.baremetal_short}} 之後，即可開始進行管理。如需相關資訊，請參閱[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
