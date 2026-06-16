---
name: gamma-kit
version: 2026-06-16-001
description: Gamma MCP를 활용하여 콘텐츠를 제작하는 Skill. 사용자가 "Gamma로 만들어줘", "슬라이드 만들어줘", "카드뉴스 만들어줘", "전자책 만들어줘", "리드마그넷 만들어줘" 등을 요청할 때 이 Skill을 사용한다. 제작 유형에 따라 references 파일을 로드하여 적용한다.
---

# gamma-kit — Gamma 제작 스킬

Gamma MCP로 콘텐츠를 제작할 때 사용하는 스킬.
문체(어떻게 쓸 것인가)는 mystyle 스킬이 담당하고, 이 스킬은 제작(어떻게 만들 것인가)을 담당한다.

## 작동 방식

1. 사용자가 **제작 유형을 명시**하면 → 해당 references 파일을 읽고 적용
2. 유형이 **불분명**하면 → 아래 목록을 안내하고 선택을 요청
3. 콘텐츠(내용·주제)가 없으면 → 요청 후 제작
4. mystyle이 함께 필요한 유형(카드뉴스, 전자책)은 → mystyle 스킬도 같이 로드

## 제작 유형 목록

| 사용자 표현 | 로드할 파일 | mystyle 연동 |
|---|---|---|
| 강의 슬라이드, 슬라이드, 발표자료 | `references/slide.md` | 불필요 |
| 카드뉴스 | `references/card-news.md` | 필요 (card-news.md) |
| 전자책, ebook | `references/ebook.md` | 필요 (book.md) |
| 리드마그넷, 무료자료, PDF | `references/lead-magnet.md` | 불필요 |

## 파일 로드 규칙

- 제작 유형이 결정되면 **해당 파일 하나만** 읽는다
- mystyle 연동이 필요한 경우, mystyle의 해당 references 파일도 같이 읽는다
- Gamma MCP 도구는 `generate` (신규 생성) / `generate_from_template` (템플릿 기반) 중 파일에 명시된 방식을 따른다

## 공통 원칙

- 생성 후 gammaUrl을 반드시 사용자에게 공유한다
- 템플릿 ID / 테마 ID는 각 references 파일에 명시된 값을 사용하고, 임의로 변경하지 않는다

---

*gamma | Gamma 제작 스킬 | 2026-06-16-001*
