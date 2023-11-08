# 멀티미디어실습

> 2023년 가을학기에 진행한 git 수업 정리

## 2023-09-27
- commit
    - 사진 찍기와 유사
    - git의 기본 단위로, 논리적 변경이 있을 때 생성

- commit 메시지
    - 코멘트 역할
    - 코드 변경분을 한 마디로 설명
    - 명령어
        - git commit -m "커밋 메시지"
        - git commit --message "커밋 메시지"

- 얼마나 자주 커밋을 만들어야 하나
    - 커밋 단위가 너무 작을 경우, 불필요한 커밋들이 생성
    - 커밋 단위가 너무 클 경우, 장애 발생시 빠른 대응이 어려움
        - ex) 30분 안에 리뷰 가능하도록 커밋 크기 조절
 
## 2023-10-04
- IT 프로젝트
    - 동시에 여러 파일을 건드림
    - 일반 문서 수정과 같이 '저장' 버튼 클릭만으로 한번에 수정한 파일들을 저장하게 하면, 불필요한 파일들이 커밋에 포함
        - ex)`.vs`: visual studio로 프로젝트 열었을 때 생기는 폴더
    - staging area라는 영역을 따로 두고, 커밋에 포함시킬 코드만 스테이징 영역에 추가하게 한 다음, 커밋을 생성

- 스테이징 영역
    - 수정된 여러 파일 중에서 최종적으로 커밋에 포함시킬 파일
    - working directory -> staging area -> repository
    - 명령어
        - git add 파일명

- gitignore
    - 루트 경로에 있은 `.gitignore`파일은 버전관리 하지 않을 파일의 목록을 관리하는 용도
    - 사용하는 운영체제, 에디터, 프로그래밍 언어, SDK, 라이브러리 등의 종류에 따라 의도치 않은 파일 생성시, `.gitignore`파일에서 관리
        - ex) https://github.com/RyanNielson/PixelCamera2D/blob/master/.gitignore
    - 처음 프로젝트 세팅하면 여러 툴을 사용해 자동으로 `.gitignore`파일에 들어갈 내용을 생성
        - 웹사이트
            - ex) https://www.toptal.com/developers/gitignore
        - VSCode 익스텐션
            - gitignore by CodeZombie
         
## 2023-10-18
- 저장소
    - 일반 폴더와 저장소의 차이는 `.git` 숨김폴더가 유무차이
        - 일반 폴더는 `.git` 숨김폴더 O
        - 저장소는 `.git` 숨김폴더 X
    - `.git` 숨김폴더를 삭제하면 커밋 이력등도 같이 삭제

- 브랜치
    - 커밋을 가리키는 포인터
    - 이슈 생성, 이슈에 해당하는 브랜치 생성
        - `git branch` <--만들어진 브랜치 확인
        - `git branch 브랜치명` <--새로운 브랜치 생성
    - 작업 시작할 땐, 생성한 브랜치로 전환(switch)
        - `git switch 브랜치명`
        - `git checkout 브랜치명`

## 2023-11-08
- 브랜치 병합
    - 브랜치 병합시 충돌이 일어나지 않게 하려면 두 브랜치에서 수정한 코드가 겹치지 않아야 함
    - 명령어
        - git merge
