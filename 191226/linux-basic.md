# 리눅스 기본 명령어 정리

## mkdir

폴더를 생성한다. (make directory)

```bash
$ mkdir myfolder
```

## ls

디렉토리 목록 보기

- 옵션  
  -l : 자세히 출력  
  -a : 숨김파일, 숨김 디렉토리 출력  
  -t : 파일을 시간순으로 출력하여 최근 파일이 먼저 출력  
  -r : 정렬순서를 내림차순으로 출력

```bash
$ ls -al
total 176
drwxr-xr-x+  34 daae  staff   1088 12 26 12:03 .
drwxr-xr-x    5 root  admin    160 12  5 17:21 ..
-r--------    1 daae  staff      8 12 10 16:52 .CFUserTextEncoding
-rw-r--r--@   1 daae  staff  10244 12 26 17:32 .DS_Store
drwx------    8 daae  staff    256 12 26 17:32 .Trash
-rw-------    1 daae  staff   9855 12 25 22:22 .bash_history
drwx------  150 daae  staff   4800 12 26 12:01 .bash_sessions
drwx------    4 daae  staff    128 12 16 09:59 .config
-rw-------    1 daae  staff      0 12 13 13:03 .dbshell
drwx------    3 daae  staff     96 12 16 09:59 .local
-rw-------    1 daae  staff      0 12 12 09:09 .mongorc.js
-rw-------    1 daae  staff     21 12 11 23:05 .node_repl_history
drwxr-xr-x    7 daae  staff    224 12 25 19:37 .npm
drwxr-xr-x   27 daae  staff    864 12 11 10:36 .nvm
-rw-------    1 daae  staff      0 12 16 09:38 .python_history
drwx------    3 daae  staff     96 12 13 10:14 .ssh
-rw-------    1 daae  staff  16916 12 20 15:16 .viminfo
drwxr-xr-x    4 daae  staff    128 12 10 17:30 .vscode
-rw-r--r--    1 daae  staff    116 12 21 14:37 .yarnrc
drwx------@   3 daae  staff     96 12 10 17:06 Applications
drwx------@  27 daae  staff    864 12 26 18:44 Desktop
drwx------@   3 daae  staff     96 12 10 16:56 Documents
drwx------+  17 daae  staff    544 12 26 18:39 Downloads
drwx------@  67 daae  staff   2144 12 18 16:00 Library
drwx------+   4 daae  staff    128 12 18 16:02 Movies
drwx------+   5 daae  staff    160 12 18 16:02 Music
drwx------+   8 daae  staff    256 12 26 16:51 Pictures
drwxr-xr-x    3 daae  staff     96 12 11 09:41 Postman
drwxr-xr-x+   4 daae  staff    128 12 10 16:52 Public
drwxr-xr-x   96 daae  staff   3072 12 21 16:09 node_modules
-rw-r--r--    1 daae  staff  27694 12 21 16:09 package-lock.json
drwxr-xr-x    4 daae  staff    128 12 20 10:53 study
drwxr-xr-x    5 daae  staff    160 12 20 11:05 work
-rw-r--r--    1 daae  staff     86 12 11 11:02 yarn.lock
```

## pwd

현재 작업중인 디렉토리 출력

```bash
$ pwd
/Users/daae
```

## cd

change directory. 경로 이동

```bash
$ cd ~/work
$ pwd
/Users/daae/work
```

## cat

파일의 내용을 출력한다.(파일 여러 개를 합쳐 하나로 만들거나, 새로운 파일을 만들 때도 사용한다.)

```bash
$ cat > file1
file1
$ cat file1
file1
```

## echo

문자열 출력. 환경변수 읽을 때 유용하게 이용할 수 있다

```
$ echo $HOME
/home/centos
```

## vi

vi 편집기: 텍스트 문서를 편집할 수 있는 에디터

```bash
vi file1
```

1. 편집기에 들어왔을 때 입력모드로 전환하려면 i를 누른다.
2. 입력 후 esc를 누르면 명령모드로 들어온다.
3. :wq로 저장 후 나갈 수 있다.

