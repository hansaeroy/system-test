# README_CONTEXT.md
# 클린하우스 프로젝트 컨텍스트 사용법

Codex 작업 시작 전에 다음 파일을 순서대로 읽는다.

1. 01_FACTS.md
2. 02_FINAL_PLAN.md
3. 03_DESIGN_DIRECTION.md
4. 04_PRODUCTION_SPEC.md

## 현재 상태
- FACTS: 확정
- FINAL PLAN: 확정
- DESIGN DIRECTION: 시안 비교 중
- PRODUCTION SPEC: 아직 미확정

## 지금 해야 할 일
현재는 전체 구현 단계가 아니다.

먼저 03_DESIGN_DIRECTION.md를 기준으로 디자인 시안을 만들고,
A/B/C 중 하나를 선택한다.

선택 후 03_DESIGN_DIRECTION.md를 최종 아트 디렉션으로 업데이트하고,
그 다음 04_PRODUCTION_SPEC.md를 확정한다.

그 이후 Codex 구현을 시작한다.

## Codex 시작 프롬프트 예시
작업 전에 프로젝트 루트의 다음 파일을 모두 읽고 기준으로 사용해.

- 01_FACTS.md
- 02_FINAL_PLAN.md
- 03_DESIGN_DIRECTION.md
- 04_PRODUCTION_SPEC.md

우선순위:
1. FACTS는 임의 변경 금지
2. FINAL_PLAN의 정보 구조와 전환 흐름 유지
3. DESIGN_DIRECTION을 시각적 기준으로 우선 적용
4. PRODUCTION_SPEC에 따라 실제 구현

문서 간 충돌이 있으면 임의 판단하지 말고 먼저 보고해.

현재 03_DESIGN_DIRECTION.md가 DESIGN EXPLORATION 상태라면
전체 구현을 시작하지 말고 디자인 방향 확정이 필요한 상태임을 먼저 알려줘.
