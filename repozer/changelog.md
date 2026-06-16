# repozer — changelog

> 제작자: 이태원쌤 (leetaewon.com)  
> 스킬 저장소: github.com/leetaewon/claude-skills  
> 라이선스: MIT

---

## 2026-06-16-001

**CLAUDE.md + index.md 분리 구조 반영**

- 관리 대상 파일을 `CLAUDE.md` 단독에서 `CLAUDE.md` + `index.md` 두 파일로 확장
- 두 파일 독립 버전 관리 구조 도입 (`<!-- version: YYYY-MM-DD-NNN -->`)
- 실행 로직 변경: 저장소 전체 탐색 → 두 파일만 읽고 버전 비교
- 상태 판단 4가지 추가: 동기화됨 / 교체 필요 / 신규 생성 필요 / 복제본만 없음
- 신규 생성 케이스에서만 기존 저장소 탐색 로직 실행하도록 분기
- 스킬 frontmatter에 `version` 필드 추가
- 프로젝트 지식 복제본 네이밍 규칙 명시: `{저장소명}-CLAUDE.md`, `{저장소명}-index.md`

---

## 2026-05-01-001

**최초 작성**

- 정보형 저장소 분석 후 `저장소명-CLAUDE.md` 생성
- 저장소 탐색 절차 (project_knowledge_search 반복 호출)
- 정보형 / 프로세스형 판단 로직
- 상태 A (신규 생성) / 상태 B (개선 여부 판단) 분기
