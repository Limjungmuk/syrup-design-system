# Syrup Design System — Grid List 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Grid List` 페이지 → [Grid List 섹션 `8945:8663`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8945-8663) |
| 섹션 크기 | 1440 × 7985 |
| 컴포넌트 수 | **14개** (Component Set 12 · Component 2) |
| 사용 가이드라인·예제 기준일 | 2026-11-11 |
| 기존 마스터 상세 조사 기준일 | 2026-10-12 (아래 이력 참고) |
| 문서 구성 | Guidelines 4개 · Usage A–G 7개 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **자주 사용하는 기능으로 빠르게 이동할 수 있는 메뉴 컴포넌트예요.**
> 주요 서비스나 기능을 한눈에 보여주고 빠르게 접근할 수 있도록 할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Grid List / List Item` | `9021:9815` |
| `Grid List / Todo / List Item` | `9711:5068` |
| `Grid List / Bank / List Item` | `9742:13975` |
| `Grid List / Icon / 56 / Meal` | `8945:10856` |
| `Grid List / Icon / 56 / Home` | `8945:14141` |
| `Grid List / Icon / 56 / Pocket` | `8945:14216` |
| `Grid List / Icon / 56` | `8948:20848` |
| `Grid List / Icon / 48` | `9002:9916` |
| `Grid List / Todo / Icon` | `9704:47234` |
| `Grid List / Bank / Icon` | `9742:10700` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Grid List — Master Component](#1-grid-list--master-component)
3. [Grid List / Todo · Bank](#2-grid-list--todo--bank)
4. [Child Item — List Item](#3-child-item--list-item)
5. [Icon 세트 7종](#4-icon-세트-7종)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [점검 필요 사항 — 기존 기록](#점검-필요-사항)
8. [사용 가이드라인](#사용-가이드라인)
9. [사용 예제](#사용-예제)
10. [문서 구성과 AI 도구 사용 기준](#문서-구성과-ai-도구-사용-기준)
11. [확인 사항](#확인-사항)

---

## 사용 가이드라인

2026-11-11 [피그마 Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-5530)의 최신 내용을 반영했어요.

### 1. 정보량에 맞는 유형을 사용해요

아이콘과 이름만으로 구분할 수 있는 항목은 아이콘형을 사용해요. 설명이나 혜택을 함께 안내해야 하면 카드형을 사용해요.
리워드를 받는 행동이 필요한 경우에는 버튼이 있는 카드형을 선택해요.

### 2. 같은 목록의 열과 정렬을 유지해요

같은 목록에서는 항목의 폭과 간격을 일정하게 유지하고, 아이콘과 텍스트의 시작 위치를 맞춰요.
2열 카드형과 3열 목록형은 각 컴포넌트의 구성을 유지하고, 문구가 길어져도 같은 행의 높이가 맞도록 사용해요.

### 3. 배지와 리워드를 구분해서 보여줘요

새 항목이나 보유 개수는 아이콘 옆 배지로 표시해요. 배지의 종류와 숫자는 실제 정보에 맞게 사용해요.
받을 수 있는 리워드는 버튼에 금액을 표시하고, 메뉴의 보유 개수와 혼동되지 않도록 구분해요.

### 4. 3열 목록의 마지막 항목은 오른쪽 구분선을 숨겨요

구분선이 있는 3열 목록은 각 행의 마지막 항목에 Last=True를 사용해요.
할 일과 금융기관 목록 모두 오른쪽 외곽에 세로 구분선이 남지 않도록 구성해요.

## 사용 예제

[Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-5531)는 A–G 순서로 구성해요. 아래 매핑은 AI 도구에서 컴포넌트를 선택할 때 참고해요.

### A. 주요 메뉴

아이콘과 이름을 한 줄로 배치해 주요 메뉴로 연결해요. 새로 안내할 항목은 New 배지를 함께 표시할 수 있어요.

- 컴포넌트: `Grid List · Variant=Top`
- 현재 예제 참조 마스터: `8945:10808`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7074)

### B. 보유 내역 메뉴

메뉴별 보유 개수를 숫자 배지로 표시해요. 각 배지는 해당 항목의 아이콘 가까이에 배치해요.

- 컴포넌트: `Grid List · Variant=My`
- 현재 예제 참조 마스터: `8948:21094`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7173)

### C. 여러 혜택 메뉴

여러 메뉴를 아이콘과 이름으로 묶어 보여줘요. 같은 열과 행의 정렬을 유지해 항목을 빠르게 찾을 수 있도록 구성해요.

- 컴포넌트: `Grid List · Variant=혜택모음`
- 현재 예제 참조 마스터: `8948:21337`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7272)

### D. 설명이 있는 카드

아이콘과 제목, 짧은 설명을 함께 보여줘요. 같은 목록 안에서는 카드의 폭과 정보 위치를 일정하게 유지해요.

- 컴포넌트: `Grid List · Variant=더많이모으기`
- 현재 예제 참조 마스터: `9021:10195`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7582)

### E. 리워드 받기 카드

이미지와 참여 조건, 받을 수 있는 리워드를 함께 보여줘요. 리워드를 받는 행동은 카드 아래 버튼으로 제공해요.

- 컴포넌트: `Grid List · Variant=참여하고모으기`
- 현재 예제 참조 마스터: `9024:7852`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7742)

### F. 할 일과 기록 횟수

할 일의 아이콘과 이름, 기록 횟수를 3열로 보여줘요. 문구가 두 줄이 되어도 같은 행의 높이를 맞추고 마지막 열의 오른쪽 구분선을 숨겨요.

- 컴포넌트: `Grid List / Todo`
- 현재 예제 참조 마스터: `9704:38812`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7807)

### G. 금융기관 선택

금융기관의 로고와 이름을 3열로 배치해요. 점검 중인 항목은 상태를 함께 표시하고, 각 행의 마지막 항목은 오른쪽 구분선을 숨겨요.

- 컴포넌트: `Grid List / Bank`
- 현재 예제 참조 마스터: `11836:113097`
- [피그마 예제](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11857-7952)

## 문서 구성과 AI 도구 사용 기준

- 가이드라인 1번의 아이콘형과 예제 A는 모두 `Grid List / Variant=Top` 마스터 `8945:10808`을 사용해요. 예제 A는 사용자가 교체한 최신 인스턴스를 기준으로 반영했어요. `My` 유형으로 대체하지 않아요.
- 설명량에 따라 `Icon`, `Card`, `CTA Card`를 구분해요. `CTA Card`의 리워드 금액은 행동 버튼이며 메뉴의 숫자 배지와 역할이 달라요.
- `.primitive / Grid List / Badge`는 `Type=Count / New`로 구분해요. 보유 개수와 새 항목 여부는 실제 정보에 맞게 표시하고, 모든 항목에 임의로 배지를 붙이지 않아요.
- 3열 Todo·Bank 목록의 각 행 마지막 항목은 `Last=True`, 앞선 항목은 `Last=False`로 구성해요. `Last`는 선택·완료 상태가 아니라 오른쪽 구분선 처리 속성이에요.
- Todo의 `Time`은 횟수 정보 표시 옵션, Bank의 `Badge`는 점검 중 등 상태 표시 옵션이에요. 서로 같은 의미로 해석하지 않아요.
- 같은 행의 텍스트가 두 줄로 늘어나면 행 안의 항목 높이를 맞춰요. 한 항목만 임의로 축소하거나 구분선 정렬이 어긋나게 배치하지 않아요.
- 예제 F는 Todo 목록 중 2행, G는 금융기관 목록 중 4행을 보여주는 문서용 축약이에요. 가이드라인 4번은 각 목록을 2행씩 보여줘요. 이를 실제 목록의 최대 항목 수나 고정 높이로 해석하지 않아요.
- 현재 문서의 Bank 인스턴스는 `11836:113097`을 참조해요. 기존 규격 기록의 `9911:11822`와 ID가 다르므로 실제 적용 시 최신 디자인의 참조와 속성을 먼저 확인해요.
- 카드형의 아이콘·이미지·문구·리워드 버튼과 중첩 컴포넌트 구조를 유지해요. 예제의 상품명·금액·횟수·배지 숫자는 샘플이며 운영 기준이 아니에요.
- Top 아이콘에 사용된 Sandoll Gyeokdonggulim은 기존 자산의 일부예요. 편집 환경에 글꼴이 없어도 임의로 다른 글꼴로 교체하거나 아이콘을 다시 그리지 않아요.
- Usage 예제는 폭 360, 가로 간격 40, 섹션 여백 100으로 한 줄에 배열해요. 설명 끝과 Slot 사이 간격은 50이며 Slot 패딩은 0, 좌측·상단 정렬, 높이 Hug로 사용해요.
- 단독 컴포넌트는 Slot 안에 바로 배치해요. 문서용 Slot의 여백과 실제 Grid List의 자체 패딩을 구분하고, 컴포넌트 자체 여백은 유지해요.
- 섹션의 문서 규격은 실제 앱 화면의 공통 폭이나 카드 간격을 강제하는 규칙이 아니에요. 해당 마스터의 Auto Layout과 화면 영역을 기준으로 배치해요.
- Section 1의 아노테이션 5개를 제거했고, 잔여 0개를 확인했어요.

## 확인 사항

- 이번 업데이트는 가이드라인 4개, 예제 7개와 최신 Top 적용 내용을 문서에 반영한 작업이에요. 마스터의 속성명·variant 이름을 변경하지 않았어요.
- 현재 사용 기준은 위 가이드라인·예제를 우선해요. 아래 2026-10-12 조사 기록의 노드 수·폰트 수·스타일 수·토큰 수·미사용 집계는 당시 결과이며 이번에 전수 재검사하지 않았어요.
- 기존 `Property 1` 명칭과 네이밍 정리 전 이름은 과거 기록이에요. 현재 확인한 배지 속성은 `Type`, Todo·Bank 아이콘 속성도 `Type`이에요.
- 기존 기록의 `My` 간격 25, CTA Card의 겹침 간격 등은 문서 예제의 규칙과 구분해요. 음수 값이라는 이유만으로 의도된 겹침 구조를 임의로 없애지 않아요.

---

## 기존 마스터 규격과 점검 기록 (2026-10-12)

> 아래는 상세 규격·조사 결과와 결정 이력을 보존한 기록이에요. 집계 수치와 남은 과제는 현재 상태로 단정하지 않으며, 최신 사용 기준은 위 내용을 우선해요.

## 구성 한눈에 보기

섹션 높이 7,985 · 노드 **1,796개**로 Card 다음으로 큽니다. 다만 **부피의 대부분이 아이콘 에셋**입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Grid List` · `Todo` · `Bank` |
| y 4953 → 5093 | Child Item → List Item | List Item 3종 · Badge |
| y 6007 | Icon | 아이콘 세트 **7종** |

