# Git 기본



## Git 초기화

```
$ git init
```

- 처음 한번만 실행
- 절대 홈 디렉토리에서 `init`을 실행하지 않는다.
  - 터미널에서 현재 위치가 `~`인지 아닌지 확인한다.
- 이미 Git이 생성된 폴더 내에서 다시 `init`을 하지 않는다.



## Git 기초

```$ git <명령어> <인자> <옵션>```



### 사용자 정보 설정

```$ git config --global user.name "<사용자이름>"```

```$ git config --global user.email "<이메일주소>"```

- -/.gitconfig 파일에 저장됩니다.
- .gitconfig의 내용을 출력

```$ git config --global --list ```



## 로컬 저장소

- 작업공간(working directory / working tree) : 사용자가 일반적인 작업을 하는 공간. 눈에 보이는 곳
- 스테이지(staging area) : 커밋을 할 파일/폴더를을 등록하는 공간 
- 저장소(commits) : staging area의 파일들의 변경사항들이 저장되는 곳



### Git 초기화

```$ git init```

- 현재 디렉토리를 Git으로 관리하겠다는 명령어
- `.git`이라는 중간 폴더가 생성된다.
- 터미널에 `(master)`가 표시된다



- 주의사항
- 이미 git에 의해 관리되는 폴더 내부에서 다시 init을 실행하지 않는다.
- 홈 디렉토리(`~`)에서 실행하지 않는다.



## git status

- working directory 와 staging area에 있는 파일의 현재 상태를 알려주는 명령어
- 어떤 작업을 하기 전에 수시로 status를 확인하는 습관을 가지자.
- 파일의 상태
  - untracked : Git이 관리하지 않는 파일들(한번도 staging area에 등록되지 않은 파일들)
  - tracked : Git이 관리하는 파일



## git add

- working directory의 파일을 staging area에 등록
- 등록된 파일을 Git이 추적 관리한다.

```
$ git add a.txt
$ git add my_folder
$ git add my_forder/a.txt

# 모든 파일들을 등록
$ git add
```



## git commit

- Stanging area에 등록된 파일의 변경사항을 하나의 버전(커밋)으로 저장하는 명령어
- `커밋 메세지`를 작성해야 한다
  - 변경사항을 잘 표현할 수 있도록 의미있게 작성한다.
- 최초 커밋 시에는 (root-commit) 이 출력된다.





