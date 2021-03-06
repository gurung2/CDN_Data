<!-- more -->
hexo와 github page를 이용하여 만든 블로그에 아름다움을 입혀보자. hexo는 jeykyll과 마찬가지로 블로그에 테마를 입힐 수 있다. hexo와 github page에 테마를 입히는데 어려움은 없지만 테마가 개발자 개개인이 오픈소스로 만들어 제공하기 때문에 테마마다 사용이나 설정법이 약간 다를 수 있다.
<!-- more -->

<!-- excerpt -->
<!-- excerpt -->

`hexo`와 `github page`를 이용하여 만든 블로그에 아름다움을 입혀보자. `hexo`는 `jeykyll`과 마찬가지로 블로그에 테마를 입힐 수 있다. `hexo`와 `github page`에 테마를 입히는데 어려움은 없지만 테마가 개발자 개개인이 오픈소스로 만들어 제공하기 때문에 테마마다 사용이나 설정법이 약간 다를 수 있다. 

`hexo`와 `github page`에 테마를 입히는 것이 `hexo`와 `github page`를 사용하여 블로그를 구축하는 것보다 어려울 수 있다. 일단 **Document가 한글이 아니기 때문**인데 먼저 이 포스트에서 하나의 테마를 잡아 적용을 해보고 원하는 테마를 골라서 별도로 적용해보자. 

- - -

## Hexo 테마 선택하기

