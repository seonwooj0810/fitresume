# 개인정보 처리방침

**최종 업데이트: 2026년 4월 7일**

## 개요

`fitresume` Claude Code 플러그인(이하 "플러그인")은 전적으로 사용자의 로컬 컴퓨터에서 실행됩니다. 개인 데이터를 수집하거나 외부 서버로 전송하거나 저장하지 않습니다.

## 처리되는 데이터

플러그인을 사용할 때 다음 데이터는 사용자의 컴퓨터에만 남습니다.

- 마스터 이력서(사용자가 입력으로 제공)
- 채용 공고(사용자가 입력으로 제공)
- 생성된 맞춤 이력서 JSON 및 .docx 출력 파일

## 하지 않는 일

- 이력서나 채용 공고의 어떤 데이터도 수집하지 않습니다.
- 이력서나 개인정보를 어떤 제3자 서비스로도 전송하지 않습니다.
- 어떤 종류의 분석, 추적, 원격 측정(telemetry)도 사용하지 않습니다.
- 입력이나 출력을 저장하거나 기록하지 않습니다.

## Claude / Anthropic

이 플러그인은 Claude Code 스킬로 실행됩니다. `/build-tailored-resume`를 호출하면 이력서와 채용 공고가 사용자의 로컬 Claude Code 세션에서 진행되는 대화 컨텍스트의 일부로 Claude(Anthropic의 AI)에 전달됩니다. Claude가 해당 데이터를 처리하는 방식은 Anthropic의 개인정보 처리방침을 따릅니다.

https://www.anthropic.com/privacy

## 서드파티 의존성

플러그인은 다음 오픈소스 Python 라이브러리를 로컬에서 사용합니다.

- [python-docx](https://python-docx.readthedocs.io/) — DOCX 생성
- [lxml](https://lxml.de/) — XML 처리

두 라이브러리 모두 데이터를 외부로 전송하지 않습니다.

## 문의

이 개인정보 처리방침에 관한 문의는 다음 주소에서 이슈를 등록해 주세요.
https://github.com/seonwooj0810/fitresume/issues
