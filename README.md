## 시험일정 6.8 1시50분까지
![image](https://github.com/chihyeonwon/Linux_master/assets/58906858/00ca3be8-d19b-4dcf-a534-c76e0353b0ae)
![image](https://github.com/chihyeonwon/Linux_master/assets/58906858/268b183f-a8b7-47d7-a4e3-f30c901c4cd6)
```
자유 소프트웨어인 리눅스를 공부할 수 있어서 좋다~

리눅스 소스 코드가 공개되어 있는 대표적인 오픈 소스 프로젝트다.
Linux 재단에 따르면 퍼블릭 클라우드 컴퓨팅 워크로드의 90%, 스마트폰의 82%, 임베디드 기기의 62%, 슈퍼 컴퓨터 시장의 99%가 Linux로 작동한다.
모바일 운영체제로 유명한 Android 역시 Linux 커널을 가져다 쓰고 있다.
GNU 프로젝트가 주도한 시스템 소프트웨어 및 라이브러리로 이루어진 Linux 배포판을 GNU/Linux라 부르기도 한다.

2007년부터 2019년 사이의 Linux 커널 참여자 중 회사순위를 보면
1위 Intel (10.01%), 2위 Red Hat (8.90%), 3위 IBM (3.79%), 4위 SUSE (3.49%), 5위 Linaro (3.17%), 6위 Google (2.79%), 7위 삼성전자 (2.58%),
8위 AMD (2.28%), 9위 르네사스 (1.99%), 10위 Texas Instruments (1.78%), 11위 Oracle (1.70%), 12위 Broadcom (1.23%), 13위 Huawei (1.2%),
14위 Mellanox (1.19%), 15위 NXP (1.18%), 16위 ARM (0.98%), 17위 Linux 재단 (0.78%) 등으로 모두 반도체/통신/IT/시스템 업체임을 알 수 있다.
```
## 취득 목적
```
리눅스마스터 2급을 보게 된 이유는 안드로이드 개발자가 되고자 하는 마음에 공부를 하였습니다.
안드로이드는 리눅스 기반에서 탄생된 프로그램입니다.
즉, 리눅스에서 안드로이드 스튜디오가 만들어졌기에 안드로이드 개발자가 되려면 리눅스를 조금이라도 알아야 될 것 같아
자격증을 취득하기로 마음을 먹었습니다.

많은 앱개발자들이 리눅스 커널을 띄어놓고 테스트를 해보며 개발하는 모습을 유튜브로 간접적으로 확인해서
나도 앱개발자가 되면 어차피 리눅스로 테스트를 하면서 개발하겠다라고 생각하고
그러면 미리 뭔지 알아놓으면 나중에 편하겠지?"라고 생각했습니다.
```
## 24.05.04 1차 합격
![image](https://github.com/chihyeonwon/Linux_master/assets/58906858/9a80fafc-5686-4a49-a5c2-d48b27e57fb8)

## 2차 접수 24.06.08 Seoul 2시
![image](https://github.com/chihyeonwon/Linux_master/assets/58906858/6f47d706-6aa2-4280-ade9-e8369332b696)

## 1차 50문제 한 문제 CBT
## 2차 80문제 CBT
```
신분증, 수험표(가채점용)

Cent OS 7 -> 21년도 기출부터 적용, 기출풀고 틀린문제 개념 정리, 반복
21~23년 10회 기출
```
## 24.05.05 파일 시스템 관련 명령어
```
소유권 변경 -> chown(소유자, 그룹), chgrp(그룹만)
허가권 변경 -> chmod

-R 옵션으로 하위 모든 파일에 대한 소유권과 허가권을 변경할 수 있음

chown 옵션 소유자or:그룹명 파일명 (앞에 콜론으로 소유자와 그룹을 구분함)

ls -l 파일형식과 허가권을 알 수 있다.
파일 형식은 허가권 맨 앞 한자리

- : 일반파일, d 디렉토리파일, s 소켓, p 파이프, I 바로가기 아이콘(심볼릭), c 문자 특수

허가권은 rwx로 8진수 숫자모드로 지정한다.
```
## 24.05.06 파일 시스템의 관리, 셸(Shell)
```
ext3 : ex2의 확장판, 저널링 파일 시스템 
저널링 파일 시스템 : 저널(로그)를 이용한 빠르면서도 안정적인 복구
JFS : IBM사의 독자적인 저널링 파일 시스템

네트워크 파일 시스템
CIFS : SMB를 확장한 파일 시스템
NFS : 네트워크 파일 시스템

기타 파일 시스템
NTFS : 윈도우 기반 파일 시스템
UDF : ISO 9660 파일 시스템 대체용

mount : 디바이스와 디렉터리를 연결하는 명령어
unmount : 디바이스와 디렉터리 연결을 해제하는 명령어

mount -t smbfs : 삼파 파일 시스템 마운트
mount -o loop : iso 마운트
-o remount : 파티션을 재마운트
-o noatime : 파일이 변경되기 전까지 access time이 변경되지 않음

eject : 보조기억장치의 미디어를 해제하고 장치를 제거하는 명령어
eject -r : 시디롬 마운트 해제
eject -f : 플로피 마운트 해제

fdisk : 파티션의 생성, 기존 파티션 삭제 등을 수행
fdisk -v : fdisk 버전 표시
fdisk -n : 파티션 생성
fdisk -d : 파티션 삭제
fdsik -p : 디스크 정보 표시

mkfs : 리눅스 파일 시스템 생성하는 명령어
mkfs -t 파일 시스템 : 생성할 파일 시스템 타입 지정
mkfs -c : 파일 시스템 생성 전 배드블록을 검사

mke2fs : ext2, 3, 4 타입의 파일 시스템을 생성하는 명령어
mke2fs -t 파일 시스템 타입 지정
mke2fs -j : 저널링 파일 시스템 ext3로 지정

fsck : 무결성을 검증하고 대화식으로 복구하는 명령어
/lost+found 디렉토리에서 오류를 수정하게 되며 복구되면 파일은 사라진다.

du : 디스크 사용량을 확인하는 명령어
df : 마운트된 디스크의 하드디스크 용량 확인 명령어

-h : 용량 단위로 표시
-T : 파일 시스템 유형과 파티션 정보 출력
-k : 1K 블록사이즈
-i : inode 사용률 확인

셸 : 명령어 해석기, 스크립트 언어, 자체 프로그래밍 기능
$ : 본셸 , % C셸

본셸

ksh : AT&T사의 데이비드 콘이 개발
bash : 리눅스 기본 쉘, GNU 프로젝트, Posix와 호환

C셸

csh : C언어의 특징, 빌조이가 개발, 히스토리, 별명, 작업제어
tcsh : csh의 확장판, 명령어 편집 기능 제공

셸 확인 명령어 : /etc/shells = chsh -l : 사용 가능한 셸을 나열한다.

셸 변경 명령어 :
chsh -s 계정명 셸(일반 사용자 환경)
usermod -s 셸 계정명(관리자 환경)

환경변수(전역변수) : env 대문자
셸 변수(지역변수) : set

PS1 : 셸 프롬프트 선언 시 사용
PS2 : 2차 셸 프롬프트 선언 시 사용
USER : 사용자이름
PWD : 현재 디렉토리 절대경로명
TERM : 터미널 종류의 이름
LANG : 기본 지원 언어

프롬프트 설정 방식
\W : 마지막 디렉터리만 표시
\w : 현재 작업중인 디렉터리 절대 경로
\u : 현재 사용자의 이름
\h : 호스트 이름

전역 설정 파일 : etc로 시작
지역 설정 파일 : 홈디렉토리에서 숨김파일로 시작

/etc/profile : 전역, 모든 사용자 환경설정
/etc/bashrc : 별칭과 bash에 관련한 함수 모음 전역

~/.bash_profile : 지역, 개개인 사용자 환경설정
~/bashrc : 별칭과 bash에 관련한 함수 모음 지역

bash History
!! : 마지막 실행한 명령어
!n : n번째 실행
!string : string으로 시작하는 명령문
!?문자열? : 문자열을 포함하는 명령문

HISTSIZE : 히스토리의 스택크기
HISTFILESIZE : 히스토리의 물리적인 크기
HISTFILE : 히스토리 파일 위치
HISTTIMEFORMAT : 히스토리 수행 시간 출력 형태 지정
```
## 24.05.07 프로세스 관리
```
가장 먼저 실행되는 프로세스 : init init의 pid는 1
fork() :새로운 프로세스를 만들때 기존 프로세스를 복제한다.
exec() : 새로운 프로세스를 만들때 기존 프로세스에 코드를 덮어씌운다.

데몬 : 리눅스 시스템이 부팅 시 자동으로 실행되는 백그라운드 프로세스

stand alone(단독실행) : 서비스 요청이 많은 것을 메모리에 상주시킨다
ex) http, mysql, nameserver, sendmail
실행 스크립트 위치 : /etc/inetd.d

inetd 데몬(슈퍼데몬) : 다른 데몬들의 상위에 존재하는 stand alone 데몬
보안상의 이유로 리눅스 커널 2.4부터 xinetd 가 inetd 역할을 수행
ex) FTP, telnet,rlogin

시그널
2 - SIGINT Ctrl+C 입력시 종료
3 - SIGQUIT Ctrl+\ 입력시 코어덤프
9 - SIGKILL 종료
15 - SIGTERM 종료
19 - SIGSTOP 종료
20 - SIGTSTP Ctrl+Z 입력 시 프로세스 대기로 전환
```
## 24.05.07 프로세스 유틸리티
```
ps -Z : 작업 종료 후 회수되지 않아 메모리에 적재되어 있는 상태
RSS: 실제 사용하는 메모리의 량을 나타낸다.
ps -aux : 현재 실행디ㅗ고 있는 모든 프로세스의 정보를 알 수 있다.
pstree -p : 프로세스 id 값을 프로세스의 정보를 트리구조로 출력한다.
pstree : 실행 중인 프로세스들을 트리 구조로 나타낸다.

jobs : 백그라운드로 실행 중인 프로세스를 확인한다, 프로세스 대기 상태를 확인한다.
ctrl + z : 프로세스 대기 상태로 전환(포어그라운드 프로세스를 백그라운드 프로세스로 전환)
fg 작업번호 혹은 fg %작업번호

백그라운드로 작업하고자 할 때 명령어 뒤에 &를 붙인다.

kill -1 %6 = kill -HUP : 6번인 프로세스에게 재시작요청을 한 번 보낸다.
KILL -9 : 강제 종료
Killall -l : 시그널 목록
Kill -l : 시그널 옵션, 더 자세함
nice : 일반 사용자는 nice값을 증가시킬 수 밖에 없다. 우선순위를 낮출 수 밖에 없다.
renice -0 5546 <- 기존의 값에서 -0으로 변경한다.
nice -10 bash <- 기존 -5에서 +10 -> 5
프로세스 ni값의 범위 : -20 ~ 19 우선순위는 낮을 수록 높다.
top : 운영 상태를 실시간 모니터링 하는 명령어
top 명령어로 실행 중인 상태에서 다양한 명령어를 사용하여 프로세스 상태를 제어할 수 있다.

top -T : 명령어 라인 항목을 ON/OFF 할 수 있다.
top k : 특정 프로세스를 종료할 수 있다.

nohup : 터미널이 닫혀도 실행 중인 프로세스를 백그라운드 프로세스로 작업할 수 있게 해준다.
(명령어 맨 뒤에 &을 붙인다)

crontab : 분, 시, 일, 월, 요일, 명령어
crontab : -u 특정 사용자
-e : 수정
```
## 24.05.08 에디터 종류, 활용
```
pico편집기 : 복제 프로그램 nano, Aboil Kasar, Pine이라는 e-mail 클라이언트와 같이 배포
pico Ctrl + O : 파일 저장, Ctrl + A : 시작 부분으로 이동 Ctrl + X : 프로그램 종료

emacs 편집기 : 리처드 스톨만이 개발한 고성능 문서 편집기, 강력한 질의, 치환 명령
명령어의 형태가 alt, ctrl 키와의 조합, LISP에 기반의 환경 설정 언어
Ctrl + F: 커서를 오른쪽으로 이동

vi 편집기 : 모드 편집기
vi 편집기에서 특정 문자열 치환 방식 s/바꿀문자열/바뀔문자열/g

vi +num  num으로 이동, 생략일 때는 마지막 줄로 이동한다.
vi :$ : 편집 중인 텍스트 파일의 가장 마지막 줄로 이동
vi n 같은 방향으로 다음 문자열 검색
/ 아래방향으로 검색, ? 위 방향으로 검색

vi -r : 비정상적인 종료되었을 때 파일 복구

.exrc 는 vi 편집기의 환경 설정 등록, 해당 파일에서 set 명령 사용 시에는 :콜론을 붙임
:set nu

vi : 빌조이, vim : 브람 무레나르가 개발

set ai <- 자동 들여쓰기 기능
nano 편집기 <- 윈도우의 메모장과 유사

리눅스에서 사용하는 편집기의 종류 : vi, vim, emacs

gedit 드로그앤 드롭이 가능하고 그롬 데스크톱 환경용으로 개발된 자유 소프트웨어 텍스트 편집기
```
## 24.05.09 소프트웨어 설치 및 삭제
```
패키지의 파일 형식 : 패버릴아 패키지명-번호-릴리즈번호-아키텍처번호
아키텍처 : i686 or i586 인텔 cpu 아키텍처

rpm -h : 패키지 설치 과정을 #로 표시한다.
rpm -V 검증 결과 -> S 파일 크기, -V 권한(다이제스트 값)변경, -T 수정일 변경

rpm --force 옵션에 포함되는 옵션 3개 : replacepkgs(재설치), replacefiles(이미설치된것을덮어씀), oldpackage(구버전 다운그레이드)
-qip : rpm 파일에 대한 정보
rpm -e : 패키지 삭제

rpm -Uvh : -U 설치되어있다면 업그레이드, 없다면 설치
rpm -v 검사할때 사용
rpm -ql : 패키지목록
rpm -qi : 패키지정보

데비안 계열 우분투 의존성 해결 -> apt-get
레드햇 계열 의존성 해결 -> yum

yum remove : 패키지 제거
yum search : 패키지에서 문자열 포함된 것 찾기
yum groupinstall : 그룹을 설치하기 위한 방법

데비안 패키지 관리인 deb 파일의 형식 : 패버릴아

dpkg -s : 패키지의 정보 출력
dpkg -i : 지정된 패키지를 설치

apt-get 명령어가 의존성과 충돌성 해결을 위해 참조하는 파일 : /etc/apt/sources.list

데비안 우분투 : dpkg , apt-get
레드햇 : rpm , yum
```
## 24.05.10 소스 파일 설치
```
파일 아카이브 : 다수 개의 파일이나 디렉터리를 하나로 묶는 것
명령어 tar
tar -c : 새로운 아카이브 파일 tar 생성
tar -x : tar로 묶은 것을 원본으로 복원 (묶음 해제)
tar -t : 아키이브 파일 안의 목록 나열
tar -f : 아카이브 파일명 지정
tar -v : 처리하고 있는 파일 정보를 출력
tar -z : gzip으로 압축하거나 해제
tar -J : xz 옵션으로 압축 파일인 tar.xz에 사용

압축률 compress < gzip < bzip2 < xz

.Z compress
.gz gzip
gzip -l 파일 정보를 나타냄
gunzip 파일 압축 해제
zcat 압축 파일의 내용을 출력

.bz2 bzip2, bunzip2

xz -d 강한 파일 압축 해제

컴파일 순서 configure -> make -> make install (일반 파일)
Mysql의 cmake 는 생성과 설치만 한다. cmake -> make install
cmake는 크로스컴파일을 지원, 평행 빌드 지원, 타임스탬프 지원
```
## 24.05.11 주변 장치 연결 및 설정
```
프린터 인쇄 시스템 LPRng, CUPS

LPRng : BSD 유닉스 계열, 프린터 스풀링과 네트워크 프린터 서버 지원
설정 파일 : /etc/printcap

CUPS : 애플이 개발한 오픈 소스 프린팅 시스템
HTTP 기반의 IPP (포트: 631)를 사용하여 웹 기반으로 프린터를 제어
설정 파일 : /etc/cups

/etc/cups/cupsd.conf : 프린터 데몬 환경 설정 파일
/etc/cups/printers.conf : 프린터 큐 환경 설정
/etc/cups/classes.conf : CUPS 프린터 데몬의 클래스 설정 파일
cupsd : CUPS의 프린터 데몬

cups 인쇄 시스템 : 로컬 접속으로 프린터를 직접 연결할 수 있다.
직렬 포트 : /dev/lp0 파일로 가능
usb 포트 : /dev/usb/lp0 파일로 가능

windows printer via samba : 윈도우 <-> 리눅스 프린터 설정 시 사용 삼바 기반의 smb 프로토콜 사용 smb/cifs

사운드 카드 지원 시스템 : OSS, ALSA

OSS :표준 유닉스에 기반, 유닉스 운영체제에서 사운드를 만들고 캡처

ALSA : 사운드 카드용 장치 드라이버를 제공, gpl 라이센스를 따른다, 사운드 여러 개 장치를 관리

스캐너 지원 : SANE, XSANE

SANE : 이미지 관련 하드웨어를 제워하는 API
SCSI 스캐너 : /dev/sg0, /dev/scanner로 인식
usb 스캐너 : /dev/usb/scanner, /dev/usbscanner로 인식

XSANE : X-Windows 기반의 스캐너 프로그램
x-windows에서 xsane이라고 입력하면 실행
다양한 장치, 이미지 수정 작업을 할 수 있다.
```
## 24.05.14 주변 장치 활용
```
bsd 계열 : lpr, lpq, lprm, lpc
system V 계열 : lp, lpstat, cancel

lpr, lp : 프린터 요청을 한다.
lpr -# : 인쇄할 매수를 지정
lp -n : 인쇄할 매수를 지정

lpq : 큐에 있는 작업 목록을 출력
lpc : 라인프린터 컨트롤 프로그램

lpstat : 프린터 큐의 상태를 확인

alsactl : alsa 사운드 카드를 제어
alsamixer : 커서 라이브러리 기반의 오디오 프로그램
cdparanoia : 오디오 CD로 부터 음악 파일 추출

sane-find-scanner : scsi 스캐너와 usb 스캐너 관련 장치 파일을 찾아주는 명령어
scanimage : 이미지를 스캔
scanimage -d : sane 장치 파일명 입력
scanimage --format : 이미지 형식 지정
scanimage -L : 사용가능한 스캐너 목록 출력

scandf : 여러 개의 사진을 스캔

xcam : GUI 기반으로 스캐너나 카메라로부터 이미지를 스캔
```
## 24.05.15 X-윈도우 개념 및 사용법
```
x-윈도우 : 그래픽 사용자 인터페이스GUI를 제공한다.
플랫폼과 독립적으로 작동하는 그래픽 시스템이다.
X-윈도우는 X11, X, X Window System 이라 한다.
Bob Scheifler와 Jim Gettys가 x-윈도우를 처음 개발
오픈 소스 프로젝트 디자인을 만들었다.
네트워크 기반의 그래픽 환경
서버프로그램과 클라이언트 프로그램으로 나누어 작동한다.
오픈 데스크톱 환경으로 KDE, GNOME, XFCE 등이 있다.

XProtocol : X 서버와 클라이언트 사이의 메시지 타입, 메시지 교환 방법을 지정
Xlib : 윈도우 생성, 이벤트 처리, 창 조회, 키보드 처리와 같은 라이브러리 제공, 저수준
XCB : Xlib 보다 향상된 스레드 기능을 지원하고 확장성이 뛰어남, 라이브러리의 크기가 작고 단순, XProtocol에 직접 접근
Xtoolkit : XT intrinsic, XView, Xaw, Motif, Qt, GTK 등이 있음
xFree86 : 인텔 86 계열의 유닉스 운영체제에서 동작하는 X 서버

X-윈도우 실행 : 터미널 윈도우로 로그인한 경우에는 몇 개의 프로그램을 실행해야 한다.
startx는 X-윈도우를 실행하는 스크립트로 시스템 환경을 초기화하고 xinit을 호출한다.
xinit에 매개변수 인자를 전달하는 옵션은 --이다

X-Windows 강제 종료 : ctrl + alt + backspace

윈도우 매니저는 X 윈도우 상에서 창의 배치와 표현을 담당
twm -> fvwm
window Maker : 현재는 GNOME 과 KDE에 통합
BlackBox : 넥스트스텝의 인터페이스를 기반으로하는 윈도우 매니저
kwm : KDE의 기본 윈도우 매니저

데스크톱 환경 : gui 사용자에게 제공하는 인터페이스 스타일로 데스크톱 관리자라고도 한다. 뒤에 E나 e가 붙음

KDE : 오픈소스 데스크톱 환경, QT Toolkit을 기반으로 한다. Unix/linux, solaris freeBSD 등이 있다.

GNOME : gnu에서 만든 공개형 데스크톱으로 소스 공개 자유 소프트웨어이다.

LXDE
XFCE

디스플레이 매니저 : X windows system 상에서 작동하는 프로그램, 사용자에게 그래픽 로그인 화면을 띄워주고
아이디와 패스워드를 입력받아 인증을 진행하고 인증이 정상적으로 완료되면 세션을 진행한다. 뒤에 m이 붙음

gdm : CentOS 운영체제에서 사용, GNOME의 디스플레이 매니저, GTK 라이브러리를 사용해 구현됨
```
## 24.05.15 X-윈도우 활용
```
xhost는 x 서버에 접속할 수 잇는 클라이언트를 지정하거나 해제 ip 주소 기반
환경변수 display로 x 서버 프로그램이 실행되는 클라이언트 주소를 지정한다.

xauth .Xauthority 파일의 쿠키 내용을 추가, 삭제, 리스트를 출력하는 유틸리티
xauth는 mmc 방식의 인증 방식을 사용하기 위한 필수 유틸리티 이다.
ip주소나 호스트 명이 아닌 x 윈도우 실행시에 생성되는 키 값으로 인증

$HOME/.Xauthority에 대해 읽기 쓰기 권한 Xauthority 파일에는 매직 쿠키가 있어야 한다.
매직 쿠키 값 : MIT-MAGIC-COOKIE-1이라는 쿠키값을 가진다.

xauth add, xauth list $diplay

오피스 LibreOffice Write 문서작성기, impress : 프레젠테이션, Calc : 스프레드 시트, Draw 드로잉
gedit 텍스트 편집

gimp 이미지편집
imageMagick
eog : GNOME 의 이미지 편집
kolourpaint : Ubuntu의 이미지 편집
gThumb GNOME 데스크톱 이미지 뷰어
gwenview : KDE의 이미지 뷰어

멀티미디어 : totem : 음악관리
thythmbox : 통합형 음악관리

개발 : eclipse

dolphin : kde용 파일 관리자
kSnapshot : 스크린샷 프로그램
```
## 24.05.16 네트워크 개념
```
Eternet/ IEEE 802.3 -> CSMA/CD 사용
Token Ring/ IEEE 802.5 -> 통신 회선의 길이 제한이 없으며 확장성이 용이하지 않음
FDDI (Fiber-Distributed Data Interface) : Token Passing 사용

MAN : MAN은 LAN보다 크고 WAN보다는 작은 도시권 통신망
DQDB : MAN에서 사용되는 IEEE 802.6 규격인 QPSX의 제어접속에 사용된다.

패킷 교환망
X.25  :ITU-T의 표준화 통신 규약, DCE, DTE 사이에 이루어진 상호작용
가변길이 프레임 전송을 지원하는 프레임릴레이의 근간을 이룸

ATM : Frame을 Cell로 나누어서 전송

SAN : 스토리지를 위해 고안된 스토리지 전용 고속 네트워크
호스트 컴퓨터 종류에 구애받지 않고 별도의 연결된 저장장치 사이에 대용량의 데이터를
전송시킬 수 있는 고속 네트워크이다.

LAN 토플로지
성형 : 중앙 컴퓨터 고장 시 전체 네트워크 사용이 불가능
망형 : 장애 발생 시 다른 시스템에 영향이 적고 우회할 수 있는 경로가 존재하여 신뢰성이 높은 방식
회선 구축 비용이 많이 듦
버스형 : 하나의 통신회선에 여러 컴퓨터를 연결해서 전송
링형 : 토큰 패싱이라는 방식을 통해 데이터 전송 , 각 노드가 좌우 인접 노드와 연결
논리적인 순환형 토플로지로 하나의 노드장애가 전체 토플로지에 영향

CSMA/CD : 단말기가 전송로의 신호 유무를 조사하고 다른 단말기가 신호를 송출하는지 확인

토큰 패싱 : Token passing, FDDI
Token 의 흐름에 따라 전송 순서가 결정된다.
free token -> busy token -> free token

브릿지 : 주소에 따라 목적지 포트로 프레임을 전달
스위치 : 브릿지보다 빠르게 데이터를 전송, 브릿지와 유사
라우터 : 서로 다른 통신망과 프로토콜을 사용하는 네트워크 간의 통신을 가능하게 함
게이트웨이 : 서로 다른 통신망이나 프로토콜을 사용하는 네트워크 간의 통신을 가능하게 하는 장비를 통칭

이기종 : 양쪽을 568-B 로 연결
같은 컴퓨터 종류 : 한쪽 568-A 한쪽 568-B

568-A : 녹파주갈
568-B : 주파녹갈

ISO : 국제표준기구는 OSI 모델을 정의하였다.
프로토콜 : 형식, 의미, 순서 (Syntax, Semantic, timing)
TCP, UDP

SYN_RECEIVED : SYN는 서버에게서 받았지만 아직 클라이언트 측으로부터 응답은 받지 못한 상태
ESTABLISED : 서버와 클라이언트가 서로 연결된 상태

IP 주소
A 클래스 0
B 클래스 10
C 클래스 110

사설 A : 10.0.0.0 ~ 10.255.255.255
사설 B : 127.16.0.0 ~ 127.31.255.255
사설 C : 192.168.0.0 ~ 192.168.255.255

서브넷팅 : 특정 네트워크를 여러 개의 네트워크로 분리하여 브로드캐스트 도메인을 나누는 것


기준에서 늘어난 네트워크 ID 비트를 서브넷 ID라고 부른다.
26 -> 8/8/8/2 <- 끝에 2비트를 서브넷 ID 2의 2승 서브넷 4개
```
## 24.05.17 인터넷 서비스의 종류
```
WWW 서비스 : HTTP를 기반으로 한 멀티미디어와 하이퍼텍스트를 통합한 정보 검색 시스템, 분산 클라이언트 - 서버 모델을 기반으로 함

고퍼 시스템 : 미국의 미네소타 대학에서 개발된 정보 검색 서비스
인터넷상의 정보들을 체계적으로 분류하여 사용자가 특정 정보가 저장되어 있는 서버의 주소를 모르더라도 멘 방식의 인터페이스를 이용하여 쉽게 찾을 수 있다.

SMTP : 송신, 메일 서버 간의 메시지 교환
POP3, IMAP : 수신, 도착한 메일을 사용자 컴퓨터에서 확인할 때

FTP : TCP/IP에 의해 제공되는 호스트 간의 파일 복사
포트 20 : 일반 데이터용 , 21번 제어용 데이터
익명 로그인 : 아이디 anonymous 비밀번호 란에 enter

DNS : 호스트 이름을 IP주소로 변환하거나 조회해주는 프로토콜
DNS 최상위 도메인 7개 : org 비영리기관, net 네트워크 기관, com:영리목적
edu 교육기관, gov 정부기관, mil 군사기관 int : 국제기관
kr, jp,fr 국가기관

dns 설정 정보나 질의응답을 점검하기 위한 명령어 : nslookup, dig

ssh는 암호화뿐만 아니라 압축 기술도 제공한다.
telnet을 이용하여 특정 인터넷 서비스의 활성화 상태를 확인할 수 있다.

ssh -l = telnet -l : 원격 시스템에 사용될 로그인 이름을 설정

NFS : 리눅스-리눅스, 네트워크 기반에 다른 시스템과 파일 시스템을 공유
다른 컴퓨터의 시스템을 마운트하고 공유하여 자신의 디렉터리인 것처럼 사용할 수 있다. RPC 연결에 관여하는 데몬이다.

RPC : 동적으로 서비스와 포트를 연결할 때 사용하는 프로토콜
동적으로 포트를 할당받기 위해 원격 서비스 rpcbind를 접속한다 .port 111
```
## 24.05.18 인터넷 서비스의 설정
```
리눅스가 지원하는 네트워크 인터페이스 종류
lo :루프백 인터페이스
dl : D-Link-DE-600 포켓 어댑터 시리즈의 인터페이스
plip : 병렬 라인 인터페이스
sl : SLIP 인터페이스

모듈 적재 수동 방법
/sbin/lsmod :현재 적재되어 있는 모듈들의 정보 확인
/sbin/insmod : 적재하고자 하는 모듈을 삽입 insert
/sbin/rmmod : 현재 적재되어 있는 모든 모듈을 제거 remove
/sbin/modprobe : 모듈의 적재 및 제거

/etc/config/network : 네트워크 설정 파일: 네트워크 허용 여부 설정
/etc/config/network-scripts : 네트워크 인터페이스의 네트워크 환경 설정 정보

/etc/resolve.conf : 도메인명과 네임서버를 지정
/etc/hosts : 도메인주소와 ip주소를 1:1로 매핑

/etc/host.conf : dns 서비스를 제공할 때 먼저 이 파일을 검사하여 파일의 설정에 따라 서비스

ip 주소 설정 방버 2가지
네트워크 설정 파일 : /etc/sysconfig/network, /etc/sysconfig/network-scripts
명령어 설정 파일 : ifconfig를 이용하여 ip주소를 할당
유틸리티를 이용한 주소 설정, gnome-control-center, nm-connection-editor
x윈도 그래픽 모드에서는 상위 2개를 이용해 설정

라우팅:송신 패킷이 목적지까지 전송할 수 있도록 경로를 설정하는 작업
명령어 route는 라우팅 테이블을 설정하거나 확인
목적지 경로가 라우팅 테이블에 없다면 : default 게이트웨이로 트래픽을 전송할 수 있게 설정할 수 있다.

네트워크 경로 상태 확인 : traceroute
네트워크 연결 상태 확인 : ss, netstat
라우팅 테이블 확인 : route
nic 상태 확인 : ethtool , mii-tool, arp

mii-tool : 네트워크 인터페이스의 속도와 전송모드 등을 확인 nic
ethtool : 네트워크 인터페이스의 물리적 연결 여부를 확인할 수 있는 명령어
```
## 24.05.19 응용 분야 - 기술 동향
```
리눅스 관련 시스템 종류

고계산용 클러스터 (hpc cluster)
high performance computing 클러스터 = 베어울프(beowulf) 클러스터
고성능의 계산능력을 제공하기 위한 목적으로 제공, 과학계산용으로 활용가치가 높다.

부하 분산 클러스터 (LVS(Linux Vitual Server))
다수 개의 서버가 로드밸런서에 연결되어 서비스를 제공한다.

고가용성 클러스터 (HA(High Availability))
로드밸런서와 백업 서버 사이에서 주기적으로 통신을 하며 이상 유무를 점검한다.

임베디드 시스템
컴퓨터의 하드웨어 제어인 프로세스, 메모리 입출력장치와 하드웨어를 제어하는 소프트웨어가 조합되어 특정한 목적을 수행하는 시스템

임베디드 시스템의 장점
기능성과 학장성이 우수하다. 공개되어 있음
로열티가 없으므로 가격 경쟁력이 우수하다. 안정성이 우수하다.

임베디드 리눅스 단점
RTOS 보다 많은 메모리를 요구한다.
사용자 모드와 커널 모드 메모리 접근이 복잡하여 제품화하기 위한 솔루션 구성이 어렵다.
```
## 24.05.20 응용 분야 - 활용 기술
```
Xen : 케임브리지 대학교에서 개발이 시작
반가상화, 전가상화 모두 가능

KVM : Qumaranent에서 개발한 하이퍼바이저
x86 시스템 기반으로 cpu 전가상화 방식
인텔 vt amd-v 기반으로 동작하는 공개형 기술

virtual box : 이노테크가 개발, 현재는 오라클 개발 중인 상용, 사유 소프트웨어
전가상화만 지원

IaaS : 서버나 스토리지 같은 하드웨어 자원만을 임대해 주는 클라우드 서비스
PaaS : 소프트웨어 서비스를 개발하기 위한 플랫폼을 제공하는 서비스
SaaS : 클라우드 환경에 동작하는 응용 프로그램을 서비스 형태로 제공

빅데이터 : 기존 데이터베이스 관리 도구의 데이터 수집, 저장, 관리, 분석 역량을
넘어서는 데이터, 정형, 반정형, 비정형으로 구분

하둡 : 대용량 데이터를 분산 처리할 수 있는 자바 기반의 오픈 소스 프레임워크이다.

리눅스 기반의 공개형 운영체제
마에모 : 노키아가 스마트폰 및 태블릿 용으로 만든 소프트웨어 플랫폼
모블린 : 인텔과 리눅스 재단이 개발한 오픈 소스 운영체제
타이젠 : 인텔과 삼성을 구축으로 한 리눅스 재단
ios : 애플 사에서 개발
안드로이드 : 구글에서 만든 스마트폰용 운영체제
Bada OS

타이젠 : 리눅스 커널을 기반, 오픈 소스 모바일 운영체제
웹 OS : 리눅스 커러 되는 모바일 운영체제

GENIVI : 오픈 소스 기반의 차량 멀티미디어 플랫폼 표준화 활동
BMW 등 유럽, 북미 자동차 OEM과 자동차 부품업체들을 중심으로 결성됨
```
개념 끝 기출 10개 18일 반복

## 기출 1회 38/24
```
삼바로 공유된 디렉터리를 공유하는 과정
삼바 서버를 통해 인도우 공유 폴더를 마운트하여 리눅스 디렉터리처럼 사용
smbfs

chsh : 로그인 shell 을 변경 스크립트에 New shell 이 있다.

$ cd /disk1 ; tar cvf -, | (cd /disk2; tar xvf -)
disk1 내용을 압축한 후 disk2로 옮긴 후 압축을 해제한다.

사용자의 로그인 셸을 확인하는 명령어
SHELL 변수의 내용을 확인, /etc/passwd 파일의 내용을 확인, finger 명령의 -l 옵션을 사용

vi -r : 손상된 파일의 내용을 불러오고 복구하고 편집한다.

emacs 단축키 : ctrl + X 종료
ctrl + K  줄 삭제, ctrl + D 위치한 글자삭제 , alt + d 위치한 부분부터 단어 삭제

lspci : 시스템에 설치된 장치 목록을 출력해 주는 명령

ALSA에 관한 내용으로 틀린 것 : 표준 유닉스 장치 시스템 콜 -> OSS

x서버에서 보내온 키 값을 설치하는 명령 : xauth add $DISPLAY .키값

RFC : 인터넷에서 기술을 구현하는 데 필요한 절차 등을 제공하는 공문서 간행물

ICANN : IP주소, 프로토콜 범주와 포트 번호 할당, 중재

/etc/sysconfig/network : 리눅스 처음 설치 시에 호스트 명을 설정하였는데 www로 변경하고 부팅 시에도 계속적으로 적용되도록 -> 네트워크 연결 설정

Xen 서버 가상화를 사용할 때 설치되는 네트워크 장치명 : xenbr0

LAN 및 MAN 관련 표준을 제정한 기관 : IEEE

웹키트 레이아웃 엔진 : 크롬
```
## 기출 2회 32/24
```
스티키 비트 설정 방법 : chmod o+t data/ 8진수 1XXX 나 기호 o+t로 설정 가능
fdisk 명령을 실행하면 파티션의 속성id를 확인할 수 있다.
swap : 82, Linux 83, Linux LVM : 8e, fd: Linux RAID

/etc/fstab의 첫 번째 필드 형식에 올 수 있는 것
파일 시스템 장치명 /dev/sdb1, 볼륨 라벨 LABEL=/home, UUID

repquota /home : /home 영역에 설정된 사용자 쿼터 정보를 출력

셸 환경 변수를 설정하는 방법으로 틀린 것 : TMOUT=/bin/logout
일정시간 이후 로그아웃시키도록 설정할 수 있는 명령어이다.

배쉬쉘 명령행 편집 기능 : Ctrl + E : 맨 왼쪽으로 이동

본 셸 특징 : 조건 구문, 반복구문이 존재, alias 미 존재

프로세스 우선 순위 : NI 참고 우선순위 범위는 -20 ~ 19 이다.

SIGKILL : 키보드 입력이 없음
SIGINT : Ctrl + C
SIGQUIT : Ctrl + \

inetd : 프로세스가 메모리에 항상 상주하지 않고 서비스 요청이 들어왔을 때 관련 프로세스를 실행

killall -9 1234 : PID가 1234인 프로세스를 강제로 종료

Kill 1234 -> default 아무것도 없을 때는 15번 -> 강제종료

vi 편집기에서 커서를 왼쪽으로 이동 hjkl 왼쪽 아래 위 오른쪽
왼쪽이면 h

zypper : 수세 리눅스 저장소 기반의 패키지 관리 프로그램
YaST : 오픈 수세 기능

rpm -q : 검색하고자 하는 패키지의 이름과 버전을 표시

tar 파일에 추가로 묶는 과정
tar -r

dpkg -L : 패키지가 설치한 파일 목록 확인

wayland : 기존의 X를 대체할 목적으로 등장한 프로젝트로 클라이언트와 대화할 수 있는 compositer를 위한 프로토콜

X 윈도 실행 시에 생성되는 관련 키 값의 저장 경로 : $HOME/.Xauthority

로컬시스템에서 사용 중인 네트워크 카드의 맥주소를 확인하는 명령어 : ip, ifconfig

텔넷 명령을 이용해서 로컬 시스템의 웹 서버 동작을 확인 : telnet localhost 80

루프백 네트워크가 속해있는 IPv4의 클래스 : A클래스 127.0.0.1에서 127은 첫 번째 옥텟이 0100 0000 0으로 시작 A클래스

리눅스와 리눅스 시스템 간의 디렉터리 공유 : NFS

/etc/hosts : ip주소와 호스트이름을 매핑
```
## 기출 3회 30/24
```
mke2fs -j -T largefile /dev/hdb1 : /dev/hdb1 을 저널링 파일 시스템으로 만들고, i-node의 크기를 1MB로 지정한다.

리눅스 파일 시스템 설명 : sysfs 는 리눅스에서 사용하는 가상 파일 시스템이다.

그룹명 변경 : chown :kait lin.txt , chgrp kait lin.txt

edquota : 사용자나 그룹에 쿼터를 설정할 때 사용하는 명령어

bash : 브라이언 폭스가 gnu프로젝트를 위해 개발, 명령 히스토리,명령어 완성 기능, 히스토리 치환, 명령행 편집 등을 지원

히스토리 목록 중에서 5번째에 사용한 명령을 실행하는 것 : !5

프로세스 우선순위 변경 명령어 : nice, renice, top -r

ps aux 명령으로 출력되는 항목 : USER, RSS 실제 메모리 용량, TTY, PID

nohup 명령어 설명 : 실행한 명령을 자동으로 백그라운드로 보내지 않고 & 를 사용해야 한다.

vi 편집 사용 시 생성된 .exrc 파일 안에 행 번호 설정 set nu를 한다. 안에서 설정은 콜론안씀

vi 편집기에서 바로 직전에 실행한 줄 삭제 명령을 취소하여 복원 -> u

원격지 서버에 접속하여 사용하던 중 네트워크가 차단되면서 비정상적으로 종료되었을 때 생성되는 파일
-> .~.swp 스왑 파일이 복구 모드로 열리게 된다.
.lin.txt.swp

rpm : 소스 프로그램을 설치하기 위한 도구로 아닌 것 -> 패키지 관리 도구

tar jxvf : j -> bz2파일에 사용한다.

의존성이 있는 패키지가 존재할 경우에도 삭제하는 옵션 --nodeps

dpkg 명령어를 이용해 환경 설정 파일은 남기고 패키지를 삭제 -> -r
모두 삭제 -R

lprm : 프린터 큐에 대기 중인 작업을 삭제하는 명령어
cancel : 프린터 작업 취소

ip주소 기반으로 접근을 허가 : xhost
x 클라이언트에서 원격지의 x서버에 프로그램이 전달되기 위해서 실행되는 터미널이 정의되어 있는 환경 변수인
display를 설정해야 한다.

startx -- -depth 8 : 256 color 모드로 x 윈도를 실행하는 명령어

Window Manager : 직접 비디오 카드,마우스,키보드 등에 접근하지 않고 디스플레이 서버를 통해 접근
데스크톱 환경 구성에 도움을 주기 위해 설계 도크, 태스크바 등 다양한 유틸리티 제공

telnet 192.168.0.3(ip주소) 포트
포트는 생략가능 telnet ip주소 포트 3가지

FTP : TCP 프로토콜 기반으로 많이 사용되고 있다.

최상위 도메인 : kr, com, edu

ssh : 문제 안에 key가 있음

0 ~ 1023번 : 잘 알려진 포트로 사용되는 포트 범위
```
## 기출 4회 34/19
```
vfat : FAT-32 파일을 마운트 할 때 지정하는 유형 값
df : 파티션 별로 사용량을 확인
du : 디렉터리 별로 사용량을 황긴
fdisk : 파티션 분할 명령어

loop : .iso 마운트 시 사용

chmod 3770 /project -> SET-GID가 설정된다.

blkid : 디스크 파티션에 부여된 UUID의 값을 확인할 때 사용하는 명령어

PS : 사용자가 로그인 하여 현재 이용 중인 셸을 확인할 수 있는 명령어

tcsh : 켄 그리어가 테넥스 운영체제에 명령행 완성 기능을 반영하면서 시작, 편집 기능도 추가로 지원

top : 동작 중인 프로세스를 종료할 수 있음 -k pid
-> 동작 중인 프로세스의 디스크 사용률을 사용할 수는 없음

vi 모드 중 ex 명령 모드 : 치환, 저장, 종료의 역할이 수행

vi -r /etc/hosts -> 수정 중이던 파일로 복구할 수 있는 명령어

tar -j , -J
j -> bz2파일에 적용
J -> xz 파일에 적용
C -> 대상 (특정) 디렉터리에 푼다. 경로 설정

yum delete totem : yum 기반으로 totem 패키지 삭제하는 명령어가 아님
remove, erase

synaptic : APT 패키지 관리 시스템으로 GTK+ 기반의 GUI 도구

rpm -F : 이전이 있는 경우만 설치, 패키지 업그레이드 시 사용
현재 시스템에 설치된 패키지만 찾아서 업데이트한다.

lpr -# 인쇄매수 lp -n 인쇄매수

SOAP 프로토콜 기반의 네트워크 프린터 설정 -> 네트워크 프린터를 설정할 수 없는 환경

x 윈도에 적용되는 라이선스 : MIT 라이선스

konqueror : KDE 기반의 파일 뷰어

gnome 초기 파일 관리자 : nautlus
gnome2 : metacity
gnome3 : mutter

nautlus -> metacity -> mutter

KDE와 관련있는 라이브러리 QT
GNOME과 관련 -> GTK+

B클래스 대역에 할당된 사설IP주소의 호스트 개수 65534 2의 16승 -2

세션 계층 : 데이터의 전송 순서 및 동기점 위치를 제공

Cat 5e : 기본적으로 100HZ의 대역폭, 기가비트 이더넷인 1000BASE-T에도 적합

메일을 전송 -> mail -s "메일제목" 수신메일주소 < 전송파일명

네트워크 사용 유무지정, 호스트명 설정, 게이트웨이 주소 설정 : /etc/config/network

dhcp 서버 : 회사 내에서 인터넷에 접속할 때마다 ip추옫ㄹ이 수시로 발생하고 있다.

채널 본딩 : 호스트 컴퓨터에 두 개 이상의 네트워크 인터페이스를 장착한 후에 안정성이나 속도를 높이기 위해 구성하는 기술

레드햇은 KVM 기반의 상용화 제품으로 RHEV를 시판하고 있다.
레드햇, KVM, RHEV
```
## 기출 5회 33/25
```
umask의 값이 0022일 때 생성되는 파일의 허가권은?
0666 - 0022 = 0644 rw-r--r--

mke2fs -j ext4 /dev/sdb1 <- -j는 ext3을 만드므로 틀린 명령어

--T : Sticky 비트

최근에 실행한 명령어 10개를 호가인하는 명령어 -> history 10

chsh -l : 사용가능한 셸의 종류를 출력

/var/spool/cron : 일반 사용자가 등록한 cron 작업 관련 파일이 저장되는 디렉터리 경로

ps -x : ps 명령으로 동작 중인 데몬을 확인할 때 사용하는 옵션

kill 15 : kill 명령 시 기본적으로 전송되는 시그널 번호

자동 들여쓰기 기능 : vi, nano

:ab 자주 입력되는 단어를 약어로 설정
:set 환경변수 표시
:map : 특정 키에 특정 기능을 하도록 설정
:set all : 설정되어 있는 모든 환경변수와 값을 표시

저장소 기반 패키지 관리 기법이 아닌 것 : yaST

zcat : gzip으로 압축된 파일의 내용을 확인하는 명령

pnm : scanimage 명령어를 사용하여 이미지 스캔할 때 기본적으로 적용되는 이미지 형식

OSS : BSD라이선스 기반으로 소스를 추가로 공개, GPL 기반, Hannu Savolainen에 의해 개발

GTK+ : XSANE 스캐너 프로그램 개발 시 기반이 된 라이브러리

x WINDOWS 시스템 초기 부터 최근 순 나열 -> XFree86 -> X.org -> Wayland

X 윈도 관련 프로그램의 종류 : xfce 윈도우 환경

이동통신 분야의 5G 제정과 관련된 국제 기구 : ITU 국제 전기통신 연합

Samba 서비스 구성 : smb, cifs, netbios

시스템 간 파일을 주고 받는 서비스 : ssh, ftp, nfs
원격 전송 -> telnet

리눅스 커널 기반의 운영체제 -> webOS
QNX : 유닉스 커널 운영체제
iOS : 애플 운영체제 
BlackBerry OS : 안드로이드 운영체제
```
## 기출 6회 28/19
```
usrquota : 사용자 쿼터를 설정하기 위해 /etc/fstab에 설정하는 항목 값

특정 파이션의 속성을 Raid로 변경하기 위해서는 t 명령을 누른 후에 fd 키를 눌러서 설정한다.

파일의 허가권을 알지 못하는 상태에서 chmod 755 lin.txt 명령과 동일한 명령
-> chmod u=rwx, go=rw lin.txt

특수 권한인 Set-Bit를 활용한 사례로 가장 거리가 먼 것
실행 파일에 Sticky Bit를 설정 -> 실행파일보다 파일 공유에 활용

특수 권한인 Set-Bit가 설정된 파일로 알맞는 것
/usr/bin/passwd

설정된 umask의 값을 확인할 때 사용하는 명령
umask -S

관리자 계정으로 ihduser의 로그인 셸을 변경하고자 할 때 수정하는 파일
-> etc/passwd

alias 목록 표시 명령어 -> alias

시그널 이름과 번호를 확인 -> kill -l

daemon : 주기적이고 지속적인 서비스 요청을 처리하기 위해 계속 실행되는 프로세스 통칭 용어

emacs는 강력한 질의 및 치환을 가지고 있다. esc 키 입력 후에 % 키를 누르면 화면 하단에 query replace: 프롬프트가
나오면서 질의를 통한 치환을 진행할 수 있다.

pico 에디터 : 구문강조 x

질의를 통한 치환 기능 -> emacs

.exrc : vi 에디터 실행시 지속적으로 지정한 설정을 이용

yum 명령의 저장소 관련 파일들이 위치하는 디렉터리 : /etc/yum.repos.d

기존에 생성된 ihd.tar파일에 lin.txt 파일을 추가한다.

tar rvf -r : 추가

totem 패키지를 설치하는 과정에서 질의 시 무조건 승낙하는 명령어
yum install -y totem

rpm 설치 관련 옵션으로 틀린 것
-f 질의 관련

kait.txt 파일 내용을 인쇄하기 위한 명령으로 갖아 거리가 먼 것
cat kait.txt < /dev/lp0

인쇄 하려면 >

usb로 연결된 스캐너 검색 : sane-find-scanner -v
직렬스캐너 검색 : sane-find-scanner-p

xcam : GUI 기반 이미지 스캔, 뷰어

Okular : 문서뷰어

xauth list $DISPLAY : 지정된 표시장치의 쿠키 값 확인

xhost : 접근할 수 있는 호스트 지정 및 해제

NetBIOS : 세션층에서 TCP/IP 등을 연결하는 프로그램

CIFS : 인터넷을 통해 원격지 컴퓨터상으로 서비스요청

ssh -p : 포트 22가 아닌 다른 포트로 접속할 수 있게 함

ssh 인증 파일의 경로 : ~.ssh/authorized_keys

ss : 서버에 접속한 클라이언트의 ip주소 및 포트 번호 확인

시스템에 설정된 ip주소를 확인하는 명령 : ip addr show

etc/servies : 포트번호 관리

임베디드 리눅스 : 커널과 루트 파일시스템 등 상대적으로 많은 메모리를 차이

햐나의 작업을 여러 개로 구성된 노드을 이용해서 처리 -> 고성능 클러스터
여러 대의 서버에 부하를 분산 -> 부하분산 클러스터
```
## 기출 7회 34/26
```
edquota posein 활성화 : 쿼터 설정화면

fdsik : 모든 디스크의 파티션 설정 상황

umount : 마운트 해제

ls 파일이나 디렉터리의 소유권을 확인

사용자가 로그인 직후에 부여된 셸 확인 명령이 아닌 것 : chsh -l : 설정가능한 셸확인

사용 가능한 셸의 목록 : cat /etc/shells

ps aux : 실제 실행 우선순위는 알 수 없다.

top -t : cpu on/off
top -m : 메모리 on/off

jobs 명령 시 - 기호 붙은 것 : 앞으로 실행될것, + 실행중인것
+가 우선순위가 더높다.

저장된 crontab 설정 파일을 삭제하기 전에 사용자에게 확인 : crontab -ir 사용자 확인 info

top 명령 맨뒤 8080은 포트번호가 아니라 pid임

./configure --prefix : 지정된 디렉터리에 소스 설치

tar -J : xz 파일에 활용
tar -j : bz2 파일에 활용

NDMP : 백업과 복구 표준화 프로토콜

cdparanoia : 음악 추출

고수준의 라이브러리 : QT, GTK+, XT, Xaw, FLTK, TK

X Protocol tcp포트 6000번

ip 주소를 확인하는 명령어의 조합 : ip, ifconfig

DQDB 프로토콜 제정 -> IEEE, IEEE802.6

TCP/IP : 미국방성 연구, 컴퓨터 기종에 상관없이 정보 교환이 가능하게 해주는 통신 프로토콜

직접 개발한 모바일 게임 앱을 사용자들에게 제공 : 아마존의 AWS

로드밸런서 : 부하분산 클러스터
```
## 기출 8회 36/24
```
디렉터리에 부여되는 W권한 : 파일의 생성, 삭제 권한

시스템 계정에 설정되는 셸 : /sbin/nologin

cron에 관한 설명 : 주기적으로 실행되는 작업만 등록하여 사용할 수 있다.
운영에 필요한 작업은 /etc/crontab에 저장

시그널 : 시그널은 프로세스 간 메시지를 보내는 통신을 할 때 사용한다.

vi +/ihd/etc/hosts : /etc/hosts 파일을 열면서 ihd라는 문자열이 있는 곳에 커서를 둔다.

vi 편집기 $: 줄의 끝을 의미, ^ 줄의 시작, < 단어의 시작, > 단어의 끝

환경설정과 관련된 옵션 정보 확인 : --help

tar -r 추가, tar -t 파일 안의 내용 출력

rpm -e --nodeps : 패키지 의존성을 무시하고 제거

데비안 파일 형식 : deb

cups가 제공하는 장치 드라이버는 어도비의 ppd형식의 텍스트 파일을 이용하여 설정

리눅스를 시작할 때 x윈도가 실행되도록 관련 설정 파일 : id:5:initdefault

리눅스 부팅 시 x 윈도를 실행하기 위해 부팅 모드를 설정할 수 있는 파일 : /etc/inittab

ipv4 a 클래스 대역에 할당된 사설 네트워크 대역의 개수 : 10.0.0.0 ~ 10.255.255.255로 하나의 대역

네트워크 인터페이스 관련 파일 : /etc/sysconfig/network-scripts

이더넷 케이블의 배열 순서인 T568B를 표준화한 기구 : EIA

웹 서비스에 사용되는 포트 번호 : 80

오페라 : 윈도우, macOS, 노르웨이에서 개발

/etc/resolv.conf : 네임서버 dns 서버 지정

xen : cpu의 반가상화 KVM : CPU의 전가상화, Virtual Box : 전가상화만 지원

이탈리아 : 아두이노
영국 : 라즈베리 파이
```
## 기출 9회 32/27
```
chown 명령을 사용하여 소유권 변경 시 참조하는 파일 : /etc/passwd

특수 권한이 설정되어 있는 파일로 틀린 것 ; /dev/null

소유 그룹 변경 명령어인 chgrp 명령어를 이용하여 원본 파일은 그대로 둔채
심볼릭 파일의 그룹 소유권만 변경 : -h

특수 권한을 사용하면 보안이 약화될 수 도 있음 일시적으로 root 권한 얻음

Set-UID : 4 , Set-GID : 2, Sticky Bit : 1

리눅스 파일 시스템 : ext, vfat, ntfs
네트워크 기반 : smb, cifs

dash : POSIX와 호환되는 /bin/sh를 가능한 작게 구현한 셸, 빠른 작업 수행 but history X

바로 직전에 내린 명령을 실행할 때 사용하는 명령 : !!

시스템 전체에 적용되는 환경변수와 시작 관련 프로그램 설정 : /etc/profile

사용자의 프롬프트를 변경할 때 사용하는 환경 변수 : PS1

gedit : 윈도우나 리눅스 등 어느 운영체제에서든 사용 가능

vi -r 복구하면서 가져온다. // 네트워크 단절 시 사용

아파치 웹 서버 프로그램이 설치되는 디렉터리를 ./configure로 지정
-> 소스파일을 다운로드하여 디렉터리를 지정한 후에 설치한다.

압축 파일을 해제 gzip -d ihd.tar.gz

lpr -r lin.txt : lin.txt 문서 파일을 출력한 후에 삭제하는 명령

시스템 A의 DISPLAY="B주소"로 변경

이더넷 카드에 연결된 케이블의 상태 : mii-tool

ssh 와 관련없는 명령 : scl

ssh - scp파일복사, sftp 파일전송, slogin alias지정

48bit 길이의 고유한 mac주소를 기반으로 상호 간 데이터 주고받음

24bit 제조사 번호, 24bit 일련번호로 이루어짐 mac 주소 -> 48bit

/etc/services : 포트번호확인
```
## 기출 10회 37/27
```







```

