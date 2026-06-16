# idea

주제를 입력하면 각도가 다른 콘텐츠 아이디어를 다수 생성하는 Claude 스킬.

타깃 독자와 채널을 자동으로 파악하고, 겹치지 않는 각도로 아이디어를 제안한다.

---

## 이런 상황에 사용하세요

- 콘텐츠 주제는 있는데 어떤 각도로 쓸지 막힐 때
- 같은 주제를 다양한 채널에 맞게 변형하고 싶을 때
- 최근 다룬 주제와 겹치지 않는 아이디어가 필요할 때

---

## 폴더 구조

```
idea/
├── README.md     ← 이 파일 (GitHub 방문자용, 스킬에 포함 안 됨)
├── SKILL.md      ← 실행 로직 (Claude에 등록하는 파일)
├── idea.skill    ← 설치용 압축 파일 (SKILL.md + changelog.md)
└── changelog.md  ← 버전 히스토리
```

---

## 설치 방법

1. [`idea.skill`](https://raw.githubusercontent.com/leetaewon/claude-skills/main/idea/idea.skill) 파일 다운로드
2. 사용자 지정 → 스킬 만들기 → 스킬 업로드 화면에서 `.skill` 파일 업로드

---

## 사용법

```
/idea                              → 주제·채널 질문 후 아이디어 생성
/idea [주제]                       → 채널만 확인 후 바로 생성
/idea [주제] | 독자: [직접 입력]   → 프로젝트 지식 무시하고 지정 독자로 생성
/idea help                         → 사용법 표시
```

---

## 버전

현재 버전: `2026-06-01-001`  
히스토리: [changelog.md](./changelog.md)

---

## 라이선스

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)