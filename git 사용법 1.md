# Git

- Repository

  특정 디렉토리를 버전 관리하는 저장소 

   git init 명령어로 로컬(=내 컴퓨터<->원격) 저장소를 생성 ---> 안보이는데 숨김항목으로 되어 있어서 체크 해야 보임 (하일확장명, 숨긴항목)

  .git 디렉토리에 버전 관리에 필요한 모든 것이 들어있음

​		하나의 프로젝드(=폴더)를 하나의 git 으로 만드는 것임

​			-> 폴더가 아닌 파일을 관리하니 빈 폴더는 해당이 X

- git 의특징(작업 -> add -> commit)

  - gitbash 에서 git add . 입력  ---> '.' 은 현재 파일 주소를 의미

    Git 기본기 

    - woriking directory : 내가 작업하고 있는 실제 디렉토리
      - 분장
    - staging area: 커밋으로 남기고싶은, 특정 버전으로 관리하고 싶은 파일 있는 곳
      - 무대
    - repository: 커밋들이 저장되는 곳
      - 사진폴더

    ---> 분장을 하여(작업을 하고)----> 무대에 오른다{git add . (전체가 해당될 경우) or   git add ~~~ (~만 해당 될 경우)으로 업데이트}

    ​			(untracked 상태)	-------->  staged    --------> committed

    ​											git add                  git commit

    --->commit 이 진행 되고 나서 부터 untracked 파일 은 modified 가 되어 다시 git add / git commit 계속 반복

     git status --> commit 상태여부 및 commit 해당 사항 확인 가능

    ​	{git add . 하기 전에 git status 하면 modified(붉은색) 인데 git add . 하면 녹색 new file 로 바뀜}

  - git add ~~ : ~~ 파일을 staged 상태로 보냄 

  - git commit -m "~~~": 커밋 메세지( = ~~ )로 컷밋의 이름을 저장함.

  - 

  - SSAFY@DESKTOP MINGW64 ~/Desktop/Git/git_test (master)
    $ git commit -m"스타트캠프마지막날"
    [master (root-commit) **6b8d26c]** 스타트캠프마지막날
     1 file changed, 1 insertion(+)
     create mode 100644 readme.md

    -----> root-commit 옆에 적히 문자열은 commit 주소

    