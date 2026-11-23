# Syrup Design System — List Row 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `List Row` 페이지 → [List Row 섹션 `8983:7440`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8983-7440) |
| 마스터 섹션 크기 | 1440 × 6115 (2026-11-11 확인) |
| 컴포넌트 수 | **20개** (Component Set 14 · Component 6) |
| 사용 가이드라인·예제 기준일 | 2026-11-11 |
| 기존 상세 조사 기준일 | 2026-10-12 (아래 이력 참고) |
| 문서 구성 | Guidelines 5개 · Usage A–P 16개 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **리스트에서 하나의 항목을 행 단위로 보여주는 컴포넌트예요.**
> 아이콘이나 버튼 등 다양한 부가 요소와 같이 사용할 수 있어요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `List Row / Now / Icon` | `9595:12728` |
| `List Row / Every Day / Icon` | `9354:10147` |
| `List Row / Check-In` | `9922:24043` |
| `List Row / Personality Test` | `9920:21861` |
| `List Row / Golden Time` | `10575:4001` |

2026-11-11 중복 이름을 Item·Icon·Image 역할로 구분했어요. 상위 묶음 이름과 원본 연결은 유지해요.
- `List Row / Now / Icon`: 이번에 공개 이름으로 정리한 개별 에셋 `9595:12728` / 기존 상위 묶음 `9354:14876`.
- `List Row / Every Day / Icon`: 이번에 공개 이름으로 정리한 개별 에셋 `9354:10147` / 기존 상위 묶음 `9661:6149`.

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Master Component — 단일 6종](#1-master-component--단일-6종)
3. [Master Component — Component Set 9종](#2-master-component--component-set-9종)
4. [Child Item — 아이콘 5종](#3-child-item--아이콘-5종)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [점검 필요 사항 — 기존 기록](#점검-필요-사항)
7. [사용 가이드라인](#사용-가이드라인)
8. [사용 예제](#사용-예제)
9. [문서 구성과 AI 도구 사용 기준](#문서-구성과-ai-도구-사용-기준)
10. [확인 사항](#확인-사항)

---

## 사용 가이드라인

2026-11-11 [피그마 Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-6849)의 내용을 반영했어요.

### 1. 정보와 행동에 맞는 유형을 사용해요

콘텐츠나 리워드를 안내하는 행과, 이름·값을 보여주는 행을 구분해 사용해요.
버튼·화살표·체크 표시 등 오른쪽 요소는 각 컴포넌트의 역할에 맞게 유지해요.

### 2. 참여 상태에 맞춰 문구와 버튼을 변경해요

참여 전·진행 중·결과 확인·완료 상태는 해당 컴포넌트의 상태 옵션으로 구분해요.
버튼 문구와 체크 표시, 안내 문구가 실제 상태와 일치하도록 구성하고, 이용 불가 상태를 완료 상태와 혼동하지 않도록 해요.

### 3. 선택과 화면 이동을 구분해요

목록에서 항목을 고를 때는 Default와 Selected 상태를 사용해요.
다음 화면에서 내용을 입력하거나 선택하는 항목은 Navigation 유형을 사용하고, 선택 표시와 이동 화살표를 구분해요.

### 4. 문구와 보조 정보에 맞는 구성을 선택해요

미션 문구가 두 줄로 필요한 경우에는 2 Line=True를 사용해요.
분류·시간·설명 등 선택 옵션이 있는 정보는 필요한 경우에 표시하고, 같은 목록에서는 텍스트와 오른쪽 요소의 정렬을 유지해요.

### 5. 수치의 의미와 단위를 함께 보여줘요

순위·횟수·금액은 무엇을 뜻하는지 알 수 있도록 이름과 단위를 함께 표시해요.
같은 목록의 수치는 같은 위치에 정렬하고, 내역의 항목명과 날짜 등 수치를 이해하는 데 필요한 정보를 유지해요.

## 사용 예제

[Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-6850)는 A–P 순서로 구성해요. 아래 컴포넌트 매핑은 AI 도구에서 유형과 상태를 선택할 때 참고해요.

### A. 현재 할 일 안내

현재 할 일과 남은 시간, 받을 수 있는 리워드를 함께 보여줘요. 여러 항목이 있으면 현재 위치를 인디케이터로 안내해요.

- 컴포넌트: `List Row / Now`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7439)

### B. 리워드와 바로가기

아이콘과 설명을 함께 보여줘요. 리워드를 받는 행과 다른 화면으로 이동하는 행은 오른쪽 요소로 구분해요.

- 컴포넌트: `List Row / Every Day · Type=Default / Link`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7502)

### C. 미션 참여

미션 문구와 분류, 리워드를 함께 보여줘요. 문구 길이에 맞춰 한 줄형과 두 줄형을 선택해요.

- 컴포넌트: `List Row / Mission · 2 Line=False / True`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7602)

### D. 퀴즈 참여와 결과

참여 가능·진행 중·결과 확인·정답·오답·참여 예정 상태를 구분해요. 각 상태의 안내 문구와 오른쪽 버튼을 함께 변경해요.

- 컴포넌트: `List Row / Quiz · Open / Pending / Result / Correct / Incorrect / Upcoming`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7658)

### E. 참여 완료 표시

참여 항목의 이름과 완료 여부를 보여줘요. 항목의 유형에 맞는 아이콘을 사용하고, 완료 상태는 문구와 체크 표시로 구분해요.

- 컴포넌트: `List Row / Task · Check-In / Personality Test / Golden Time`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7791)

### F. 할 일의 실행 상태

실행할 할 일과 받을 수 있는 리워드를 보여줘요. 완료와 이용 불가 상태는 각각의 상태 옵션으로 구분해요.

- 컴포넌트: `List Row / Todo / Task · Default / Completed / Disabled`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7864)

### G. 할 일 선택과 이동

목록에서 고른 항목은 선택 표시로 구분해요. 다음 화면으로 이어지는 항목은 화살표가 있는 Navigation 유형을 사용해요.

- 컴포넌트: `List Row / Todo / Selection · Default / Selected / Navigation`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-7955)

