# 전자책(ebook) 제작 가이드

## mystyle 연동

전자책 제작 시 mystyle의 `references/book.md`를 함께 로드하여 문체 가이드를 적용한다.

## Gamma 설정

| 항목 | 값 |
|---|---|
| 제작 방식 | `generate` |
| design_type | `document` |
| themeId | (없음 — Gamma 기본 테마 적용. 본인 테마 ID 있으면 여기에 추가) |
| templateId | (없음 — 전용 템플릿 있으면 여기에 추가하고 제작 방식을 `generate_from_template`으로 변경) |
| 언어 | `ko` |
| dimensions | `a4` or `letter` |

## 전자책 구성 원칙

- 분량: 10~30페이지 권장 (리드마그넷 성격이면 너무 두껍게 하지 않음)
- 챕터 수: 3~5개
- 1챕터당 핵심 개념 1개 + 독자 적용 지점 1개
- 마지막 챕터 or 페이지에 다음 단계 CTA 포함

## 전자책 구조

```
표지 — 제목 + 부제 + 저자명
→ 들어가며 — 이 책을 쓰게 된 계기 (가볍게)
→ 챕터 1~N — 개념 → 경험 → 독자 적용 지점
→ 마무리 — 핵심 정리 + 다음 단계 CTA
```

## Gamma 생성 시 inputText 작성 요령

- 챕터별 제목 + 핵심 내용을 정리해서 전달
- textMode: `generate` (아웃라인 기반으로 확장)
- 이미지 소스: `aiGenerated` or `placeholder`
- textOptions.amount: `detailed` (전자책은 텍스트 밀도가 높아야 함)

## 주의사항

- "이 책에서는 ~를 다룹니다" 교재형 선언 금지
- 핵심 정리 박스 과용 금지
- 검증 안 된 내용은 "아직 해보지 않았지만" 명시
- 마지막에 반드시 다음 단계 CTA 포함
