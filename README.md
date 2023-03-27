# Demo1
깃허브 사용 _ 김한규 교수님  </br> 


# --- Github의 다양한 기능 ---

- Github action

- Static page web hosting using github

- Github gist - sharing code snippets </br>                     



#  - new repository 'demo' 만들기  // master 아니라 main

   - personal access token

// personal access token 만들어 보관하기

// 오른 편 위쪽 settings->왼편 아래 <>developer settings

   ->왼편 위 personal access token -> 오른 편 위

   -> generate token => 복사하여 잘 보관

   (credential manager를 사용하여 매번 입력하지 않고 사용)

// MS가 github 인수 후 사용자 편의를 위해 다양한 기능을

   추가 했으나 기존 git 명령어들을 타이핑 하지 않고 간단히

   같은 일을 할 수 있는 UI 제공됨

   예를 들면 gist를 사용하면 더 편리 - 그러나 공부에는?

 

(1) mkdir repo1; cd repo1  // git init 하지 않았음

ls -al // repo1에 아무 것도 없는 것 확인

// github demo repo에 파일 만들어 두고 실험

git clone <github repo url> . // git init 없이

ls -al // github 의 repository가 clone된 것 확인

cd demo

git status // git init 하지 않았어도 git을 사용할 수 있도록

           repository가 복제된 것 확인

      // main branch 에 유의

// "origin/main" 는 "remote tracking branch"로서

 "origin"이라고 이름붙여진 remote repository에 있는 "main"이란

 브랜치의 local copy

 
  - origin/main 는 LOCAL branch!!!

  - origin/main 브랜치는 origin 이라는 remote repo를

    가리키는 pointer 가 아님!!!

git remote // origin branch 생성된 것 확인

git branch  // 현재 브랜치 local repo의 main 만 보임

git branch -a // 출력 설명

ls -al // swedemo/demo repo의 파일 복제되어 온 것 확인

 

vim file1

// 파일 작업 후 add, commit 하고 git status 확인

/* git diff // file1 수정 사항 확인 */

git status

 // 생략 가능  git add . // git add -A

git commit -am 'file1 modified in local repo'

git status

// 출력문 설명 - git push

// github demo repo에 push

git push origin main // credential 확인

// github repo에 push되었는지 commit 메시지 및 내용 확인

// github에서 history도 확인

 

// 통상 push 이전에 pull하여 동기화 권장

git pull origin main // pull = fetch & merge

 

// git credential 에 personal access token 저장

 
git config --global credential.helper cache

// 저장된 credential을 지울 때

git config --global --unset credential.helper

 

 

 

(2) github demo repo에서 git 명령들을 GUI로 제공하는 것을 설명

- repository에서 파일 생성, commit

- 수정 후 commit

- 새로운 branch 만들고 새 파일 만들고, 기존 파일 수정 후 commit

- pull request 확인

- branch에서 기존 파일 merge conflict 생기도록 수정 후 commit

- pull request에서 merge conflict 확인

 

(3) github contribution - fork // 다른 github 계정을 만들어 데모

    그림을 먼저 설명

 

 

 

