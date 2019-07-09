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


# 예비 풀에서 디바이스 재활성화
{: #bm-reactivating-spare-pools}

디바이스를 예비 풀에 추가하면 디바이스 목록에서 해당 상태는 디바이스가 표준 상호작용에 적격임을 나타내는 활성에서 예비 풀로 변경됩니다. 예비 풀의 일부인 디바이스는 해당 기능에만 전용되며 기타 디바이스와 같이 일반적인 일상 조치에는 사용될 수 없습니다. 일반적인 기능으로 돌아갈 수 있도록 예비 풀에서 디바이스를 제거하려면 이를 재활성화해야 합니다.
{:shortdesc}

## 예비 풀에서 디바이스 재활성화

1. 고유 인증 정보를 사용하여 [{{site.data.keyword.cloud}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/){: new_window}에 액세스하십시오.
2. 탐색줄에서 **디바이스 > 예비 풀**을 선택하여 *예비 풀* 화면에 액세스하십시오.
3. 원하는 디바이스의 **조치 > 디바이스 재활성화**를 선택하십시오.
4. 서버를 재활성화하려면 **예**를 클릭하십시오. 조치를 취소하려면 **아니오**를 클릭하십시오.

## 다음 단계
재활성화 프로세스를 시작하고 나면 디바이스가 오프라인이 되고 펌웨어가 업데이트되며 디바이스가 일반 용도로 사용할 수 있게 됩니다. 재활성화 프로세스는 약 1시간 걸립니다. 예비 풀에서 제거된 디바이스는 더 이상 장애 복구 메소드로 사용할 수 없습니다. 예비 풀에 다시 디바이스를 추가하여 언제든 디바이스를 여분 풀에 반환할 수 있습니다. 자세한 정보는 [예비 풀에 디바이스 추가](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools)를 참조하십시오.
