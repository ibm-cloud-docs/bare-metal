---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 取消備用儲存區
{: #cancel-spare-pools}

已新增至備用儲存區的裝置只能從 {{site.data.keyword.cloud}} 主控台的「備用儲存區」畫面取消。取消備用儲存區中的裝置，與取消「裝置清單」內的裝置相同。請遵循下列步驟，以取消備用儲存區中的裝置。
{:shortdesc}

## 取消備用儲存區

1. 從要取消的裝置備份您想要保留的任何資料。

   取消裝置會導致移除已取消裝置中的所有資料。取消裝置之後，就無法擷取裝置上所儲存的所有資訊。
   {:tip}

2. 使用您的唯一認證來存取 [{{site.data.keyword.cloud}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/){: new_window}。
3. 從「導覽列」中選取**裝置 > 備用儲存區**，以存取*備用儲存區* 畫面。
4. 選取特定裝置的**動作 > 取消裝置**。
5. 從**原因**下拉清單中，選取取消原因。
6. 在提供的文字框中，輸入簡短取消說明。
7. 按一下**繼續**，以繼續下一個畫面。按一下**取消**，以停止取消處理程序，並回到「備用儲存區」畫面。
8. 選取**資料流失確認**，以確認在取消處理程序期間可能會發生資料流失。
9. 按一下**取消裝置**，以取消裝置。按一下**關閉**，以停止取消處理程序，並回到「備用儲存區」畫面。

## 後續步驟
要求取消備用儲存區中的裝置之後，會排定裝置進行取消。接著會立即從帳戶中收回並移除裝置。
