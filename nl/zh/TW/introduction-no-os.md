---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# 無 OS 選項
{: #bm-no-os}

**無 OS** 選項是用來訂購不含作業系統的 {{site.data.keyword.baremetal_long}}。

## 訂購不含 OS 的 {{site.data.keyword.baremetal_short}}
{: #ordering-no-os}

1. 使用[建置自訂裸機伺服器](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)所概述的步驟來訂購您的伺服器。
2. 在**映像檔**下選取**無 OS**。
3. 完成伺服器訂單。 

## 變更為無 OS
{: #changing-to-no-os}

伺服器可以重新配置成沒有任何 OS。重新配置是透過 OS 重新載入來完成。如需相關資訊，請參閱[重新載入 OS](/docs/infrastructure/software?topic=software-reloading-the-os)。

1. 按一下**裝置** > **裝置清單**。
2. 選取要重新配置為無 OS 的伺服器。
3. 按一下 **OS 重新載入**，然後輸入適用的資訊。

## 在無 OS 伺服器上安裝作業系統
{: #installing-os-on-no-os-server}

在沒有任何作業系統的 {{site.data.keyword.baremetal_short}} 上，安裝作業系統的方法有兩種。

### 選項 1：PXE 伺服器
{: #option-1}

沒有任何作業系統的 {{site.data.keyword.baremetal_short}} 可以設定成從 PXE 設定開機並載入 OS。在具有 PXE 設定（這通常涉及執行 DHCP 及 TFTP 常駐程式）的網路環境中部署 {{site.data.keyword.baremetal_short}}，並配置新伺服器 BIOS 以從網路配接卡開機。如果要無 OS 選項能正常運作，PXE 設定需要在與 {{site.data.keyword.baremetal_short}} 相同的 VLAN 中，或需要使用 DHCP 轉遞。

可能需要開立支援問題單，要求以基本模式重新分組交換器埠，這個選項才能運作。原因是 PXE 通訊協定不需要與鏈結聚集的相容性 (LACP)，這現在是提供備援的標準功能。另一個選項是訂購具有「未結合」上行鏈路（無鏈結聚集）的伺服器，然後在安裝 OS 之後將它們變更為備用上行鏈路。
{: note}

### 選項 2：IPMI 裝置
{: #option-2}

透過包括的 IPMI 裝置從 ISO 開機，將作業系統安裝在沒有任何作業系統的 {{site.data.keyword.baremetal_short}} 上。如需從 ISO 開機的相關資訊，請參閱[在裸機伺服器上裝載 ISO](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server)。
