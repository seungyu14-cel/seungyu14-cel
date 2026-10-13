# SPORTS SISEON — 근거를 확인하는 콘텐츠 제작

[프로필로 돌아가기](../README.md) · [저장소](https://github.com/seungyu14-cel/Sports-Card-New)

## 목적

스포츠 자료를 인스타그램 카드뉴스로 가공하면서 원문의 수치·선수명·경기 정보를 유지하고, 생성 결과에 대한 검수 절차를 만드는 개인 프로젝트입니다.

## 제작 구조

1. MD 업로드 또는 붙여넣기로 제작 원문 입력
2. 원문 구간에서 사용할 근거 선택
3. Ollama를 활용한 카드별 문구 작성
4. 역할별 기준과 근거에 따라 검토
5. 결과 PNG와 검토 자료 출력

KBO 제작 경로에는 LangChain 근거 검색과 LangGraph 카드별 검수·수정 구조가 문서화되어 있습니다. 이 구조를 모든 리그에서 동일하게 검증한 것으로 확대해 설명하지 않습니다.

## 검증과 개선

- 모델이 원문에 없는 근거를 반환하는 문제를 다룹니다.
- 마크다운 기호·공백 등 표현 차이와 실질적인 사실 불일치를 구분합니다.
- 문제가 있는 구간·카드를 다시 처리하고 통과하지 못하면 검토 대기로 둡니다.
- 새로운 MD 형식을 넣을 때 발생하는 오류를 지속적으로 확인하고 있습니다.
- Feedback Memory는 수정 규칙을 참고하는 기록 구조이며 모델 가중치 학습과 구분합니다.

현재 근거 확인 범위는 업로드된 원문입니다. 원문 자체의 사실성에 대한 공식 기록 검증을 대체하지 않습니다. 외부 게시 자동화에는 별도의 인증과 계정 설정이 필요합니다.

## 확인할 자료

- [현재 기능과 실행 방법](https://github.com/seungyu14-cel/Sports-Card-New/blob/main/README.md)
- [KBO 근거 기반 제작·검수 안내](https://github.com/seungyu14-cel/Sports-Card-New/blob/main/docs/KBO_GROUNDED_MILESTONE.md)
- [로컬 LLM과 피드백 운영 가이드](https://github.com/seungyu14-cel/Sports-Card-New/blob/main/docs/LOCAL_LLM_FEEDBACK_GUIDE.md)

이 소개는 2026-10-13 확인한 README와 개발 경험을 바탕으로 작성했습니다. 특정 실행의 성공률이나 공식 기록 정확도를 측정한 보고서는 아닙니다.
