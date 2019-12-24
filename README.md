# Git과 visualStudio code의 연동

## git을 컨트롤 하는 방법

- CLI (bash, terminal)
- GUI (source tree, git monitor)
- vs code

주로 사용되는 방법은 GUI환경, 가끔씩 부족한 부분에 한하여 CLI가 사용되곤 한다. 하지만 백업 기능으로 사용하기에는 텍스트에디터(vs code)도 충분히 만족스럽게 사용 가능하다.

일단 세가지의 구동방식은 당연하겠지만, 동일하다. 그냥 자신에 입맛에 맞는 프로그램을 사용하는것이 좋다.

___

### CLI

___

### GUI

___

### Vs code

#### Repository 생성 후 Git:clone

먼저 github안에 저장소를 생성하고 클론하는 방법이 가장 간편하다.

1. github 저장소 생성
2. 저장소 주소 복사
3. vs code 명령팔렛트 (cmd+shift+p)
4. git clone 입력 후 주소 입력
5. 코드 수정 후 add -> commit -> push 진행

[참조] : <https://demun.github.io/vscode-tutorial/git/>

##### git 저장소 이름 변경

git remote rename 명령으로 리모트 저장소의 이름을 변경할 수 있다. 이 경우 리모트 저장소의 브랜치 이름 또한 변경된다.

```Markdown
git remote -v
  #View existing remotes
origin  https://github.com/limprove/test-1.git (fetch)
origin  https://github.com/limprove/test-1.git (push)

git remote set0url origin https://github.com/limprove/git.git
  #Change the 'origin' remote's URL

git remote -v
```

##### git 파일 혹은 폴더명 변경

git mv oldName newName 명령으로 이름을 변경할 수 있다. mv명령어는 원래 이동명령이지만, 파일 혹은 폴더명 변경에도 사용한다.

#### 로컬저장소 생성 후 Git remote

로컬저장소에 프로젝트 생성 시 (react-creat-app 등) 로컬과 git repository를 remote 해주어야 한다.
이 경우, github에 repository 생성은 진행하여야 한다.
먼저, 로컬저장소의 프로젝트 폴더와 github에 저장소가 준비 된 경우
터미널에

```bash
$ git init
$ git add .
$ git commit -m "commit message"
$ git remote add origin #github-주소
$ git push origin master
```
만약, 먼저 생성된 .git 폴더가 있는 경우 rm -rf 명령어를 이용하여 삭제 후 진행한다.

```bash
$ rm -rf .git
```

[참조] : <https://velog.io/@loakick/Github-Action-React-Project-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0-nkk30yefpi/>