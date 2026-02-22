---
layout: page
title: 글쓰기
description: 새로운 글을 작성하고 발행하는 방법
permalink: /write/
---

# 글쓰기 가이드

이 페이지는 이 사이트에 새 글을 추가하는 절차를 정리한 페이지입니다.

## 1) 새 포스트 파일 만들기

`_posts` 폴더에 아래 형식으로 파일을 만듭니다.

`YYYY-MM-DD-title.md`

예시:

`2026-02-22-my-new-post.md`

## 2) 기본 Front Matter 작성

```yaml
---
layout: post
title: "포스트 제목"
description: "포스트 요약"
image:
  path: /assets/img/main_img2.JPG
---
```

## 3) 본문 작성

Front Matter 아래에 Markdown으로 본문을 작성합니다.

## 4) 발행

아래 순서로 커밋 후 푸시하면 GitHub Pages에 반영됩니다.

```bash
git add -A
git commit -m "Add new post"
git push
```
