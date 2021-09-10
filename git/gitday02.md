# 복습

코드블럭

> ``` java
> system.out.println("hello world")
> ```

인라인 코드블럭 : how to ` import ` 

링크: [naver]( www.naver.com)

이미지 태그: ![고양이](git%20day02.assets/%EC%82%BC%EC%83%89%EC%9D%B4.jpg)

텍스트 강조

- 볼드체: 별표 두개 양옆
- 이탤릭체: 별표 한개 양옆
- 취소선: 물결표시 두개 양옆

수평선: 별표나 하이픈이나 언더바 세개

표 만들기:

| 분류   | 특징   |
| ------ | ------ |
| 고양이 | 귀여움 |

Unix/Linux 명령어:

- ls 폴더랑 파일 리스트 출력
- cd 경로이동
- cd .. 상위 디렉토리로 이동
- cd ../..  상위 디렉토리로 두번 이동
- mkdir 폴더생성
- touch 파일생성
- rm 파일 삭제명령어
- rm -r 폴더 삭제 명령어
- 마크다운 폴더에 test01과 test02폴더가 있는 상태일때, test01에서 test02로 가는 방법은?   **cd ../test02 **

## GIT 기본명령어

- git init: .git 이라는 로컬 레포를 만듬
- git status: untracked 인 파일을 알 수 있음
- git add . : 현재 디렉토리에 있는 변경사항 모두 추가(staging area 에 올라감)
- git commit -m " blahblah"

## GIT 로컬과 리모트 연결하기

​		git remote add origin url

​		git push -u origin master

## GIT 리모트 레포 복제

git clone url

# TODAY



## how to   **PULL** 

class에서 코드를 열고 git clone 레포url 을 해버리면 class 안에 class_repo(master) 가 생김

클래스 폴더에 클래스_레포 폴더가 생기지 않고 클래스 폴더 자체가 master가 되게하는 방법

class 에서 git bash를 열고

git clone https://github.com/SamSaekE/class_repo**. git .**

그 후 클래스 리드미에서 변경사항

*** 이제 홈에서  ***

git pull origin master: origin 의 마스터 브랜치를 마스터로 가져옴

(git push origin master:  로컬의 마스터 브랜치를 오리 오리진으로 보냄)



## staging area 에서 내리기

git restore --staged 파일명.확장자

## working directory 변경사항 취소하기(내 작업 취소)



## commit 되돌리기: git reset --hard{c_id}

 // hard{c_id}는 커밋 아이디 앞 네자리

## git diff 커밋1앞네자리 커밋2앞네자리

// 커밋간 차이 보여줌

## ingnore

.git 이 있는 폴더(home)에 .gitignore 파일을 만듬

그리고 .gitignore 에 무시할 파일명을 적음.

- 특정파일 제외: 특정 파일명.확장자 (img01.png)
- 특정폴더 제외: 특정폴더명/ (data./)
- 특정확장자 제외: 별표.확장자명 (*.txt) -- 폴더 막론
- 위에다가 !text01.txt 를 덧붙이면 모든 txt는 제외하되, text01파일은 버전관리를 하게 됨.

이그노어는 시크릿파일 등에 적용.

프로젝트 처음 시작시, .git 레포 만들때 .gitignore도 만들어주는게 좋음

##  shared repo

리모트 레포의 invite 기능을 활용하여 업뎃 주고받기 가능

## 브랜치 BRANCH

= 특정 커밋을 가리키는 '포인터'

보통 마스터 브랜치를 현재 동작하고있는 버전.

파생되는 브랜치는 현재 버전에서 기능이 추가되어 실험해보는 버전

 브랜치를 합치는 방식(머지)에는 두가지 방식 존재

1. 마스터를 땡겨오지는 머지 (fast forward)
2.  머치 커밋 생성하며 머지

참고) git log --graph --oneline : 로그 쉽게 보기

## **STEP**: fast forward

1. 브랜치 생성: git branch feature-signup
2. 브랜치로 이동: git checkout feature-signup
3. 커밋 반영시,  feature-signup 브랜치를 타게 됨
4. 마스터브랜치로 이동: git checkout master
5. 다시 f-s 브랜치로 이동: git checkout feature-signup
6. 마스터를 가리키는 포인터를 f-s 브랜치의 마지막 커밋을 가리키도록 변경: git checkout master 로 변경시켜야하는 브랜치의 커밋으로 간 후, git merge feature-signup 을 이용해 마스터를 가리키던 포인터를 f-s 브랜치의 마지막 커밋을 가리키도록 함. *fast forward merge*

## STEP : merge commit btw master&test

1. master를 중심으로 합치고 싶으면 git checkout master 를 이용해 마스터로 간 후 git merge test를 통해 test 를 master로 흡수시킴
2. 충돌 발생
3. 수정 애드 <커밋-merge01>
4. 즉 새로운 커밋으로 이동하며 머지됨.

## STEP: 머지 커밋 btw master and feature

주의)머지커밋이 생기는 기준: 브랜치가 갈라진 후 마스터 브랜치가 한번이라도 변경사항이 생기게 되면 충돌이 생김