## mv

move. 파일 이동.  
 `mv [이동을 원하는 파일] [이동을 원하는 위치,이름]`

```bash
$ mv file1 ~/work/file1
$ cd ~/work
$ ls
awskey	file1	repo
```

## cp

copy. 파일 복사.  
`mv [복사를 원하는 파일] [복사를 원하는 위치,이름]`

```bash
$ cp file1 file2
$ ls
awskey	file1	file2	repo
```

## rm

remove. 파일 삭제.

```bash
$ rm file2
$ ls
awskey	file1	repo
```

## top

프로세스 당 메모리와 CPU 사용량 등 시스템 전체 상태를 실시간으로 확인, 프로세스를 관리할 수 있다.

|                                          centOS에서 top 명령어 사용                                           |                                      mac에서도 top 명령어를 사용해봤다                                       |
| :-----------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------: |
| ![cent](https://user-images.githubusercontent.com/51072198/71494709-7fa0d280-288c-11ea-8b0e-8f32d61eebc6.png) | ![mac](https://user-images.githubusercontent.com/51072198/71494723-9d6e3780-288c-11ea-809b-258393c3dcdc.png) |

- 옵션 키

| 키        | 설명                                      |
| --------- | ----------------------------------------- |
| shift + m | 메모리 사용량 우선순위 정렬               |
| shift + p | CPU 사용량 우선순위 정렬                  |
| shift + t | 실행 시간 우선순위 정렬                   |
| shift + b | 상단 정보를 블럭 형태로 표시(htop과 유사) |
| space bar | Refresh                                   |
| u         | 해당 유저의 프로스세만 표시               |
| k         | 해당 프로세스 kill                        |
| q         | top에서 빠져나옴                          |

## ip 확인

- 내부 아이피

```
ip addr show
```

```
ifconfig
```

- 외부 아이피

```
curl ipecho.net/plain; echo
```

## netstat

리눅스 네트워크 상태를 종합적으로 보여주는 명령. 포트를 확인할 수 있다.

- 옵션 없이 사용 : 현재 리눅스 서버의 열려 있는 모든 소켓에 대한 정보를 확인

```
$ netstat
```

- -i : 네트워크 인터페이스를 통해 주고 받은 패킷에 대한 정보를 확인

```bash
$ netstat -i
Kernel Interface table
Iface             MTU    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0             9001   615497      0      0 0        319251      0      0      0 BMRU
lo              65536     1954      0      0 0          1954      0      0      0 LRU
```

- -rn : 라우팅 테이블 정보를 확인

```
$ netstat -rn
Kernel IP routing table
Destination     Gateway         Genmask         Flags   MSS Window  irtt Iface
0.0.0.0         172.31.32.1     0.0.0.0         UG        0 0          0 eth0
169.254.0.0     0.0.0.0         255.255.0.0     U         0 0          0 eth0
172.31.32.0     0.0.0.0         255.255.240.0   U         0 0          0 eth0
```

- -nap

| 명령                            | 설명                         |
| ------------------------------- | ---------------------------- |
| netstat -nap                    | 열려있는 모든 포트 확인      |
| netstat -nap \| grep '포트번호' | 확인하려는 포트번호 상태확인 |
| netstat -nap \| grep LISTEN     | 현재 LISTEN중인 포트 확인    |

-n: host명으로 표시 안함  
-a: 모든소켓 표시  
-p: 프로세스ID와 프로그램명 표시

## 포트 여닫기

> - 7.0 이전 : iptables 이용
> - 7.0 이후 : Firewall Daemon(iptables 기반) 이용 권장

### iptables 이용하여 포트 추가

```
iptables -I INPUT 1 -p tcp --dport 12345 -j ACCEPT
```

- I : 새로운 규칙을 추가한다.
- p : 패킷의 프로토콜을 명시한다.
- j : 규칙에 해당되는 패킷을 처리하는 방법을 정한다.

-> 외부에서 들어오는 TCP포트 12345의 연결을 허용하는 규칙을 방화벽 1번규칙으로 추가한다.

### 추가한 설정 조회

```
iptables -L -v
```

-L: 규칙을 출력
-v: 자세히

### iptables 이용하여 포트 삭제

```
iptables -D INPUT 1
iptables -D INPUT -p tcp --dport 12345 -j ACCEPT
```

- D: 규칙 삭제

### 변경사항 저장

```
service iptables save
```

```
/etc/init.d/iptables restart
```

- 방화벽 열고 닫기

```
/etc/init.d/iptables start
/etc/init.d/iptables stop
```

### Firewall Daemon

#### 0. 설치 / 시작

```
yum install firewalld
```

```
systemctl start firewalld
systemctl enable firewalld
```

#### 1. 방화벽 살펴보기

- 방화벽에는 zone(영역)이라는 것이 존재
- 개방된 네트워크와 연결되어있다면 public zone(공개영역)에 있는 룰이 적용되고, 개인 네트워크에 있다면 다른 zone의 룰을 적용할 수 있음.
- 서버 용도로 사용 시 개방된 네트워크 public zone만 필요함, 기본 zone 역시 public zone인데 방화벽 설정파일에서 변겅 가능

  - public zone의 설정파일  
     `/etc/firewalld/zones/public.xml`

  - 방화벽 리로드  
     `firewall-cmd --reload`

- 설정파일은 xml 형식으로 되어있으며, `firewall-cmd --permanent --zone=public` 명령으로 추가했던 룰들이 저장되어있음
- 설정 변경 후 리로드 해야 적용됨

#### 2. 포트

포트를 방화벽에 추가하면 해당 포트는 허용됨

- 포트추가

예를들어 80번 포트면

```
firewall-cmd --permanent --zone=public --add-port=80/tcp
```

```
firewall-cmd --reload
```

- 포트 제거

```
firewall-cmd --permanent --zone=public --remove-port=80/tcp
```

```
firewall-cmd --reload
```

#### 3. 서비스

서비스에서 사용하는 룰을 적용하려면 아래와 같이 서비스를 추가  
단, 해당 서비스 xml 룰 파일이 /usr/lib/firewalld/services 에 있어야 사용할 수 있음

- 서비스 추가

```
firewall-cmd --permanent --zone=public --add-service=서비스
```

예) firewall-cmd --permanent --zone=public --add-service=http

