---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Avago SafeStore Encryption 서비스를 사용하여 드라이브 보안 사용
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

드라이브 보안을 설정하면 반드시 보안 키가 있어야 제거된 디스크의 저장된 데이터에 액세스할 수 있습니다. 이 키가 없으면 드라이브 데이터를 복구할 수 없습니다. {{site.data.keyword.BluSoftlayer_full}}는 베어메탈 서버에서 구매 가능한 드라이브에 대해 선택된 데이터 센터에서 SED(Self-Encrypting Drives)를 제공합니다. 10TB SATA 드라이브는 US 데이터 센터에서 사용이 가능합니다.

## 선행 조건
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* SED 드라이브가 있는 베어메탈 서버 – 10TB SATA
* LSI/AVAGO MegaRAID SAS 9361 -8i 또는 이와 유사한 LSI/AVAGO RAID 카드
* MSM(MegaRAID Storage Manager) 소프트웨어 설치

## MSM(MegaRAID Storage Manager)을 사용하여 드라이브 보안 사용
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

사용자는 MegaRAID Storage Manager를 사용하여 제거된 디스크의 데이터를 안전하게 보호하고 보안 키를 설정할 수 있습니다. 서버 시작 시에 보안 키를 요구하는 WebBIOS 인터페이스를 사용하여 MegaRAID 카드 BIOS에 진입함으로써 드라이브 보안 설정을 구성할 수도 있습니다. MegaRAID 제어기 카드 SAS 9361-8i에 대한 자세한 정보는 Broadcom 사이트, [MegaRAID SAS 9361-8i ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation)를 참조하십시오. 

### 사전 설치된 SED 드라이브 식별
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager는 지원되는 대부분의 운영 체제에서 사전 설치되어 제공됩니다. 아직 설치되지 않았으면 Broadcom 사이트에서 이를 수동으로 설치할 수 있습니다. 자세한 정보는 [MegaRAID SAS 9361-8i 다운로드](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads)를 참조하십시오.

시스템 인증 정보를 사용하여 MegaRAID Storage Manager를 열 수 있습니다. 이 예에서는 Windows 환경이 사용되며 MSM이 사전 설치되어 있습니다. 

MSM 시작 시에는 권한 부여된 사용자(관리자)와 비밀번호인 **사용자 이름**과 **비밀번호**를 입력해야 합니다.

**실제** 탭을 클릭하고 시스템에서 사용 가능한 드라이브를 클릭하십시오. **특성** 분할창에는 **예**를 보여주는 **전체 디스크 암호화 가능** 필드가 포함된 **드라이브 보안 특성** 섹션이 있습니다. 사용된 예에서는 2개의 비-SED 디스크와 4개의 SED 디스크가 사용됩니다. 

### 제어기에서 드라이브 보안 사용
{: #enabling-drive-security-at-the-controller}

1. 드라이브 보안을 사용으로 설정하려면 **실제** 탭에서 **제어기 0 :AVAGO MegaRAID SAS 9361-8i**에 마우스 오른쪽 단추를 클릭하고 **드라이브 보안 사용**을 선택하십시오. 
  * 이제 **보안 키 ID**와 **보안 키**를 입력할 수 있습니다. 보안 키가 여럿인 경우, 보안 키 ID를 사용하면 사용해야 할 보안 키의 식별에 도움이 됩니다. 보안 키를 안전한 위치에 기록해야 합니다. 보안 키는 드라이브 재구성(예: 드라이브 제거 또는 재삽임) 시에 필요합니다. 보안 키가 없으면 SED에서 작성된 볼륨에 저장된 데이터를 검색할 수 없습니다. 잊어버린 보안 키의 검색은 불가능합니다. 시작 시간 암호도 설정할 수 있어, 여기 설정된 암호가 입력될 때 시스템 일시정지 상태를 유지합니다. 시작 시간 비밀번호는 선택사항이며, 이를 설정한 경우에는 시스템 재부팅 시마다 IPMI에 로그인하여 시작 비밀번호를 입력해야 합니다. 아래로 스크롤하여 **향후 참조를 위해 보안 설정을 기록함**으로 표시된 상자를 선택한 후 **예**를 클릭하여 드라이브 보안을 사용으로 설정하십시오.
  * 드라이브 보안이 사용으로 설정되면 **제어기 0 AVAGO MegaRAID SAS 9361-8i**에 대해 노란색 키 이미지가 나타납니다. 
2. 이제 SED를 사용하여 보안 볼륨을 생성하십시오. **논리** 탭에서 **Controller0**에 마우스 오른쪽 단추를 클릭하고   
**가상 드라이브 작성**을 선택하십시오. 
3. **고급** 옵션을 선택하십시오. 화면은 **RAID 레벨** 및 **드라이브 보안 메소드**를 **FDE(Full Disk Encryption)**로 지정해야 합니다. 필요한 FDE 드라이브를 선택하고 **추가** > **드라이브 그룹 작성** > **다음**을 클릭하십시오.
4. 가상 드라이브 설정을 검토하고 필요한 변경을 수행하십시오. **읽기 정책**의 권장 설정은 **항상 미리 읽기**입니다. **쓰기 정책**의 권장 설정은 **다시 쓰기**입니다. **가상 드라이브 작성**을 클릭하십시오. **예**를 클릭하여 BBU로 인한 다시 쓰기 정책 영향을 허용하십시오. **다음**을 클릭하고 요약 화면을 검토하십시오. **완료**를 클릭하십시오.
5. 가상 디스크가 보호되는지 확인하려면 **논리** 탭과 작성된 가상 드라이브를 클릭하십시오. **드라이브 보안 특성**에서 **보안** 필드가 **예**로 표시되어 있음을 알 수 있습니다. 

서버가 SED 드라이브를 사용하여 이미 작성된 RAID 볼륨과 함께 제공된 경우에는 다음 단계에 따라 볼륨을 보호할 수 있습니다. 

**논리** 탭에서 **드라이브 그룹**에 마우스 오른쪽 단추를 클릭하고 **FDE를 사용하여 보호**를 선택하십시오. 볼륨에 대해 FDE 및 비-FDE 드라이브를 혼합하면 이 옵션이 보이지 않습니다.

드라이브 보안을 제거하려면 우선 보안 가상 디스크를 삭제한 후 제어기 0에 마우스 오른쪽 단추를 클릭하여 **드라이브 보안 사용 안함**을 설정해야 합니다. 이 기능은 내부의 데이터를 완전 삭제하며 드라이브 보안을 제거합니다. 

webBIOS를 사용하고 시작 시에 IPMI를 통해 로그인한 후 RAID BIOS에 진입하여 드라이브 보안을 설정할 수도 있습니다. <!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
