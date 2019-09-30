# Git과 visualStudio code의 연동

### git을 컨트롤 하는 방법에는 크게 3가지가 있다.
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

먼저 github안에 저장소를 생성하고 클론하는 방법이 가장 간편하다. 

1. github 저장소 생성
2. 저장소 주소 복사
3. vs code 명령팔렛트 (cmd+shift+p)
4. git clone 입력 후 주소 입력
5. 코드 수정 후 add -> commit -> push 진행

[참조] : <https://demun.github.io/vscode-tutorial/git/>

#### git 저장소 이름 변경

기존 원격 저장소 이름 변경 시 URL또한 변경이 된다. git의 url구조가 저장소 이름이 들어가기 때문이다. 

```Markdown
git remote -v
  #View existing remotes
origin  https://github.com/limprove/test-1.git (fetch)
origin  https://github.com/limprove/test-1.git (push)

git remote set0url origin https://github.com/limprove/git.git
  #Change the 'origin' remote's URL

git remote -v
```

이 후 로컬저장소와의 연동 방법을 찾아야 한다.

