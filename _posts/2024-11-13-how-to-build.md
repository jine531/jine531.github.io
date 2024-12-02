---
layout: post
title: "Github를 이용하여 Github.io Blog 제작하기"
description: Github에서 chirpy테마를 이용하여 blog 제작하는 포스팅입니다.

date: 2024-11-13 
last_modified_at: 2024-11-14 

categories: [Blog]
tags: [Blog, jekyll, Github, Git]

pin: true
toc: true
toc_sticky: true
published: true
---

# step 0 : 시작 전 준비할것

- 운영체제는 `Windows 64blt`를 기준으로 설명을 합니다.
- [Github](https://github.com/signup?source=login) 가입
- [Visual Studio Code](https://code.visualstudio.com/download) 
- [Git](https://git-scm.com/downloads) 설치

&nbsp;
&nbsp;

# step 1-1 : 깃허브 새로운 저장소 생성하기

1. 자신의 Repositories에 들어가서 `New`버튼을 눌러 새로운 저장소를 생성합니다.
2. Repository name은 user_name.github.io로 생성합니다.
    -자신의 user_namedms 깃허브 profile에서 확인 가능합니다.
ex) jine531.github.io
3. Public, Add a README file을 선택합니다.
4. `Create repository`를 눌러 생성합니다.

# step 1-2 : github 설정하기

1. Settings -> Pages -> Source -> Deploy form a branch 선택합니다.
2. https://user_name.github.io 접속하여 확인할수 있습니다.

# 만약 접속이 되지 않는 경우

Settings - Pages - Branch를 `main`으로 변경

&nbsp;
&nbsp;

# step 2-1 : VScode로 로컬에서 작업하기

1. 만들어진 저장소에 code버튼을 클릭 후 주소를 복사합니다.
2. VScode 열기 -> F1키 -> git clone 검색 -> Git:Clone 선택합니다.
3. 주소를 복사하고 클론할 리포지토리를 선택합니다

&nbsp;

# step 2-2 : 로컬 변경사항 적용

1. 클론한 Repository 파일을 엽니다.
2. `index.html` 파일 생성 후 아래 내용을 작성합니다.

```html
<html>
	<body>
		Hello! This is the first page!
	</body>
</html>
```

3. 좌측 `Sorce Control(소스 제어)` 메뉴 선택합니다.
4. `+` 버튼을 클릭하여 변경 사항 추가합니다.
5. 커밋 메세지 입력, 커밋 & 푸시합니다.
6. https://user_name.github.io 로 확인합니다.

&nbsp;
&nbsp;

# step 3-1 : Ruby를 이용하여 로컬 개발 환경 구축
1. [Ruby 공식 사이트](https://rubyinstaller.org/)에서 Ruby + Devkit 최신 버전을 다운로드하고 설치합니다.
2. 윈도우 키 또는 시작 버튼을 누르고 `Start Command Prompt with Ruby` 관리자 권한으로 실행합니다.
3. cd 명령어를 통해 Repository가 있는 위치로 이동합니다.
```bash
# ex)
cd C:\Users\jin54\Desktop\opsw\jine531.github.io
```

4. `jekyll, bundler, webrick` 설치합니다.

```bash
gem install jekyll bundler
gem install webrick
```

5. 아래 코드를 통해 설치를 확인합니다.

```bash
ruby -v
jekyll -v
bundler -v
```

&nbsp;
&nbsp;

# 3-2 : Jekyll 서버 구축

1. `jekyll` 생성합니다

```bash
jekyll new ./
# 또는
jekyll new ./ --force
```

2. bundle install

```bash
bundle install
```

3. 아래 코드로 Jekyll 서버를 실행하고 ```http://127.0.0.1:4000/``` 또는 ```http://localhost:4000/```에서 접속을 확인합니다.

```bash
bundle exec jekyll serve
```

&nbsp;
&nbsp;

# Step 4-1 : Jekyll 테마 적용

1. 테마 선택
[여기](http://jekyllthemes.org)에서 원하는 테마를 선택할 수 있습니다. 이 글을 Chirpy 테마를 기준으로 작성되었습니다.

2. [Chirpy GitHub 리포지토리](https://github.com/cotes2020/jekyll-theme-chirpy)에서 zip 파일로 다운로드하여 압축을 해제한 후, 로컬 리포지토리에 전부 복사합니다.

3. bundle install

```bash
bundle install
```

4. 아래 코드로 Jekyll 서버를 실행하고 ```http://127.0.0.1:4000/``` 또는 ```http://localhost:4000/```에서 접속을 확인합니다.

```bash
bundle exec jekyll serve
```

5. 좌측 `Sorce Control(소스 제어)` 메뉴 선택합니다.
6. `+` 버튼을 클릭하여 변경 사항 추가합니다.
7. 커밋 메세지 입력, 커밋 & 푸시합니다.

&nbsp;
&nbsp;

# Step 5 : Github Action 적용

1. GitHub 레포지토리의 Settings -> Pages -> Source -> `Github Actions` 선택합니다.
2. `Configure` 클릭합니다.
3. `Commit changes…` 클릭합니다.
4. 변경사항 커밋후 Vscode에서 Pull 또는 git clone 과정을 다시 수행합니다.

&nbsp;
&nbsp;

# Step 6 : Node.js 설치

1. [Node.js 공식 사이트](https://nodejs.org/)에서 최신 버전을 다운로드하고 설치합니다.

2. 2. Ruby 프롬프트에서 다음 명령어를 실행합니다.

```bash
npm install && npm run build
```

# 에러 발생시

1. `npm error code 3221225477` 
    - 해결 방법 : 프로젝트를 영문 경로로 이동
2. `npm error code ENOENT`
    - 해결 방법 : pakage.json 파일을 만들거나 들어가서 아래의 코드를 작성한 뒤 설치
    
    ```json
    { "name": "my-github-blog", "version": "1.0.0", 
    "scripts": { "build": "jekyll build", "serve": "jekyll serve" } }
    ```
    
&nbsp;
&nbsp;

# Step 7 : 최종 테마 상세 설정

1. `.gitignore` 파일 하단을 아래 코드로 수정합니다.

```
# Misc
# _sass/dist
# assets/js/dist
```

2. `_config.yml` 파일을 아래 코드로 수정합니다.

```
timezone: Asia/Seoul

url: "https://karina.github.io"

github:
  username: karina
```

3. 좌측 `Sorce Control(소스 제어)` 메뉴 선택합니다.
4. `+` 버튼을 클릭하여 변경 사항 추가합니다.
5. 커밋 메세지 입력, 커밋 & 푸시합니다.
6. https://user_name.github.io 로 확인합니다.