```
firewall-cmd --reload
```

- 서비스 제거

```
firewall-cmd --permanent --zone=public --remove-service=서비스
```

예) firewall-cmd --permanent --zone=public --remove-service=http

```
firewall-cmd --reload
```

#### 방화벽 기타 명령어

- 사용 가능한 서비스/포트 출력

```
firewall-cmd --list-all
```

- 허용한 포트 목록

```
firewall-cmd --list-ports
```

- 방화벽 상태 확인

```
firewall-cmd --state
```

- 활성화된 zone 목록

```
firewall-cmd --get-active-zones
```

- 현재 존재하는 서비스 목록

```
firewall-cmd --get-service
```

- public zone에 있는 서비스 목록

```
firewall-cmd --zone=public --list-services
```

#### 참고

[링크](https://conory.com/blog/42477)

## bashrc

### bash?

Bash는 Bourne Again Shell의 축약어로 리눅스에서 가장 널리 사용되는 쉘.  
bash는 다섯 개의 공통된 설정 파일들을 가지고 있다.

- /etc/profile
- /etc/bashrc
- ~/.bash_profile
- ~/.bashrc
- ~/.bash_logout

일반적으로 전역 파일들은 /etc에 위치함. /etc/profile과 /etc/bashrc는 전역설정

### bashrc

bashrc는 bash에서 작업할 때마다 수행되는 파일, 환경변수 개념.  
python이라고 입력만 해도 python3.x버전으로 연결되도록 설정할 수 있다.

- .bash_profile은 로그인 할 때
- .bashrc는 이미 로그인 한 상태에서 새 터미널 창을 열 때마다 로드됨
