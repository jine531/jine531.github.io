---
layout: post
title: "Github Blog에 댓글 기능 추가하기"
description: Github Blog에 utterances를 댓글 기능을 추가하는 포스팅입니다.

date: 2024-11-16 
last_modified_at: 2024-11-16 

categories: [Blogging, Tutorial]
tags: [Blog, utterances, chirpy, Git]

pin: true
toc: true
toc_sticky: true
published: true
---

# step 0 : 시작 전 준비할것
&nbsp;

댓글 기능을 추가할 자신의 github.io blog가 필요합니다!
자신의 github.io blog가 없다면 [이 포스팅](https://jine531.github.io/posts/how-to-build/)을 참고하여주세요!

# step 1 : utterances 설치
&nbsp;

1. [Utterances site](https://github.com/apps/utterances)에 접속합니다
&nbsp;
2. 오른쪽 ```configure``` 클릭합니다
![configure](/assets/img/configure.png)
&nbsp;
3. 적용할 ```repository``` 선택합니다
![repository](/assets/img/repository.png)
&nbsp;
4. ```only select repository```를 선택합니다
![select](/assets/img/select.png)
&nbsp;
5. ```select repository```에서 자신의 githubio 레포지토리 주소를 선택합니다

# step 2 : utterances 설정
&nbsp;

1. [Utterances](https://utteranc.es/)에 접속합니다 
&nbsp;
2. repo에 자신의 Repository를 등록합니다
![repo](/assets/img/repo.png)
&nbsp;
3. Enable Utterances에 생긴 코드를 복사하고 _layout/post.html에 붙여넣습니다
&nbsp;
4. _config.yml을 수정해줍니다
``` yml
comments:
  # Global switch for the post-comment system. Keeping it empty means disabled.
  provider: utterances
  # The provider options are as follows:
  disqus:
    shortname: # fill with the Disqus shortname. › https://help.disqus.com/en/articles/1717111-what-s-a-shortname
  # utterances settings › https://utteranc.es/
  utterances:
    repo: choi-day/choi-day.github.io
    issue_term: pathname
```
- 1. provider를 utterances로 변경
- 2. repo에 ```git id/repository``` 입력
&nbsp;
5. 저장후 psuh하기

# step 3 : 확인하기
자신의 블로그에 들어가 확인해봅시다
![comment](/assets/img/comment.png)







