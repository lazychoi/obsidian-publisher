---
share: true
title: Obsidian to github pages
---

# Obsidian to github pages
created: 2022-10-06  
last modified: 

## summary
1. github template 작업
    1. [github template](https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template) 을 나의 repository로 복사
    2. github에서 직접 `mkdocs.yml` 파일 수정

![[Pasted image 20221009075847.png | 500]]
2. github Pages 설정
    1. 깃허브 페이지는 깃헙 액션으로 만들어진다. 깃허브 액션은 메인 브랜치에 적용되어 변환된 파일은 gh-pages 브랜치에 저장된다. 따라서 웹 페이지로 공개되는 브랜치를 gh-pages로 설정해야 한다.


![[Pasted image 20221006092242.png | 500 ]]
3. obsidian 안에 git submodule로 clone한다. 왜냐면, 이미 obsidian vault가 깃허브에 private repository로 등록되어 있기 때문
4. obsidian 플러그인 설치 후 설정
    1. Repo name, Github username, Github token, 
    2. Path settings >>> Obsidian Path 선택. 나머지는 그대로 둠
    3. 

## publish 실행

1. 옵시디언에서 `cmd+p` 명령 선택 후 
2. 에러 메시지는 옵시디언에서 개발자도구를 열어(opt+cmd+i) Console에서 확인 


====


1. [obsidian-publish-mkdocs](https://github.com/jobindjohn/obsidian-publish-mkdocs) 에서 초록색 'Use this template' 버튼 눌러 깃허브 페이지로 사용할 레포지토리 생성

![[Pasted image 20221006093140.png]]
- 복사할 때는 main 브랜치만 복사한다.

2. 나의 레포지토리에 가서 깃헙 페이지로 설정



3. 이 레포지토리를 pc로 clone 한다.
4. docs 폴더를 옵시디언 볼트로 지정한다.
5. docs 폴더 안에 공개하려고 하는 노트를 넣는다.
6. git commit, git push 하면 Github actions가 웹페이지를 만든다.
7. Actions 버튼을 누르면 변환 과정을 확인할 수 있다.
8. 깃헙 주소로 가면 웹페이지 볼 수 있다.


