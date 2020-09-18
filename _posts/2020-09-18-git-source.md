---
title: Source Tree로 GUI 환경에서 git 쉽게 쓰기
categories:
  - git
tags:
  - Source Tree
  - Linux
  - CentOS
---

![Preview](/assets/contents/2020-09-18/source_tree.png)

<br>

> 자주쓰는 git 명령어 포함

<!-- more -->

---

# Source Tree 란?

![mac](/assets/contents/2020-09-18/hero-mac-screenshot.png)

<p style="color:gray; font-size:100%;" align="center">Source Tree: git branch 관리</p>

Source Tree는 프로젝트 관리 툴 Jira로 유명한 [ATLASSIAN](https://www.atlassian.com/)에서 만든 git 관리 툴이다.

Windows / Mac OS 둘 다 지원하고 게다가 무료라서 git bash 명령어에 익숙치 않은 사용자들에게 추천하는 소프트웨어이다.

![mac](/assets/contents/2020-09-18/left_image.png)

<p style="color:gray; font-size:100%;" align="center">수정된 코드가 있다면 어디가 변경되었는지도 확인 가능</p>

단순 commit은 git bash에서, branch history나 변경된 코드를 확인할 때는 주로 Source Tree를 활용한다.
<br>

# 자주쓰는 git 명령어 정리

## basic

- git `init` : git 생성
- git clone `path` : git repository에서 가져오기
- git commit -m : commit 메시지 적기
- git push romote_name b`ranch` : add하고 commit한 코드 git server에 보내기 (git push origin master)
- git pull : git서버에서 최신 코드 받아와 merge
- git fetch : git서버에서 최신 코드 받아오기 (merge는 안함)

## branch

- git checkout `branch` : branch 선택
- git checkout -t `remote/branch` : 원격 branch 선택
- git branch `branch` : branch 생성
- git branch -r : 원격 branch 목록
- git branch -a : 로컬 branch 목록
- git branch -m branch change_branch : branch 이름 바꾸기
- git branch -d branch : branch 삭제
- git push remote_name — delete branch : 원격 branch 삭제 (git push origin — delete gh-pages)
- git add file_path : 수정한 파일 선택 (git add \*)

## restore

- git reset — soft HEAD^ : 코드는 살리고 commit만 취소
- git reset — merge : merge 취소
- git reset — hard HEAD && git pull : git 코드 강제로 모두 받아오기

## config

- git config — global user.name “user_name ” : git 계정Name 변경
- git config — global user.email “user_email” : git 계정Mail변경

## stash

- git stash / git stash save “description” : 작업코드 임시저장하고 branch 변경
- git stash pop : 마지막으로 임시저장한 작업코드 가져오기
  <br>

# Reference

- [Source Tree 공식 홈페이지](https://www.sourcetreeapp.com/)
- [자주쓰는 GIT 명령어 정리](https://thecodinglog.github.io/git/2019/06/13/git-frequently.html)
- [자주 사용하는 기초 Git 명령어 정리하기](https://medium.com/@pks2974/%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EA%B8%B0%EC%B4%88-git-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-533b3689db81)

---
