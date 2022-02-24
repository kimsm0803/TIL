# Github

## [1] 원격 저장소 (Remote Repository)

###  (1) github에서 원격 저장소 생성

- 로그인 페이지 화면 오른쪽 상단 더하기(+) 버튼을 누르고 New repository를 클릭합니다.
- 화면 오른쪽 상단 더하기(+) 버튼을 누르고 New repository를 클릭합니다.



###  (2) 로컬 저장소와 원격 저장소 연결

- **저장소의 주소 복사**

- **vscode에서 로컬 저장소 만들기**

  ```bash
  kyle@KYLE MINGW64 ~/TIL
  $ git init
  Initialized empty Git repository in C:/Users/kyle/TIL/.git/
  ```

- **원격 저장소 등록**

  ```bash
  $ git remote add origin https://github.com/edukyle/TIL.git
  
  [풀이]
  git 명령어를 작성할건데, remote(원격 저장소)에 add(추가) 한다.
  origin이라는 이름으로 https://github.com/edukyle/TIL.git라는 주소의 원격 저장소를 등록한다.
  ```

- **원격 저장소 조회**

  ```bash
  $ git remote -v
  origin  https://github.com/edukyle/TIL.git (fetch)
  origin  https://github.com/edukyle/TIL.git (push)
  
  
  add를 이용해 추가했던 원격 저장소의 이름과 주소가 출력됩니다.
  ```

- **(원격 저장소 연결 삭제)**

  **로컬과 원격 저장소의 연결을 끊는 것이지, 원격 저장소 자체를 삭제하는 게 아닙니다.**

  ```bash
  $ git remote rm origin
  $ git remote remove origin
  
  
  [풀이]
  git 명령어를 작성할건데, remote(원격 저장소)와의 연결을 rm(remove, 삭제) 한다.
  그 원격 저장소의 이름은 origin이다.
  ```



### (3) 원격저장소에 업로드

```
실습 때 작성했던 TIL 파일을 Github 원격 저장소에 업로드

정확히 말하면, 파일을 업로드하는 게 아니라 커밋을 업로드 하는 것!

따라서 먼저 로컬 저장소에서 커밋을 생성해야 원격 저장소에 업로드 가능
```

#### 1. 로컬 저장소에서 커밋 생성(add, commit)

```
# 현재 상태 확인

$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        day1.md

nothing added to commit but untracked files present (use "git add" to track)
```

```
 git add day1.md
```

```
$ git commit -m "Upload TIL Day1"
[master (root-commit) f3d6d42] Upload TIL Day1
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 day1.md
```

```
# 커밋 확인

$ git log --oneline
f3d6d42 (HEAD -> master) Upload TIL Day1
```



#### 2. git push

```
로컬 저장소의 커밋을 원격 저장소에 업로드 하는 명령어

git push <저장소 이름> <브랜치 이름> 형식으로 작성합니다.

-u 옵션을 사용하면, 두 번째 커밋부터는 저장소 이름, 브랜치 이름을 생략 가능합니다.
```

```
$ git push origin master

[풀이]
git 명령어를 사용할건데, origin이라는 이름의 원격 저장소의 master 브랜치에 push 한다.

------------------------------------------------

$ git push -u origin master
이후에는 $ git push 라고만 작성해도 push가 됩니다.
```



#### 3. vscode 자격 증명

- Sign in with your browser를 클릭합니다.

- Authorize GitCredentialManager를 클릭합니다.

- 자격 증명 완료

- 이후 git push 완료

  ```
  $ git push -u origin master
  info: please complete authentication in your browser...
  Enumerating objects: 3, done.
  Counting objects: 100% (3/3), done.
  Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
  Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  To https://github.com/edukyle/TIL.git
   * [new branch]      master -> master
  Branch 'master' set up to track remote branch 'master' from 'origin'.
  ```



#### 4. 원격 저장소에서 정상 업로드 확인

>(주의) Github 원격 저장소에 절대로 파일을 드래그해서 업로드 하지 않습니다!!!! 
>
>가끔 Github를 구글 드라이브처럼 여겨서, 파일을 직접 드래그해서 올리는 경우가 있습니다. 
>
>Git 명령어를 학습했기 때문에, 반드시 git add → git commit → git push 의 단계로만 업로드 해야합니다. 
>
>그 이유는 로컬 저장소와 원격 저장소의 동기화 때문입니다. 
>
>로컬 저장소에서 변경이 먼저 일어나고, 그 변경 사항을 원격 저장소에 반영하는 형태여야 합니다. 
>
>하지만, Github에 드래그를 해서 파일을 업로드하면 원격 저장소에 변경이 먼저 일어나는 형태가 되기 때문에 이러한 행동을 지양해야 합니다.



#### 5. git push 그림으로 이해하기

![](https://hphk.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F357df618-2ddf-4f18-b96c-c1b0787a1a45%2FUntitled.png?table=block&id=53b68135-0a14-44da-af96-2cdea23226c7&spaceId=daa2d103-3ecd-4519-8c30-4f55e74c7ef4&width=2000&userId=&cache=v2)

## [2] README.md 파일 push 해보기

- `README.md`는 원격 저장소의 소개와 설명이 담겨있는 일종의 대문 역할을 함
- 반드시 파일 이름을 `README.md`로 지정해야 Github가 인식 할 수 있음

