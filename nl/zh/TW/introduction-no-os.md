---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 無 OS 選項

「無 OS」選項是用來訂購沒有作業系統的裸機伺服器。

## 如何訂購無 OS 的裸機伺服器？

透過 [SoftLayer.com](softlayer.com) 或[客戶入口網站](https://control.softlayer.com)，藉由發出裸機伺服器訂單開始。

1. 從**系統配置 > 作業系統**中，選取**其他**。
2. 選取**無作業系統**。

## 如何在無 OS 伺服器上安裝作業系統？

您可以利用下列兩種方法在無作業系統的裸機伺服器上安裝作業系統。

### 選項 1：PXE 伺服器

無作業系統的裸機伺服器可以設定成從 PXE 設定開機並載入 OS（如需相關資訊，請參閱 [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)）。只需要在具有 PXE 設定（這通常涉及執行 DHCP 及 TFTP 常駐程式）的網路環境中部署裸機伺服器，並配置新的裸機伺服器 BIOS 以從網路配接卡開機。為了讓它正常運作，請注意 PXE 設定需要在與 PXE 設定相同的 VLAN 中，或需要使用 DHCP 轉遞。

**附註：**可能需要開立支援問題單要求以基本模式重新分組交換器埠，這個選項才能運作。原因是 PXE 通訊協定不需要與鏈結聚集的相容性（即 LACP，請參閱[鏈結聚集](http://en.wikipedia.org/wiki/Link_aggregation)），這現在是提供備援的標準功能。另一個選項是訂購具有「未結合」上行鏈路（無鏈結聚集）的伺服器，然後在安裝 OS 之後將它們變更為備用上行鏈路。

### 選項 2：IPMI 裝置

透過包括的 IPMI 裝置從 ISO 開機，將作業系統安裝在無作業系統的裸機伺服器上。如需從 ISO 開機的相關資訊，請按一下[這裡](mount-iso-bare-metal-server.html)。
