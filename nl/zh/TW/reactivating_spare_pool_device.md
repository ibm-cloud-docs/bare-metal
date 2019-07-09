---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

keywords: bare metal reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 重新啟動備用儲存區中的裝置
{: #bm-reactivating-spare-pools}

裝置在新增至備用儲存區時，它在「裝置清單」內的狀態會從「作用中」（指出裝置適用於標準互動）變更為「備用儲存區」。屬於備用儲存區一部分的裝置是專用於該功能，無法像其他裝置一樣用於傳統的日常動作。若要移除備用儲存區中的裝置，以回復為其傳統功能，則必須將它重新啟動 (reactivate)。
{:shortdesc}

## 重新啟動備用儲存區中的裝置

1. 使用您的唯一認證來存取 [{{site.data.keyword.cloud}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/){: new_window}。
2. 從「導覽列」中選取**裝置 > 備用儲存區**，以存取*備用儲存區* 畫面。
3. 選取所需裝置的**動作 > 重新啟動裝置**。
4. 按一下**是**來重新啟動伺服器。按一下**否**來取消動作。

## 後續步驟
在起始重新啟動處理程序之後，裝置會離線、更新韌體，而且裝置可供一般使用。重新啟動處理程序大約需要一個小時。從備用儲存區中移除的裝置不再適合用作失效接手方法。透過將裝置重新新增至備用儲存區，裝置隨時都可以回到備用儲存區。如需相關資訊，請參閱[將裝置新增至備用儲存區](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools)。
