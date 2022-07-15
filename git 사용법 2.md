Git -2 

- submodule: git 내부에 git 생성시 ---> 트래킹 발생

- 순서 잘지켜서 라이프사이클에 맞추어 진행

- ![파일 라이프 사이클](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/67719520-a1d8-4cbb-81dd-49dea429a7f4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T043904Z&X-Amz-Expires=86400&X-Amz-Signature=6efc2acc742c9fc54833dfa8c822ebbef361a6f25df9936fe227922dd5be6af6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

- untracked: git이 관리하지 않는파일 (한번도 staging area에 올라간 적 없는 파일)

- tracked : git이 관리하는 파일

    - unmodified : 최신 상태

  - modified : 수정 되었지만 아직 staging area 에는 반영하지 않은 상태
  - staged : staging area에 올라간 상태

옵션과 인자

- 옵션
  - 동작 방식을 지정 (생략가능)
  - ex: git log --oneline ---> 커밋내역을 한 줄로 보고 싶을때 -> 부가기능이라 정상동작
- 인자
  - 동작 대상을 지정 (생략 불가능)
  - git add ---> 어떤 파일을 staging area 에 올리는지 모르니까 X
  - 이때 git add a.txt 같이 대상을 지정 할 때 a.txt를 인자라고 한다.



1. 작업
2. add
3. commit

git commit -m ""   에서 -m 빼면 VIM 모드 가 나옴 ---->

git log --oneline ---> 각 로그 제목,주소만 요약해서 나옴





A지역에서 git hub에 업로드 한후

B지역에서 자료를 가져올 파일을 만든 후 gitbashhere을 켠 후 --> git clone 주소

----> 해당 되는 repository 주소를 복붙(http 자료)

++++ git clone 주소 .

github 저장공간 만들기

Respositories -> new -> 이름 적고 생성

.git --------->github

​		(push)

git remote add origin http~~~~

git remote -v : 확인



push // pull

내가 작업해서 push 했으니 너가 pull 해 

-->(가운데에 원격 저장소를 끼고)

A  <------->원격저장소<------->B

ver.1				ver.1				ver.1

ver.2				ver.2				ver.2

ver.A				ver.B				ver.B

----> A와B가 다르기때문에 push하면 에러가 된다

----> 컴터가 a랑b중에 뭐가 최신인지는 모르겠으니

----> A랑B를 둘다 작업한걸 합쳐서 최신본을 만들어서 넘겨라

1->2->A->B 나 1->2->B->A 든 최신 순서를 만들어서 넘겨라