### 전체 목록

| # | 이름 | 타입 | Variant / Props | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Grid List` | Set | `Variant` 5종 + `Slot` | 328~360 × 80~427 |
| 2 | `Grid List / Todo` | Component | — | 328 × 529 |
| 3 | `Grid List / Bank` | Component | — | 330 × **2291** |
| 4 | `Grid List / List Item` | Set | `Variant` 3종 + `Badge` · `Image` · `Icon`(SLOT) | 56~160 × 80~208 |
| 5 | `Grid List / Todo / List Item` | Set | `Last` 2종 + `Time` | 109 × 127 |
| 6 | `Grid List / Bank / List Item` | Set | `Last` × `Badge` | 109 × 109 |
| 7 | `.primitive / Grid List / Badge` | Set | `Property 1` 2종 | 20 × 20 |
| 8 | `.primitive / Grid List / Icon / Home / 56 / Meal` | Set | `Variant` **5종** | 56 × 56 |
| 9 | `Grid List / Icon / 56 / Home` | Set | `Variant` **8종** | 56 × 56 |
| 10 | `.primitive / Grid List / Icon / Home / 56 /Pocket` | Set | `Active` 2종 | 56 × 56 |
| 11 | `Grid List / Icon / 56` | Set | `Variant` **16종** | 56 × 56 |
| 12 | `Grid List / Icon / 48` | Set | `Variant` **21종** | 48 × 48 |
| 13 | `Grid List / Todo / Icon` | Set | `Property 1` **37종** | 36 × 36 |
| 14 | `Grid List / Bank / Icon` | Set | `Property 1` **59종** | 54 × 54 |

