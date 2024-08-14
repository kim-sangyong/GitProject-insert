# 깃허브에 프로젝트 올리는 법 #

내가 올리고자 하는 프로젝트 폴더에 마우스 우클릭 후 Open Git Bash here 클릭

git config --global user.name "kim-sangyong" = 깃허브 사용자 이름
git config --global user.email "sdragon0416@gmail.com" = 내 gmail 이메일

git init = 루트 폴더에 git 폴더 생성
git add . = 내 프로젝트 모든 파일 업로드
=> 꼭 add 뒤에 띄어쓰기 후 . 붙혀야함
git status = 파일 목록 확인

git commit -m  " 커밋할 내용 " = 커밋할 내용 적으면됨

git remote add origin " 내 https 깃 주소 " = 내 https 깃 주소 적으면 됨
=> 다른 블로그들을 보면 https:/~~~~.git 으로 url이 되어 있지만 그렇게 되어 있지 않은 사람들은 당황하지 않아도 된다.
=> git init 으로 git 파일을 생성 후 https 복사 -> 터미널창에 shift+insert(붙혀넣기)를 하면 url 뒤에 .git이 붙혀져 있다.

git push -u origin master  = 마스터 브랜치에 업로드가 됨(push)

* master 브랜치에 프로젝트가 업로드가 되고 main 브렌치로 프로젝트를 올리고 싶을때 *
master 브렌치에서 main 브렌치로 전환?? 

git checkout master
git branch main master -f
git checkout main
git push origin main -f

하고 main 브랜치에 가서 프로젝트가 올라갔나 확인해보기

만약  main이 디폴트가 아니라면
git config --global init.defaultBranch main 출력하기

불필요한 master 브랜치를 지울때
git push origin --delete master 출력 후 master 브랜치가 삭제가 됐나 확인
