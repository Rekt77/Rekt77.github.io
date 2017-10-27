---
layout: post
title: "Github 블로그 만들기"
---



오늘은 Jekyll(정적 사이트 생성기)을 이용하여 간단히 깃허브 블로그 만들기를 포스팅 하겠습니다.

## 1. Git을 설치 한다.

![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/github_scm.png)

다운로드 링크 : [https://git-scm.com/downloads](https://git-scm.com/downloads)

**OS** 별로 다운로드를 진행하시면 됩니다.

## 2. Git Bash

Git Bash를 실행 하시고 아래 명령어를 입력합니다.
```
git config --gloabl user.email "본인 email"
git config --gloabl user.name "본인 username"
```

## 3. jekyllthemes에 접속

[http://jekyllthemes.org/](http://jekyllthemes.org/)에 접속 하여 원하는 테마를 선택한뒤 Hompage를 눌러 해당 Repository에 접속합니다.

![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/jekyll_1.png)

## 4. Theme fork

테마 Repository에서 우측 상단의 fork를 클릭하면 본인 계정에 새로운 Repository가 fork됩니다.

![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/jekyll_2.png)

## 5. Rename Repository

Repository에서 settings탭을 선택한뒤 Repository name 필드에 
본인의 ID.github.io 형식의 이름을 지정하고 rename 버튼을 클릭합니다.
![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/rename.png)

## 6. 접속확인 및 수정

블로그가 등록된 주소로 이동하여 테마가 적용되었는지 확인하고 Git bash를 통하여 아래 명령어를 입력합니다.
```
git clone https://github.com/본인ID/본인ID.github.io
cd ./본인 ID
```
clone이 완료 되면 clone 폴더에 있는 **_config.yml** 파일을 엽니다.
본인의 상황에 맞게 변수들의 내용을 변경합니다.

![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/configyml.png)

## 7. add, commit, push

Git bash에서 현재 자신의 위치가 clone된 폴더임을 확인한 후, 아래의 명령어를 입력합니다.

```
git add _config.yml
(변경된 파일이 있을시 전부 add 해주어야함. git status를 이용하면 어떤파일이 변경되었는지 알 수 있다.)
git commit -m "하고싶은말"
git push
```
아래는 설정이 완료된 페이지 입니다.

![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-How_to_make_Github_page/blogresult.png)