**아이콘 variant만 148종**입니다. 전체 variant의 대부분을 차지합니다.

---

## 1. Grid List — Master Component

**Node** `8948:22146` · Component Set · **5 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Top` | `Top` · `참여하고모으기` · `더많이모으기` · `혜택모음` · `My` |
| `Slot` | **SLOT** | — | — |

**variant 값에 한글 화면명이 그대로 들어가 있습니다** → [점검 2](#2-variant-값에-한글-화면명)

### Variant별 레이아웃

| Variant | 크기 | 방향 | Padding | Gap | 배경 |
| --- | --- | --- | --- | --- | --- |
| `Top` | 360 × 108 | 가로 | `400/600/300/600` (16/24/12/24) | **0** | `Color/Gray_White` |
| `혜택모음` | 360 × 280 | 세로 | `0/400/0/400` (0/16/0/16) | `Spacing/500` (20) | 없음 |
| `참여하고모으기` | 328 × 208 | 가로 | 0 | `Spacing/200` (8) | 없음 |
| `더많이모으기` | 328 × 427 | 가로 **WRAP** | 0 | `Spacing/200` (8) | 없음 |
| `My` | 360 × 80 | 가로 | `0/600/0/600` (0/24/0/24) | **25** ⚠️ | 없음 |

- **`Top`만 흰 배경**을 가집니다. 나머지는 투명한 묶음 역할입니다.
- **`더많이모으기`만 줄바꿈(WRAP)** 합니다. 아이콘이 여러 줄로 접힙니다.
- `My`의 간격 `25`는 토큰 스케일 밖입니다 → [점검 4](#4-토큰-미바인딩-값)

### 사용 텍스트 스타일

`t1360_13_medium` 20 · `t1000_15_bold` 8 · `b500_13_regular` 6 · `c100_12_regular` 2 · `t1050_14_bold` 2 · **스타일 미적용** 7건(12 Bold 4 · 9 Regular 3)

---

## 2. Grid List / Todo · Bank

variant 없는 단일 컴포넌트 2종입니다. 둘 다 **카드 형태의 큰 묶음**입니다.

| 컴포넌트 | 크기 | 방향 | Radius | Stroke |
| --- | --- | --- | --- | --- |
| `Grid List / Todo` `9704:38812` | 328 × 529 | 세로 | `Corner radius/400` (16) | `Color/Gray_850` 1px |
| `Grid List / Bank` `9911:11822` | 330 × **2291** | 가로 **WRAP** | `Corner radius/400` (16) | `Color/Gray_850` 1px |

**`Grid List / Bank`는 높이 2,291로 이 파일에서 가장 큰 컴포넌트**입니다. 은행·증권사 59종을 격자로 모두 펼쳐 놓은 형태입니다.

| 컴포넌트 | 텍스트 스타일 |
| --- | --- |
| `Todo` | `b500_13_regular` 12 · `c100_12_regular` 12 |
| `Bank` | `c100_12_regular` **63** · 스타일 미적용 1 |

---

## 3. Child Item — List Item

### Grid List / List Item

**Node** `9021:9815` · Component Set · **3 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Icon` | `Icon` · `Card` · `CTA Card` |
| `Badge` | BOOLEAN | `true` | — |
| `Image` | BOOLEAN | `false` | — |
| `Icon` | **SLOT** | — | — |

