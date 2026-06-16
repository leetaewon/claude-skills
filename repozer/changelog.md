# repozer — changelog

> 제작자: 이태원쌤 (leetaewon.com)  
> 스킬 저장소: github.com/leetaewon/claude-skills  
> 라이선스: CC BY-NC 4.0

---

## 2026-06-16-002

**복제본 출력 시 동료 파일 경로 치환 규칙 추가**

- 문제: 저장소 원본 CLAUDE.md가 `index.md`를 참조하는데, 프로젝트 지식 복제본은
  `{저장소명}-index.md`라는 이름으로 존재해 참조가 깨지는 현상 발견
  (leetaewon-contents 저장소 적용 중 발견)
- Step 2(교체·복제본 출력)에 경로 치환 규칙 추가: 본문의 `index.md`/`CLAUDE.md`
  동료 파일 참조를 `{저장소명}-index.md`/`{저장소명}-CLAUDE.md`로 치환
- 치환 대상은 동료 파일을 가리키는 인라인 코드 참조로 한정, 본문 설명은 그대로 둠
- Step 3-2(신규 생성) 고정 텍스트도 동일 표기로 수정, 저장소 원본 커밋 시
  되돌리는 방법을 별도 안내로 추가

---



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