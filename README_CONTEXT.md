# README_CONTEXT.md
# 클린하우스 프로젝트 컨텍스트 사용법

이 저장소의 `01~04` 문서는 Chat과 Codex 사이에서 사용하는 단일 프로젝트 기준 문서다.

## 읽는 순서
1. `01_FACTS.md`
2. `02_FINAL_PLAN.md`
3. `03_DESIGN_DIRECTION.md`
4. `04_PRODUCTION_SPEC.md`

## 문서 역할
### 01_FACTS.md
고객이 제공한 실제 사업 사실.
이 파일의 사실을 임의로 만들거나 바꾸지 않는다.

### 02_FINAL_PLAN.md
사이트 전략, 정보 구조, 전환 흐름, CTA 원칙.

### 03_DESIGN_DIRECTION.md
현재 디자인 모드, 비주얼 방향, 후보안, 최종 선택 상태.

### 04_PRODUCTION_SPEC.md
최종 구현 기준서.
디자인 방향 확정 전에는 NOT FINAL 상태를 유지한다.

## 작업 원칙
- 충돌 시 추측하지 말고 충돌 내용을 보고한다.
- 사업 사실은 `01_FACTS.md`를 최우선으로 따른다.
- UX/구조는 `02_FINAL_PLAN.md`를 따른다.
- 시각 방향은 `03_DESIGN_DIRECTION.md`를 따른다.
- 실제 구현은 `04_PRODUCTION_SPEC.md`가 FINAL일 때만 진행한다.

## 현재 상태
- FACTS: CONFIRMED
- FINAL PLAN: FINAL
- DESIGN DIRECTION: DESIGN EXPLORATION
- PRODUCTION SPEC: NOT FINAL

즉 현재는 디자인 시안 비교 단계이며 전체 프로덕션 구현 단계가 아니다.

## Codex 시작 지시 예시
프로젝트 작업을 시작하기 전에 `README_CONTEXT.md`와 `01_FACTS.md`부터 `04_PRODUCTION_SPEC.md`까지 순서대로 읽어라.
현재 상태 플래그를 확인하고, 문서에 없는 사업 사실은 만들지 마라.
`03_DESIGN_DIRECTION.md`가 DESIGN SELECTED가 아니고 `04_PRODUCTION_SPEC.md`가 FINAL이 아니라면 전체 프로덕션 구현을 시작하지 마라.

## 업데이트 규칙
- 사업 사실 변경 → `01_FACTS.md`
- 구조/전환/카피 방향 변경 → `02_FINAL_PLAN.md`
- 디자인 방향 선택/수정 → `03_DESIGN_DIRECTION.md`
- 최종 구현 기준 확정 → `04_PRODUCTION_SPEC.md`

전체 문서를 매번 다시 만들지 말고 변경된 파일만 업데이트한다.
