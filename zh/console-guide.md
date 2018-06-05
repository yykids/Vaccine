## Security > Vaccine > 콘솔 사용 가이드

Vaccine Agent 활성화 및 비활성화 절차와 상품 이용중 특정 상황에서 참조할수 있는 가이드입니다.

## Vaccine Agent 활성화 절차

### 리눅스 계열 Agent

1\. 설치 스크립트 '클립보드 복사'

<center>![alt](http://static.toastoven.net/prod_vaccine/linux-1.jpg)</center>
<center>[그림1] 리눅스 계열 설치 스크립트</center>

2\. 설치 대상 인스턴스 터미널 접속

3\. 관리자 권한으로 Agent 스크립트 생성 및 실행

```
[root@vaccine-test ~]# cd ~
[root@vaccine-test ~]# vi agent.sh
[root@vaccine-test ~]# chmod 744 agent.sh
[root@vaccine-test ~]# ./agent.sh
/tmp/DownloadInstallAgentPackage: OK
Downloading agent package ...
curl https://133.186.140.16:4119/software/agent/RedHat_EL7/x86_64/ -o /tmp/agent.rpm --insecure --silent
Installing agent package ...
Preparing...                          ################################# [100%]
Updating / installing...
   1:ds_agent-10.0.0-2775.el7         ################################# [100%]
Starting ds_agent (via systemctl):  [  OK  ]
HTTP Status: 200 - OK
Activation will be re-attempted 30 time(s) in case of failure
dsa_control
HTTP Status: 200 - OK
Response:
Attempting to connect to https://133.186.140.16:4120/
SSL handshake completed successfully - initiating command session.
Connected with (NONE) to peer at 133.186.140.16
Received a 'GetHostInfo' command from the manager.
Received a 'GetHostInfo' command from the manager.
Received a 'SetDSMCert' command from the manager.
Received a 'SetAgentCredentials' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetInterfaces' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetAgentStatus' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetHostMetaData' command from the manager.
Received a 'SetSecurityConfiguration' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetAgentStatus' command from the manager.
Command session completed.
[root@vaccine-test ~]#
```

4\. 웹콘솔 새로고침 및 사용시작

<center>![alt](http://static.toastoven.net/prod_vaccine/linux-2.jpg)</center>
<center>[그림2] 리눅스 계열 사용시작</center>

### 윈도우 계열 Agent

1\. 콘솔 스크립트 복사

<center>![alt](http://static.toastoven.net/prod_vaccine/window-1.jpg)</center>
<center>[그림3] 윈도우 계열 설치 스크립트</center>

2\. 설치 대상 인스턴스 터미널 접속

3\. 관리자 권한으로 Agent 스크립트 생성 및 실행

```
Microsoft Windows [Version 6.3.9600]
(c) 2013 Microsoft Corporation. All rights reserved.

C:\Users\Administrator>powershell -file "agent.ps1"


    디렉터리: C:\Users\Administrator\AppData\Roaming\Trend Micro\Deep Security Agent


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
d----      2018-06-05   오후 2:37            installer
기록이 시작되었습니다. 출력 파일은 C:\Users\Administrator\AppData\Roaming\Trend Micro\Deep Security Agent\installer\dsa_deploy.log입니다.
오후 2:37:23 - DSA download started
오후 2:37:23 - Download Deep Security Agent Package
https://133.186.140.16:4119/software/agent/Windows/x86_64/
오후 2:37:24 - Downloaded File Size:
13897728
오후 2:37:24 - DSA install started
오후 2:37:24 - Installer Exit Code:
0
오후 2:37:32 - DSA activation started
HTTP Status: 200 - OK
Activation will be re-attempted 30 time(s) in case of failure
dsa_control
HTTP Status: 200 - OK
Response:
Attempting to connect to https://133.186.140.16:4120/
SSL handshake completed successfully - initiating command session.
Connected with AES256-SHA256 to peer at 133.186.140.16
Received a 'GetHostInfo' command from the manager.
Received a 'GetHostInfo' command from the manager.
Received a 'SetDSMCert' command from the manager.
Received a 'SetAgentCredentials' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetInterfaces' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetAgentStatus' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetHostMetaData' command from the manager.
Received a 'SetSecurityConfiguration' command from the manager.
Received a 'GetAgentEvents' command from the manager.
Received a 'GetAgentStatus' command from the manager.
Command session completed.
기록이 중지되었습니다. 출력 파일은 C:\Users\Administrator\AppData\Roaming\Trend Micro\Deep Security Agent\installer\dsa_deploy.log입니다.
오후 2:38:29 - DSA Deployment Finished

C:\Users\Administrator>
```

4\. 웹콘솔 새로고침 및 사용시작

<center>![alt](http://static.toastoven.net/prod_vaccine/window-2.jpg)</center>
<center>[그림3] 윈도우 계열 사용시작</center>

## Vaccine Agent 비활성화 절차

### 리눅스 계열 Agent

1\. 웹콘솔 사용중지

<center>![alt](http://static.toastoven.net/prod_vaccine/linux-3.jpg)</center>
<center>[그림3] 리눅스 계열 사용중지</center>

2\. 백신 Agent 삭제

### 윈도우 계열 Agent

1\. 웹콘솔 사용중지

<center>![alt](http://static.toastoven.net/prod_vaccine/window-3.jpg)</center>
<center>[그림3] 윈도우 계열 사용중지</center>

2\. 백신 Agent 삭제

## Vaccine Quick 가이드

### 파일 복원 가이드

툴 다운 (32비트 윈도우 계열)
격리 파일 위치
복원

### 임시 조치 가이드

삭제
덤프

### Image 복제시 사용 가이드

Vaccine Agent 을 포함하여 Image 생성 기능을 사용한 경우 사용 가이드입니다.
사용을 원하는 인스턴스에 접속하여 다음의 스크립트를 실행이후 웹콘솔에서 새로고침 및 사용시작을 통해 사용이 가능합니다.
사용을 원치 않는 인스턴스는 불필요한 리소스가 낭비되지 않도록 설치된 Agent 삭제 후 사용을 권고 드립니다.

리눅스 계열 Agent 스크립트

```
#!/bin/bash
IP=`ifconfig eth0 | grep -w -o '[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}' | head -1`
HOSTNAME=`hostname`
/opt/ds_agent/dsa_control -r
/opt/ds_agent/dsa_control -a dsm://133.186.140.16:4120/ "group:앱키" "displayname:$IP" "hostname:$HOSTNAME"
```

윈도우 계열 Agent 스크립트

```
@echp off
set IP=powershell -Command "((Get-WmiObject win32_networkadapterconfiguration | select ipaddress) | findstr .*[0-9].\.).Split(",")[0].Split("{")[-1]"
echo %IP%
```

## 운영 문의

### 문의 대상

특정 파일 및 폴더 예외처리
Agent 설치 실패 문의
백신 이벤트 탐지 관련 문의
정상 파일 오진 신고 및 복원 관련 문의
백신으로 인한 인스턴스 오동작 조치 및 원인분석 관련 문의

### 문의 방법

문의방법: 고객센터 > 1:1 문의
대응시간: 평일 09:00~12:00, 13:00~18:00