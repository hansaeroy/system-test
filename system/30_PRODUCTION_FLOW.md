# 홈페이지 제작 진행 규칙

## 목적
온보딩과 기획 결과를 디자인 스킬과 구현 도구에 정확하게 전달하여 기획과 구현이 뒤섞이지 않도록 한다.

## 전체 제작 순서
온보딩
→ 추가확인
→ 최종기획
→ 구조 방향 결정
→ 디자인 모드 판정
→ UI/UX Skill 적용
→ 디자인 방향 확인
→ Creative Build Brief 생성
→ 제작설계서 확정
→ Codex 구현
→ QA

## 1. 디자인 모드 판정
프로젝트별 Primary Mode 하나를 선택한다.
- STANDARD
- PREMIUM
- MOTION-HEAVY
- EXPERIMENTAL

필요하면 Secondary Style을 추가한다.
예: PREMIUM + LIGHT MOTION

판정 요소:
- 사이트 목적
- 고객의 구매 판단 방식
- 업종의 시각 의존도
- 이미지/신뢰자료 품질
- 콘텐츠 밀도
- 레퍼런스
- 구현 플랫폼
- 예산/일정
- 유지관리 난이도

## 2. 범용 디자인 규칙은 기존 Skill을 우선한다.
다음은 직접 중복 작성하지 않는다.
- UI 스타일
- 디자인 시스템
- 색상 조합
- 타이포 기본 규칙
- spacing
- grid
- component design
- accessibility
- responsive fundamentals
- 일반적인 landing-page best practice
- 기본 UX anti-pattern
- frontend implementation best practice

가능하면 검증된 UI/UX Skill을 사용한다.

## 3. 우리 기획을 디자인 Skill보다 우선한다.
Skill은 다음을 임의로 바꾸면 안 된다.
- 고객 사업 사실
- Primary Conversion
- 핵심 고객
- 고객의 주요 문제
- 확정된 서비스 범위
- 가격
- 정책
- Proof
- 선택된 기본 구조

Skill의 역할은 `이미 결정된 전략과 구조를 더 완성도 높은 UI/UX로 표현하는 것`이다.

## 4. 디자인 Skill 요청 형식
최소 다음 정보를 전달한다.
- Project
- Industry
- Primary Conversion
- Target Customer
- Customer's first question
- Selected Structure
- Section Sequence
- Design Mode
- Available Evidence
- Available Images
- Restrictions

Important UX Rules:
- one key message per section
- maximum one Primary CTA per section
- do not change confirmed business facts
- do not default every section to cards

## 5. 디자인 확인 단계
전체 구현 전에 다음을 확인한다.
- Hero composition
- 정보 우선순위
- 페이지 리듬
- 이미지 전략
- 구조 적합성
- CTA 전략
- 주요 Proof 표현
- 모바일 흐름
- Motion level

## 6. 테스트용 DESIGN MOCK ASSET
디자인 방향을 확인하는 단계에서는 실제 자료가 없어도 DESIGN MOCK ASSET을 사용할 수 있다.

허용 예:
- 가상 Hero 이미지
- 가상 Before/After
- 레이아웃 확인용 후기
- 샘플 이름

단, 실제 사업 사실처럼 취급하지 않는다. 실제 공개 전 반드시 실제 자료로 교체한다.

## 7. Creative Build Brief 생성
디자인 방향이 정리된 후, 구현 도구에 단순 데이터 요약을 넘기지 않는다.

`40_CREATIVE_BUILD_BRIEF.md` 규칙에 따라 다음을 포함한 서술형 제작 브리프를 생성한다.
- 사이트 전체 경험
- 방문자의 시작 상태
- 설득과 스크롤 흐름
- Hero의 역할
- 섹션별 경험과 시각 구조
- Visual Rhythm
- Motion Direction
- Mobile Priority
- FACT / MOCK 경계
- 마지막에 사용자가 가져야 할 판단과 감정

Creative Build Brief는 최종 제작설계서와 Codex 구현 사이의 핵심 전달물로 사용한다.

## 8. 제작설계서 작성 조건
다음이 결정된 뒤 작성한다.
- 최종 구조
- Hero
- 섹션 순서
- 디자인 방향
- 이미지 전략
- CTA
- Motion
- 모바일 방향
- 실제/Mock asset 구분
- Creative Build Brief

## 9. Codex의 역할
Codex는 기본적으로 구현 엔진으로 사용한다.
Codex에게 다시 사업 전략을 처음부터 판단시키지 않는다.

Codex는 다음을 기준으로 구현한다.
1. FACT DATA
2. FINAL PLAN
3. DESIGN DIRECTION
4. CREATIVE BUILD BRIEF
5. PRODUCTION SPEC

## 10. Codex가 임의로 변경하면 안 되는 항목
- 가격
- 서비스 범위
- 정책
- 실적
- 후기 사실
- Primary CTA
- 페이지 핵심 목적
- 확정 구조

구현 과정에서 충돌이 발견되면 임의 변경하지 않고 보고한다.

## 11. QA

### Strategy QA
- 핵심 고객의 질문에 답하고 있는가
- 중요한 정보가 너무 늦게 등장하지 않는가
- Primary CTA가 명확한가

### Design QA
- 선택된 Design Direction과 일치하는가
- 카드 UI로 무의미하게 수렴하지 않았는가
- 시각적 위계가 분명한가
- 모바일에서 정보 우선순위가 유지되는가

### Fact QA
- 사실이 임의 생성되지 않았는가
- 가격/정책/범위가 원본과 동일한가

### Conversion QA
- 사용자가 다음 행동을 쉽게 이해하는가
- 한 섹션에 Primary CTA가 여러 개 경쟁하지 않는가