먼저 테마가 어떤 것들이 있는지 살펴보자.
[Hexo Theme](https://hexo.io/themes/index.html)에서 개발자들이 `hexo`를 사용하여 만든 테마 목록을 확인하고 다운받을 수 있다. 물론 우리들도 `hexo` 테마를 제작할 수 있다. 당연히 `시간`과 `노오오오오오오력`이 바탕이 되어야 한다. `hexo`자체가 대만 개발자가 개발한 프레임워크이기 때문에 중국어로 되어있는 테마를 볼 수 있다. 그런거는 그냥 패스하는 것이 정신건강에 좋을 듯 하다.

대충 둘러보면 알겠지만 그저 그런 테마들이 아니다. 모두 개인의 `Identity`가 들어가 있는 디자인들 뿐만 아니라 더 나아가 `반응형 디자인`으로 제작되어 있다. 이 `반웅형 디자인`으로 인해 우리는 하나의 페이지를 모바일에서 볼 때와 데스크 탑 브라우저에서 볼 때 모두 다른 형태의 UI, UX로 보이는 것이다. 훌륭하다. 우린 그저 가져다 쓰기만 하면 된다.

이 훌륭한 테마들 중 우리는 [Clean Blog](http://www.codeblocq.com/assets/projects/hexo-theme-clean-blog/)를 선택하고 적용해 보자. 이 [Clean Blog](http://www.codeblocq.com/assets/projects/hexo-theme-clean-blog/)는 매우 깔끔한 디자인을 가지고 있고 `jekyll`에서도 지원하는 블로그 테마이다. 

## Hexo 테마 설치하기

처음에 말했듯이 테마들은 모두 오픈소스로 되어있다. 그리고 그 오픈소스들은 `github`에 올려져있다. 우리는 [Hexo와 Github Page로 시작하는 블로그 만들기](https://kdydesign.github.io/2017/06/23/start-hexo-blog/)에서 블로그를 구축하며 대충 배워 본 `git`과 `github`사용 방법을 통해 테마 역시 `github`에서 `git`을 통해 다운 받을 것이다.

[Clean Blog Github](https://github.com/klugjo/hexo-theme-clean-blog)에 가보면 `Clean Blog`를 적용하는데 필요한 프로젝와 적용 방법과 기타 기능들에 대한 설명이 나와있다. 여기만 잘 읽고 따라하면 문제없이 적용이 된다. 물론 영어지만.

이제 진짜로 설치해보자.
이전에 [Hexo와 Github Page로 시작하는 블로그 만들기](https://kdydesign.github.io/2017/06/23/start-hexo-blog/) 포스팅에서 만들어 놓은 폴더 경로로 이동하자. 해당 폴더에 가면 `themes`라는 폴더가 존재할 것이다. 이 `themes` 경로로 가보면 처음에 `hexo` 블로그를 만들 때 기본으로 적용되는 `landscape`테마가 있다. 과감하게 삭제하지말고 혹시 모르니 폴더 전체를 백업해 놓자. 그리고 `themes` 경로에서 `마우스 우클릭`을 눌러 `Git Bash Here`메뉴를 클릭하자. 이후에 실행되는 `git bash`창에 명령어를 입력하여 `github`에 있는 소스를 다운받자.

```bash
$ git clone https://github.com/klugjo/hexo-theme-clean-blog.git
```

또는 [Clean Blog Github](https://github.com/klugjo/hexo-theme-clean-blog)에서 우측 상단에 `Clone or download`버튼을 통해 zip 압축파일로 다운받을 수 있다.

다운을 받게되면 `themes`경로 안에 `hexo-theme-clean-blog`라는 폴더가 생성되었을 것이다. 이 폴더 명을 `clean-blog`로 변경해 주자.

### 테마 소스 구조 살펴보기

잠깐 테마의 소스들이 어떻게 구성되어있는지 보자. 

|File|Description|
|---|---|
|layout|blog를 구성하는 파일|
|source|blog 구성에 필요한 리소스 파일|
|_config.yml|해당 테마의 설정 파일|

대표적인 파일을 보게 되면 `layout`, `source`, `_config.yml`이다. 이 세개의 파일들은 대부분의 테마들이 가지고 있으며 `_config.yml`의 경우는 필수이다. `hexo`블로그를 구성하는 설정파일 역시 `_config.yml`파일이다. 두 파일을 혼돈해서는 안된다.

## 테마 설정하기
우리는 `themes/clean-blog`경로에 있는 `_config.yml`을 수정하여 메뉴, 블로그 타이틀 등 블로그를 구성하는 내용들을 변경할 수 있다. `_config.yml`을 열어 원하는 내용대로 수정하자. 설정파일의 내용은 대충 아래를 보자.

```yaml
# Header
menu:
  Home: /                               #메인 페이지 경로 
  Archives: /archives                   #Archives 메뉴 경로
  Tags: /tags                           #tags 메뉴 경로
  Categories: /categories               #categories 메뉴 경로
  Github:
    url: https://github.com/klugjo/hexo-theme-clean-blog             #사용자 github url                      
    icon: github               #github icon

# Title on top left of menu. Leave empty to use main blog title
menu_title: Configurable Title          #좌측 상단 메뉴 타이틀

# URL of the Home page image
index_cover: http://www.codeblocq.com/assets/projects/hexo-theme-clean-blog/img/home-bg.jpg       #커버 이미지 경로

# Default post title
default_post_title: Untitled             #포스트 생성 시 기본 타이틀

# Comments. Choose one by filling up the information
comments:
  # Disqus comments
  disqus_shortname:
  # Facebook comments
  facebook:
    appid:                #사용자 facebook app id
    comment_count: 5
    comment_colorscheme: light

# Google Analytics Tracking ID
google_analytics:         #사용자 google analytics id

# Addthis ID
addthis:                  #사용자 addthis id

# set your own favicon
favicon:                  #브라우저 탭에 표시된 favicon 이미지 경로

# Social Accounts
twitter_url:              #사용자 twitter url
twitter_handle:
facebook_url:             #사용자 facebook url
github_url: https://github.com/klugjo/hexo-theme-clean-blog         #사용자 github url
gitlab_url:               #사용자 gitlab url
linkedin_url:             #사용자 linkin url
mailto:                   #사용자 메일
```

여기까지가 `hexo clean-blog`에 대한 설정이고 이제 브로그 자체의 설명을 변경해 보자.
블로그가 존재하는 최상위 폴더로 이동해서 `hexo`블로그의 설정파일인 `_config.yml`을 열어 수정하자.

```yaml
# Site
title: title                   #블로그 메인 타이틀 입력
subtitle: subtitle             #블로그 서브 타이틀 입력
description: description       #블로그 설명 
author: author                 #블로그 관리자 이름
language: en                   #블로그 언어(한국어 지원은 없으므로 en인 영어로 하자.)
timezone:

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: https://[계정이름].github.io
```

## Tags 페이지 만들기
`Tags` 페이지를 만들어 `tag`들을 관리하자. `tags` 페이지는 `post`를 작성할 때와 비슷한 명령어를 사용한다. 우리는 페이지를 만들 것이기 때문에 `post`가 아닌 `page`를 사용하면 된다.

```bash
$ hexo new page "tags"
```

`page`를 생헝하게 되면 `source`경로에 `tags`라는 폴더가 생기고 `index.md`라는 `markdown`파일이 생성된다. 이 `index.md` 파일을 열어 아래와 같이 수정하고 저장하다.

```yaml
---
title: All tags
type: "tags"
---


## Catetories 페이지 만들기
```
`Categories`페이지도 `Tags`페이지와 동일하게 만들면 된다.

```bash
$ hexo new page "categories"
```

```yaml
---
title: All tags
type: "categories"
---

## Post 쓰기

이제 어느 정도 테마의 설정이 끝났다. 이제 실제로 포스트를 써보록 하자.

```yaml
$ hexo new post "post-clean-blog"
```

`post`파일을 생성하고 수정하자.

```yaml
---
title: "Clean-blog 테마를 적용하다."          #post 제목
date: 2017-07-07 00:23:23                     #post 생성 날짜
tags: ["hexo", "clean-blog", "theme"]         #tags
cover: /assets/contact-bg.jpg                 #post 커버 이미지
subtitle: "처음으로 테마를 적용해보다."       #post 부제
---
```

`post`를 작성하는 `md`파일에서 상단에 들어가는 `post`와 관련된 설정값들이다. 적당하게 입력하도록 한다.

## 테마 적용하기

`hexo`테마인 `clean-blog`를 다운받았으면 이제 실제로 `hexo`블로그에서 이 테마를 사용하겠다는 언급을 해줘야한다. 블로그 최상위 폴더로 이동하여 `_config.yml`파일을 열어 아래처럼 수정하자.

```yaml
# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: clean-blog
```

그 다음 `hexo` 명령어를 통해 다시 `markup`으로 변환하고 로컬에서 확인해 보자. `hexo server`포트는 4000번이므로 [http://localhost:4000](http://localhost:4000)으로 접속하자.

```bash
$ hexo g
$ hexo server
```

- - -
`hexo`가 `jekyll`보다는 많은 테마를 제공하지는 않지만 그래도 나름대로의 깔끔한 테마들이 넘치기에 테마를 적용하는데는 문제가 없다. 다만 그 테마를 적용하기 위해서는 테마의 설정파일은 `_config.yml`을 다룰 줄 알아야하고 그 테마의 Document를 봐야한다. 물론 영어라 파악하기가 쉽지만은 않겠지만(난 그렇다.ㅠㅠ) 내가 원하는 테마를 처음에 구축해 놓으면 그 이후부터 포스팅은 `복붙`이기에 어렵지 않게 느낄 것이다.