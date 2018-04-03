---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 베어메탈 서버에 Ubuntu 서버 설치

{{site.data.keyword.IBM&reg; Cloud}}에 의해 제공되지 않는 운영 체제를 사용하려면 사용자 정의 ISO(디스크 이미지)를 마운트하여 베어메탈 서버에 설치할 수 있습니다. ISO 업로드를 마운트하려면 서버와 연관된 파일 스토리지(NAS)에 업로드하십시오. ISO를 NAS에 업로드하려면 다음 프로시저에 따라 IPMI를 사용하여 ISO에 마운트하십시오.
1. **운영 체제가 없는** 베어메탈 서버를 주문하십시오. 
* 운영 체제로 NAS에 연결하는 데 사용할 수 있는 무료 OS(예: CentOS)를 선택할 수 있습니다.
* 부트 가능한 ISO를 저장하기 위한 NAS 스토리지를 주문하십시오. 이미 Windows CIFS 서버가 있는 경우 이를 사용하여 ISO 이미지를 공유할 수 있습니다. 이 Windows CIFS 서버를 사용하여 20GB 용량의 여유 NAS를 얻을 수 있습니다. NAS를 프로비저닝한 후 고객 포털에서 NAS에 대한 설명을 볼 수 있습니다.
* https://www.ubuntu.com/download/server 에서 ISO 이미지를 다운로드하십시오.
* NAS 또는 Windows CIFS 서버에 ISO 이미지를 업로드하십시오. NAS 스토리지가 있는 경우 FTP를 사용하여 ISO 이미지를 업로드할 수 있습니다.

  샘플 FTP 프로시저는 다음과 같습니다.
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* IPMI를 사용하여 {{site.data.keyword.Bluemix_notm}}에 VPN 연결을 설정하십시오. 지원 메뉴 또는 URL([VPN 액세스](http://www.softlayer.com/VPN-Access))에서 VPN 메뉴를 시작할 수 있습니다.
* 관리 IP를 통해 IPMI에 연결하여 IPMI 가상 미디어 메뉴에서 ISO 이미지를 마운트하십시오.
  1. IPMI 신임 정보를 보십시오.
  * IPMI 보기를 로그하십시오.
  * 가상 미디어 탭을 여십시오.
  * IPMI에 대한 관리자 권한이 있는 루트 사용자가 필요합니다. 권한이 *운영자*로 표시되면 지원 티켓을 열어서 권한을 관리자로 변경하십시오.
  * ISO 이미지 연결 세부사항을 채우십시오.
    공유 호스트 = NAS의 IP 주소<br/예: 10.3.x.x
    이미지 경로 = 다음 형식의 ISO 파일 이름: \NASusername\imagefilesname.iso(예: \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    사용자 = NAS의 사용자 이름
    비밀번호 = NAS의 비밀번호
  * **마운트** 단추를 클릭하십시오.
  * 디바이스를 확인하십시오.
* KVM 뷰어를 클릭하여 실행하고 가상 미디어 메뉴에서 가상 스토리지 페이지를 여십시오. ISO 이미지를 CD-ROM 디바이스로 마운트하는 데 성공하면 **연결 상태 히스토리**에 디바이스 설명이 표시됩니다.
* SoftLayer 티켓을 통해 서버가 가상 CD-ROM을 첫 번째 디바이스로 부팅하도록 요청하십시오. 각 서버에 대해 이 요청을 완료하십시오. OS가 설치된 후에 부팅 설정을 변경할 수 있습니다.
 **참고**: BIOS에서 부팅 순서를 변경하기 위해 지원 팀에 문의할 필요는 없습니다. 이는 서버에 따라 다릅니다. 다시 한번 부팅을 시도하여 부팅 순서를 확인하십시오.
* KVM 보기에서 서버를 다시 부팅하십시오.
* 마운트된 ISO 이미지에서 OS를 설치하십시오.
* ISO에서 베어메탈 서버에 Ubuntu OS를 설치하십시오.
* 네트워크 설정(IP 주소/서브넷/게이트웨이/DNS 등)을 구성하십시오. 설치 단계 중에 올바르게 구성되지 않으면 다시 부팅한 후에 KVM 콘솔을 통해서만 이 서버에 연결할 수 있습니다.

* 가상 미디어를 마운트 해제하십시오. IPMI 가상 미디어 탭을 통해 서버에서 가상 미디어를 마운트 해제해야 합니다.
* 서버를 다시 부팅하십시오.
* 다시 부팅한 후에 SSH를 통해 서버에 액세스하십시오.
