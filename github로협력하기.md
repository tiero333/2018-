#Git 협업 방법
==============

1.Git과 SourceTree 설치
-----------------------

Git으로 협업 하기 위해 가장 첫번째로 Git을 설치한다.

설치 후 제대로 설치되어있는지 확인하기 위해 cmd에 git을 입력해보자.

git에 관련된 명령어들이 출력된다면 제대로 설치 된 것이다.

Git은 명령어로 사용하기 때문에 사용에 어려움이 있을 수 있다.

Git을 좀 더 쉽게 사용하기 위해 Git을 GUI화 시켜주는 프로그램인 SourceTree도 설치한다.

2.저장소 만들기 (init)
-----------------------

SourceTree를 실행하고 Add Repository(저장소 추가)를 누른다.

Create New Repository클릭 - Repository Type : Git - Destination Path : (자신이 지정한 디렉토리) - Create 클릭

앞으로의 작업이 내 컴퓨터에 저장되는 로컬저장소를 만들었다.


3.버전 만들기 (commit)
-----------------------

※해당 작업에 앞서 상단메뉴 Tool - Options - General탭에 Default user information에 있는 Full Name과 Email address를 입력하고 OK해주자.

Destination Path로 지정된 디렉토리 안에 새로운 파일을 추가하거나, 파일의 내용이 수정되었을 때 Git은 이 변화를 인지한다.

이 때 SourceTree를 확인하면 하단 Log/History탭 - Unstaged files에 변화가 있는 파일들이 나열되며 오른쪽에 수정된 내용들이 보여진다.

여기서 Git에 동기화 할 파일들을 선택하고 Stage Selected를 클릭한다.

Stage Selected된 파일들은 Staged files에 나열되는데 이 때 상단에 있는 Commit을 클릭한다.

Commit을 클릭하면 하단 File Status탭으로 이동되는데 하단 공란에 작업 내용을 입력할 수 있다.

작업 내용을 입력하고 입력란 바로 아래 있는 Commit을 클릭하면 Git에 작업한 내용들이 반영된다.

Git에 반영된 내용은 SourceTree의 Log/History탭에서 확인할 수 있다.

4.원격 저장소
--------------

Git은 기본적으로 로컬저장소에 저장하는 방식이다.

이 방식은 기기가 고장나거나 외부 기기를 이용하여 작업을 이어갈 때 무용지물이 된다.

하지만 원격 저장소를 통해 Git을 저장한다면 백업과 외부에서의 접근이 가능하다.

작업중인 기기가 고장나거나 프로젝트를 공유해야 하는 경우에 모두 유용하게 사용 가능한 것이다.

원격 저장소에는 여러가지 종류가 있지만 가장 보편적인 github를 이용하도록 하겠다.


4.1.원격 저장소 만들기
----------------------

github.com에 로그인하고(계정이 없다면 가입) 메인 페이지에서 Start a project를 클릭한다.

Repository name을 입력 후 하단의 메뉴들은 자신의 기호에 맞게 설정한 후 Create repoasitory를 클릭한다.

4.2.SourceTree에 원격 저장소 연결하기
-------------------------------------

github에 만든 repository를 클릭한다.

오른쪽 중간쯤에 있는 초록색 Clone or download을 클릭한다.

Clone with HTTPS 하단에 있는 URL를 복사한다.

SourceTree 상단 Repository메뉴 - Add romote... - Remotes - Add - Remote name : (자신이 입력) - URL/Path : (github에서 복사한 URL 입력) - OK클릭

이렇게 하면 SourceTree 왼쪽 REMOTES항목 아래에 github와 연결된 원격 저장소가 생성된다.

5.협업하기
-----------

원격 저장소에 프로젝트가 올라가있으면 외부에서 접근이 가능하고, 이것은 곧 협업이 가능하다는 의미가 된다.

내 프로젝트에 다른 사람을 참가시키거나 내가 다른사람의 프로젝트에 참여해보자.

5.1.원격 저장소 복제
--------------------

다른 사람의 프로젝트를 함께 진행하기 위해서는 그 사람의 원격 저장소에서 소스들을 자신의 로컬 저장소로 복제하여 가져와야 한다.

협업 할 프로젝트의 github에서 Clone or download 클릭 - HTTPS URL 복사 - SourceTree에서 상단의 '+'클릭 - Clone - Source Path/URL : (붙여넣기) - Destination Path : (
복사한 프로젝트를 저장하고 git과 연동시킬 로컬 저장소 선택) - Name : (직접 입력) - Clone 클릭

