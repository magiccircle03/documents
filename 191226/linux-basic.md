# 리눅스 기본 명령어 정리

## mkdir

폴더를 생성한다. (make directory)

```bash
mkdir myfolder
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

## 메모리 확인

## 하드 용량 확인

## ip 확인

```
ip addr show
```

맥에선

```
ifconfig
```

## 방화멱 여닫기

## bashrc
