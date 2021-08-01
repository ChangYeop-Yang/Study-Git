# ■ Study-Git

깃(Git)은 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템이다. 소프트웨어 개발에서 소스 코드 관리에 주로 사용되지만 어떠한 집합의 파일의 변경사항을 지속적으로 추적하기 위해 사용될 수 있다. 기하학적 불변 이론을 바탕으로 설계됐고, 분산 버전 관리 시스템으로서 빠른 수행 속도에 중점을 두고 있는 것이 특징이며 데이터 무결성, 분산, 비선형 워크플로를 지원한다.

## 🛠 Git Branch Policy

* `[master]` 브랜치(Branch)에는 직접 Commit을 올리지 않습니다.
* 기능을 개발하기에 앞서 `[master]` 브랜치(Branch)를 기준으로 새로운 브랜치(Branch)를 생성합니다.
* 새롭게 생성하는 브랜치(Branch)의 이름은 `[feature/기능이름]` 형식으로 명명하고 기능을 개발하는 한 명만 커밋 작업을 수행합니다.
* `[feature/기능이름]` 브랜치에서 기능 개발이 종료되면 `[master]` 브랜치에 이를 합칩니다.

## 🛠 Git Command

* [amend](https://backlog.com/git-tutorial/kr/stepup/stepup7_1.html) (Amend last commit): 가장 최근의 Commit 작업에 대하여 수정을 할 수 있는 명령어입니다. 스테이지에 올린 변경사항이 기존 커밋 작업에 추가되어 덮어씌워집니다.

## 🛠 Git 용어 정리 

## :mega: REFERENCE

* [Git - Wikipedia](https://ko.wikipedia.org/wiki/깃_(소프트웨어))
* [팀 개발을 위한 Git GitHub 시작하기, 한빛미디어, 정호영, 진유림](https://book.naver.com/bookdb/book_detail.nhn?bid=15986509)
