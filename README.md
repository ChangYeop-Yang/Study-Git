# ■ Study-Git

깃(Git)은 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템이다. 소프트웨어 개발에서 소스 코드 관리에 주로 사용되지만 어떠한 집합의 파일의 변경사항을 지속적으로 추적하기 위해 사용될 수 있다. 기하학적 불변 이론을 바탕으로 설계됐고, 분산 버전 관리 시스템으로서 빠른 수행 속도에 중점을 두고 있는 것이 특징이며 데이터 무결성, 분산, 비선형 워크플로를 지원한다.

## 🛠 Git Branch Policy

* `[master]` 브랜치(Branch)에는 직접 Commit을 올리지 않습니다.
* 기능을 개발하기에 앞서 `[master]` 브랜치(Branch)를 기준으로 새로운 브랜치(Branch)를 생성합니다.
* 새롭게 생성하는 브랜치(Branch)의 이름은 `[feature/기능이름]` 형식으로 명명하고 기능을 개발하는 한 명만 커밋 작업을 수행합니다.
* `[feature/기능이름]` 브랜치에서 기능 개발이 종료되면 `[master]` 브랜치에 이를 합칩니다.

## 🛠 Git Commit Message Policy

* 제목과 본문을 빈 줄로 분리합니다.
* 제목은 `50자 이내`로 작성하여야 합니다.
* 제목을 영문자로 작성하는 경우에는 첫 글자는 대문자로 표시합니다.
* 제목에는 마침표를 넣지 않습니다.
* 제목을 영문자로 작성하는 경우에는 동사원형을 시작하여야 합니다.
* 본문으 72자 단위마다 줄바꿈을 하여 작성하여야 합니다.
* `어떻게(How)` 보다는 `무엇(What)`과 `왜(Why)`를 설명하여 작성하여야 합니다.

## 🛠 Git Command

