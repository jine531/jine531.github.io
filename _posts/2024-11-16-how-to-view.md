---
layout: post
title: "Github Blog 방문자 조회수 설정하기"
description: 내 Github Blog를 몇 명이 조회 하였는지 알 수있는 기능을 추가하는 포스팅입니다.

date: 2024-11-16 
last_modified_at: 2024-11-16 

categories: [Blog]
tags: [Blog, chirpy, Git]
author: jine

pin: true
toc: true
toc_sticky: true
published: true
---

# step 0 : 시작 전 준비할것
&nbsp;

조회수 기능을 추가할 자신의 github.io blog가 필요합니다!
자신의 github.io blog가 없다면 [이 포스팅](https://jine531.github.io/posts/how-to-build/)을 참고하여주세요!

&nbsp;
# step 1 : GoatCounter 가입하기
1. [GoatCounter](https://www.goatcounter.com/)에 접속합니다
2. ```Sign up``` 클릭
![Goat1](https://github.com/user-attachments/assets/27c13047-9780-4427-9bc5-b44e72974248)
3. 회원가입을 진행하며 알맞게 채워주면 됩니다
- Code : 자신만의 코드, ```https://mycode.goatcounter.com/```형식으로 채우면 됩니다
- Site domain : 자신의 블로그 주소, ex : ```jine531.github.io```
- Email address : 인증할 이메일 주소
- Password : 8자리 이상의 비밀번호
- Fill in 9 here : 로봇인시 검사, ```9```라고 적으면 됩니다
![Goat 2](https://github.com/user-attachments/assets/7ef9c701-b483-44ca-88e8-e1e7191822b5)
4. 이메일 인증을 해줍니다

&nbsp;
# step 2 : 설정하기
1. 자신의 goatcounter로 접속 ex) jine531.goatcounter.com
2. 우측 위 Settings 선택
![Goat3](https://github.com/user-attachments/assets/156afb27-9d8e-43a0-8901-f2a884fd926e)
3. ```Allow adding visitor counts on your website``` 체크하기
![Goat4](https://github.com/user-attachments/assets/9006cd8a-5452-4805-a46a-d7cdf32295f5)
4. 아래 Save하면 끝

&nbsp;
# step 3 : 내 _config.yml 수정하기
1. 자신의 ```_config.yml``` 파일에 접속
2. ```goatcounter```의 ```id```를 자신의 코드로 변경
```yml
...
  google:
    id: # fill in your Google Analytics ID
  goatcounter:
    id: jin543131
  umami:
    id: # fill in your Umami ID
    domain: # fill in your Umami domain
...
```
3. ```pageviews```의 ```provider```를 goatcounter로 변경
```yml
...
pageviews:
  provider: goatcounter
...
```
4. 저장후 push하기
5. 결과확인
![Goat5](https://github.com/user-attachments/assets/00c62c84-232b-4878-a08b-b6277b9a9b42)