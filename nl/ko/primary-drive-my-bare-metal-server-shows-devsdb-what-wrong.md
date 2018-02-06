---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 베어메탈 서버의 기본 드라이브가 /dev/sdb로 표시됩니다. 무엇이 문제입니까?

IPMI의 가상 디스크가 /dev/sda 슬롯을 차지한 것이 원인일 수 있습니다. IPMIView에 연결하여 가상 미디어 탭을 찾아서 사용하지 않도록 안전하게 설정할 수 있습니다. **옵션 > 사용 안함**을 선택하고 **적용** 단추를 클릭하여 변경을 수행하십시오. 베어메탈 서버가 다음에 다시 부팅될 때 기본 드라이브가 /dev/sda를 표시합니다.