### H. 등록한 할 일 관리

등록한 할 일의 이름과 반복 일정, 시간을 함께 보여줘요. 수정과 삭제는 각 항목에 연결된 버튼으로 제공해요.

- 컴포넌트: `List Row / Todo / Management`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8017)

### I. 순위와 리워드

참여자의 순위와 실적, 리워드를 함께 보여줘요. 순위에 맞는 유형을 선택하고 내 항목은 Me 옵션으로 구분할 수 있어요.

- 컴포넌트: `List Row / Ranking · Rank=1 / 2 / 3 / 4 · Me`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8072)

### J. 실적 순위

순위와 이름, 모은 금과 참여 횟수를 함께 보여줘요. 같은 목록 안에서 각 수치의 위치와 단위를 맞춰요.

- 컴포넌트: `List Row / Report / Ranking`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8162)

### K. 발표와 당첨 상태

발표 예정·당첨·미당첨·미참여 상태를 구분해요. 해당 회차의 정보와 결과 문구를 함께 보여줘요.

- 컴포넌트: `List Row / Status · Upcoming / Winner / Not Winner / Not Entered`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8212)

### L. 쇼핑 적립 안내

쇼핑 혜택의 이름과 설명, 적립 가능한 금액을 함께 보여줘요. 금액의 단위와 최대 혜택 등의 조건을 유지해요.

- 컴포넌트: `List Row / Shopping / Gold`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8286)

### M. 이름과 값

하나의 항목명과 대응하는 값을 나란히 보여줘요. 금액 등 수치의 의미와 단위를 함께 표시해요.

- 컴포넌트: `List Row / Value`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8365)

### N. 상세 내역

항목명과 날짜, 수량 등 상세 값을 나란히 보여줘요. 내용이 길어지면 줄바꿈을 허용하고 항목명이 대응하는 값을 유지해요.

- 컴포넌트: `List Row / History · Type=OPS03_1`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8414)

### O. 참여 내역

참여자와 처리 정보를 간결한 행으로 보여줘요. 같은 목록에서 정보의 순서와 정렬을 일관되게 유지해요.

- 컴포넌트: `List Row / History · Type=RC01`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8472)

### P. 프로모션 안내

참여할 혜택과 행동을 짧은 문구로 안내해요. 해당 혜택을 설명하는 이미지와 문구를 함께 사용해요.

- 컴포넌트: `List Row / Coupon / Promotion`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11867-8524)

## 문서 구성과 AI 도구 사용 기준

