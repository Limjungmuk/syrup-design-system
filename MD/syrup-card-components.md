# Syrup Design System — Card 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Card` 페이지 → [Card 섹션 `9354:40597`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9354-40597) |
| 마스터 섹션 크기 | 1440 × 약 9921 (2026-11-11 확인) |
| 컴포넌트 수 | **21개** (Component Set 11 · Component 10) |
| 사용 가이드라인·예제 기준일 | 2026-11-11 |
| 기존 마스터 상세 조사 기준일 | 2026-10-08 (아래 이력 참고) |
| 문서 구성 | Guidelines 5개 · Usage A–P 16개 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **콘텐츠를 카드 형태로 보여주는 컴포넌트예요.**
> 이미지와 텍스트를 조합해 뉴스, 광고, 이벤트 등 다양한 콘텐츠를 표현할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Card / Invite / Icon` | `9669:5780` |
| `Card / My / Icon` | `10034:137009` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Component Set 7종](#1-component-set-7종)
3. [Component 10종](#2-component-10종)
4. [Child Item — Card Item](#3-child-item--card-item)
5. [Icon](#4-icon)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [점검 필요 사항 — 기존 기록](#점검-필요-사항)
8. [사용 가이드라인](#사용-가이드라인)
9. [사용 예제](#사용-예제)
10. [문서 구성과 AI 도구 사용 기준](#문서-구성과-ai-도구-사용-기준)
11. [확인 사항](#확인-사항)

---

## 사용 가이드라인

2026-11-11 피그마의 [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-7548) 문구를 반영했어요.

### 1. 정보의 목적에 맞는 카드를 사용해요

콘텐츠를 소개하고 행동으로 연결하는 카드와 수치·현황을 요약하는 카드를 구분해 사용해요.
각 카드가 제공하는 제목·본문·수치·버튼의 역할을 유지하고, 필요한 정보 구조에 맞는 유형을 선택해요.

### 2. 필요한 정보만 선택해서 보여줘요

제목·단계 안내·버튼·인디케이터 등 선택 옵션이 있는 요소는 화면에 필요한 정보에 맞춰 표시해요.
안내가 필요할 때는 단계를 함께 보여주고, 진행 현황만 필요할 때는 해당 정보만 남겨 간결하게 구성해요.

### 3. 이미지 영역은 필수로 사용해요

이미지가 포함된 카드는 이미지 영역을 유지하고, 콘텐츠에 맞는 이미지를 함께 사용해요.
Image=False는 배경색 등을 확인하기 위한 옵션으로, 실제 화면에서 이미지를 생략하는 용도로 사용하지 않아요.

### 4. 선택 상태와 사용할 수 없는 상태를 구분해요

선택형 카드는 현재 선택한 항목과 선택하지 않은 항목을 구분해요. 선택할 수 없는 경우에는 Disabled 유형을 사용해요.
선택 표시·문구·보조 링크가 실제 상태에 맞도록 구성하고, 사용할 수 없는 이유가 있으면 함께 안내해요.

### 5. 수치의 의미와 단위를 함께 보여줘요

금액·개수·순위 등 수치가 무엇을 뜻하는지 제목과 단위를 함께 표시해요.
적립 예정과 완료, 만료 예정처럼 구분이 필요한 정보는 항목명과 기한을 유지해 혼동하지 않도록 해요.

## 사용 예제

[Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-7549)는 A–P 순서로 구성해요. 아래 컴포넌트명과 속성은 AI 도구에서 유형을 선택할 때 참고하는 매핑이에요.

### A. 콘텐츠와 리워드 안내

이미지와 제목, 출처, 리워드 정보를 함께 보여줘요. 이미지와 문구가 같은 콘텐츠를 설명하도록 구성해요.

- 컴포넌트: `Card / News`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-7979)

### B. 순위가 있는 콘텐츠

여러 콘텐츠를 순위와 함께 묶어 보여줘요. 순위·설명·리워드 등 각 정보의 위치를 유지해 비교하기 쉽게 구성해요.

- 컴포넌트: `Card / Now · Ranking`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8014)

### C. 단계별 참여 안내

참여 목표와 현재 진행 개수, 필요한 절차를 함께 보여줘요. 상황에 따라 제목이나 단계 안내를 표시하는 옵션을 선택해요.

- 컴포넌트: `Card / Todo / Step`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8109)

### D. 수치 요약

적립 예정과 적립 완료처럼 서로 다른 수치를 항목명과 함께 요약해요. 같은 단위를 일관되게 표시해요.

- 컴포넌트: `Card / Summary · SG02`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8171)

### E. 만료 예정 안내

만료 예정 금액과 남은 기한을 함께 보여줘요. 만료 전 필요한 행동과 유의사항을 보조 문구로 안내해요.

- 컴포넌트: `Card / Summary · OPS03_01`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8190)

### F. 순위와 추가 행동

현재 순위와 실적, 예상 리워드를 함께 보여줘요. 추가 행동이 필요한 경우 버튼과 조건 설명을 함께 제공해요.

- 컴포넌트: `Card / Invite / Ranking`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8220)

### G. 초대 코드와 내역

복사할 코드와 참여 내역을 묶어 보여줘요. 코드 복사와 전체 내역 확인을 서로 다른 행동으로 구분해요.

- 컴포넌트: `Card / Invite / Code · Default`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8261)

### H. 정보 입력과 완료 상태

정보 입력 기한과 대상 리워드, 필요한 행동을 안내해요. 입력을 마친 경우 버튼 문구와 상태를 함께 변경해요.

- 컴포넌트: `Card / Tax`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8294)

### I. 결과와 참여 방법

결과·기간·발표 정보를 요약하거나 참여 방법을 단계별로 보여줘요. 전달할 내용에 맞는 카드 구성을 선택해요.

- 컴포넌트: `Card / Thunderbolt · Default / Step`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8321)

### J. 금과 스탬프 현황

모은 금과 보유 스탬프를 각 단위에 맞게 보여줘요. 관련된 목록과 행동을 해당 현황 아래에 함께 구성해요.

- 컴포넌트: `Card / Shopping · Gold / Stamp`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8386)

### K. 두 상품 비교

교환할 상품을 나란히 보여줘요. 상품명과 이미지, 필요한 스탬프 수와 받기 버튼을 함께 구성해요.

- 컴포넌트: `Card / Stamp · Grid`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8540)

### L. 여러 상품 비교

여러 교환 상품을 구분선과 함께 배열해요. 랜덤 지급 여부와 교환 조건을 버튼 주변에서 확인할 수 있도록 안내해요.

- 컴포넌트: `Card / Stamp · Compare`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8582)

### M. 혜택 조건과 받기

혜택 내용과 적용 조건, 예시와 유의사항을 묶어 보여줘요. 받을 수 있는 혜택은 관련 버튼으로 연결해요.

- 컴포넌트: `Card / Shopping / Naver`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8697)

### N. 차트로 수치 비교

선택한 기간의 수치 변화를 차트로 보여줘요. 기준 단위와 시점, 주요 수치를 함께 확인할 수 있도록 구성해요.

- 컴포넌트: `Card / Chart`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8722)

### O. 표로 수치 비교

날짜별 값과 변동 정보를 같은 열에 맞춰 보여줘요. 항목명·단위·등락 표시를 일관되게 유지해요.

- 컴포넌트: `Card / Table`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8762)

### P. 선택과 이용 조건

선택한 항목과 선택하지 않은 항목, 선택할 수 없는 항목을 구분해요. 필요한 등록 행동이나 이용 조건도 함께 안내해요.

- 컴포넌트: `Card / My · Selected / Default / Disabled`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11849-8857)

## 문서 구성과 AI 도구 사용 기준

- 가이드라인 5개와 예제 16개를 기준으로 유형을 선택해요. 예제에 없는 카드가 사용 불가하거나 폐기된 것은 아니에요. `Card / AD`, `Card / SA`, `Card / Todo` 등은 기존 마스터를 별도로 확인해요.
- 이미지가 포함된 카드에는 실제 콘텐츠 이미지를 사용해요. `Image=False`는 배경색 등을 확인하는 옵션이며, 이미지 생략이나 텍스트 전용 카드로 변경하는 기준이 아니에요. 이미지 영역을 숨기거나 높이를 0으로 줄이지 않아요.
- 가이드라인 3번의 왼쪽은 실제 이미지 적용, 오른쪽은 배경 확인용 `Image=False` 비교예요. 예제 A와 가이드라인 1번에는 이미지를 표시해요.
- 제목·단계·버튼·인디케이터 등은 해당 컴포넌트가 제공하는 옵션 안에서 조절해요. 모든 카드에 같은 속성이 있다고 가정하지 않아요.
- `Selected`는 현재 선택, `Disabled`는 이용 불가를 뜻해요. `Card / My`의 `State` BOOLEAN을 공통 선택 상태로 해석하지 않아요.
- `Card / Summary`의 `SG02`는 적립 예정·완료 수치 요약, `OPS03_01`은 만료 예정 금액과 기한 안내에 사용된 예제예요. 코드 이름만으로 임의의 의미를 추정하지 않아요.
- 마스터 인스턴스와 중첩 구조를 유지하고, 필요한 이미지·텍스트·수치를 상황에 맞게 변경해요. 예제의 금액·날짜·코드·상품명은 샘플이며 운영 정책이나 계산 규칙이 아니에요.
- 문서용 Usage는 360 폭의 예제를 40 간격으로 한 줄에 배열하고, 섹션 여백은 100으로 구성해요. 설명 끝과 Slot 사이 간격은 50이며 Slot은 패딩 없이 좌측·상단 정렬, 높이 Hug로 사용해요. 카드 자체 패딩은 유지해요.
- 하나의 카드만 있는 예제는 Slot 안에 인스턴스를 바로 배치해요. 복수 카드의 비교·간격이 필요한 경우에만 보조 컨테이너를 사용해요.
- 위 문서 배치 값은 실제 화면의 카드 폭·간격·패딩을 일괄 지정하는 규격이 아니에요. 실제 사용 시 해당 마스터와 화면 레이아웃을 따라요.
- Section 1의 아노테이션 41개를 제거했어요. 참고 화면은 마스터나 사용 규칙을 대체하지 않아요.

## 확인 사항

- 이번 업데이트 범위는 가이드라인·예제와 이미지 사용 기준이에요. 마스터의 속성명이나 variant 구성은 변경하지 않았어요.
- 아래 2026-10-08 규격·점검 기록은 당시 조사 결과예요. 노드 수, 미바인딩 수, 스타일 수, 외부 라이브러리 수와 정리 과제를 현재 상태로 단정하지 않아요.
- 기존 표에 기록된 카드 높이는 현재 예제와 다를 수 있어요. 제목 줄 수·선택 옵션·variant에 따라 달라지므로 현재 인스턴스의 Auto Layout과 마스터를 우선해요.
- 현재 예제의 대표 크기에는 News 320×270, Todo / Step 328×151, Summary(SG02) 328×94, Stamp(Grid) 328×232, Stamp(Compare) 328×516, My(Selected) 328×84, My(Disabled) 328×114 등이 있어요. 이를 모든 카드나 상태의 고정 규격으로 확대하지 않아요.

---

## 기존 마스터 규격과 점검 기록 (2026-10-08)

> 아래 내용은 기존 문서의 상세 조사 및 결정 이력을 보존한 기록이에요. 최신 사용 기준은 위 가이드라인·예제를 우선해요. 당시 수치와 미해결 항목은 이번에 전수 재검사하지 않았어요.

## 구성 한눈에 보기

지금까지 문서화한 페이지 중 **가장 큽니다.** 섹션 높이 9,945, 노드 915개, 텍스트 259개입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | 완성형 카드 **17종** |
| y 8193 → 8333 | Child Item → Card Item | `.primitive` 카드 **2종** |
| y 9379 | Icon | `.primitive` 아이콘 **2종** |

다른 페이지와 성격이 다릅니다. Chip·Button처럼 **하나의 컴포넌트를 variant로 확장한 구조가 아니라**, 서비스 화면별로 만들어진 **독립적인 카드들을 모아 둔 카탈로그**에 가깝습니다. 이름도 `Card / News` · `Card / Tax` · `Card / Shopping`처럼 **용도별**로 나뉩니다.

### 전체 목록

| # | 이름 | 타입 | Variant / Props | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Card / Invite / Code` | Set | `Property 1` 2종 + `List Footer` | 312 × 195~240 |
| 2 | `Card / Thunderbolt` | Set | `Type` 3종 + `Arrow` · `Text` | 328 × 103~222 |
| 3 | `Card / Now` | Set | `Type` 2종 + `Indicator` | 328 × 178 / 354 |
| 4 | `Card / Shopping` | Set | `Property 1` 2종 + `적립예정금` · `Bubble` | 326 × 251 / 259 |
| 5 | `Card / Stamp` | Set | `Layout` 2종 | 328 × 235 / 668 |
| 6 | `Card / Summary` | Set | `Property 1` **6종** | 326~328 × 67~155 |
| 7 | `Card / My` | Set | `Property 1` 3종 + `Text Button` · `State` | 326~328 × 114 / 144 |
| 8 | `Card / News` | Component | `Indicator` | 320 × 288 |
| 9 | `Card / AD` | Component | — | 320 × 242 |
| 10 | `Card / SA` | Component | — | 360 × 258 |
| 11 | `Card / Invite / Ranking` | Component | `Ranking` | 312 × 186 |
| 12 | `Card / Tax` | Component | — | 312 × 153 |
| 13 | `Card / Shopping / Naver` | Component | — | 320 × 215 |
| 14 | `Card / Todo / Step` | Component | `Title` · `Button` · `Indicator` · `Step` | 328 × 151 |
| 15 | `Card / Todo` | Component | — | 328 × 155 |
| 16 | `Card / Chart` | Component | — | 328 × 362 |
| 17 | `Card / Table` | Component | — | 328 × 392 |
| 18 | `.primitive / Card / News` | Set | `Horizontal` 2종 + 4 BOOLEAN + SLOT | 320 × 110 / 250 |
| 19 | `.primitive / Card / Shopping` | Set | `Type` 2종 + 7 BOOLEAN + SLOT | 328 × 100 / 156 |
| 20 | `Card / Invite / Icon` | Set | `Property 1` 4 × `Size` 2 (**8종**) | 24 / 32 정사각 |
| 21 | `Card / My / Icon` | Set | `Property 1` 3종 | 20~22 정사각 |

