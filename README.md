# ■ Study-Git

깃(Git)은 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템이다. 소프트웨어 개발에서 소스 코드 관리에 주로 사용되지만 어떠한 집합의 파일의 변경사항을 지속적으로 추적하기 위해 사용될 수 있다. 기하학적 불변 이론을 바탕으로 설계됐고, 분산 버전 관리 시스템으로서 빠른 수행 속도에 중점을 두고 있는 것이 특징이며 데이터 무결성, 분산, 비선형 워크플로를 지원한다.

## 🛠 Git Branch Policy

* `[master]` 브랜치(Branch)에는 직접 Commit을 올리지 않습니다.
* 기능을 개발하기에 앞서 `[master]` 브랜치(Branch)를 기준으로 새로운 브랜치(Branch)를 생성합니다.
* 새롭게 생성하는 브랜치(Branch)의 이름은 `[feature/기능이름]` 형식으로 명명하고 기능을 개발하는 한 명만 커밋 작업을 수행합니다.
* `[feature/기능이름]` 브랜치에서 기능 개발이 종료되면 `[master]` 브랜치에 이를 합칩니다.

## 🛠 Git Command

* `A` → [amend](https://backlog.com/git-tutorial/kr/stepup/stepup7_1.html) (Amend last commit): 가장 최근의 Commit 작업에 대하여 수정을 할 수 있는 명령어입니다. 스테이지에 올린 변경사항이 기존 커밋 작업에 추가되어 덮어씌워집니다.

* `C` → [cherry-pick](https://backlog.com/git-tutorial/kr/stepup/stepup6_4.html): 다른 브랜치(Branch)에서 지정한 커밋을 복사하여 현재 작업중인 브랜치(Branch)로 가져오는 경우 사용하는 명령어입니다. 
  * 해당 명령어는 특정 브랜치(Branch) 잘못 추가한 커밋으로 올바른 브랜치(Branch)로 옮기는 경우에 사용합니다.
  * 다른 브랜치(Branch)의 커밋 작업을 현재 브랜치(Branch)에 추가하여 작업을 수행하는 경우에 사용합니다.

* `R` → [reset](https://git-scm.com/book/ko/v2/Git-도구-Reset-명확히-알고-가기): 이전의 작업을 수행 한 특정 커밋 시점으로 브랜치(Branch)의 작업환경을 변경하는 명령어입니다. 
  * `[Mixed]` 모드는 변경사항을 작업 스테이지 아래로 두어서 다시 사용자가 커밋 작업을 수행 할 파일을 추가할 수 있도록 합니다. 
  * `[Soft]` 모드는 변경사항을 다시 작업 스테이지의 위로 올려서 바로 커밋 작업을 수행할 수 있도록 합니다. 
  * `[Hard]` 모드는 현재 작업중인 모든 변경 사항을 폐기하며 일반적으로 많이 사용하고 있습니다.


## 🛠 Git 용어 정리 

## :mega: REFERENCE

* [Git - Wikipedia](https://ko.wikipedia.org/wiki/깃_(소프트웨어))
* [팀 개발을 위한 Git GitHub 시작하기, 한빛미디어, 정호영, 진유림](https://book.naver.com/bookdb/book_detail.nhn?bid=15986509)
