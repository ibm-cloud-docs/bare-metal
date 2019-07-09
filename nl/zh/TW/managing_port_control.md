---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 管理裝置的埠控制
{: #bm-manage-port-control}

與帳戶相關聯的每一台裝置都有兩個網路埠，用於接收送入的資料流量；一個用於公用網路資料流量，而另一個用於專用網路資料流量。您可以隨時啟用或停用這些埠，以控制裝置收到的網路資料流量。請完成下列步驟來更新裝置的埠控制設定。

## 開始之前
* 導覽至主控台的裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/bare-metal?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者可以調整許可權。

如需許可權的相關資訊，請參閱[標準基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取](/docs/bare-metal?topic=virtual-servers-managing-device-access)。

## 管理裝置的埠控制

1. 存取**裝置清單**，然後選取要更新的**裝置名稱**。  
2. 按一下裝置的**動作**下拉清單。
3. 選取**埠控制**。
4. 完成下列其中一個動作，以更新*公用網路* 及/或*專用網路* 下拉方框：
   * 選取想要的速度以啟用網路存取。
   * 選取「已斷線」以停用網路存取。
5. 按一下「更新」按鈕。
6. 按一下「關閉」按鈕來關閉視窗。

## 後續步驟

如果您選取**已停用**，則會停止對裝置介面之停用埠的網路存取。如果您選取**已啟用**，則已啟用的埠可以進行網路存取。埠控制會保留在選取的設定中，直到手動變更為止。
