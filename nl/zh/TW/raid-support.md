---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID 支援問題單資訊
{:# bm-raid-support-ticket}

如果您遇到有關在裸機伺服器上使用 RAID 的問題或疑問，可以在 [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} 討論區中找到答案。您也可以開立支援問題單。如需支援問題單的相關資訊，請參閱[開立支援問題單](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}。
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> 建立支援問題單時，您需要提供 RAID 日誌檔。RAID 日誌檔中的資訊對於遺失 RAID 配置的回復至關重要。提供日誌檔可協助支援團隊識別磁碟機順序、陣列成員資格、陣列幾何佈置及纜線安裝問題。視您使用的 RAID 控制器類型是 Adaptec 還是 LSI 而定，請使用下列指令來取得 RAID 日誌檔。

**附註：**授與在起始更新時重新啟動/關閉電源的許可權，或要求將磁碟機熱交換，可加速支援問題單程序。

<b>Adaptec RAID 卡</b><br>
請使用下列指令來取得 Adaptec RAID 卡的日誌檔。請務必在支援問題單中包含此日誌檔的完整輸出。

`arcconf getconfig 1/arcconf getlogs 1 device tabular`。

<b>LSI RAID 卡</b><br>
請使用下列指令來取得 LSI RAID 卡的日誌檔。您需要在支援問題單包含這些日誌檔的完整輸出。
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**重要事項：**在開始疑難排解之前，請務必先備份任何工作。
