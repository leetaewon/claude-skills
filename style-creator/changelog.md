# style-creator — changelog

> 제작자: 이태원쌤 (leetaewon.com)  
> 스킬 저장소: github.com/leetaewon/claude-skills  
> 라이선스: MIT

---

## 2026-06-10-001

**v1.1 — 플랫폼 매핑 로직 추가**

- 미지원 플랫폼 처리를 위한 `references/platform-mapping.md` 추가
- 플랫폼 3개 이상 선택 시 우선순위 안내 로직 추가
- 스킬 이름 커스텀 기능 추가 (기본값: `mystyle`)

---

## 2026-06-01-001

**v1.0 — 최초 작성**

- 인터뷰 기반 문체 스킬 자동 생성기
- 생성 흐름: 스킬 이름 확인 → 플랫폼 선택 → 인터뷰(레이어 1~3) → 파일 생성
- 결과물: `SKILL.md` + 플랫폼별 `references/*.md` 세트
- `references/interview.md` — 레이어별 인터뷰 질문
- `references/template.md` — 생성 파일 템플릿
