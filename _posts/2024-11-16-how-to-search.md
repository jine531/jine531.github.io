---
layout: post
title: "Github Blog 검색 노출시키기"
description: 내 Github Blog를 Goolgle과 Naver에 노출시키는 포스팅입니다.

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

# Naver 검색 노출하기!
&nbsp;
## step 1 : Naver seaerch advisor 사용하기
1. [Naver Search Advisor](https://searchadvisor.naver.com/)에 접속합니다
2. ```웹마스터 도구 사용하기``` 클릭
![naver1](https://github.com/user-attachments/assets/a69746f0-4358-423a-a36b-552a7cbc6cdc)
3. 자신의 블로그 주소를 등록합니다
![naver2](https://github.com/user-attachments/assets/d0289369-aaed-4808-b925-bb75740e94da)


&nbsp;
## step 2 : 소유권 학인하기
1. ```HTML 태그``` 선택하고 복사하기
![naver3](https://github.com/user-attachments/assets/ac3f35a5-2d89-4d12-9b77-aa5d369bf0b9)
2. ```HTML_includes의 head.html``` 파일 열기
3. 아무곳에나 복사하기
4. 저장후 push하기

&nbsp;
## step 3 : 사이트맵 제출하기
1. 왼쪽 메뉴의 요청 사이트맵 선택
2. 사이트맵 제출의 자신의 **블로그주소.sitemap.xml** 입력하기
![naver4](https://github.com/user-attachments/assets/2e553ef1-bafe-41e5-9480-a2114a3640b8)

&nbsp;
[참고사이트](https://jaehee-kim24.github.io/posts/github%EB%B8%94%EB%A1%9C%EA%B7%B8_%EA%B2%80%EC%83%89%EB%85%B8%EC%B6%9C%ED%95%98%EA%B8%B0_naver/)

&nbsp;
&nbsp;
# Google 검색 노출하기!
&nbsp;
## step 1 : Google seaerch console 사용하기
1. [Google Search Console](https://search.google.com/search-console/about)에 접속합니다
2. 시작하기 클릭
![google1](https://github.com/user-attachments/assets/6a6a3915-edcf-49e6-9c4e-dbd95638ae7d)
3. URL 접두어 선택하고 블로그 주소 등록
![google2](https://github.com/user-attachments/assets/945cad4f-b21a-44eb-b821-ae38744c479e)

&nbsp;
## step 2 : 소유권 학인하기
1. HTML 태그 선택하고 content 안의 내용을 복사 하기
![google3](https://github.com/user-attachments/assets/1e3c9446-495b-4c6e-835f-47d88d250b11)
2. ```_config.yml``` 파일에 들어가기
3. google 뒤 content 뒷부분 붙여넣기
```
webmaster_verifications:
  google: 복사한 부분
  bing: # fill in your Bing verification code
  alexa: # fill in your Alexa verification code
  yandex: # fill in your Yandex verification code
  baidu: # fill in your Baidu verification code
  facebook: # fill in your Facebook verification code
```
4. 저장후 push하기
5. 사이트에서 성공 확인하기
![google4](https://github.com/user-attachments/assets/c4dae14b-e820-4bf0-ad31-5579fd471bed)

&nbsp;
## step 3 : 사이트맵 제출하기
1. 왼쪽 메뉴의 Sitemaps 클릭하기
2. 새 사이트맵 추가에 **자신의 주소/sitemap.xml** 입력하기
![google5](https://github.com/user-attachments/assets/fbdda082-2dc6-4543-9f38-f5f9181eb7f1)

&nbsp;
&nbsp;
[참고사이트](https://jaehee-kim24.github.io/posts/github%EB%B8%94%EB%A1%9C%EA%B7%B8_%EA%B2%80%EC%83%89%EB%85%B8%EC%B6%9C%ED%95%98%EA%B8%B0/)