---

## 1. Component Set 7종

### Card / Invite / Code

**Node** `9669:11864` · 2 variants · 312 폭

친구 초대 코드를 보여주는 카드입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `Empty` | `Empty` · `Default` |
| `List Footer` | BOOLEAN | `true` | — |

| Variant | 크기 | 의미 |
| --- | --- | --- |
| `Default` | 312 × 240 | 초대받은 친구 목록이 있는 상태 |
| `Empty` | 312 × 195 | "아직 선물을 받은 친구가 없어요" |

공통 — Padding `500/500/0/400` (20/20/0/16), Gap `Spacing/500`(20), Radius `Corner radius/300`(12), Fill `Color/Gray_White`, Stroke `Color/Gray_850` 1px

> **하단 패딩만 `0`** 입니다. `List Footer`가 자체 여백을 갖기 때문으로 보이지만, `List Footer=false`로 끄면 아래가 붙습니다.

### Card / Thunderbolt

**Node** `9718:23071` · 3 variants · 328 폭

번개 적립(이벤트) 안내 카드입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Default` | `Default` · `Step` · `Title` |
| `Arrow` · `Text` | BOOLEAN | `true` | — |

| Variant | 크기 | Padding | Radius | Fill |
| --- | --- | --- | --- | --- |
| `Default` | 328 × 103 | `600/500/600/500` | `r400`(16) | `Gray_White` |
| `Step` | 328 × 208 | `600/500/600/500` | `r400`(16) | `Gray_White` |
| `Title` | 328 × 222 | **0** | **0** | **없음** |

**`Type=Title`만 카드 형태가 아닙니다.** 배경·라운드·패딩이 전부 없는 투명 래퍼로, 제목 영역과 카드를 함께 묶은 묶음입니다. 같은 `Type` 축에 "카드 2종 + 래퍼 1종"이 섞여 있습니다 → [점검 4](#4-일부-variant가-카드가-아니라-래퍼)

### Card / Now

**Node** `9562:36348` · 2 variants · 328 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Action` | `Action` · `Ranking` |
| `Indicator` | BOOLEAN | `true` | — |

