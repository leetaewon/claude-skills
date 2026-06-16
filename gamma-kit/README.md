# gamma-kit

Gamma MCP를 활용해 콘텐츠를 제작하는 Claude 스킬.

슬라이드, 카드뉴스, 전자책, 리드마그넷 등 제작 유형에 따라 references 파일을 자동으로 로드하여 적용한다.

---

## 이런 상황에 사용하세요

- Gamma로 강의 슬라이드나 발표자료를 만들 때
- 카드뉴스, 전자책, 리드마그넷을 Gamma로 제작할 때
- mystyle 스킬과 연동하여 나만의 문체가 적용된 콘텐츠를 만들 때

---

## 폴더 구조

```
gamma/
├── README.md              ← 이 파일 (GitHub 방문자용, 스킬에 포함 안 됨)
├── SKILL.md               ← 실행 로직 (Claude에 등록하는 파일)
├── gamma-kit.skill            ← 설치용 압축 파일 (SKILL.md + changelog.md + references/)
├── changelog.md           ← 버전 히스토리
└── references/
    ├── slide.md           ← 강의 슬라이드 제작 가이드
    ├── card-news.md       ← 카드뉴스 제작 가이드
    ├── ebook.md           ← 전자책 제작 가이드
    └── lead-magnet.md     ← 리드마그넷 제작 가이드
```

---

## 설치 방법

1. [`gamma-kit.skill`](https://raw.githubusercontent.com/leetaewon/claude-skills/main/gamma-kit/gamma-kit.skill) 파일 다운로드
2. 사용자 지정 → 스킬 만들기 → 스킬 업로드 화면에서 `.skill` 파일 업로드

---

## 사용법

제작 유형을 명시하면 자동으로 해당 references 파일을 로드한다.

```
"슬라이드 만들어줘"
"카드뉴스 만들어줘"
"전자책 만들어줘"
"리드마그넷 만들어줘"
"Gamma로 만들어줘"
```

---

## 테마·템플릿 ID 적용 (선택)

기본 상태로도 바로 사용 가능하다. Gamma 기본 테마가 자동으로 적용된다.

본인의 Gamma 테마나 템플릿을 적용하고 싶으면 `references/` 파일을 열어 해당 항목에 ID를 추가하면 된다.

```
themeId | (없음 — Gamma 기본 테마 적용. 본인 테마 ID 있으면 여기에 추가)
```

Gamma 테마 ID 확인: Gamma 앱 → Brand → Themes → 사용할 테마 선택 → URL의 ID 값

---

## mystyle 스킬과 연동

카드뉴스, 전자책 제작 시 mystyle 스킬이 함께 있으면 자동으로 연동된다.

→ [mystyle 스킬 보기](../mystyle/)

---

## 버전

현재 버전: `2026-06-16-001`  
히스토리: [changelog.md](./changelog.md)

---

## 라이선스

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)