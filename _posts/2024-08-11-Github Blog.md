---
layout: single
title: "Github Blog (with Minimal Mistakes)"
categories: Github
tag: [Github Blog, Minimal Mistakes, Jekyll Theme]
toc: true
---

# 실시간 모니터링

문제: 

- 블로그 수정 시, 실시간으로 빠르게 변경 사항을 확인하고 싶다

해결:

- Ruby로 서버를 열어, 로컬 호스트로 실시간 변경사항 모니터링
- `bundle exec jekyll serve`
- [localhost:4000](http://localhost:4000) 접속

---

# _config.yml

- `_config.yml`파일로 웹 페이지의 기본적인 세팅을 수정해 줄 수 있다.
- 자세한 것은 아래 “Minimal Mistakes” 문서 참고

---

# Comments

- disqus로 댓글을 설정 해줌 → 추가적인 기능이 있는데 유료임
    - 관리는 disqus 웹사이트에서 할 수 있다

→ 추가적인 무료이면서 좋은 것이 필요할 듯

---
# Category & Tag

하나의 카테고리, 여러 개의 태그

- 예시:
    - 카테고리: coding
    - 태그: python, c++, java, etc…

`_pages/category-archive.md`

- 카테고리 레이아웃 설정 → `_data/navigation.yml`파일 설정할 때, `_pages/category-archive.md` 파일에 설정한 목록들을 매핑해야됨
    - Title 등

`_data/navigation.yml`

- 네비게이션 바 설정
- API 설계 느낌

`_psts/페이지.md`

- 예시:

```
---
layout: single
title: "첫 포스팅 (테스트)"
categories: test
---
```
---

# 404 Page
깃헙 블로그에서 없는 페이지로 이동을 하였을 때 (url 입력으로), Not Found 페이지를 띄우는 데, 매우 안 이쁘다.
- 404 Page를 만들어주자 $\rightarrow$ `_pages/404.md`에서 설정 해줄 수 있다.
- `hengyinayo/카테고리/없는페이지`여야지 반영되고, `hengyinayo/카테고리/태그/없는페이지`면 반영이 되지 않는다.

---
Reference:

https://www.youtube.com/watch?v=--MMmHbSH9k&list=PLIMb_GuNnFwfQBZQwD-vCZENL5YLDZekr&index=2

https://mmistakes.github.io/minimal-mistakes/