| Variant | 크기 |
| --- | --- |
| `Action` | 328 × 178 |
| `Ranking` | 328 × 354 |

공통 — **Padding 0 · Radius 0 · 배경 없음**, Gap `Spacing/400`(16)

두 variant 모두 **래퍼**입니다. 실제 카드 모양은 안쪽 `.primitive / Card / Shopping` 인스턴스가 갖습니다.

### Card / Shopping

**Node** `9938:33002` · 2 variants · 326 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `Gold` | `Gold` · `Stamp` |
| `Pending Gold` | BOOLEAN | `true` | — |
| `Bubble` | BOOLEAN | `true` | — |

(2026-10-08 `적립예정금` → `Pending Gold` 정리 완료 → [점검 2](#2-프로퍼티-네이밍이-제각각))

| Variant | 크기 |
| --- | --- |
| `Gold` | 326 × 251 |
| `Stamp` | 326 × 259 |

공통 — Padding `500/400/500/400` (20/16/20/16), **가로 오토레이아웃**, Radius `r400`(16), Stroke `Color/Gray_850` 1px

이 페이지에서 **스타일 미적용 텍스트가 가장 많이 몰려 있는 컴포넌트**입니다(22건) → [점검 5](#5-스타일-미적용-텍스트-38건)

### Card / Stamp

**Node** `9573:37232` · 2 variants · 328 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Layout` | VARIANT | `Grid` | `Grid` · `Compare` |

| Variant | 크기 | 용도 |
| --- | --- | --- |
| `Grid` | 328 × 235 | 스탬프 격자 보기 |
| `Compare` | 328 × **668** | 매장 비교 보기 |

공통 — Padding `Spacing/400`(16) 사방, Radius `r400`(16), Stroke `Color/Gray_850` 1px, Gap `Grid` 12 · `Compare` 16

`Compare`는 **높이가 668로 이 페이지에서 가장 큽니다.** `Grid`의 약 3배입니다.

### Card / Summary

**Node** `9935:26524` · **6 variants** · 326~328 폭

이 페이지에서 **variant가 가장 많은 컴포넌트**입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `CP02` | `CP02` · `CG09` · `SG02` · `CS02` · `OPS03_01` · `OPS03_02` |

**variant 값이 전부 화면 코드**입니다. 디자인 시스템 안에서는 의미를 알 수 없습니다 → [점검 3](#3-card--summary-variant-값이-화면-코드)

| Variant | 크기 | 방향 | Padding | Stroke |
| --- | --- | --- | --- | --- |
| `CP02` | 326 × 70 | 가로 | `600` 사방 | `Gray_850` 1px |
| `CG09` | 326 × 155 | 세로 | **0** | `Gray_850` 1px |
| `SG02` | 326 × 94 | 가로 | `500/600/500/600` | `Gray_850` 1px |
| `CS02` | 326 × 67 | 가로 | `500/600/500/600` | **`Gray_900`** 1px |
| `OPS03_01` | 328 × 135 | 세로 | **0** | **`Gray_900`** 1px |
| `OPS03_02` | 326 × 87 | 가로 | `500/0/500/0` | `Gray_850` 1px |

전부 Radius `r400`(16)이고 `OPS03_01`을 뺀 나머지는 Fill `Color/Gray_White`입니다.

**테두리 색이 두 가지로 갈립니다** — `Gray_850` 4종 vs `Gray_900` 2종 → [점검 6](#6-테두리-색이-컴포넌트마다-다름)

### Card / My

**Node** `10034:137103` · 3 variants · 326~328 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Property 1` | VARIANT | `Default` | `Default` · `Selected` · `Disabled` |
| `Text Button` | BOOLEAN | `true` | — |
| `State` | BOOLEAN | `true` | — |

| Variant | 크기 | 방향 | Fill | Stroke |
| --- | --- | --- | --- | --- |
| `Default` | 326 × 114 | 가로 | `Gray_White` | `Color/Gray_800` 1px |
| `Selected` | 326 × 114 | 가로 | `Gray_White` | **`Color/Primary_Orange` 1px** |
| `Disabled` | 328 × **144** | **세로** | **`Color/Gray_950`** | **없음** |

공통 — Padding `Spacing/500`(20) 사방, Radius `r300`(12)

선택 상태를 **테두리 색**으로 표현하는 점은 `Chip / Filter / Item`와 같은 방식입니다.

**`Disabled`만 구조가 다릅니다** — 높이가 30 더 크고, 방향이 세로이며, 테두리 없이 회색 면으로 칠합니다.

> `State` BOOLEAN은 **`Disabled` variant에만 연결**되어 있습니다. `Default`·`Selected`에서는 토글해도 아무 변화가 없습니다 → [점검 7](#7-ℹ-card--my의-state가-한-variant에만-연결됨--의도된-설계)

---

## 2. Component 10종

variant 없는 단일 컴포넌트입니다.

| 컴포넌트 | 크기 | Padding | Gap | Radius | Fill | Stroke |
| --- | --- | --- | --- | --- | --- | --- |
| `Card / News` `9517:26231` | 320 × 288 | 0 | `300`(12) | 0 | 없음 | — |
| `Card / AD` `9552:23643` | 320 × 242 | 0 | 0 | `r400`(16) | `Gray_White` | — |
| `Card / SA` `9562:30657` | 360 × 258 | `500/600/750/600` | `500`(20) | 0 | 없음 | `Gray_900` **하단 1px만** |
| `Card / Invite / Ranking` `9668:6099` | 312 × 186 | `500/400/500/400` | `500`(20) | `r300`(12) | 없음 | `Gray_850` 1px |
| `Card / Tax` `9718:23592` | 312 × 153 | `500` 사방 | `500`(20) | `r400`(16) | 없음 | `Gray_900` 1px |
| `Card / Shopping / Naver` `9669:21503` | 320 × 215 | `500` 사방 | `250`(10) | `r250`(10) | `Gray_White` | — |
| `Card / Todo / Step` `9699:25790` | 328 × 151 | `500/400/500/500` | `400`(16) | `r400`(16) | `Gray_White` | `Gray_850` 1px |
| `Card / Todo` `9716:6021` | 328 × 155 | 0 | 0 | `r400`(16) | `Gray_White` | `Gray_850` 1px |
| `Card / Chart` `9938:29590` | 328 × 362 | `600/0/200/0` | `200`(8) | `r400`(16) | `Gray_White` | `Gray_850` 1px |
| `Card / Table` `9938:29624` | 328 × 392 | 0 | 0 | `r400`(16) | 없음 | `Gray_850` 1px |

### 눈에 띄는 점

- **`Card / SA`는 카드가 아닙니다.** 테두리가 `strokeBottomWeight = 1`, 나머지 세 변은 `0`입니다. 라운드도 0이라 **아래 구분선이 있는 목록 행**에 가깝습니다. 이름만 Card 계열입니다.
- **`Card / News`는 래퍼**입니다. 라운드·배경이 없고 Gap만 12입니다. 실제 카드는 안쪽 `.primitive / Card / News`가 그립니다.
- `Card / Todo / Step`의 좌우 패딩이 `400/500`(16/20)으로 **비대칭**입니다. 다른 카드는 모두 좌우가 같습니다.
- `Card / Chart`는 좌우 패딩이 0이고 상하만 `600/200`(24/8)입니다. 차트가 카드 폭을 꽉 채우기 때문입니다.

---

## 3. Child Item — Card Item

### .primitive / Card / News

**Node** `9517:26464` · 2 variants · 320 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Horizontal` | VARIANT | `False` | `False` · `True` |
| `Image` · `Time` · `AD` · `Badge` | BOOLEAN | `true` | — |
| `Image Slot` | **SLOT** | — | — |

| Variant | 크기 | 방향 | Padding | Stroke |
| --- | --- | --- | --- | --- |
| `False` | 320 × 250 | 세로 | **0** | 없음 |
| `True` | 320 × 110 | 가로 | `400/500/400/500` | `Gray_850` 1px |

둘 다 Radius `r400`(16), Fill `Color/Gray_White`.

세로형은 **이미지가 위에 꽉 차고**, 가로형은 **텍스트 왼쪽 + 썸네일 오른쪽**입니다. 그래서 세로형만 패딩이 0입니다.

### .primitive / Card / Shopping

**Node** `9562:31098` · 2 variants · 328 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Action` | `Action` · `Ranking` |
| `Discount` · `AD` · `Blur` | BOOLEAN | `false` | — |
| `Partner` · `Badge` · `Ranking` · `Image` · `Title` | BOOLEAN | `true` | — |
| `Image Slot` | **SLOT** | — | — |

| Variant | 크기 | 방향 | Padding | Radius | Fill |
| --- | --- | --- | --- | --- | --- |
| `Action` | 328 × 156 | 세로 | `Spacing/150`(6) 사방 | `r300`(12) | **그라데이션** |
| `Ranking` | 328 × 100 | 가로 | 0 | `r200`(8) | `Gray_White` |

**BOOLEAN 프로퍼티가 7개**로 이 페이지에서 가장 많습니다. 할인·광고·블러·파트너·배지·순위·이미지·제목을 각각 켜고 끌 수 있어 조합이 넓습니다.

`Action`의 배경은 **선형 그라데이션**이고, 이는 토큰에 바인딩되어 있습니다.

> 두 primitive 모두 **SLOT 프로퍼티(`Image Slot`)** 를 씁니다. 파일 전체에서 SLOT을 쓰는 몇 안 되는 컴포넌트입니다.

---

## 4. Icon

### Card / Invite / Icon

**Node** `9669:5780` · **8 variants** (`Property 1` 1~4 × `Size` L/S)

| Size | 크기 |
| --- | --- |
| `L` | 32 × 32 |
| `S` | 24 × 24 |

4 × 2 = **8조합이 모두 존재하는 완전 매트릭스**입니다.

`Property 1`의 값이 `1` · `2` · `3` · `4`라 **무엇을 고르는지 알 수 없습니다.** 실제로는 초대 순위(1~4등) 뱃지이고, 별 모양 안에 숫자가 들어갑니다.

| 순위 | 별 색 |
| --- | --- |
| 1 · 3 | `#FFD00E` (금색) |
| 2 | `#FFBC57` |
| 4 | `#FEFEFE` |

숫자 텍스트는 `L` = 16 ExtraBold, `S` = 12 ExtraBold로 **둘 다 스타일 미적용**입니다.

### Card / My / Icon

**Node** `10034:137009` · 3 variants

| Variant | 크기 | 내용 |
| --- | --- | --- |
| `OCB` | 20 × 20 | OCB 로고 |
| `Npay` | 20 × 20 | 네이버페이 로고 |
| `Cash` | **22 × 22** | 현금 아이콘 |

**`Cash`만 22로 2px 큽니다.** 나란히 놓이는 아이콘이라 정렬이 어긋날 수 있습니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 카드 폭 | **326 / 328**이 표준 · 312(Invite·Tax) · 320(News·AD·Naver) · 360(SA) |
| 라운드 | **`Corner radius/400`(16)** 가 기본 · `r300`(12) · `r250`(10) · `r200`(8) |
| 테두리 | **`Color/Gray_850` 1px**이 기본 · `Gray_900` · `Gray_800` · 선택 시 `Primary_Orange` |
| 배경 | `Color/Gray_White` · 비활성 `Color/Gray_950` |
| 패딩 | `Spacing/500`(20) 또는 `Spacing/600`(24)이 가장 흔함 · 좌우 `Spacing/400`(16)도 사용 |
| 간격 | `Spacing/500`(20) · `Spacing/400`(16) · `Spacing/300`(12) |
| 레이아웃 | 대부분 세로 오토레이아웃, 요약형은 가로 |

### 자주 쓰이는 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `b400_14_regular` | 본문 (가장 많음) |
| `t1000_15_bold` · `t800_17_bold` | 카드 제목 |
| `t1300_15_medium` · `t1360_13_medium` | 보조 정보 |
| `b500_13_regular` · `c100_12_regular` | 캡션 · 메타 |
| `t1050_14_bold` · `t1060_13_bold` | 강조 라벨 · 버튼 |

### 폰트

| 폰트 | 건수 | 비고 |
| --- | --- | --- |
| Pretendard Regular | 107 | |
| Pretendard Bold | 92 | |
| Pretendard Medium | 42 | |
| Pretendard ExtraBold | 9 | **Syrup 타입 스케일에 없는 굵기** |
| Pretendard SemiBold | 8 | **Syrup 타입 스케일에 없는 굵기** |

전부 Pretendard로 통일되어 있습니다. 다만 ExtraBold·SemiBold는 토큰화된 텍스트 스타일에 존재하지 않는 굵기입니다 → [점검 5](#5-스타일-미적용-텍스트-38건)

---

## 점검 필요 사항

이 페이지는 **지금까지 문서화한 14개 페이지 중 정리할 항목이 가장 많습니다.** 서비스 화면에서 쓰던 카드를 그대로 모아 온 흔적이 남아 있습니다.

> 페이지 이름에 붙어 있던 **🔴 표시가 제거**되어 현재는 `Card`입니다.

### 1. ✅ 원격 텍스트 스타일 14건 로컬 교체 (2026-10-08 완료)

로컬에 같은 이름의 스타일이 있는데도 **다른 라이브러리의 스타일이 적용**되어 있었습니다.

| 스타일 | 건수 | 위치 | 처리 |
| --- | --- | --- | --- |
| `b400_14_regular` | 13 | `Card / Stamp` 10 · `Card / Thunderbolt` 3 | ✅ 동일 이름 로컬로 교체 |
| `b300_15_regular` | 1 | `Card / Thunderbolt` | ✅ 동일 이름 로컬로 교체 |
| `Body/SemiBold/14` | 3 | `Card / Thunderbolt` | ✅ **`t1050_14_bold`로 교체** |

**Card 페이지의 원격 텍스트 스타일은 0건**입니다.

#### ⚠️ 무손실이 아니었습니다

교체 전 "무손실"로 예상했으나, **같은 이름인데 라인하이트가 달랐습니다.**

| 스타일 | 원격 | 로컬 | 차이 |
| --- | --- | --- | --- |
| `b400_14_regular` | 14px / LH **21** / LS −0.5 | 14px / LH **18** / LS −0.5 | LH **−3** |
| `b300_15_regular` | 15px / LH **23** / LS −0.5 | 15px / LH **19** / LS −0.5 | LH **−4** |

폰트·크기·자간은 같고 **라인하이트만 줄었습니다.** `Button / Alert`에서 겪은 것과 같은 패턴입니다.

그 결과 일부 카드 높이가 줄었습니다.

| 컴포넌트 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Card / Thunderbolt` ▸ `Default` | 328 × 103 | 328 × **100** |
| `Card / Thunderbolt` ▸ `Step` | 328 × 208 | 328 × **202** |
| `Card / Stamp` ▸ `Grid` | 328 × 235 | 328 × **232** |
| `Card / Stamp` ▸ `Compare` | 328 × 668 | 328 × **656** |

렌더링은 스크린샷으로 확인했고 **잘림·겹침은 없습니다.** 로컬 스타일이 Syrup 기준이므로 이 값이 올바른 상태입니다.

#### 처리 방식

원본이 어디냐에 따라 두 가지로 나뉘었습니다.

| 방식 | 대상 | 비고 |
| --- | --- | --- |
| **원본 수정** | `9110:26603` · `9110:26927` (Product Grid) · `9718:13075` (Card) | `Card / Stamp` 10건은 Product Grid 원본 2개를 고쳐 일괄 반영 |
| **인스턴스 오버라이드** | `Card / Thunderbolt` 3건 | 원본이 **외부 라이브러리 컴포넌트**(`Icon Size=M, …`)라 이 파일에서 수정 불가 |

> `Card / Thunderbolt`와 `Card / Shopping` 일부는 **다른 Figma 라이브러리의 컴포넌트를 인스턴스로 품고 있습니다.** 원본을 이 파일에서 고칠 수 없어 오버라이드로만 대응됩니다. 근본 해결은 해당 라이브러리 쪽 정리가 필요합니다.

#### `Body/SemiBold/14` → `t1050_14_bold` (2026-10-08)

Syrup 스케일에 없는 이름이라 대체 스타일 결정이 필요했고, **14px Bold**로 정했습니다.

| | 폰트 | 크기 | LH | LS |
| --- | --- | --- | --- | --- |
| `Body/SemiBold/14` (원격) | Pretendard **SemiBold** | 14 | 21 | — |
| `t1050_14_bold` (로컬) | Pretendard **Bold** | 14 | **18** | −0.3 |

굵기와 라인하이트가 모두 바뀌었지만 **`Card / Thunderbolt` 크기는 변화 없습니다**(`Default` 328×100 · `Step` 328×202 · `Title` 328×222). 단계 설명이 2줄이라 줄어든 라인하이트가 기존 여백에 흡수되었습니다.

`Card / Thunderbolt`의 Stepper가 외부 라이브러리에서 **로컬 컴포넌트로 전환**되면서 원본 수정이 가능해졌고, 같은 스타일을 쓰던 `Stepper` 페이지 19건도 함께 해소되었습니다.

#### 파일 전체 현황

Card 페이지는 **0건**입니다. 다른 페이지에 17건이 남아 있습니다.

| 페이지 | 스타일 | 건수 | 로컬 동일 이름 |
| --- | --- | --- | --- |
| `Header` | `syrup_typo/syrup_typo_t1400` 5 · `t1400_20_regular` 1 | 6 | 일부 있음 |
| `AD` | `typeset_lg_medium` 2 · `syrup_typo/c200` 2 | 4 | 없음 |
| `Product List` | `typeset_xs_bold` 2 · `b100_17_regular` 2 | 4 | 없음 |
| `Tab` | `b100_17_regular` 2 · `b400_14_regular` 2 | 4 | 일부 있음 |
| `Product Grid` | `b400_14_regular` | 1 | **있음** |

`t1400_20_regular` · `b400_14_regular` **4건은 동일 이름 로컬로 바로 교체 가능**하고, 나머지 13건은 Syrup 스케일에 없는 이름이라 대체 스타일 결정이 필요합니다.

### 2. 프로퍼티 네이밍이 제각각

같은 페이지 안에서 축 이름 규칙이 세 가지로 갈립니다.

| 컴포넌트 | 프로퍼티명 | 문제 |
| --- | --- | --- |
| `Card / Invite / Code` | `Property 1` | Figma 기본 이름 |
| `Card / Shopping` | `Property 1` · ~~`적립예정금`~~ → **`Pending Gold`** ✅ | 기본 이름 (한글명은 해결) |
| `Card / Summary` | `Property 1` | 기본 이름 |
| `Card / My` | `Property 1` | 기본 이름 |
| `Card / Invite / Icon` | `Property 1` | 기본 이름 |
| `Card / My / Icon` | `Property 1` | 기본 이름 |
| `Card / Thunderbolt` · `Card / Now` · `.primitive / Card / Shopping` | `Type` | ✅ 양호 |
| `Card / Stamp` | `Layout` | ✅ 양호 |
| `.primitive / Card / News` | `Horizontal` | ✅ 양호 |

**`Property 1`이 6개 컴포넌트에 남아 있습니다.** 파일 전체 61개 중 6개가 이 페이지입니다.

#### ✅ 한글 프로퍼티명 정리 (2026-10-08 완료)

`적립예정금`은 **파일 전체에서 유일한 한글 프로퍼티명**이었습니다. 다른 BOOLEAN은 모두 영문(`Bubble` · `Image` · `Badge` …)이라 혼자 튀었습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Card / Shopping` BOOLEAN | `적립예정금` | **`Pending Gold`** |

이로써 파일 전체의 프로퍼티명이 영문으로 통일됐습니다.

#### 남은 `Property 1` 6건

| 컴포넌트 | 현재 | 제안 |
| --- | --- | --- |
| `Card / Invite / Code` | `Property 1` | `State` (`Empty`/`Default`이므로) |
| `Card / Shopping` | `Property 1` | `Type` |
| `Card / Summary` | `Property 1` | `Type` |
| `Card / My` | `Property 1` | `State` (`Default`/`Selected`/`Disabled`이므로) |
| `Card / Invite / Icon` | `Property 1` | `Rank` |
| `Card / My / Icon` | `Property 1` | `Type` |

### 3. `Card / Summary` variant 값이 화면 코드

| 값 | 성격 |
| --- | --- |
| `CP02` · `CG09` · `SG02` · `CS02` | 대문자 + 2자리 |
| `OPS03_01` · `OPS03_02` | 대문자 + 언더스코어 |

#### ✅ 표기 통일 (2026-10-08 완료)

`cg09` 하나만 소문자여서 표기가 어긋나 있었습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| variant 값 | `cg09` | **`CG09`** |
| `Property 1` 옵션 | `[CP02, cg09, SG02, CS02, OPS03_02, OPS03_01]` | **전부 대문자** |

#### 남은 사항

코드 체계는 **팀 내 공용어로 유지**합니다. 다만 디자인 시스템만 봐서는 각 코드가 어떤 화면인지 알 수 없어, 컴포넌트를 처음 쓰는 사람은 6개를 하나씩 눌러 보며 찾아야 합니다.

**Figma Description에 코드 ↔ 화면 매핑을 적어 두면** 이 부분이 해소됩니다.

### 4. 일부 variant가 카드가 아니라 래퍼

배경·라운드·패딩이 전부 없어 **카드 모양을 갖지 않는 항목**이 섞여 있습니다.

| 컴포넌트 | 해당 variant | 상태 |
| --- | --- | --- |
| `Card / Thunderbolt` | `Type=Title` | 패딩 0 · 라운드 0 · 배경 없음 |
| `Card / Now` | `Type=Action` · `Type=Ranking` (**둘 다**) | 패딩 0 · 라운드 0 · 배경 없음 |
| `Card / News` | (단일 컴포넌트) | 라운드 0 · 배경 없음 |
| `Card / SA` | (단일 컴포넌트) | 라운드 0 · **하단 테두리 1px만** |

`Card / Now`와 `Card / News`는 **안쪽 `.primitive`가 카드를 그리고 바깥은 묶음 역할**만 합니다. 구조상 자연스럽습니다.

문제는 **`Card / Thunderbolt`** 입니다. 같은 `Type` 축에 카드 2종(`Default`·`Step`)과 래퍼 1종(`Title`)이 섞여 있어, `Type`을 바꾸면 **카드가 사라지는 것처럼 보입니다.**

`Card / SA`는 **카드가 아니라 하단 구분선이 있는 목록 행**입니다. Card 페이지가 아니라 List Row 계열이 어울립니다.

### 5. 스타일 미적용 텍스트 38건

텍스트 스타일 없이 폰트·크기를 직접 지정한 항목입니다. (보드 표기용 6건 제외)

| 크기 · 굵기 | 건수 | 주요 위치 |
| --- | --- | --- |
| **11 Medium** | **12** | `Card / Shopping` (금액·안내 라벨) |
| 16 ExtraBold | 5 | `Card / Invite / Icon` 4 · `Card / Invite / Ranking` 1 |
| 12 ExtraBold | 4 | `Card / Invite / Icon` |
| 10 Bold | 3 | `Card / Todo / Step` (단계 번호) |
| 14 Regular | 3 | `Card / AD` · `Card / Shopping` |
| 17 Regular | 2 | `Card / Shopping` |
| 11 Bold | 2 | `Card / Now` · `.primitive / Card / Shopping` |
| 10 Regular | 2 | `Card / News` · `.primitive / Card / News` (AD 표기) |
| 그 외 | 5 | 24 Bold · 15 Regular · 12 Bold · 12(굵기 혼합) · 14 SemiBold 각 1 |

세 묶음으로 나뉩니다.

**(1) 토큰에 있는데 안 쓴 경우** — `14 Regular`(→`b400_14_regular`), `15 Regular`(→`b300_15_regular`), `17 Regular`, `24 Bold` 등은 대응하는 로컬 스타일이 있어 **바로 교체 가능**합니다.

**(2) 스케일 밖 굵기** — **SemiBold 8건 · ExtraBold 9건**은 Syrup 텍스트 스타일에 아예 없는 굵기입니다. Pretendard 자체는 통일되어 있지만 굵기 체계를 벗어납니다. 숫자 뱃지(`16/12 ExtraBold`)처럼 **의도적 예외**일 수 있으니 판단이 필요합니다.

**(3) 작은 크기 — ℹ️ 토큰화하지 않음 (2026-10-08 결정)**

`10 Regular` · `10 Bold` · `11 Medium` · `11 Bold` 등 **10~11px 구간은 토큰으로 만들지 않습니다.** Bubble 때 정한 "너무 작은 폰트는 예외로 보고 시스템으로 관리하지 않는다"는 기준을 그대로 적용합니다.

`11 Medium`이 12건으로 `Card / Shopping` 한 곳에 몰려 있어 13 Medium 때와 같은 검토 대상으로 봤지만, **11px은 크기 자체가 기준선 아래**라 등록하지 않기로 했습니다.

> 13 Medium은 토큰(`t1360_13_medium`)으로 등록한 선례가 있습니다. **13px이 시스템으로 관리하는 하한**이라고 보면 됩니다.

### 6. 테두리 색이 컴포넌트마다 다름

바깥 프레임에 테두리를 가진 컴포넌트·variant **22개**를 전수 조사한 결과입니다.

| 토큰 | HEX | 건수 |
| --- | --- | --- |
| `Color/Gray_800` | **#E4E4E4** (가장 진함) | **1** |
| `Color/Gray_850` | **#EDEDED** (기준) | **16** |
| `Color/Gray_900` | **#F2F2F2** (가장 연함) | **4** |
| `Color/Primary_Orange` | — | 1 |

세 회색이 매우 가깝습니다. `Gray_850` ↔ `Gray_900`은 **5단계 차이라 나란히 두지 않으면 구분이 거의 안 됩니다.**

#### `Gray_900` 4건의 내역

| # | 위치 | Node | 평가 |
| --- | --- | --- | --- |
| 1 | `Card / Summary` ▸ `CS02` | `9935:26531` | **정리 대상** |
| 2 | `Card / Summary` ▸ `OPS03_01` | `9937:28944` | **정리 대상** |
| 3 | `Card / Tax` | `9718:23592` | **정리 대상** |
| 4 | `Card / SA` | `9562:30657` | **별개 — 카드 테두리 아님** |

**`Card / Summary`가 가장 문제입니다.** 같은 컴포넌트셋 6종 중 4종은 `Gray_850`, 2종은 `Gray_900`으로 갈려 있습니다. 크기·라운드·패딩이 거의 같은 요약 카드끼리 테두리만 다르며, 화면에서 차이를 알아보기 어려워 **의도로 보기 어렵습니다.**

`Card / Tax`(312 폭)는 같은 폭의 `Card / Invite / Ranking`이 `Gray_850`을 쓰는 것과 어긋납니다.

**`Card / SA`는 성격이 다릅니다.** 테두리가 `0/0/1/0`으로 **하단 1px만** 있고 라운드도 0입니다. 카드 외곽선이 아니라 **목록 구분선**이라 위 3건과 같은 기준으로 볼 수 없습니다 → [점검 4](#4-일부-variant가-카드가-아니라-래퍼)

#### `Gray_800` 1건 — **의도된 강조**

`Card / My` ▸ `Default` `10034:136953` 한 건입니다.

| Variant | 테두리 |
| --- | --- |
| `Default` | `Color/Gray_800` (#E4E4E4, 더 진함) |
| `Selected` | `Color/Primary_Orange` |
| `Disabled` | 없음 (`Color/Gray_950` 면) |

**라디오 버튼처럼 고르는 선택형 카드**라 평소에도 테두리가 또렷해야 하고, 선택 시 오렌지로 바뀝니다. 정리 대상이 아닙니다.

#### 정리 방향

Border 문서에서 **"1px 구분선·보더는 `Color/Gray_850`"** 으로 정리한 기준에 맞추면, **`Summary` 2건 + `Tax` 1건 = 3건**을 `Gray_850`으로 바꾸면 카드 테두리가 하나로 통일됩니다. 세 색이 워낙 가까워 **시각적 변화는 거의 없습니다.**

### 7. ℹ️ `Card / My`의 `State`가 한 variant에만 연결됨 — **의도된 설계**

| Variant | `Text Button` 연결 | `State` 연결 |
| --- | --- | --- |
| `Default` | ✅ | ❌ |
| `Selected` | ✅ | ❌ |
| `Disabled` | ✅ | ✅ |

`State` BOOLEAN은 **`Disabled`에서만 레이어를 토글**합니다. 나머지 두 variant에서는 패널에 보이지만 켜고 꺼도 변화가 없습니다.

**의도된 설계이며 정리 대상이 아닙니다.** `Disabled` 상태에서만 추가로 보여줄 안내 요소가 있고, 다른 상태에는 해당하지 않기 때문입니다.

> 사용 시 참고 — `Default`·`Selected`에서 `State`를 토글해도 아무 일이 일어나지 않는 것이 정상입니다.

### 8. 미바인딩 색상 25건 — 대부분 로고·일러스트

| 색 | 건수 | 성격 |
| --- | --- | --- |
| `#1F80FF` | 6 | Thunderbolt 아이콘·시간 표기, Grid Scroll 아이콘 |
| `#FE0955` | 4 | `Card / My` · My/Icon (네이버페이 계열 로고) |
| `#FFD00E` · `#FFBC57` · `#FEFEFE` | 6 | Invite/Icon 별 뱃지 |
| `#00C01E` · `#00A1FF` | 2 | 파트너 로고 (네이버 등) |
| `#000000` | 2 | backdrop-filter 레이어 |
| 그 외 | 5 | `#2B67BD` · `#BE820B` · `#D8D8D8` · `#FCE8E1` · `#2B67BD` |

**대부분은 브랜드 로고와 일러스트 색**이라 토큰화 대상이 아닙니다. Badge·Button에서 정리한 기준과 같습니다.

다만 **`#1F80FF` 6건은 확인이 필요합니다.** `Card / Thunderbolt`의 `Time` 텍스트와 `.primitive / Stepper / NumberIcon` 배경에 쓰이는데, 로고가 아니라 **UI 색**으로 보입니다. `Color/Secondary_Blue`(#3496F4)가 이미 있어 역할이 겹칩니다.

### 9. ✅ 외부 라이브러리 Color 토큰 8건 교체 (2026-10-08 완료)

이름은 Syrup과 같은데 **다른 라이브러리의 변수에 바인딩**되어 있었습니다.

| 토큰 | 건수 | 위치 | 원격 값 | 로컬 값 |
| --- | --- | --- | --- | --- |
| `Color/Gray_100` | 3 | `Card / Shopping` 내부 | #222222 | #222222 |
| `Color/Gray_500` | 2 | `Card / Now` 내부 | #999999 | #999999 |
| `Color/Gray_White` | 1 | `Card / Now` 내부 | #FFFFFF | #FFFFFF |
| `Color/Secondary_Yellow` | 1 | `Card / Shopping` 내부 | #FFBE3B | #FFBE3B |
| `Color/Gray_400` | 1 | `Card / Shopping` 내부 | #777777 | #777777 |

**값이 전부 동일해 무손실 교체**였습니다. 스타일 교체(점검 1)와 달리 여기서는 실제로 차이가 없었습니다.

| 위치 | 처리 |
| --- | --- |
| `Card / Now` 3건 | 원본(Indicator 페이지)은 이미 로컬이었고, **Card 페이지 쪽 오버라이드가 원격**이라 해당 노드를 직접 교체 |
| `Card / Shopping` 5건 | 원본이 외부 라이브러리 컴포넌트라 오버라이드로 교체 → 이후 **해당 레이어가 통째로 삭제**되어 무의미해짐 ([12](#12-기타-정리-대상)) |

**Card 페이지의 외부 Color 토큰은 0건**이 되었습니다. 남은 외부 토큰은 `Spec docs` 7건(문서 레이아웃 전용, 의도된 사용)뿐입니다.

> 점검 1의 스타일 교체로 해당 텍스트에 걸려 있던 **외부 타이포그래피 변수**(`fontSize` · `lineHeights` · `letterSpacing` 등 각 14건)도 함께 해소되었습니다.

### 10. ⚠️ 제어문자 8건 — **오탐이었음 (2026-10-08 정정)**

초판에 "텍스트 안에 U+2028(줄 구분자)이 8건 있다"고 적었으나 **사실이 아닙니다.**

검출에 쓴 정규식이 `[\u0000-\u001F]`였는데, 이 범위에 **일반 개행 `\n`(U+000A)이 포함**됩니다. 두 줄짜리 텍스트는 모두 걸려들었고, 그것을 제어문자로 잘못 보고했습니다.

실제 값을 구분해 재검사한 결과입니다.

| 구분 | Card 페이지 | 파일 전체 |
| --- | --- | --- |
| **U+2028 / U+2029** (줄·문단 구분자 — 진짜 문제) | **0건** | **2건** |
| **진짜 제어문자** (개행·탭 제외) | **0건** | **0건** |
| 일반 개행 `\n` 포함 텍스트 (정상) | 8건 | 137건 |

**Card 페이지에는 고칠 것이 없었습니다.** 제가 8건으로 센 것은 전부 **정상적인 두 줄 텍스트**입니다.

파일 전체에 남은 진짜 U+2028은 **2건**이며, 둘 다 보드 설명문 오버라이드입니다.

| 페이지 | Node | 내용 |
| --- | --- | --- |
| `AD` | `I10403:6795;8444:9504` | "광고 정보를 노출하는 영역이에요.⏎사용자에게…" |
| `Text Field` | `I8795:37748;8444:9504` | "사용자가 텍스트를 입력하거나…⏎검색어…" |

> Bottom CTA 문서에 기록된 **2026-10-01 제어문자 14건 정리는 별개이며 정확합니다.** 그쪽은 텍스트 본문이 아니라 **레이어·variant 이름**에 들어 있던 U+0008 · U+001D로, 이번 오탐과 성격이 다릅니다.

### 11. 라운드 `83.33` 6건 — 디자인 값 아님

| 위치 | 건수 |
| --- | --- |
| `Card / Todo / Step` › `Icon` | 3 |
| `Card / Thunderbolt` › `.primitive / Stepper / NumberIcon` | 3 |

전부 **중첩 인스턴스 내부의 원형 아이콘**입니다. 원형 벡터를 사이즈에 맞춰 확대·축소하면서 라운드 값이 비례해 따라간 수치로, Checkbox의 `0.67px` 획이나 Dialog의 `116.84`와 같은 성격입니다.

**렌더링은 완전한 원이라 문제가 없고**, 원본 컴포넌트(Progress Stepper)에서 나온 값이라 이 페이지에서 고칠 대상도 아닙니다.

### 12. 기타 정리 대상

#### ✅ `Card / Shopping`의 보이지 않는 `alarm` 행 제거 (2026-10-08 완료)

두 variant에 **적립 알림 행**(종 아이콘 + "알림 받기")이 들어 있었으나, 양쪽 모두 화면에 나오지 않는 상태였습니다. 숨기는 방식도 서로 달랐습니다.

| Variant | Node | 레이어 | 숨김 방식 |
| --- | --- | --- | --- |
| `Gold` | `9938:30070` | `syrup_home_alert_on` 18×18 | `alarm` 프레임 **`visible = false`** |
| `Stamp` | `9938:30395` | `syrup_ico_16_alert_on_gray400` 16×16 | **레이어 자체 숨김** (구버전 잔재) |
| `Stamp` | `9938:30396` | `syrup_home_alert_on` 18×18 | `alarm` 프레임 **`opacity = 0`** |

`Stamp`에는 아이콘 교체 과정에서 **구버전과 신버전이 겹쳐** 있었습니다. `opacity = 0`은 레이어 목록에서 켜진 것처럼 보여 찾기가 더 어려웠습니다.

**`alarm` 프레임이 통째로 제거**되어 세 건 모두 해소되었습니다. 보이지 않던 행이라 **카드 크기는 변화 없습니다**(`Gold` 326×251 · `Stamp` 326×259).

정리로 페이지 수치가 함께 줄었습니다.

| 항목 | 정리 전 | 정리 후 |
| --- | --- | --- |
| 노드 수 | 915 | **893** |
| 텍스트 수 | 259 | **254** |
| 미바인딩 색상 | 25 | **22** (`#BE820B` · `#D8D8D8` 소멸) |
| 스타일 미적용 (컴포넌트) | 38 | **35** |
| `Card / Shopping` 외부 인스턴스 | 3 | **0** |

#### 외부 라이브러리 인스턴스 현황 (10건)

| 소속 | 레이어 | 크기 | 표시 | 비고 |
| --- | --- | --- | --- | --- |
| `Card / Table` | 투자 손익 아이콘 5개 | 10×10 | 보임 | |
| `Card / Now` | `.primitive / Indicator / Dot` · `AD` | 30×6 · 21×14 | 보임 | |
| `Card / Todo / Step` | `syrup/18/arrow_right_gray200` | 18×18 | 보임 | |
| `Card / Thunderbolt` | `syrup_alarm_tit_bg` | 288×156 | 보임 | **유지 결정** |
| `.primitive / Card / Shopping` | `AD` | 21×14 | 안 보임 | BOOLEAN으로 꺼짐 |

`Card / Thunderbolt`의 Stepper는 2026-10-08에 **로컬 컴포넌트로 전환**되었고, 남은 외부 인스턴스는 배경 이미지 `syrup_alarm_tit_bg` 하나입니다.

#### 남은 항목

- **숨겨진 빈 Section Header** `9517:41222` — Master Component 섹션 중간(y 3401)에 `visible=false`인 빈 헤더가 남아 있습니다. 화면에는 안 보이지만 레이어 목록을 어지럽힙니다.
- **`Card / My / Icon`의 `Cash`만 22 × 22** — 나란히 쓰이는 `OCB` · `Npay`는 20 × 20입니다.
- **`Card / Todo / Step` 좌우 패딩 비대칭** — `400/500`(16/20). 다른 카드는 모두 좌우 동일합니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-08)

| 항목 | 내용 |
| --- | --- |
| `적립예정금` → `Pending Gold` ([2](#2-프로퍼티-네이밍이-제각각)) | 파일 전체 프로퍼티명 영문 통일 |
| `cg09` → `CG09` ([3](#3-card--summary-variant-값이-화면-코드)) | Summary 코드 표기 통일 |
| 원격 텍스트 스타일 **17건** → 로컬 ([1](#1--원격-텍스트-스타일-14건-로컬-교체-2026-10-08-완료)) | 14건 동일 이름 교체 + `Body/SemiBold/14` 3건 → `t1050_14_bold`. **페이지 잔여 0건** |
| 외부 Color 토큰 **8건** → 로컬 ([9](#9--외부-라이브러리-color-토큰-8건-교체-2026-10-08-완료)) | 값 동일, 무손실. **잔여 0건** |
| 테두리 `Gray_900` **3건** → `Gray_850` ([6](#6-테두리-색이-컴포넌트마다-다름)) | `Summary` CS02 · OPS03_01 · `Card / Tax` |
| 보이지 않는 `alarm` 행 **3건** 제거 ([12](#12-기타-정리-대상)) | `Card / Shopping` 외부 인스턴스 **0건** |
| `Card / Thunderbolt` Stepper 로컬 전환 ([12](#12-기타-정리-대상)) | `Stepper` 페이지 원격 스타일 19건도 함께 해소 |

### ⚠️ 정정

| 항목 | 내용 |
| --- | --- |
| 제어문자 8건 ([10](#10--제어문자-8건--오탐이었음-2026-10-08-정정)) | **오탐.** 검출 정규식이 일반 개행을 포함. Card 페이지 실제 0건 |

### ℹ️ 의도 확인 — 정리 대상 아님

| 항목 | 판단 |
| --- | --- |
| 10~11px 텍스트 ([5](#5-스타일-미적용-텍스트-38건)) | **토큰화하지 않음** — 13px이 시스템 관리 하한 |
| `Card / My`의 `State` ([7](#7-ℹ-card--my의-state가-한-variant에만-연결됨--의도된-설계)) | **의도된 설계** |
| `Card / My` `Default`의 `Gray_800` ([6](#6-테두리-색이-컴포넌트마다-다름)) | **의도된 강조** — 선택형 카드 |
| 미바인딩 색상 25건 ([8](#8-미바인딩-색상-25건--대부분-로고일러스트)) | 대부분 로고·일러스트 |
| 라운드 `83.33` 6건 ([11](#11-라운드-8333-6건--디자인-값-아님)) | 벡터 스케일 값 |

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Property 1` 6건 이름 정리 ([2](#2-프로퍼티-네이밍이-제각각)) | 이름만 변경 | 낮음 |
| 2 | 숨겨진 빈 Section Header 제거 ([12](#12-기타-정리-대상)) | 정리 | 낮음 |
| 3 | 스케일 밖 굵기 SemiBold 8 · ExtraBold 9 ([5](#5-스타일-미적용-텍스트-38건)) | 판단 필요 | 중간 |
| 4 | `#1F80FF` 6건 토큰화 여부 ([8](#8-미바인딩-색상-25건--대부분-로고일러스트)) | 판단 필요 | 중간 |
| 5 | `Card / Thunderbolt` · `Card / SA` 구조 ([4](#4-일부-variant가-카드가-아니라-래퍼)) | 구조 변경 | 높음 |

### 이 페이지 밖으로 이어지는 과제

| 항목 | 내용 |
| --- | --- |
| 원격 텍스트 스타일 **17건** | `Header` 6 · `AD` 4 · `Product List` 4 · `Tab` 4 · `Product Grid` 1<br>이 중 `t1400_20_regular` · `b400_14_regular` **4건은 동일 이름 로컬로 즉시 교체 가능** |
| U+2028 줄 구분자 **2건** | `AD` · `Text Field` 각 1건 (보드 설명문 오버라이드) |