- List Row는 정보 구조별 컴포넌트를 모은 카탈로그예요. 모든 행을 하나의 공통 컴포넌트로 대체하거나 같은 높이로 강제하지 않아요. 정보량과 행동에 맞는 유형을 선택해요.
- `Every Day`의 `Type=Default`는 리워드 안내, `Type=Link`는 이동을 구분하는 예제예요. 오른쪽 버튼과 화살표의 역할을 바꾸지 않아요.
- `Mission`의 `2 Line`은 VARIANT의 `False / True` 값이에요. 분류 문구의 표시는 `Text` BOOLEAN으로 조절해요. 한 줄·두 줄 구성과 보조 정보 표시는 서로 다른 옵션이에요.
- `Task`는 `Type=Check-In / Personality Test / Golden Time`과 `Completed=True / False`를 사용해요. `Time`은 해당 컴포넌트가 제공하는 보조 정보 옵션이에요.
- `Todo / Task`는 `State=Default / Completed / Disabled`로 실행 상태를 구분해요. `Todo / Selection`의 `State=Default / Selected / Navigation`은 선택과 이동을 구분하는 다른 상태 체계예요. `Selected`를 수령 완료나 참여 완료로 해석하지 않아요.
- `Quiz`는 참여·결과의 6개 상태, `Status`는 발표·당첨의 4개 상태를 사용해요. 두 컴포넌트의 상태 이름을 공통 상태로 합치지 않아요.
- `Ranking`의 `Rank=4`는 4위 이후 순위의 기본 표현에도 사용돼요. 순위 숫자는 실제 값으로 표시하고, 내 항목은 `Me` 옵션으로 구분해요.
- `History`는 화면 코드별로 정보 구조가 달라요. 예제 N은 `OPS03_1` 상세 항목, O는 `RC01` 참여 내역이에요. 예제에 없는 `SG02`, `CS02`, `CS06`, `OPS03`, `CTG01`을 폐기된 유형으로 판단하지 않아요.
- 버튼·체크·화살표·시간·설명 등은 각 컴포넌트의 원래 역할과 선택 옵션 안에서 변경해요. 마스터 인스턴스와 중첩 구조, 자체 패딩을 유지해요.
- 이미지가 사용된 행은 콘텐츠에 맞는 이미지와 문구를 함께 구성해요. 문서의 예제 금액·날짜·횟수·이름은 샘플이며 운영 정책이나 계산 기준이 아니에요.
- Usage는 폭 360의 예제를 가로 간격 40, 섹션 여백 100으로 한 줄에 배열해요. 설명 끝과 Slot 사이 간격은 50이며, Slot은 패딩 0·좌측/상단 정렬·높이 Hug로 사용해요.
- 단독 행은 Slot 안에 바로 배치하고, 상태 비교나 복수 행 배치가 필요한 경우에만 보조 컨테이너를 사용해요. 현재 복수 행 예제의 간격 16은 문서에서 비교하기 위한 값이며 실제 화면의 모든 행 간격을 규정하지 않아요.
- 문서의 예제 열 폭 360과 각 행의 실제 컴포넌트 폭은 구분해요. 배치할 때 마스터의 폭과 Auto Layout을 기준으로 텍스트·오른쪽 요소가 눌리거나 겹치지 않도록 해요.
- Section 1의 아노테이션 53개를 제거했고, 잔여 0개를 확인했어요.

## 확인 사항

- 이번 작업은 가이드라인 5개와 예제 A–P 16개를 추가한 내용이에요. 마스터의 높이·패딩·속성명·variant를 일괄 변경한 작업은 아니에요.
- 마스터 섹션은 2026-11-11 확인 기준 1440×6115예요. 기존 기록의 1440×6040과 구분해요.
- 아래의 노드 수·미사용 집계·미바인딩 수·외부 토큰 수는 2026-10-12 당시 결과예요. 현재 Section 1과 문서에 인스턴스가 존재하므로 ‘마스터 15종 전부 사용 0건’은 현재 상태가 아니에요.
- 과거의 높이 통일·구분선 색 통일·간격 변경 제안은 구현 규칙이나 완료된 변경으로 해석하지 않아요. 적용 시 현재 마스터와 최신 가이드라인을 우선해요.
- 과거 스타일·토큰 감사 수치는 이번 문서 반영 작업에서 전수 재검사하지 않았어요.

---

## 기존 마스터 규격과 점검 기록 (2026-10-12)

> 아래는 상세 규격 및 결정 이력을 보존한 기록이에요. 당시 수치와 점검 제안은 현재 상태로 단정하지 않으며, 최신 사용 기준은 위 가이드라인·예제를 우선해요.

## 구성 한눈에 보기

섹션 6,040 · 노드 **978개**로 [Card](syrup-card-components.md) · [Grid List](syrup-grid-list-components.md) 다음입니다.

[Card](syrup-card-components.md)와 같은 **카탈로그형 페이지**입니다. 하나의 컴포넌트를 variant로 확장한 것이 아니라, **서비스 화면별 행(row)을 모아 둔 구조**입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | 완성형 행 **15종** |
| y 4755 | Child Item | 아이콘 세트 **5종** (65 variant) |

### 전체 목록

#### Master — 단일 Component (6)

| # | 이름 | Props | 크기 |
| --- | --- | --- | --- |
| 1 | `List Row / Now` | `Indicator` · `Time` · `Price` · `Discount` | 328 × 90 |
| 2 | `List Row / Coupon / Promotion` | — | 312 × 82 |
| 3 | `List Row / Todo / Management` | — | 328 × 84 |
| 4 | `List Row / Report / Ranking` | — | 360 × 84 |
| 5 | `List Row / Shopping / Gold` | — | 360 × 86 |
| 6 | `List Row / Value` | — | 290 × 35 |

#### Master — Component Set (9)

