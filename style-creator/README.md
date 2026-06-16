# style-creator

나만의 문체 스킬(mystyle)을 처음부터 만들어주는 Claude 스킬.

인터뷰를 통해 사용자의 플랫폼·정체성·서사 방식·표현 선호도를 파악하고, 즉시 사용 가능한 문체 스킬 파일 세트를 자동 생성한다.

---

## 이런 상황에 사용하세요

- 나만의 글쓰기 스타일을 Claude에 반영하고 싶을 때
- `mystyle` 스킬을 처음 만들 때
- 기존 문체 스킬을 새로 교체하거나 개선하고 싶을 때
- style-creator로 생성 → 사용하면서 업데이트 → 교체하는 사이클로 운영할 때

---

## 폴더 구조

```
style-creator/
├── README.md                     ← 이 파일 (GitHub 방문자용, 스킬에 포함 안 됨)
├── SKILL.md                      ← 실행 로직 (Claude에 등록하는 파일)
├── style-creator.skill           ← 설치용 압축 파일 (SKILL.md + changelog.md + references/)
├── changelog.md                  ← 버전 히스토리
└── references/
    ├── interview.md              ← 플랫폼 선택 + 레이어별 인터뷰 질문
    ├── template.md               ← SKILL.md + 플랫폼 파일 템플릿
    └── platform-mapping.md      ← 미지원 플랫폼 처리 규칙
```

---

## 설치 방법

1. [`style-creator.skill`](https://github.com/leetaewon/claude-skills/raw/refs/heads/main/style-creator/style-creator.skill) 파일 다운로드
2. 사용자 지정 → 스킬 만들기 → 스킬 업로드 화면에서 `.skill` 파일 업로드

---

## 사용법

아래 중 하나를 말하면 자동으로 인터뷰가 시작된다.

```
"내 문체 스킬 만들어줘"
"mystyle 만들고 싶어"
"style-creator 실행해줘"
"나만의 글쓰기 스타일을 AI에 반영하고 싶어"
```

### 생성 결과물

인터뷰 완료 후 아래 파일 세트가 자동 생성된다.

```
{스킬명}/
├── SKILL.md
└── references/
    ├── {플랫폼1}.md
    ├── {플랫폼2}.md
    └── ...
```

생성된 파일을 Claude 프로젝트에 등록하면 바로 사용 가능하다.

---

## mystyle과의 관계

| | mystyle (공개용) | style-creator로 생성한 파일 |
|---|---|---|
| 내용 | 채널별 범용 문체 가이드 | 나만의 맞춤 문체 가이드 |
| 용도 | 바로 설치해서 사용 | 개인화된 스킬로 교체 |
| 업데이트 | 저장소에서 배포 | 본인이 직접 관리 |

---

## 버전

현재 버전: `2026-06-10-001`  
히스토리: [changelog.md](./changelog.md)

---

## 라이선스

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.ko)