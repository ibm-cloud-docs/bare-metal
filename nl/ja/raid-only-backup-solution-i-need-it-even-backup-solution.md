---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID は、必要な唯一のバックアップ・ソリューションですか? そもそも、バックアップ・ソリューションですか?

RAID は、バックアップ・ソリューションではありません。RAID は、速度/耐障害性を向上させるために複数の物理ディスクが 1 つのアレイに結合された、単一の使用可能なデータ・ディスクを作成します。

SoftLayer では、以下のいくつかのバックアップ・ソリューションを用意しています。

1. [Evault Backup](../infrastructure/backup/index.html)。複数のサーバーでのバックアップを自動化できるエンタープライズ・バックアップ・ソリューションです。データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [Network Attached Storage (NAS)](../infrastructure/network-attached-storage/nas.html)。業界標準であり、重要なデータのサーバー外でのストレージを提供します。データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [R1Soft CDP](../infrastructure/backup/r1soft.html)。中央管理およびデータ・リポジトリーを備えた、ハイパフォーマンスのディスク間サーバー・バックアップを提供します。R1Soft CDP は、ブロック・レベルでデータを保護します。サーバー上の固有のディスク・ブロックが保管されるのは、すべてのリカバリー・ポイントを通して 1 回のみのため、ストレージの効率が向上します。