| # | 이름 | Variant 축 | 종 | 크기 |
| --- | --- | --- | --- | --- |
| 7 | `List Row / Every Day` | `Type` + `Info` | 2 | 328 × 61 |
| 8 | `List Row / Mission` | `2 Line` + `Image` · `Text` | 2 | 328 × 52 / 58 |
| 9 | `List Row / Quiz` | `State` | **6** | 328 × 43 |
| 10 | `List Row / Task` | `Type` × `Completed` + `Time` | **6** | 314 × 58 |
| 11 | `List Row / Ranking` | `Rank` + `Me` | 4 | 312 × 66 / 68 |
| 12 | `List Row / Todo / Task` | `State` | 3 | 328 × 59 |
| 13 | `List Row / Todo / Selection` | `State` | 3 | 328 × 64 |
| 14 | `List Row / Status` | `State` | 4 | 326 × 43 |
| 15 | `List Row / History` | `Type` + `Cancel` · `Description` | **7** | 292~360 × 19~136 |

#### Child Item — 아이콘 (5)

| # | 이름 | Variant | 크기 |
| --- | --- | --- | --- |
| 16 | `List Row / Every Day / Icon` | `Type` **21종** | 55 × 55 |
| 17 | `List Row / Now / Icon` | `Type` **17종** | 50 × 50 |
| 18 | `List Row / Check-In` | `Type` **15종** | 30 × 30 |
| 19 | `List Row / Personality Test` | `Type` **8종** | 30 × 30 |
| 20 | `List Row / Golden Time` | `Type` **4종** | 30 × 30 |

**아이콘 variant만 65종**입니다.

