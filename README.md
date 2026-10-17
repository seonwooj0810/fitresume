# fitresume

기존 이력서를 채용 공고에 맞춰 조정하는 Claude Code 플러그인입니다. **사용자가 확인한 사실만** 쓰고, 공고 키워드를 억지로 끼워 넣지 않으며, 파일은 **수정안을 보여 주고 승인을 받은 뒤에만** 고칩니다.

## 설치

```
/plugin marketplace add seonwooj0810/fitresume
/plugin install fitresume --marketplace seonwooj0810/fitresume
```

로컬 개발 중에는 `claude --plugin-dir ./fitresume`로 바로 불러올 수 있습니다.

## 사용

```
/fitresume:build-tailored-resume [이력서 파일 경로]
```

"공고에 맞춰 이력서 수정", "이력서 맞춤화", "tailor my resume" 같은 말로도 실행됩니다.

## 워크플로

각 단계 끝의 GATE에서 사용자 확인을 받아야 다음으로 넘어갑니다.

| 단계 | 내용 |
|---|---|
| Stage 1 | 입력: 마스터 이력서(또는 경력 목록)와 채용 공고 |
| Stage 2 | JD 분석 (2a 회사 조사는 선택) |
| Stage 3 | 전략: 무엇을 앞세우고 무엇을 뺄지 |
| Stage 4 | 내용 조정: 선별과 순서, 재작성, 문체 점검 |
| Stage 5 | 형식 점검과 100점 만점 채점 |
| Stage 6 | 수정안 제안 |
| Stage 7 | 승인 후에만 적용과 검증 |

## 지키는 원칙

- 이력서, 사용자, 프로젝트 지침이 확인한 사실만 씁니다. 빈칸을 추론으로 채우지 않습니다.
- 두 출처가 어긋나면 임의로 고르지 않고 사용자에게 묻습니다.
- 작업 디렉터리의 `AGENTS.md`/`CLAUDE.md`가 정한 콘텐츠 규칙이 스킬 기본값보다 우선합니다.
- Word 렌더러, JSON 스키마 단계, 키워드 개수 게이트는 쓰지 않습니다.

## 구조

```
fitresume/
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── skills/build-tailored-resume/SKILL.md   # 스킬 본문
├── PRIVACY.md
├── LICENSE
└── README.md
```

## 라이선스

MIT. 자세한 내용은 [LICENSE](LICENSE)를 참고하세요.
