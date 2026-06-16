# repozer

정보형 GitHub 저장소의 `CLAUDE.md`와 `index.md`를 관리하는 Claude 스킬.

버전 비교로 변경된 파일만 교체하고, 파일이 없으면 신규 생성한다.

---

## 이런 상황에 사용하세요

- GitHub 저장소를 Claude 프로젝트 지식에 연결해서 사용 중인 경우
- 저장소 파일이 바뀔 때마다 프로젝트 지식 복제본을 수동으로 교체하기 번거로울 때
- 새 저장소에 `CLAUDE.md`와 `index.md`를 처음 만들 때

---

## 폴더 구조

```
repozer/
├── README.md        ← 이 파일 (GitHub 방문자용, 스킬에 포함 안 됨)
├── SKILL.md         ← 실행 로직 (Claude에 등록하는 파일)
├── repozer.skill    ← 설치용 압축 파일 (SKILL.md + changelog.md)
└── changelog.md     ← 버전 히스토리
```

---

## 설치 방법

1. [`repozer.skill`](https://raw.githubusercontent.com/leetaewon/claude-skills/main/repozer/repozer.skill) 파일 다운로드
2. 사용자 지정 → 스킬 만들기 → 스킬 업로드 화면에서 `.skill` 파일 업로드

---

## 사용법

```
/repozer [저장소명]
```

예시:
```
/repozer leetaewon-brand
/repozer leetaewon-contents
/repozer leetaewon-wiki
```

---

## 버전

현재 버전: `2026-06-16-001`  
히스토리: [changelog.md](./changelog.md)