> **마스터 15종 전부 인스턴스 0건**입니다 → [점검 6](#6-마스터-15종-전부-사용-0건)

---

## 1. Master Component — 단일 6종

| 컴포넌트 | 크기 | Padding | Gap | 배경 | Radius |
| --- | --- | --- | --- | --- | --- |
| `List Row / Now` | 328 × 90 | `Spacing/400`(16) 사방 | `Spacing/250`(10) | 없음 | `r300` (12) |
| `List Row / Value` | 290 × 35 | 0 | `Spacing/500`(20) | 없음 | 0 |

나머지 4종(`Coupon / Promotion` · `Todo / Management` · `Report / Ranking` · `Shopping / Gold`)은 **variant·프로퍼티가 전혀 없는 고정 레이아웃**입니다.

`List Row / Now`만 BOOLEAN 4개(`Indicator` · `Time` · `Price` · `Discount`)로 요소를 켜고 끌 수 있습니다.

---

## 2. Master Component — Component Set 9종

### 행 높이 체계

| 높이 | 컴포넌트 |
| --- | --- |
| **43** | `Quiz` · `Status` |
| **52 / 58** | `Mission` |
| **58** | `Task` |
| **59** | `Todo / Task` |
| **61** | `Every Day` |
| **64** | `Todo / Selection` |
| **66 / 68** | `Ranking` |
| 19~136 | `History` (7종 제각각) |

**높이가 43부터 136까지 제각각**입니다. 공통 높이 체계가 없습니다 → [점검 5](#5-행-높이가-통일되어-있지-않음)

### 경계 처리

| 방식 | 컴포넌트 |
| --- | --- |
| **하단 1px 구분선** | `Mission` (`Color/Gray_850`) · `History` (**`Color/Gray_900`**) |
| **사방 테두리 + 라운드** | `Ranking` · `Todo / Task` · `Todo / Selection` |
| **없음** | `Quiz` · `Status` · `Task` · `Every Day`(배경만) |

하단 구분선 두 컴포넌트가 **서로 다른 회색**을 씁니다 → [점검 4](#4-구분선-색이-갈림)

### 선택·상태 표현

| 컴포넌트 | 활성·선택 | 비활성·기본 |
| --- | --- | --- |
| `Todo / Task` | `Color/Primary_Orange` 1px (`Default` · `Completed`) | `Color/Gray_850` 1px (`Disabled`) |
| `Todo / Selection` | `Color/Primary_Orange` 1px (`Selected`) | `Color/Gray_850` 1px (`Default` · `Navigation`) |
| `Ranking` | `Color/Primary_Orange` 1px (1~3위) | `Color/Gray_850` 1px (4위~) |

**세 컴포넌트가 같은 방식**(오렌지 테두리로 강조)을 씁니다. 일관된 규칙입니다.

### `List Row / Ranking` — 순위별 배경

| Rank | 배경 | 테두리 |
| --- | --- | --- |
| `1` | `Color/Third_Pastel_Yellow` | `Primary_Orange` |
| `2` | `Color/Third_Pastel_Blue` | `Primary_Orange` |
| `3` | **`#FFF5F0`** ⚠️ 미바인딩 | `Primary_Orange` |
| `4` | `Color/Gray_White` | `Gray_850` |

**1·2위는 토큰, 3위만 직접 입력**입니다 → [점검 3](#3-미바인딩-색상)

### `List Row / History` — 화면 코드

| Type | 크기 | 방향 |
| --- | --- | --- |
| `SG02` | 360 × 86 | 세로 |
| `CS02` | 360 × 68 | 세로 |
| `CS06` | 360 × 136 | 가로 |
| `OPS03` | 360 × 74 | 가로 |
| `OPS03_1` | 360 × **19** | 세로 |
| `RC01` | 312 × 34 | 가로 |
| `CTG01` | 292 × 26 | 가로 |

[Card](syrup-card-components.md)의 `Card / Summary`와 **같은 화면 코드 체계**입니다(`SG02` · `CS02` · `OPS03`이 양쪽에 등장). 두 페이지를 함께 정리하면 좋습니다.

---

## 3. Child Item — 아이콘 5종

| 컴포넌트 | 크기 | Variant | 인스턴스 |
| --- | --- | --- | --- |
| `List Row / Every Day / Icon` | 55 × 55 | **21** | 2 |
| `List Row / Now / Icon` | 50 × 50 | **17** | 1 |
| `List Row / Check-In` | 30 × 30 | **15** | 2 |
| `List Row / Personality Test` | 30 × 30 | **8** | 2 |
| `List Row / Golden Time` | 30 × 30 | **4** | 2 |

variant 값이 전부 **한글 서비스명**입니다(`지금할일` · `라방출첵` · `골드익스프레스` · `행운지수` …).

2026-10-12에 **5종 모두 프로퍼티명이 `Type`으로 통일**되었습니다 → [점검 1](#1--property-1-9건-정리-2026-10-12-완료)

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 행 폭 | **328**이 표준 · 312 · 326 · 360 |
| 행 높이 | **43~68** (History는 19~136) |
| 좌우 패딩 | `Spacing/500`(20) · `Spacing/600`(24) · `Spacing/400`(16) |
| 간격 | `Spacing/250`(10) · `Spacing/400`(16) · `Spacing/500`(20) |
| 라운드 | `Corner radius/400`(16) · `Corner radius/300`(12) |
| 구분선 | 하단 1px — `Color/Gray_850` 또는 `Color/Gray_900` |
| 강조 테두리 | `Color/Primary_Orange` 1px |
| 기본 테두리 | `Color/Gray_850` 1px |
| 배경 | `Color/Gray_White` 또는 없음 |

---

## 점검 필요 사항

### 1. ✅ `Property 1` **9건** 정리 (2026-10-12 완료)

파일 전체 잔여 55건 중 **이 페이지가 9건**으로 가장 많았습니다.

| 컴포넌트 | 변경 전 | 변경 후 | 값 |
| --- | --- | --- | --- |
| `List Row / Every Day` `9661:6149` | `Property 1` | **`Type`** | `Default` · `Link` |
| `List Row / Quiz` `9960:8504` | `Property 1` | **`State`** | `Open` · `Pending` · `Result` · `Correct` · `Incorrect` · `Upcoming` |
| `List Row / Ranking` `9961:20797` | `Property 1` | **`Rank`** | `1` · `2` · `3` · `4` |
| `List Row / Status` `9991:62461` | `Property 1` | **`State`** | `Upcoming` · `Winner` · `Not Winner` · `Not Entered` |
| `List Row / History` `9991:62362` | `Property 1` | **`Type`** | 화면 코드 7종 |
| `.primitive / … / Now` `9595:12728` | `Property 1` | **`Type`** | 서비스명 17종 |
| `.primitive / … / Check-In` `9922:24043` | `Property 1` | **`Type`** | 서비스명 15종 |
| `.primitive / … / Personality Test` `9920:21861` | `Property 1` | **`Type`** | 서비스명 8종 |
| `.primitive / … / Golden Time` `10575:4001` | `Property 1` | **`Type`** | 서비스명 4종 |

값의 성격에 따라 **`Type` · `State` · `Rank`** 세 가지로 나눠 지정했습니다.

아이콘 세트 5종이 **모두 `Type`으로 통일**되었습니다(기존에 `Every Day`만 `Type`이었음).

**`List Row` 페이지의 `Property 1`은 0건**이 되었습니다. 파일 전체로는 **46개** 컴포넌트셋에 남아 있습니다(55 → 46).

### 2. ✅ 프로퍼티명·값 표기 정리 (2026-10-12 완료)

네 가지 표기 문제를 함께 정리했습니다.

#### `Cancle` → `Cancel` — 오타

`List Row / History` `9991:62362`의 BOOLEAN 프로퍼티명에 오타가 있었습니다.

| 변경 전 | 변경 후 |
| --- | --- |
| **`Cancle`** | **`Cancel`** |

> [Button](syrup-button-components.md)의 `Coner`(→ `Corner`), [List Footer](syrup-list-footer-components.md)의 `Viariant`(→ `Variant`)와 같은 유형입니다.

#### `select` → `State` — 소문자

`List Row / Todo / Selection` `9971:29378`의 프로퍼티명이 **소문자**였습니다. 파일 전체에서 소문자로 시작하는 프로퍼티명은 이 하나였습니다.

| 변경 전 | 변경 후 | 값 |
| --- | --- | --- |
| **`select`** | **`State`** | `Default` · `Selected` · `Navigation` |

#### `Disabled` → `State` — 이름과 값이 어긋남

`List Row / Todo / Task` `9971:29408`의 프로퍼티명이 `Disabled`인데 값이 3개였습니다.

| 변경 전 | 변경 후 | 값 |
| --- | --- | --- |
| **`Disabled`** | **`State`** | `Default` · `Completed` · `Disabled` |

`Disabled`라는 이름은 boolean을 연상시키는데 실제로는 상태 축이었고, 값 중 하나와 이름이 같아 **`Disabled=Disabled`** 라는 어색한 조합이 생겼습니다.

바로 옆 `Todo / Selection`과 함께 **`State`로 통일**되어, 두 컴포넌트의 축 이름이 같아졌습니다.

#### `NotWinner` · `NotEntered` → 공백 추가

`List Row / Status` `9991:62461`의 값 표기입니다.

| 변경 전 | 변경 후 |
| --- | --- |
| **`NotWinner`** | **`Not Winner`** |
| **`NotEntered`** | **`Not Entered`** |

`State` 옵션이 `["Upcoming", "Winner", "Not Winner", "Not Entered"]`로 **띄어쓰기 표기로 통일**되었습니다.

### 3. 미바인딩 색상

아이콘 세트 내부를 제외한 수치입니다.

| 색 | 건수 | 위치 | 성격 |
| --- | --- | --- | --- |
| `#D9D9D9` | 3 | — | 회색, Gray 스케일 밖 |
| `#F4F7FE` | 2 | — | 연한 파랑 배경 |
| `#7654FF` | 2 | — | 보라 |
| **`#FFF5F0`** | 1 | **`Ranking` ▸ `3`위 배경** | **1·2위는 토큰** |
| `#00C01E` · `#009D35` | 2 | 네이버 계열 로고 | 브랜드 |
| `#FFD00E` · `#FFBC57` | 2 | 별 뱃지 | [Card](syrup-card-components.md)와 동일 |
| `#FF6315` | 1 | `Primary_Orange`와 **같은 값** | **바인딩 가능** |
| 그 외 | 4 | `#F4F4F4` · `#F1F1F1` · `#969696` 등 | 회색 계열 |

#### ⚠️ 두 건을 추가 조사한 결과 (2026-10-12)

초판에 "바로 처리 가능"으로 적었으나, **위치를 특정해 보니 둘 다 단순 바인딩 대상이 아니었습니다.**

**`#FF6315` 1건 — Lottie 애니메이션 내부**

| 항목 | 값 |
| --- | --- |
| Node | `I9960:8468;9206:13304` |
| 레이어 | `뒤` (ELLIPSE 12 × 12) |
| 위치 | `List Row / Quiz` ▸ `State=Open` › `head` › **`Lottie / Quiz`** 인스턴스 내부 |

값은 `Color/Primary_Orange`와 정확히 같지만, **Lottie 애니메이션 에셋의 내부 도형**입니다. 아이콘·일러스트 내부를 토큰화 대상에서 제외해 온 기준([Card](syrup-card-components.md) · [Grid List](syrup-grid-list-components.md) · [Badge](syrup-badge-components.md))에 따르면 **같은 범주**입니다.

바인딩하려면 Lottie 페이지의 원본을 고쳐야 하는데, 애니메이션 에셋은 별도 도구로 내보내는 자산이라 **Figma 토큰과 연결할 실익이 적습니다.** 현행 유지를 권합니다.

**`#FFF5F0` 1건 — 대응 토큰 없음**

| 항목 | 값 |
| --- | --- |
| Node | `9961:20795` (`List Row / Ranking` ▸ `Rank=3` 컴포넌트 자체) |

Third Pastel 팔레트와 대조한 결과 **일치하는 토큰이 없습니다.**

| 토큰 | 값 | `#FFF5F0`과 |
| --- | --- | --- |
| `Color/Third_Pastel_Yellow` | #FFF9E2 | 다름 (1위 배경) |
| `Color/Third_Pastel_Blue` | #F1F6FF | 다름 (2위 배경) |
| `Color/Third_Pastel_Coral` | #FFEADE | **가장 가깝지만 다름** |

1·2위가 토큰인데 3위만 직접 입력된 상태입니다. **`Third_Pastel_Coral`(#FFEADE)로 바꿀지, 3위용 토큰을 신설할지 디자인 판단이 필요**합니다. 전자는 색이 눈에 띄게 달라집니다.

### 4. 구분선 색이 갈림

하단 1px 구분선을 쓰는 두 컴포넌트가 다른 색입니다.

| 컴포넌트 | 색 |
| --- | --- |
| `List Row / Mission` | **`Color/Gray_850`** (#EDEDED) |
| `List Row / History` | **`Color/Gray_900`** (#F2F2F2) |

[Border 문서](syrup-border-components.md)의 **"1px 구분선·보더는 `Color/Gray_850`"** 기준에 따르면 `History`가 예외입니다.

> [List Footer](syrup-list-footer-components.md)(상단 1px `Gray_900`)와 [Card](syrup-card-components.md)의 `Card / SA`(하단 1px `Gray_900`)도 같은 상태입니다. **세 건을 함께 판단**하는 편이 좋습니다.

### 5. 행 높이가 통일되어 있지 않음

| 높이 | 컴포넌트 수 |
| --- | --- |
| 43 | 2 |
| 52 · 58 · 59 · 61 · 64 | 각 1~2 |
| 66 · 68 | 1 |
| 19~136 | `History` 7종 |

**43부터 136까지 11가지 높이**가 쓰입니다. 리스트에 여러 종류의 행이 섞이면 리듬이 깨집니다.

높이가 제각각인 이유는 **상하 패딩이 토큰 밖 값**이기 때문입니다.

| 패딩 | 건수 | 컴포넌트 |
| --- | --- | --- |
| **22** | 8 | `Ranking` |
| **16.5** | 6 | `Todo / Task` |
| **14** | 4 | `Task` ▸ `Personality Test` |
| **10.5** | 4 | `Task` ▸ `Golden Time` |
| `1.5` · `1.24` | 6 | 내부 요소 |

[Header](syrup-header-components.md)의 `9.5`, [List Footer](syrup-list-footer-components.md)의 `22.5`와 같은 **높이 역산 값**입니다.

특히 **`List Row / Task`는 같은 컴포넌트셋 안에서 `Type`에 따라 상하 패딩이 다릅니다.**

| Type | 상하 패딩 | 높이 |
| --- | --- | --- |
| `Check-In` | `Spacing/400` (16) | 58 |
| `Personality Test` | **14** | 58 |
| `Golden Time` | **10.5** | 58 |

높이는 58로 같은데 **패딩만 다릅니다.** 안쪽 아이콘·텍스트 높이가 달라 역산 값이 달라진 것으로 보입니다. **높이 58 고정 + 패딩 0 + 세로 중앙 정렬**로 바꾸면 세 variant가 통일됩니다.

### 6. 마스터 15종 전부 사용 0건

| 구분 | 인스턴스 |
| --- | --- |
| 마스터 **15종** | **전부 0** |
| 아이콘 primitive 5종 | 9 (전부 `List Row` 페이지 안) |

**마스터가 하나도 쓰이지 않습니다.** [Card](syrup-card-components.md) · [Label](syrup-label-components.md) · [List Header](syrup-list-header-components.md)에서도 비슷한 양상이었지만, 15종 전부 0건인 것은 이 페이지가 처음입니다.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

행(row)은 리스트 안에 반복 배치되는 요소라, **Figma 보드에서는 대표 1개만 그려 두고 실제 화면은 다른 파일에서 조립**하는 방식일 수 있습니다.

### 7. 스타일 미적용 텍스트 19건

보드 표기 4건을 제외한 수치입니다.

| 크기 · 굵기 | 건수 | 위치 |
| --- | --- | --- |
| `11 Bold` | 4 | `Ranking` ("나") |
| `11 Regular` | 3 | `Now` (`1` · `/` · `2`) |
| `12 ExtraBold` | 3 | `Ranking` (순위 숫자) |
| `11 Medium` | 2 | `Shopping / Gold` · `Quiz` |
| `16 Bold` | 2 | `Value` |
| `9 ExtraBold` | 2 | — |
| `14 Black` | 1 | `Now` ("지금 할 일") |
| `14 Bold` | 1 | `Every Day` |
| **`5.43 Regular`** | **1** | ⚠️ 소수점 크기 |

세 가지로 나뉩니다.

**(1) 토큰이 있는 크기** — `16 Bold`(→ `t900_16_bold`) · `14 Bold`(→ `t1050_14_bold`)는 대응 스타일이 있습니다. line-height 차이만 확인하면 적용 가능합니다.

**(2) 9~12px** — **토큰화하지 않기로 한 범주**입니다. 그대로 두는 것이 기준에 맞습니다.

**(3) 스케일 밖 굵기·크기**
- **`14 Black`** 1건 — Pretendard Black은 Syrup 타입 스케일에 **없는 굵기**입니다. 파일 전체에서 이 1건뿐입니다.
- **`5.43 Regular`** 1건 — 아래 참고

#### ℹ️ `5.43 Regular` — 안드로이드 런처 아이콘 잔재 (2026-10-12 확인)

초판에 "작업 중 축소된 흔적"으로 적었는데, 위치를 특정해 보니 성격이 달랐습니다.

| 항목 | 값 |
| --- | --- |
| Node | `9922:24123` |
| 레이어 | `Place icon background` |
| 경로 | `List Row / Check-In` ▸ `Type=오락2` › `Shapes` › `launcher icon` › **`ic_launcher_background`** |
| 표시 | **`visible: false`** |

**안드로이드 앱 아이콘(`ic_launcher`) 에셋을 가져오면서 딸려 온 플레이스홀더 텍스트**입니다. 숨겨져 있어 렌더링에 영향이 없고, 아이콘 에셋 내부라 디자인 값도 아닙니다.

**정리 대상이 아닙니다.** 다만 같은 경로에 다른 런처 아이콘 잔재가 더 있을 수 있어, 아이콘 세트를 정리할 때 함께 보면 좋습니다.

### 8. 외부 토큰 6건

| 토큰 | 건수 |
| --- | --- |
| `Spec docs` (문서 전용) | 5 |
| **`border:strokes`** | **2** |
| **`Color:fills`** | **1** |

`border` · `Color` 3건은 **다른 라이브러리 변수**입니다. [Card](syrup-card-components.md)에서 정리한 것과 같은 유형이라 교체 가능성이 있습니다.

### 9. 토큰 상태 — 보통

| 항목 | 결과 |
| --- | --- |
| **원격 텍스트 스타일** | **0건** |
| **제어문자 · U+2028** | **0건** |
| 미바인딩 fill | 20건 (아이콘 세트 제외) |
| 미바인딩 padding | `22` 8 · `16.5` 6 · `14` 4 · `10.5` 4 · 소수 8 |
| 미바인딩 gap | `63` · `68` 각 2 · `72` · `66` · `129` · `14` 각 1 · 소수 2 |
| 미바인딩 radius | 소수 6건 (아이콘 내부) |
| 스타일 미적용 | 19건 |
| 폰트 | Pretendard **Black 1 · ExtraBold 5 · SemiBold 2** — 스케일 밖 굵기 |

**`List Row / Quiz`의 간격이 63 · 66 · 68 · 72로 variant마다 다릅니다.** 오토레이아웃 간격으로 좌우 요소를 밀어내는 방식인데, `primaryAxisAlignItems`를 `SPACE_BETWEEN`으로 바꾸면 **고정값 없이 자동 정렬**됩니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| `Property 1` **9건** ([1](#1--property-1-9건-정리-2026-10-12-완료)) | `Type` 6 · `State` 2 · `Rank` 1 — **페이지 내 0건** |
| `Cancle` → `Cancel` ([2](#2--프로퍼티명값-표기-정리-2026-10-12-완료)) | 오타 수정 |
| `select` → `State` ([2](#2--프로퍼티명값-표기-정리-2026-10-12-완료)) | 파일 내 유일한 소문자 프로퍼티명 해소 |
| `Disabled` → `State` ([2](#2--프로퍼티명값-표기-정리-2026-10-12-완료)) | `Todo / Task` · `Todo / Selection` 축 이름 통일 |
| `NotWinner` · `NotEntered` ([2](#2--프로퍼티명값-표기-정리-2026-10-12-완료)) | 띄어쓰기 표기로 통일 |

전부 **이름만 변경**이며 크기·렌더링 변화가 없습니다. 작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### ℹ️ 조사 후 제외 — 정리 대상 아님

| 항목 | 판단 |
| --- | --- |
| `#FF6315` 1건 ([3](#3-미바인딩-색상)) | **Lottie 애니메이션 내부** — 일러스트 범주 |
| `5.43 Regular` 1건 ([7](#7-스타일-미적용-텍스트-19건)) | **안드로이드 런처 아이콘 잔재** · 숨김 상태 |

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Quiz` 간격 → `SPACE_BETWEEN` ([9](#9-토큰-상태--보통)) | 구조 개선 | 중간 |
| 2 | `Task` 상하 패딩 통일 ([5](#5-행-높이가-통일되어-있지-않음)) | 구조 변경 | 중간 |
| 3 | `Ranking` 3위 배경 `#FFF5F0` ([3](#3-미바인딩-색상)) | **토큰 신설 판단** | 중간 |
| 4 | 구분선 색 통일 ([4](#4-구분선-색이-갈림)) | **타 페이지와 함께 판단** | 중간 |
| 5 | 외부 토큰 3건 교체 ([8](#8-외부-토큰-6건)) | 값 확인 필요 | 중간 |
| 6 | `14 Black` 굵기 ([7](#7-스타일-미적용-텍스트-19건)) | 판단 필요 | 낮음 |