| Variant | 크기 | Padding | Gap | 배경 | Radius |
| --- | --- | --- | --- | --- | --- |
| `Icon` | 56 × 80 | 0 | `Spacing/150` (6) | 없음 | 0 |
| `Card` | 160 × 137 | `Spacing/400` (16) 사방 | `Spacing/400` (16) | `Color/Gray_White` | `r400` (16) |
| `CTA Card` | 160 × 208 | 0 | **−24** ⚠️ | `Color/Gray_White` | `r400` (16) |

`Card`·`CTA Card`는 `Color/Gray_850` 1px 테두리를 가집니다.

> **`CTA Card`의 간격이 `−24`(음수)** 입니다. 요소를 의도적으로 겹치게 만드는 기법이지만 토큰화할 수 없는 값입니다 → [점검 4](#4-토큰-미바인딩-값)

### Grid List / Todo / List Item

**Node** `9711:5068` · Component Set · **2 variants** · 109 × 127

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Last` | VARIANT | `False` | `False` · `True` |
| `Time` | BOOLEAN | — | — |

자식은 `Icon` + `Text`이며, 할 일 아이콘과 이름·횟수("직접입력하기 / 35회")를 담습니다. `Grid List / Todo` 안에서 **12곳**에 쓰입니다(`Last=False` 8 · `Last=True` 4).

Bank 쪽과 마찬가지로 `Last`는 격자 마지막 칸의 구분선을 처리하는 용도입니다.

> 2026-10-12까지 **오류 상태**여서 프로퍼티를 읽을 수 없었습니다 → [점검 1](#1--primitive--grid-list--todo--list-item-오류-해소-2026-10-12-완료)

### Grid List / Bank / List Item

**Node** `9742:13975` · Component Set · **2 variants** · 109 × 109

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Last` | VARIANT | `False` | `False` · `True` |
| `Badge` | BOOLEAN | `true` | — |

공통 — Padding `500/200/500/200` (20/8/20/8), Gap `Spacing/50` (2), Stroke `Color/Gray_850`

**테두리 두께가 `mixed`** 입니다. 변마다 다른 값을 써서 격자 구분선을 만드는 방식입니다. `Last`는 마지막 칸에서 오른쪽 선을 지우는 용도로 보입니다.

### .primitive / Grid List / Badge

**Node** `10477:3538` · Component Set · **2 variants** · 20 × 20

| Variant | 배경 | 내용 |
| --- | --- | --- |
| `Count` | `Color/Primary_Orange` | 숫자 |
| `New` | `Color/Secondary_Red` | "N" |

둘 다 `Corner radius/circle`. 프로퍼티명이 `Property 1`입니다 → [점검 3](#3--property-1--type-2026-10-12-완료)

---

## 4. Icon 세트 7종

**148개 variant**로 이 페이지 부피의 대부분을 차지합니다.

| 컴포넌트 | 크기 | variant | 인스턴스 | 내용 |
| --- | --- | --- | --- | --- |
| `Grid List / Bank / Icon` | 54 × 54 | **59** | 65 | 은행 · 증권사 로고 |
| `Grid List / Todo / Icon` | 36 × 36 | **37** | 21 | 할 일 아이콘 (영양제 먹기 · 물마시기 …) |
| `Grid List / Icon / 48` | 48 × 48 | **21** | 8 | 제휴처 · 미션 |
| `Grid List / Icon / 56` | 56 × 56 | **16** | 16 | 멤버십 · 쿠폰 · 제휴 브랜드 |
| `Grid List / Icon / 56 / Home` | 56 × 56 | **8** | 5 | 홈 주요 메뉴 |
| `Grid List / Icon / 56 / Meal` | 56 × 56 | **5** | **0** | 아침·점심·저녁·간식·오픈전 |
| `Grid List / Icon / 56 / Pocket` | 56 × 56 | **2** | **0** | `Active` True/False |

`Todo / Icon`만 다른 페이지(`List Row` 7건)에서도 쓰이고, 나머지는 모두 `Grid List` 페이지 안에서만 쓰입니다.

> **`Meal`(5종)과 `Pocket`(2종)은 인스턴스가 0건**입니다 → [점검 9](#9-meal--pocket-아이콘-세트-사용-0건)

### 크기 체계

| 크기 | 용도 |
| --- | --- |
| 56 × 56 | 홈 메인 메뉴 (4개 세트) |
| 54 × 54 | 은행 로고 |
| 48 × 48 | 제휴처 · 미션 |
| 36 × 36 | 할 일 |

이름 규칙은 2026-10-12에 **`Icon / {크기} / {용도}`** 로 통일했습니다 → [점검 5](#5--아이콘-세트-이름-규칙-통일-2026-10-12-완료)

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 묶음 폭 | **328** (본문 영역) · **360** (화면 전체 폭) |
| 카드 라운드 | `Corner radius/400` (16) |
| 카드 테두리 | `Color/Gray_850` 1px |
| 카드 배경 | `Color/Gray_White` |
| 아이콘 간격 | `Spacing/200` (8) |
| 아이콘–라벨 간격 | `Spacing/150` (6) |
| 좌우 여백 | `Spacing/600` (24) — 360 폭 기준 |
| 배지 | 20 × 20 원형 (`Primary_Orange` / `Secondary_Red`) |

### 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `c100_12_regular` | 아이콘 라벨 (가장 많음 — Bank에서만 63건) |
| `t1360_13_medium` | 메뉴 라벨 |
| `t1000_15_bold` | 카드 제목 |
| `b500_13_regular` | 보조 설명 |
| `t1050_14_bold` | 강조 |

---

## 점검 필요 사항

### 1. ✅ `Grid List / Todo / List Item` 오류 해소 (2026-10-12 완료)

**Node** `9711:5068` — 파일 전체에서 **유일하게 오류 상태인 컴포넌트셋**이었습니다. `componentPropertyDefinitions`를 읽으면 예외가 발생했습니다.

```
Component set has existing errors
```

원인은 **두 번째 variant의 이름**이었습니다.

| Node | 변경 전 | 변경 후 |
| --- | --- | --- |
| `9704:47456` | `Last=False` | 변화 없음 |
| `9711:5069` | `Last=True, Property 2=Grid List, Property 3=Todo, Property 4=List Item, Property 5=True` | **`Last=True`** |

**컴포넌트 경로(`Grid List / Todo / List Item`)가 variant 프로퍼티로 잘못 해석**된 상태였습니다. 이름 변경 중 `/`와 `,`가 섞이면서 Figma가 경로 조각들을 프로퍼티로 읽은 것으로 보입니다.

두 variant의 **구조는 동일**했으므로(109 × 127, 자식 `Icon` + `Text`) **이름만 고쳐 해소**했습니다.

#### 결과

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 프로퍼티 읽기 | ❌ 예외 발생 | ✅ `Last=[False, True]` · `Time#9711:0` BOOLEAN |
| variant 이름 | 경로가 섞인 5개 축 | **`Last` 1개 축** |
| 크기 · 구조 | 109 × 127 | 변화 없음 |

숨어 있던 **`Time` BOOLEAN 프로퍼티도 이제 정상적으로 노출**됩니다. 오류 상태에서는 읽을 수 없던 값입니다.

#### 파일 전체 검증

| 항목 | 결과 |
| --- | --- |
| 컴포넌트셋 **178개** 전수 프로퍼티 읽기 | **오류 0건** |
| 인스턴스 **1,828개** | **끊긴 참조 0건** |
| 이 컴포넌트셋 사용처 | `Grid List / Todo` 내부 12곳 (`Last=False` 8 · `Last=True` 4) — 정상 |

**파일 전체에 컴포넌트셋 오류가 0건**이 되었습니다. Bottom Sheet `Select Item`(2026-09-21 해결)에 이은 마지막 건이었습니다.

### 2. Variant 값에 한글 화면명

`Grid List`의 `Variant` 값 5개 중 3개가 **한글 화면 이름**입니다.

| 값 | 성격 |
| --- | --- |
| `Top` · `My` | 영문 — 위치·영역 |
| **`참여하고모으기`** · **`더많이모으기`** · **`혜택모음`** | **한글 — 화면 섹션명** |

같은 축에 **영문 구조명과 한글 콘텐츠명이 섞여** 있습니다. 서비스 화면 이름이 바뀌면 variant 이름도 따라 바뀌어야 하는 구조라, 디자인 시스템 쪽에서는 `Row` · `Grid` · `GridWrap` 같은 **형태 기반 이름**이 더 안정적입니다.

다만 실제로 다섯 가지가 레이아웃 형태로도 구분됩니다.

| Variant | 형태 |
| --- | --- |
| `Top` | 가로 1줄 + 흰 배경 |
| `My` | 가로 1줄 (배경 없음) |
| `참여하고모으기` | 가로 1줄 (328 폭) |
| `더많이모으기` | 가로 **줄바꿈** |
| `혜택모음` | **세로** |

`Card / Summary`의 화면 코드(`CP02` · `CG09` …)와 같은 성격의 결정이 필요합니다 — 팀 공용어로 유지할지, 형태 기반으로 바꿀지입니다.

### 3. ✅ `Property 1` → `Type` (2026-10-12 완료)

3개 컴포넌트에 Figma 기본 생성 이름이 남아 있어 **무엇을 고르는 축인지 알 수 없었습니다.** 특히 아이콘 세트 두 개는 값이 37개·59개로 많아 축 이름이 비어 있으면 더 찾기 어려웠습니다.

| 컴포넌트 | 변경 전 | 변경 후 | 값 | 인스턴스 |
| --- | --- | --- | --- | --- |
| `.primitive / Grid List / Badge` `10477:3538` | `Property 1` | **`Type`** | `Count` · `New` | 4 |
| `Grid List / Todo / Icon` `9704:47234` | `Property 1` | **`Type`** | 할 일 **37종** | 21 |
| `Grid List / Bank / Icon` `9742:10700` | `Property 1` | **`Type`** | 금융사 **59종** | 65 |

variant 이름도 함께 바뀌었습니다 (`Property 1=산업은행` → **`Type=산업은행`**). 인스턴스 **90건**은 Figma가 자동으로 따라가며, 끊긴 참조는 0건입니다.

파일 전체 기준으로는 `Property 1`이 **58개 컴포넌트셋**에 남아 있고, **`Grid List` 페이지는 0건**이 되었습니다.

### 4. 토큰 미바인딩 값

#### 간격 — 스케일 밖

| 값 | 건수 | 위치 |
| --- | --- | --- |
| `14` | 3 | 간격 |
| `35` | 3 | 간격 |
| **`−24`** | 3 | `Grid List / List Item` ▸ `CTA Card` (요소 겹침용 음수) |
| `25` | 1 | `Grid List` ▸ `My` |
| `1` | 6 | 패딩 (격자 구분선 두께로 추정) |

Spacing 스케일(2 · 4 · 6 · 8 · 10 · 12 · 16 · 20 · 24 · 30)에 없는 값들입니다. **음수 간격은 토큰화 자체가 불가능**하며, 겹침 효과를 위한 의도적 사용으로 보입니다.

> 패딩 `100`(8건)과 `546`(2건)은 문서 보드 레이아웃 전용입니다.

#### 라운드 — 소수점 63건

| 값 | 건수 | 값 | 건수 |
| --- | --- | --- | --- |
| `118.8` | 9 | `85.89` | 6 |
| `1.5` | 6 | `0.49` | 4 |
| `8.35` | 4 | `65.57` | 4 |
| `24.45` | 4 | `94.56` · `103.64` · `3.45` · `3.34` · `100.89` · `43.03` | 각 2 |

**전부 아이콘·일러스트 내부의 벡터 도형**입니다. 원형·둥근 사각형을 사이즈에 맞춰 확대·축소하면서 라운드 값이 비례해 따라간 수치로, Card의 `83.33`·Checkbox의 `0.67px`와 같은 성격입니다.

**디자인 값이 아니므로 토큰화 대상이 아닙니다.**

#### 색상 — 브랜드 로고

| 색 | 건수 | 성격 |
| --- | --- | --- |
| `#FFFFFF` | 67 | 아이콘 내부 흰색 |
| `#FAC109` · `#FABE00` | 11 | KB · 국민 계열 로고 |
| `#E21E2D` · `#E72410` | 9 | 금융사 로고 |
| `#004187` · `#0083CA` | 7 | 금융사 로고 |
| 그 외 | 다수 | 은행·증권사·제휴처 로고 |

**아이콘 세트 내부는 감사에서 제외**했고, 위 수치는 그 밖의 영역 기준입니다. 금융사 로고는 브랜드 자산이라 토큰화 대상이 아닙니다.

> 미바인딩 stroke `#9747FF` 12건은 Figma가 컴포넌트셋에 자동으로 그리는 점선 테두리입니다.

### 5. ✅ 아이콘 세트 이름 규칙 통일 (2026-10-12 완료)

두 가지가 어긋나 있었습니다.

1. **공백** — `56 /Pocket`만 슬래시 뒤 공백이 없었습니다. Figma는 ` / `를 폴더 구분으로 쓰므로 에셋 패널에서 다른 그룹으로 떨어졌습니다.
2. **순서** — `Icon / Home / 56 / Meal`과 `Icon / 56 / Home`이 뒤섞여 `Home`이 상위인지 하위인지 일관되지 않았습니다.

**`Icon / {크기} / {용도}`** 로 통일했습니다.

| Node | 변경 전 | 변경 후 |
| --- | --- | --- |
| `8945:10856` | `.primitive / Grid List / Icon / **Home / 56 /** Meal` | `.primitive / Grid List / Icon / **56 /** Meal` |
| `8945:14216` | `.primitive / Grid List / Icon / **Home / 56 /**Pocket` | `.primitive / Grid List / Icon / **56 / **Pocket` |
| `8945:14141` | `Grid List / Icon / 56 / Home` | 변화 없음 |
| `8948:20848` | `Grid List / Icon / 56` | 변화 없음 |
| `9002:9916` | `Grid List / Icon / 48` | 변화 없음 |

결과적으로 `Icon / 56` 아래 `Home` · `Meal` · `Pocket` 세 용도가 **같은 계층에 나란히** 놓입니다.

두 컴포넌트셋 모두 **인스턴스가 0건**이라 이름 변경의 영향을 받는 곳이 없었습니다 → [점검 9](#9-meal--pocket-아이콘-세트-사용-0건)

> `Todo / Icon`·`Bank / Icon`은 `Icon /` 아래가 아니라 `Todo /`·`Bank /` 아래에 있습니다. 기능 묶음이 다르므로 그대로 두었습니다.

### 6. 스타일 미적용 텍스트 30건

보드 표기 6건을 제외한 수치입니다.

| 크기 · 굵기 | 건수 | 위치 |
| --- | --- | --- |
| **9 Regular** | 14 | 아이콘 라벨 (Meal 세트 · `금한돈` · `금 주는` 등) |
| **12 Bold** | 13 | 배지 숫자 · `점검중` · `할인적립` |
| `10 Regular` · `11 Regular` · `9 ExtraBold` | 3 | 기타 |

**모두 9~12px 구간**으로, **토큰화하지 않기로 한 범주**(13px이 시스템 관리 하한)입니다. Badge·Card에서 적용한 기준과 같습니다.

다만 **`12 Bold` 13건은 재검토 여지**가 있습니다. 13px Bold(`t1060_13_bold`)는 토큰으로 등록한 선례가 있고, 12px은 하한 13px에 한 단계만 모자랍니다. 배지 숫자·상태 라벨처럼 반복 사용되는 요소라 지속적으로 나온다면 등록 검토 대상입니다.

### 7. Sandoll Gyeokdonggulim 폰트 15건

| 폰트 | 건수 |
| --- | --- |
| Pretendard Regular | 105 |
| Pretendard Bold | 27 |
| Pretendard Medium | 21 |
| **Sandoll Gyeokdonggulim Regular** | **15** |
| Pretendard SemiBold | 4 |
| Pretendard ExtraBold | 1 |

Sandoll Gyeokdonggulim은 2026-10-01 파일 전체 폰트 통일 때 **의도적으로 제외한 폰트**입니다. 이 페이지의 15건도 같은 기준으로 유지합니다.

> SemiBold 4 · ExtraBold 1은 Syrup 타입 스케일에 없는 굵기입니다. Card 페이지와 같은 성격의 건으로, 판단이 필요합니다.

### 9. `Meal` · `Pocket` 아이콘 세트 사용 0건

이름 정리 작업 중 확인한 결과입니다.

| 컴포넌트 | variant | 파일 내 인스턴스 |
| --- | --- | --- |
| `Grid List / Icon / 56 / Meal` | 5 | **0** |
| `Grid List / Icon / 56 / Pocket` | 2 | **0** |
| `Grid List / Icon / 56 / Home` | 8 | 5 |
| `Grid List / Icon / 56` | 16 | 16 |
| `Grid List / Icon / 48` | 21 | 8 |
| `Grid List / Todo / Icon` | 37 | 21 |
| `Grid List / Bank / Icon` | 59 | 65 |

`Meal`(아침·점심·저녁·간식·오픈전)과 `Pocket`(`Active` True/False)은 **파일 어디에서도 인스턴스로 배치되지 않았습니다.**

다만 **이 수치만으로 "미사용"을 단정할 수 없습니다.** Chip `Primary` 때와 같은 한계입니다.

| 범위 | 포함 여부 |
| --- | --- |
| 이 Figma 파일 내 인스턴스 | ✅ |
| 라이브러리를 가져다 쓰는 **다른 파일** | ❌ |
| 디태치된 인스턴스 | ❌ |
| 개발 코드에서의 사용 | ❌ |

`Meal`은 식사 기록 기능, `Pocket`은 홈 주머니 기능과 연결된 것으로 보입니다. **실제 서비스 화면에 쓰이는지 확인이 필요**하며, 쓰이지 않는다면 Chip `Primary`처럼 정리 대상입니다.

### 8. 토큰 상태 — 양호

| 항목 | 결과 |
| --- | --- |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 7 — 문서 레이아웃 전용 |
| 제어문자 (U+2028) | **0건** |
| 미바인딩 fill (아이콘 제외) | 브랜드 로고 위주 |

아이콘 에셋을 빼면 **색상·간격·라운드가 대체로 토큰에 바인딩**되어 있습니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| 오류 컴포넌트셋 이름 수정 ([1](#1--primitive--grid-list--todo--list-item-오류-해소-2026-10-12-완료)) | **파일 전체 컴포넌트셋 오류 0건 달성** |
| 아이콘 세트 이름 통일 ([5](#5--아이콘-세트-이름-규칙-통일-2026-10-12-완료)) | `Icon / {크기} / {용도}` · 2건 |
| `Property 1` → `Type` ([3](#3--property-1--type-2026-10-12-완료)) | 3개 컴포넌트셋 · 인스턴스 90건 자동 반영 |

세 건 모두 **이름만 변경**이며 크기·렌더링 변화가 없습니다. 작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Meal` · `Pocket` 세트 실사용 확인 ([9](#9-meal--pocket-아이콘-세트-사용-0건)) | 서비스 확인 필요 | 낮음 |
| 2 | `12 Bold` 13건 토큰화 여부 ([6](#6-스타일-미적용-텍스트-30건)) | 판단 필요 | 중간 |
| 3 | Variant 한글 화면명 ([2](#2-variant-값에-한글-화면명)) | 팀 합의 필요 | 중간 |
| 4 | SemiBold · ExtraBold 굵기 ([7](#7-sandoll-gyeokdonggulim-폰트-15건)) | 판단 필요 | 중간 |