* `I` → [init](https://git-scm.com/book/ko/v2/Git의-기초-Git-저장소-만들기): 현재 폴더에 대하여 Git 작업을 위한 저장소를 생성하는 명령어입니다. 

* `A` → [amend](https://backlog.com/git-tutorial/kr/stepup/stepup7_1.html) (Amend last commit): 가장 최근의 Commit 작업에 대하여 수정을 할 수 있는 명령어입니다. 스테이지에 올린 변경사항이 기존 커밋 작업에 추가되어 덮어씌워집니다.

* `C` → [cherry-pick](https://backlog.com/git-tutorial/kr/stepup/stepup6_4.html): 다른 브랜치(Branch)에서 지정한 커밋을 복사하여 현재 작업중인 브랜치(Branch)로 가져오는 경우 사용하는 명령어입니다. 
  * 해당 명령어는 특정 브랜치(Branch) 잘못 추가한 커밋으로 올바른 브랜치(Branch)로 옮기는 경우에 사용합니다.
  * 다른 브랜치(Branch)의 커밋 작업을 현재 브랜치(Branch)에 추가하여 작업을 수행하는 경우에 사용합니다.

* `C` → [config](https://backlog.com/git-tutorial/kr/reference/config.html): 현재 사용중인 Git 환경에 적용 된 옵션을 확인하거나, 옵션에 대한 설정 값을 변경할 수 있습니다. 또한, `config` 명령어에는 지역 옵션(Local Option), 전역 옵션(Global Option), 시스템 환경 옵션(System Option)이 있습니다.
  * `[Local Option]`: 현재 Git 저장소에서만 유요한 옵션입니다.
  * `[Global Option]`: 현재 사용자를 위한 옵션입니다.
  * `[System Option]`: 현재 사용중인 PC 전체의 사용자를 위한 옵션입니다.

* `R` → [reset](https://git-scm.com/book/ko/v2/Git-도구-Reset-명확히-알고-가기): 이전의 작업을 수행 한 특정 커밋 시점으로 브랜치(Branch)의 작업환경을 변경하는 명령어입니다. 
  * `[Mixed]` 모드는 변경사항을 작업 스테이지 아래로 두어서 다시 사용자가 커밋 작업을 수행 할 파일을 추가할 수 있도록 합니다. 
  * `[Soft]` 모드는 변경사항을 다시 작업 스테이지의 위로 올려서 바로 커밋 작업을 수행할 수 있도록 합니다. 
  * `[Hard]` 모드는 현재 작업중인 모든 변경 사항을 폐기하며 일반적으로 많이 사용하고 있습니다.

* `R` → [revert](https://backlog.com/git-tutorial/kr/stepup/stepup7_2.html): 이전의 작업을 수행 한 특정 커밋 시점으로 브랜치(Branch)의 작업환경을 변경하는 명령어이며 `reset` 명령어와는 다르게 이전 시점으로 변경에 대한 커밋 기록이 추가되는 차이점이 있습니다.

* `S` → [stash](https://git-scm.com/book/ko/v2/Git-도구-Stashing과-Cleaning): 커밋하지 않은 변경 사항들을 임시 저장소에 보관하는 명령어입니다. 하지만, Tracked 상태인 작업 파일들에 대해서만 사용할 수 있습니다.

* `S` → [status](https://www.atlassian.com/git/tutorials/inspecting-a-repository): 현재 Git 저장소의 상태를 사용자에게 알려주는 명령어입니다. 해당 명령어는 Git 저장소에서만 수행할 수 있는 명령어입니다. 
  * `git status -s`: 변경 된 파일이 많은 경우에 사용자가 보기 편하도록 요약항 상태를 보여주는 명령어입니다.

* `H` → [help](https://git-scm.com/book/ko/v2/시작하기-도움말-보기): Git에서 사용되는 각 명령어들에 대한 도움말을 볼 수 있는 명령어입니다.
  * `git help <command>`: 해당 명령엉 대항 사용자 도움말을 표시합니다. 사용자 도움말에는 명령엉 대한 의미와 세부적인 옵션들을 안내합니다.

## 🛠 Git 용어 정리 

* [branch](https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html): 특정 기준에서 줄기를 나누어 독립적인 작업을 수행할 수 있도록 하는 기능입니다.

* [working tree](https://backlog.com/git-tutorial/git-workflow/): Git 작업 폴더를 가리키는 용어입니다.

* [rebase](https://backlog.com/git-tutorial/kr/stepup/stepup2_8.html): `Pull requests` 작업을 수행 시 하나의 브랜치(Branch) 줄기에 다른 브랜치(Branch) 커밋 베이스를 잘라내어 하나로 만드는 작업을 수행하는 명령어입니다. `merge` 명령어와의 차이점은 `Pull requests` 작업 시 충돌(Conflict) 발생 시 수정에 대한 커밋 이력이 남지만 `rebase`는 그러한 이력이 남지 않습니다. 또한, `rebase` 작업을 완료하기 위해서는 CLI 환경에서 `git push -f [remote branch name]` 명령어 작업을 수행하여야 합니다.

|📷 rebase IMAGE 001|📷 rebase IMAGE 002|📷 rebase IMAGE 003|
|:-----------------:|:-----------------:|:------------------:|
|![image](https://user-images.githubusercontent.com/20036523/127768643-40f0d3b0-5e22-4533-a93d-b5c34db990b4.png)|![image](https://user-images.githubusercontent.com/20036523/127768664-9b71c68b-dc73-4d99-babe-e4bc2c40019e.png)|![image](https://user-images.githubusercontent.com/20036523/127768673-1905367b-2f88-4cc2-8bbe-0b0e17dd2e9f.png)|

## :mega: REFERENCE

* [Git](https://git-scm.com)
* [Git - Wikipedia](https://ko.wikipedia.org/wiki/깃_(소프트웨어))
* [팀 개발을 위한 Git GitHub 시작하기, 한빛미디어, 정호영, 진유림](https://book.naver.com/bookdb/book_detail.nhn?bid=15986509)
