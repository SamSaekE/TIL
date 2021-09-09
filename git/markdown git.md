# GIT " 분산 버전관리 시스템" 

## 기본 특징

* 코드의 히스토리 파악 가능. 단, git은 변경사항만을 저장

* GITHub: 분산 버전 관리 시스템인 GIT 기반의 저장소 

* 명령어를 통해서 사용: CLI(Command Line Interface) 방식

  (참고)CLI<->GUI

## REPOSITORY

* 특정 디렉토리를 버전 관리하는 저장소
* 명령어 ``git init`` : 로컬 저장소를 생성해서 숨김폴더인  .git 를 통해 버전관리를 하게됨
*  git init 을 입력하지 않으면 local repository가 생성되지 않음. 
* 리모트에서 repo를 만들고 clone 해오면 git init을 할 필요 없음. 이미 .git 이 만들어져있음.
*즉 git init은 로컬에서 버전관리를 해나갈때 쓰는 것
## COMMIT

* 3가지 영역에서 동작
  1. working directory : 내가 작업하고 있는 실제 디렉토리
  2. staging area:커밋으로 남기고 싶은/특정 버전으로 관리하고 싶은 파일이 있는 곳
  3. repository: 커밋들이 저장되는 곳

## git status

파일 상태 확인



## git add .
- 파일을 staging area에 올림.
- 모든 파일을 올리려면 . 을 이용하며, 특정 파일만 올리려면 파일명.타입 형식으로 작성


## git commit -m "commit_message(자세히)"



## git diff



## git remote add origin https://github.com/SamSaekE/remote_repo.git

리모트 레포 연결하기

origin= remote repository

## git push -u origin(repo_name) master(local.branch) : 오리진으로 내 로컬에 있는 마스터에 대한 변경사항(commit)을 푸시할게

* 마스터 : 브랜치...?

* -u는 한번만 쓰면 다음부터는 안쓰면 됨

* git push origin master 를 안해주면 remote  repository 에 수정사항이 (commit)이 반영이 안되는 건가요??

  yes. local repository 에는 commit 저장하면서 반영이 됏더라도 git push origin master 를 안해주면 remote repository 에 반영이 안됨.




## git hub repository에서 local repository 로 가져오기(clone)

* 로컬과 리모트를 연결한 후(git remote add origin ~) 로컬에서 리모트로 푸시하던 방식과 달리 
* 리모트 레포를 만들고 로컬로 복제해와서 연결 과정을 거치지 않음
* 위의 방법보다 더 자주쓰는 방법



# 간단한 Unix/Linux 명령어

* ls: 현재 위치의 폴더 파일 목록 보기
* 현재 위치 이동하기: cd <path>, cd ..
* 폴더 생성하기: mkdir <name>
* 폴더 삭제하기: rm -r <name>
* 파일 생성하기: touch <name>
* 파일 삭제하기: rm <name>

