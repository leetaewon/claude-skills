# mystyle

채널별 일반적인 작법 원칙에 맞게 글을 작성하는 Claude 스킬.

매체를 명시하면 해당 references 파일을 자동으로 로드하여 적용한다.
이 스킬은 채널 관례(분량, 구조, 격식 수준)만 담은 **범용 가이드**다. 특정한 어투나 말버릇을 강제하지 않는다.

---

## 이런 상황에 사용하세요

- 채널별 글쓰기 관례(분량, 구조)를 참고해서 쓰고 싶을 때
- 페이스북, 뉴스레터, 블로그 등 매체마다 다른 작법으로 쓰고 싶을 때
- style-creator로 나만의 문체를 만들기 전, 기본 틀로 사용하고 싶을 때

---

## 폴더 구조

```
mystyle/
├── README.md              ← 이 파일 (GitHub 방문자용, 스킬에 포함 안 됨)
├── SKILL.md               ← 실행 로직 (Claude에 등록하는 파일)
├── mystyle.skill          ← 설치용 압축 파일 (SKILL.md + changelog.md + references/)
├── changelog.md           ← 버전 히스토리
└── references/
    ├── newsletter.md      ← 뉴스레터 작법 가이드
    ├── facebook.md        ← 페이스북 작법 가이드
    ├── linkedin.md        ← 링크드인 작법 가이드
    ├── blog-naver.md      ← 네이버 블로그 작법 가이드
    ├── blog-brunch.md     ← 브런치 작법 가이드
    ├── card-news.md       ← 카드뉴스 작법 가이드
    ├── youtube.md         ← 유튜브 작법 가이드
    └── book.md            ← 책 집필 작법 가이드
```

---

## 설치 방법

1. [`mystyle.skill`](https://raw.githubusercontent.com/leetaewon/claude-skills/main/mystyle/mystyle.skill) 파일 다운로드
2. 사용자 지정 → 스킬 만들기 → 스킬 업로드 화면에서 `.skill` 파일 업로드

---

## 사용법

매체를 명시하면 자동으로 트리거된다.

```
"페이스북 포스팅 써줘"
"뉴스레터로 작성해줘"
"네이버 블로그용으로 써줘"
"내 스타일로 써줘"
```

---

## 나만의 문체로 발전시키기

이 스킬은 채널 관례만 담은 범용 출발점이다.
**style-creator** 스킬로 인터뷰 기반 맞춤 문체를 만들면, 이 스킬을 교체해서 개인화할 수 있다.

→ [style-creator 스킬 보기](../style-creator/)

---

## 버전

현재 버전: `2026-06-16-001`  
히스토리: [changelog.md](./changelog.md)
