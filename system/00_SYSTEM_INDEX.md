# 홈페이지 제작 시스템 — Core Files

이 폴더는 범용 UI/UX 지식이 아니라, 우리 제작 시스템만의 고유한 판단 로직을 저장한다.

## 필수 파일

1. `10_ONBOARDING_INTERPRETATION.md`
   - 온보딩 해석
   - 사업 사실과 제작 판단 분리
   - 추가질문 최대 3개
   - READY / NEED_INFO / WAITING_ASSETS / MANUAL_REVIEW 판정

2. `20_WEBSITE_STRATEGY.md`
   - Primary Conversion 결정
   - 고객의 첫 질문과 의사결정 장애물 분석
   - 사이트 구조 선택
   - 섹션 순서와 CTA 전략 확정

3. `30_PRODUCTION_FLOW.md`
   - 온보딩부터 디자인, 제작설계서, Codex 구현, QA까지의 운영 흐름
   - 범용 UI/UX 스킬과 우리 시스템의 역할 분리
   - 디자인 모드, Mock Asset, Codex 전달 규칙

4. `40_CREATIVE_BUILD_BRIEF.md`
   - 온보딩과 최종기획을 실제 제작 AI가 이해하기 쉬운 서술형 제작 브리프로 변환
   - 사이트가 어떤 경험이어야 하는지, 스크롤 흐름과 감정 변화를 정의

## 범용 디자인 규칙 처리

다음 영역은 이 시스템에서 직접 중복 정의하지 않고, 검증된 UI/UX 스킬을 우선 활용한다.

- Typography 세부 규칙
- Color system
- Spacing
- Grid
- Component design
- Accessibility
- Responsive fundamentals
- 일반적인 Landing Page best practice
- UI anti-pattern
- Frontend implementation best practice

## 전체 실행 순서

온보딩
→ 온보딩 해석
→ 필요 시 추가질문 최대 3개
→ 최종기획 / 전환 전략
→ 구조 방향 결정
→ 디자인 모드 판정
→ UI/UX Skill 적용
→ 디자인 방향 확인
→ Creative Build Brief 생성
→ 제작설계서 확정
→ Codex 구현
→ QA

## 우선순위

충돌 시 아래 순서를 우선한다.

1. 확정된 사업 FACT
2. 최종기획 / 전환 전략
3. 선택된 구조와 Creative Build Brief
4. 디자인 방향
5. UI/UX Skill의 범용 지식
6. 구현 세부 판단

## 기존 프로젝트별 파일과의 관계

`01_FACTS.md`, `02_FINAL_PLAN.md`, `03_DESIGN_DIRECTION.md`, `04_PRODUCTION_SPEC.md` 같은 파일은 특정 고객/프로젝트의 실행 결과물이다.

이 `system/` 폴더의 파일은 그 결과물을 만들어내는 공통 운영 규칙이다.
