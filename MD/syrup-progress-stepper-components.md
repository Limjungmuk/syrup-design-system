# Syrup Design System — Progress Stepper 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Progress Stepper` 페이지 → [Progress Stepper 섹션 `8914:27119`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8914-27119) |
| 섹션 크기 | 1440 × 5967 |
| 컴포넌트 수 | **24개** (Master 11 · Child Item 13) |
| Variant 총수 | **76개** (Master 15 · Child Item 61) |
| 기준일 | 2026-11-10 (가이드라인 4개·Usage A~L 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **시스템이나 과업의 진행 단계를 시각적으로 보여주는 프로그레스바 형태의 컴포넌트에요.**
> 진행 상태를 안내해야하는 경우 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Master Component 11종](#master-component-11종)
3. [Child Item 13종](#child-item-13종)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 상태 참조 기준](#예제-레이아웃과-상태-참조-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)
9. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

현재 페이지는 마스터 섹션(1440 × 5967), Guidelines, Usage로 구성되어 있어요. Section 1은 사용자가 삭제했으며 현재 페이지에 없음을 확인했어요. 기존 노드 789개·텍스트 227개 및 과거 인스턴스 집계는 2026-10-12 점검 기록으로, 새 문서 예제를 포함한 현재 페이지 전체 집계가 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 2,974) | Master 11종 |
| y 3548 | Section Header | Child Items |
| y 3688 | (높이 2,215) | Child Item 13종 |

### 서비스별로 하나씩 만든 구조

이 페이지는 **하나의 범용 Stepper를 여러 방식으로 조합한 것이 아니라, 서비스 11개가 각자 자기 Stepper를 가진** 형태입니다. 각 Master는 해당 진행 방식에 맞는 전용 Child Item을 사용해요. Check-In처럼 여러 하위 컴포넌트로 구성된 유형도 있어요.

| # | Master | Child Item | 도메인 |
| --- | --- | --- | --- |
| 1 | `Progress Stepper / Collect` | `.primitive / … / Collect` | 금 모으기 |
| 2 | `Progress Stepper / Pig` | `.primitive / … / Pig` | 돼지 저금통 |
| 3 | `Progress Stepper / Quiz` | `.primitive / … / Quiz` | 퀴즈 |
| 4 | `Progress Stepper / News` | `.primitive / … / News` | 뉴스 |
| 5 | `Progress Stepper / Movie` | `.primitive / … / Movie` | 영화 |
| 6 | `Progress Stepper / Mission` | `.primitive / … / Mission` | 미션 |
| 7 | `Progress Stepper / Lottery` | `.primitive / … / Lottery` | 복권 |
| 8 | `Progress Stepper / Personality-Test` | `.primitive / … / Personality-Test` | 성격 테스트 |
| 9 | `Progress Stepper / Check-In` | `.primitive / … / Check-In / {List Item, Button, Checkbox}` | 출석 체크 |
| 10 | `Progress Stepper / Express` | `.primitive / … / Express` | 익스프레스 |
| 11 | `Progress Stepper` | `.primitive / … / Search` | 검색 (**이름 불일치**) |

11번만 Master 이름에 서비스명이 없고, Child Item은 `Search`입니다. 나머지 10쌍이 모두 이름을 공유하는 것과 어긋납니다 → [점검 2](#2-마스터와-child-item-이름이-어긋남).

### 전체 목록

| # | 이름 | 타입 | Variant 축 | 대표 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Progress Stepper / Collect` | Component | `Line`=SLOT | 328 × 64 |
| 2 | `Progress Stepper / Pig` | Component | `Line`=SLOT | 328 × 99 |
| 3 | `Progress Stepper / Personality-Test` | Component | — | 328 × 137 |
| 4 | `Progress Stepper / Movie` | Component | — | 194 × 132 |
| 5 | `Progress Stepper / Mission` | Component | — | 360 × 125 |
| 6 | `Progress Stepper / Check-In` | Component | `Line`=SLOT | 316 × 123 |
| 7 | `Progress Stepper / Quiz` | Component | — | 328 × 155 |
| 8 | `Progress Stepper / Lottery` | Component | `Line`=SLOT | 328 × 109 |
| 9 | `Progress Stepper / News` | **Set 2** | `Scroll` | 320 × 142 |
| 10 | `Progress Stepper` | **Set 2** | `Property 1` (5·10) | 360 × 184 |
| 11 | `Progress Stepper / Express` | **Set 3** | `Color` (Purple·Blue·Orange) | 360 × 229 |
| 12 | `.primitive / … / Collect` | Set 3 | `Button` · `Property 1` | 8 × 62 |
| 13 | `.primitive / … / Pig` | Set 2 | `Active` | 36 × 58 |
| 14 | `.primitive / … / Quiz` | Set 3 | `Property 1` | 40 × 61 |
| 15 | `.primitive / … / News` | Set 3 | `Time` · `Property 1` | 40 × 62 |
| 16 | `.primitive / … / Movie` | Set 2 | `Text` · `Active` | 62 × 62 |
| 17 | `.primitive / … / Lottery` | Set 6 | `Property 1` (Left·Center·Right) · `Active` | 19 × 36 |
| 18 | `.primitive / … / Mission` | Set 2 | `Active` | 99 × 125 |
| 19 | `.primitive / … / Personality-Test` | Set 9 | `Property` (1·2·3) · `Step` | 44 × 61 |
| 20 | `.primitive / … / Search` | Set 4 | `Active` · `Size` (L·S) | 90 × 82 |
| 21 | `.primitive / … / Express` | **Set 11** | `Text` · `Color`(5) · `Active` · `Special` | 64 × 64 |
| 22 | `.primitive / … / Check-In / List Item` | Component | `Bubble` | 74 × 113 |
| 23 | `.primitive / … / Check-In / Checkbox` | Set 3 | `Property 1` | 18 × 18 |
| 24 | `.primitive / … / Check-In / Button` | **Set 12** | `Step` (1~4) · `Property` | 74 × 80 |

과거에는 Master 11종의 인스턴스가 0건으로 기록되었지만, 현재는 Guidelines·Usage에 인스턴스가 있어요. 기존 0건을 현재 사용량이나 변경 영향 범위로 해석하지 않아요. → [과거 점검 9](#9-마스터-11종-전부-인스턴스-0건)

---

## Master Component 11종

### 1. Progress Stepper / Collect — `9240:10678`

**328 × 64** · 가로 오토레이아웃 · Padding `0 / 16 / 0 / 16` (`Spacing/400`) · Gap 0

| 레이어 | 타입 | 크기 | 색상 |
| --- | --- | --- | --- |
| `Stepper` | Frame | 296 × 64 | — |
| └ `Line` | **SLOT** | 296 × 12 | `Color/Gray_850` |
| &nbsp;&nbsp;└ `Gauge` | Rect | 12 × 12 | `Color/Secondary_Yellow` |
| └ `Stepper Item` ×4 | Instance | 8 × 34 / 8 × 62 | — |

진행 바 위에 금액 표시 아이템 4개가 올라갑니다. 첫 아이템만 34 높이(버튼 없음), 나머지 3개는 62입니다.

### 2. Progress Stepper / Pig — `9244:11428`

**328 × 99** · 세로 오토레이아웃 · Padding `0 / 8 / 0 / 8` (`Spacing/200`) · Gap **3** (토큰 없음)

| 레이어 | 타입 | 크기 | 색상 |
| --- | --- | --- | --- |
| `Bubble Wrapper` | Frame | 312 × 38 | — |
| └ `Bubble` | Instance | 44 × 38 | [Bubble](syrup-bubble-components.md) 페이지 |
| `Stepper` | Frame | 314 × 58 | — |
| └ `Line` | **SLOT** | 314 × 12 | `Color/Third_Pastel_Coral` |
| &nbsp;&nbsp;└ `Gauge` | Rect | 14 × 12 | `Color/Primary_Orange` |
| └ `Stepper Item` ×4 | Instance | 36 × 58 | — |

### 3. Progress Stepper / Personality-Test — `9223:25550`

**328 × 137** · 세로 오토레이아웃 CENTER/CENTER
Padding `20 / 24 / 16 / 24` (`Spacing/500·600·400·600`) · Gap 16 (`Spacing/400`)
배경 `Color/Gray_White` · 라운드 16 (`Corner radius/400`)

| 레이어 | 내용 |
| --- | --- |
| `Text` 280 × 24 | 「매일 5개 완료하고 30금 받기」 17 Bold `t800_17_bold` `Color/Gray_100` + 새로고침 아이콘 24 |
| `Stepper` 280 × 61 | `Line` 240 × 12 `Color/Gray_800` + `Gauge` 121 × 12 · `Stepper Item` ×3 (44 × 61) |

흰 배경과 라운드를 가진 카드형 Master예요. News·Quiz 등도 각자의 배경·테두리 구성을 사용해요.

### 4. Progress Stepper / Movie — `9223:23532`

**194 × 132** · 가로 오토레이아웃 CENTER · Padding 0 · Gap 4 (`Spacing/100`)

`Stepper Item` 62 × 62 **5개만** 나열됩니다. 진행 라인(`Line`) 없이 동그라미 5개가 곧 단계 표시입니다.

### 5. Progress Stepper / Mission — `9223:25469`

**360 × 125** · 가로 오토레이아웃 **SPACE_BETWEEN** · Padding `0 / 20 / 0 / 20` (`Spacing/500`) · Gap 0

`Stepper Item` 99 × 125 **3개**. Movie와 마찬가지로 라인이 없고, 간격을 `SPACE_BETWEEN`으로 벌립니다.

### 6. Progress Stepper / Check-In — `9263:12060`

**316 × 123** · 가로 오토레이아웃 SPACE_BETWEEN/CENTER
Padding `10 / 0 / 0 / 0` (`Spacing/250`) · Gap **14** (토큰 없음)

| 레이어 | 타입 | 크기 | 색상 |
| --- | --- | --- | --- |
| `Line` | **SLOT** | 244 × 10 | `Color/Gray_800` |
| └ `Gauge` | Vector | 80 × 10 | `Color/Primary_Orange` |
| `Stepper Item` ×4 | Instance | 74 × 113 | — |

Child Item이 3종(`List Item` / `Button` / `Checkbox`)으로 쪼개진 **유일한 Master**입니다.

### 7. Progress Stepper / Quiz — `9206:10071`

**328 × 155** · 세로 오토레이아웃
Padding `20 / 24 / 16 / 24` · Gap 16 (`Spacing/400`)
배경 **`#545B69`** (토큰 없음) · 라운드 16 (`Corner radius/400`)

| 레이어 | 내용 |
| --- | --- |
| `Title` 280 × 42 | 「3일 연속으로 맞히고」 16 Bold `t900_16_bold` · `Title 2`(「최대」 + `Gold` + 「받기」 + [Icon Button / Info](syrup-icon-button-components.md)) |
| └ `Alarm` 81 × 21 | 외부 아이콘 `syrup_ico_16_alerm_off_primary` + 「알림받는 중」 14 Regular `b400_14_regular` ✅ |
| `Stepper` 280 × 61 | `Line` 280 × 16 **`#6F7581`** + `Gauge` 158 × 16 (**숨김 상태**) · `Stepper Item` ×3 (40 × 61) |

`Gauge`가 **`visible: false`**로 꺼져 있어 진행률이 보이지 않습니다. 다른 Master는 모두 게이지가 켜져 있어, 의도인지 확인이 필요합니다.

**유일한 다크 배경 Master**이며, 배경·라인 색 2종이 토큰에 없습니다 → [점검 5](#5-미바인딩-색상-39건).

### 8. Progress Stepper / Lottery — `9280:12952`

**328 × 109** · 세로 오토레이아웃 MIN/CENTER
Padding `20 / 16 / 20 / 20` (`Spacing/500·400·500·500` — **좌우 비대칭**) · Gap 16 (`Spacing/400`)
라운드 16 (`Corner radius/400`) · 배경 없음

| 레이어 | 내용 |
| --- | --- |
| `Title` 292 × 19 | 15 Bold `t1000_15_bold` `Color/Gray_100` + [Text Button](syrup-text-button-components.md) 인스턴스 |
| `Stepper Wrapper` → `Stepper` 288 × 36 | `Line` **SLOT** 288 × 12 `Color/Gray_White` · `Stepper Item` ×5 (19 × 36) |

레이어명 `Stepper_wrapper`는 `Stepper Wrapper`로 정리했습니다 ✅. 좌 20 / 우 16 패딩 비대칭은 의도인지 확인이 필요합니다.

### 9. Progress Stepper / News — `9223:23142` · Set 2

| Property | Type | Options |
| --- | --- | --- |
| `Scroll` | VARIANT | `False` · `True` |

**320 × 142** (`Scroll=False`) · 세로 오토레이아웃 MIN/CENTER
Padding `20 / 16 / 20 / 16` · Gap **18** (토큰 없음)
배경 `Color/Gray_White` · 테두리 `Color/Gray_850` 1px · 라운드 16 (`Corner radius/400`)

| 레이어 | 내용 |
| --- | --- |
| 헤더 288 × 22 | `img_gold` 26 × 14.21 + `title` 17 Bold `t800_17_bold` `Color/Gray_Black` · [Indicator](syrup-indicator-components.md) 25 × 13 |
| `Stepper` 288 × 62 | `Line` (**LINE 노드** 253 × 0) · `Stepper Item` ×6 (40 × 62) |

라인을 SLOT이나 Frame이 아닌 **LINE 노드**로 그린 유일한 Master입니다. 2겹 중첩된 `Frame 1171276632`는 `Header` / `Title`로 정리했습니다 ✅.

이 컴포넌트에 페이지의 **패딩 10 미바인딩이 36건, 라운드 23이 4건** 몰려 있습니다 → [점검 6](#6-미바인딩-수치-패딩--간격--라운드---일부-완료).

### 10. Progress Stepper — `9293:11510` · Set 2

| Property | Type | Options |
| --- | --- | --- |
| `Property 1` | VARIANT | `5` · `10` |

**360 × 184** (`Property 1=5`) · 가로 오토레이아웃 CENTER · Padding 0 · Gap 16 (`Spacing/400`)

`.primitive / Progress Stepper / Search` 인스턴스 90 × 82를 **5개 또는 10개** 나열합니다. 흰 배경 카드가 가로로 늘어선 형태입니다.

`Property 1`의 값이 `5|10`이므로 실제 의미는 **단계 개수**입니다 → [점검 1](#1-property-1--property--step-속성명-11건).

### 11. Progress Stepper / Express — `9204:10150` · Set 3

| Property | Type | Options |
| --- | --- | --- |
| `Color` | VARIANT | `Purple` · `Blue` · `Orange` |

**360 × 229** (`Color=Purple`) · 오토레이아웃 없음 (절대 배치) · 배경 **`#F2EBFB`**

| 레이어 | 타입 | 크기 | 색상 |
| --- | --- | --- | --- |
| `Line` | Vector | 347 × 117 | `Color/Gray_White` |
| `Gauge` | Vector | 107 × 20 | **`#CEB3F0`** |
| `Stepper Item` | Instance | 108 × 108 | — |
| `Stepper Item` ×3 | Instance | 64 × 64 | `Color/Gray_900` |
| `Stepper Item` | Instance | 92 × 92 | `Color/Primary_Orange` |
| `Stepper Item` | Instance | 64 × 64 | **`#9D50FF`** |

곡선 경로를 따라 단계가 배치된 **유일한 비정형 Stepper**라 오토레이아웃을 쓰지 않습니다. 아이템 크기도 64 / 92 / 108로 섞여 있습니다.

이 속성값은 원래 **`Purlpe`** 오타였고 2026-10-12에 `Purple`로 고쳤습니다 → [점검 3](#3-purlpe-오타---완료).

---

## Child Item 13종

### 12. `.primitive / … / Collect` — `9240:10615` · Set 3

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Button` | BOOLEAN | `true` | — |
| `Property 1` | VARIANT | — | `Disabled` · `Available` · `Completed` |

**8 × 62** (`Disabled`) · 세로 오토레이아웃 MIN/CENTER · Gap 8 (`Spacing/200`)

| 레이어 | 내용 |
| --- | --- |
| 단계 점 8 × 8 | `Color/Secondary_Yellow` |
| 「300금」 | 13 Medium `t1360_13_medium` `Color/Gray_200` |
| `Button` 56 × 24 | 배경 `Color/Gray_900` · `Text` 11 Bold **스타일 미적용** `Color/Gray_300` |

### 13. `.primitive / … / Pig` — `9244:11529` · Set 2

| Property | Options |
| --- | --- |
| `Active` | `False` · `True` |

**36 × 58** · 세로 오토레이아웃 · Gap 4 (`Spacing/100`)
`Ellipse` 36 × 36 `Color/Third_Pastel_Coral` + 「Gold」 11 Bold **스타일 미적용** `Color/Primary_Orange`
`Time` 13 Regular `b500_13_regular` `Color/Gray_250`

### 14. `.primitive / … / Quiz` — `9240:10150` · Set 3

| Property | Options |
| --- | --- |
| `Property 1` | `Disabled` · `Available` · `Completed` |

**40 × 61** · 세로 오토레이아웃 · Gap 4 (`Spacing/100`)
`Ellipse` 40 × 40 **`#6F7581`** + 「5금」 14 Bold `t1050_14_bold` `Color/Gray_600`
「1콤보」 12 Regular `c100_12_regular` `Color/Gray_600`

### 15. `.primitive / … / News` — `9223:22936` · Set 3

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Time` | BOOLEAN | `true` | — |
| `Property 1` | VARIANT | — | `Disabled` · `Available` · `Completed` |

**40 × 62** · 세로 오토레이아웃 CENTER/CENTER · Gap 4 (`Spacing/100`)
`Gold` 40 × 40 `Color/Third_Pastel_Coral` — **단, 외부 라이브러리의 `color/third_pastel_coral`에 바인딩** → [점검 4](#4-로컬-토큰과-이름이-같은-외부-변수---완료)
「Gold」 / `Time` 13 Bold `t1060_13_bold` `Color/Secondary_Coral`

### 16. `.primitive / … / Movie` — `9223:23488` · Set 2

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Text` | BOOLEAN | `true` | — |
| `Active` | VARIANT | — | `False` · `True` |

**62 × 62** (`Active=True`) · 세로 오토레이아웃 CENTER/CENTER · Padding 0 (`Spacing/0`) · Gap 0 (`Spacing/0`)
테두리 `Color/Primary_Orange` **2px** · 라운드 `Corner radius/circle`
`Oval` 54 × 54 `Color/Primary_Orange` + `Text` 19 Bold `t700_19_bold` `Color/Gray_White`

**패딩·간격·라운드·테두리가 모두 토큰에 묶인 페이지 내 모범 사례**입니다.

### 17. `.primitive / … / Lottery` — `9280:13039` · Set 6

| Property | Options | 의미 |
| --- | --- | --- |
| `Property 1` | `Left` · `Center` · `Right` | **위치** |
| `Active` | `False` · `True` | 상태 |

**19 × 36** · 세로 오토레이아웃 · Gap 6 (`Spacing/150`)
`Ellipse` 8 × 8 **`#1F80FF`** · 「0개」 13 Medium `t1360_13_medium` `Color/Gray_200`

### 18. `.primitive / … / Mission` — `9223:23725` · Set 2

| Property | Options |
| --- | --- |
| `Active` | `True` · `False` |

**99 × 125** · 세로 오토레이아웃 · Padding 0 (`Spacing/0`) · Gap 8 (`Spacing/200`)
`Image` 99 × 99 `Color/Gray_White` (내부 `Image` 76 × 76 + [Checkbox](syrup-checkbox-components.md) 24 × 24)
`Time` 14 Regular `b400_14_regular` `Color/Gray_400`

`Active` 옵션 순서가 **`True` → `False`**로, 다른 컴포넌트(`False` → `True`)와 반대입니다.

### 19. `.primitive / … / Personality-Test` — `9223:25611` · Set 9

| Property | Options | 의미 |
| --- | --- | --- |
| `Property` | `1` · `2` · `3` | **위치** |
| `Step` | `Disabled` · `Available` · `Completed` | **상태** |

**44 × 61** · 세로 오토레이아웃 · Gap 4 (`Spacing/100`)
`🟧syrup_img_personality_test_progress01_on` 44 × 40 `Color/Gray_800`
「5금」/「10금」 14 Bold `t1050_14_bold` · 「1개」 12 Regular `c100_12_regular` `Color/Gray_400`

레이어명의 **🟧 접두사는 파일 전체 100건의 이미지 에셋 관례**라 유지했습니다. 다만 `on` 상태 에셋 이름이 `Disabled` variant에도 그대로 쓰입니다.

### 20. `.primitive / … / Search` — `9293:10405` · Set 4

| Property | Options |
| --- | --- |
| `Active` | `False` · `True` |
| `Size` | `L` · `S` |

**90 × 82** (`Active=True, Size=L`) · 세로 오토레이아웃 CENTER/CENTER
Padding `0 / 8 / 0 / 8` (`Spacing/200`) · Gap 2 (`Spacing/50`)
배경 `Color/Gray_White` · 테두리 `Color/Gray_200` 1px · 라운드 16 (`Corner radius/400`)

| 레이어 | 내용 |
| --- | --- |
| `Text` 74 × 20 | 16 Bold `t900_16_bold` `Color/Gray_100` |
| `Badge` 58 × 26 | 배경 **`#FF5252`** · `Image` 16 × 10 · 「당첨」 14 Bold `t1050_14_bold` `Color/Gray_White` |

### 21. `.primitive / … / Express` — `9188:34316` · Set 11

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Text` | BOOLEAN | `true` | — |
| `Color` | VARIANT | — | `Disabled` · **`Purple`** · `Blue` · `Orange` · `Primary` |
| `Active` | VARIANT | — | `False` · `True` |
| `Special` | VARIANT | — | `False` · `True` |

**64 × 64** · 세로 오토레이아웃 CENTER/CENTER · Padding 0 (`Spacing/0`) · Gap 0 (`Spacing/0`)
배경 `Color/Gray_900` · 테두리 `Color/Gray_White` **5px** · 라운드 `Corner radius/circle`
「15금」 15 Bold `t1000_15_bold` `Color/Gray_600`

**11 variant는 5 × 2 × 2 = 20의 불완전 매트릭스**입니다.

| Color | Active=F, Special=F | Active=T, Special=F | Active=F, Special=T | Active=T, Special=T |
| --- | --- | --- | --- | --- |
| `Disabled` | ✅ | — | — | — |
| `Purple` | — | ✅ | ✅ | ✅ |
| `Blue` | — | ✅ | ✅ | ✅ |
| `Orange` | — | ✅ | ✅ | ✅ |
| `Primary` | — | ✅ | — | — |

Figma는 빠진 조합을 선택했을 때 **임의의 다른 variant로 대체**하므로, 의도적 생략이라면 `Disabled`/`Primary`를 별도 축으로 분리하는 편이 안전합니다.

### 22. `.primitive / … / Check-In / List Item` — `9272:14770` · Component

| Property | Type | Default |
| --- | --- | --- |
| `Bubble` | BOOLEAN | `true` |

**74 × 113** · 세로 오토레이아웃 · Gap 4 (`Spacing/100`)

| 레이어 | 내용 |
| --- | --- |
| `Icon` 74 × 92 | `Check-In / Button` 인스턴스 74 × 80 · `Check-In / Checkbox` 18 × 18 `Color/Primary_Orange` |
| `Time` | 12 Medium **스타일 미적용** `Color/Opacity_Black_200` |
| `Bubble` | [Bubble](syrup-bubble-components.md) 인스턴스 58 × 31 |

Child Item 중 **유일하게 다른 Child Item 2개를 품는 2단 구조**입니다. 레이어명 `time`은 `Time`으로 정리했습니다 ✅.

### 23. `.primitive / … / Check-In / Checkbox` — `9263:14762` · Set 3

| Property | Options |
| --- | --- |
| `Property 1` | `Disabled` · `Available` · `Completed` |

**18 × 18** · 배경 `Color/Gray_800` · 라운드 `Corner radius/circle` · 자식 없음

이름은 Checkbox지만 **[Checkbox](syrup-checkbox-components.md) 컴포넌트와 무관한 원형 점**입니다. 같은 Master 안의 `Mission`은 실제 Checkbox 인스턴스를 쓰므로 혼동 여지가 있습니다.

### 24. `.primitive / … / Check-In / Button` — `9263:14673` · Set 12

| Property | Options | 의미 |
| --- | --- | --- |
| `Step` | `1` · `2` · `3` · `4` | **위치** |
| `Property` | `Available` · `Disabled` · `Completed` | **상태** |

**74 × 80** · 오토레이아웃 없음
`Bubble` Vector 60 × 65.61 `Color/Gray_White` · `Image` 50 × 50 `Color/Primary_Orange`

19번 `Personality-Test`와 **`Property`·`Step`의 의미가 정확히 뒤바뀌어** 있습니다 → [점검 1](#1-property-1--property--step-속성명-11건).

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-6699)

### 1. 서비스의 진행 방식에 맞는 유형을 사용해요

누적 금액·참여 횟수·완료한 미션 등 각 서비스의 진행 방식에 맞는 Progress Stepper를 사용해요.
목표 조건과 보상, 단계 구성을 함께 유지하고 다른 서비스의 형태를 임의로 섞지 않아요.

- 비교: Collect · 누적 금액 / Express · 경로형 도전
- [가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-6701)

### 2. 조건 달성과 보상 수령 완료를 구분해요

보상을 직접 받는 단계는 조건을 달성하면 Available, 보상 수령이 끝나면 Completed로 표시해요.
아직 조건을 충족하지 못한 단계는 Disabled로 두고, 받을 수 있는 단계가 완료로 보이지 않도록 해요.

- 비교: Available · 받기 가능 / Completed · 수령 완료
- [가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-6785)

### 3. 현재 진행값과 목표 조건을 함께 보여줘요

현재 횟수나 누적값을 각 단계의 목표 조건과 함께 보여줘요.
선의 진행 위치와 활성 단계는 실제 진행값에 맞추고, 보상 수령 여부는 단계별 상태로 구분해요.

- 비교: Pig · 현재 횟수 / News · 참여 횟수와 목표
- [가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-6906)

### 4. 단계 수에 맞는 구성을 사용해요

검색형은 5개와 10개 구성 중 해당 미션의 단계 수에 맞는 유형을 사용해요.
각 구성의 아이템 크기와 배열을 유지하고, 한 구성을 임의로 축소하거나 단계를 추가해 맞추지 않아요.

- 비교: 5개 · 큰 아이템 / 10개 · 작은 아이템
- [가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7018)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-6700)

예제 설명은 Figma의 현재 문구와 동일하게 진행 상태·표현 방식 중심으로 작성했어요. 아래 연결 컴포넌트 열은 AI가 에셋을 선택하기 위한 참조 정보이며 화면에 노출할 설명이나 서비스 사용처 문구가 아니에요.

| 예제 | 설명 | 연결 컴포넌트 | 표시 크기 | 링크 |
| --- | --- | --- | --- | --- |
| A. 누적 금액 보상 | 누적 금액에 따른 보상 단계를 보여줘요. 단계별 목표 금액과 보상, 수령 상태를 함께 표시해요. | `Collect` | 328 × 64 | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7322) |
| B. 반복 참여 횟수 | 현재 참여 횟수와 구간별 보상을 보여줘요. 말풍선의 횟수와 진행 위치가 실제 진행값에 맞도록 구성해요. | `Pig` | 328 × 99 | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7362) |
| C. 연속 참여 보상 | 연속 참여에 따른 단계와 보상을 보여줘요. 받을 수 있는 보상과 이미 받은 보상을 구분해요. | `Quiz` | 328 × 155 | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7414) |
| D. 누적 시청 보상 | 현재 횟수와 목표 횟수, 구간별 보상을 보여줘요. 단계 조건과 보상 수령 상태를 함께 확인할 수 있도록 해요. | `News · Scroll=False` | 320 × 142 | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7473) |
| E. 완료 개수별 보상 | 완료한 개수에 따른 보상을 보여줘요. 각 단계의 조건과 현재 받을 수 있는 보상을 구분해요. | `Personality-Test` | 328 × 137 | [E](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7523) |
| F. 체크인 미션 보상 | 수령 전에는 ‘5금 받기’와 진행 지점으로, 수령 후에는 ‘5금 적립’ 문구와 체크 표시로 구분해요. | `Check-In` | 316 × 123 | [F](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7574) |
| G. 반복 참여 완료 표시 | 반복 참여 항목의 활성 상태를 보여줘요. 각 항목에 표시된 보상과 참여 상태를 함께 확인할 수 있도록 해요. | `Movie` | 194 × 132 | [G](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7659) |
| H. 순서별 미션 완료 | 첫 번째·두 번째·세 번째 단계의 완료 여부를 보여줘요. 완료한 항목은 체크 표시로 구분해요. | `Mission` | 360 × 125 | [H](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7687) |
| I. 복권 지급 조건 | 완료 개수에 따른 지급 단계를 보여줘요. 단계의 진행 상태와 지급 수량을 함께 안내해요. | `Lottery` | 328 × 109 | [I](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7715) |
| J. 검색 미션 5개 | 5개 단계로 구성해요. 각 단계의 행동과 결과 표시를 기존 아이템 구성에 맞춰 보여줘요. | `Progress Stepper · Property 1=5 · Item Size=L` | 360 × 184 | [J](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7758) |
| K. 검색 미션 10개 | 10개 단계로 구성해요. 작은 아이템을 두 줄로 배열한 구성을 유지해 전체 단계를 보여줘요. | `Progress Stepper · Property 1=10 · Item Size=S` | 360 × 168 | [K](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7796) |
| L. 경로형 도전 | 경로를 따라 이어지는 보상과 현재 도전할 단계를 보여줘요. 컬러와 스페셜 단계 구성을 유지해요. | `Express · Color=Blue` | 360 × 229 | [L](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11808-7861) |

## 예제 레이아웃과 상태 참조 기준

### 문서 배치

- Guidelines는 **960 × 1695**, Usage는 **4960 × 545**예요. 흰 배경·모서리 24의 기존 섹션 스타일을 사용해요.
- 예제 **A~L 12개를 가로 한 줄**로 배치해요. 예제 폭 360, 가로 간격 40, 섹션 상하좌우 여백 100이에요. 두 줄로 나눈 이전 배치는 현재 기준이 아니에요.
- 제목·설명 영역은 가장 긴 설명 높이에 맞춰 예제 시작점을 정렬하고, 설명 영역 끝과 Slot 사이 간격은 50을 유지해요.
- Slot은 패딩 0, 좌측·상단 정렬, 높이 Hug예요. 컴포넌트는 원래 크기로 직접 배치하며 Slot 폭 360에 맞춰 모든 컴포넌트를 늘리거나 줄이지 않아요.
- 예제 구성에 필요하지 않은 전체 서비스 화면과 별도 ‘화면’ 래퍼는 사용하지 않았어요. 컴포넌트 자체의 패딩·이미지·배경은 해당 표현에 필요한 규격으로 유지했어요.
- 사용처·컴포넌트 이름은 예제 설명 문구에서 제거했어요. 에셋 연결 정보는 이 MD의 참조 표에서 확인해요.

### 대표 상태와 전체 상태 디자인

- 예제는 유형별 **대표 장면 한 개씩** 보여줘요. 모든 진행 상태를 각 예제에 반복해서 나열하지 않아요.
- 공통적인 조건 미충족·받기 가능·수령 완료 구분은 가이드라인 2번에서 설명해요.
- 체크인의 수령 전후 변화는 예제 F 설명에 담았어요. 별도 가이드라인 5번은 2번과 중복되어 삭제했으며 현재 가이드라인은 **1~4번**이에요.
- 예제 F는 현재 ‘5금 적립’과 체크 표시로 완료한 단계, 다음 보상의 받기 가능 상태를 함께 보여주는 대표 장면 한 개예요. 수령 전후 화면 두 개가 추가되어 있다는 뜻이 아니에요.
- 전체 상태 디자인은 기존 디자인 파일을 참고해요. 사용자가 Section 1을 삭제했고 현재 페이지에 없음을 확인했으므로 Section 1을 전체 상태의 참조 위치로 안내하지 않아요. 별도 파일의 링크는 전달되지 않아 임의로 만들지 않았어요.

### AI가 상태를 적용할 때

- `Disabled / Available / Completed`는 직접 보상을 수령하는 유형의 상태 기준이에요. 값 이름은 하위 컴포넌트에 따라 `Property 1`, `Property`, `Step`에 연결되어 있으므로 실제 에셋의 속성을 확인해요.
- 모든 유형에 동일한 State 속성이 있다고 가정하지 않아요. Pig·Movie·Mission·Lottery·Search 등은 `Active`로 표현하는 구조도 있어요. 단순 활성 상태를 보상 수령 완료로 임의 해석하지 않아요.
- Search의 상위 `Property 1=5 / 10`은 단계 개수이고, 하위 Search의 `Size=L / S`는 아이템 크기예요. 임의의 이름으로 속성을 바꾸거나 자동으로 없는 단계 수를 만들지 않아요.
- Check-In은 버튼·체크 표시·연결선의 상태를 함께 확인해요. 받기 가능한 버튼과 수령 완료 체크가 같은 단계에 섞여 표시되지 않도록 해요.
- 실제 진행값, 단계별 목표 조건, 보상 수령 여부는 각각 확인해요. 목표 달성만으로 Completed 처리하거나 진행값과 관계없이 선을 채우지 않아요.
- 샘플 금액·횟수·보상은 각 사용처의 데이터예요. 예제의 숫자를 모든 서비스의 공통 조건으로 적용하지 않아요.
- 5개·10개는 검색형 자체의 단계 배열이고, Usage의 한 줄 배치 규칙과는 별개예요. Usage를 한 줄로 바꿨다고 10개 아이템의 두 줄 배열을 펼치지 않아요.
- 기존 상태별 디자인을 참고하며 임의로 전환 시간·스프링 값 등 새 애니메이션 공통 규칙을 추가하지 않아요.

---

## 설계 규칙 요약

> 이 절의 토큰·외부 참조·스타일 집계는 기존 마스터 보드의 과거 기록이에요. 현재 문서 예제까지 포함한 재집계 결과는 아니에요.

### 라인 표현 4가지

| 방식 | 사용처 |
| --- | --- |
| **SLOT** `Line` | Collect · Pig · Check-In · Lottery |
| **Frame** `Line` | Personality-Test · Quiz |
| **LINE 노드** | News |
| **Vector** | Express |
| **라인 없음** | Movie · Mission · Progress Stepper(Search) |

`Line`을 SLOT 속성으로 노출한 4종은 **게이지 길이를 인스턴스에서 교체**할 수 있습니다. 나머지는 게이지 폭을 직접 수정해야 합니다.

### 게이지 색 조합

| Master | Line (트랙) | Gauge (채움) |
| --- | --- | --- |
| Collect | `Color/Gray_850` | `Color/Secondary_Yellow` |
| Pig | `Color/Third_Pastel_Coral` | `Color/Primary_Orange` |
| Personality-Test | `Color/Gray_800` | — |
| Check-In | `Color/Gray_800` | `Color/Primary_Orange` |
| Quiz | `#6F7581` | `Color/Third_Pastel_Coral` |
| Lottery | `Color/Gray_White` | — |
| Express | `Color/Gray_White` | `#CEB3F0` |

트랙 색이 `Gray_800` / `Gray_850` / `Third_Pastel_Coral` / `Gray_White` / 미토큰으로 **5가지**입니다. 배경 위에서의 대비를 맞춘 결과로 보이나, `Gray_800`과 `Gray_850`이 나란히 쓰이는 것은 통일 여지가 있습니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| Padding | **전량 `Spacing/*` 바인딩** ✅ (News 계열 포함) |
| Gap | 16(`Spacing/400`) · 8(`Spacing/200`) · 4(`Spacing/100`) · 2(`Spacing/50`) · 6(`Spacing/150`) 바인딩 |
| 라운드 | **전량 바인딩** ✅ — 16(`Corner radius/400`) · circle |
| 텍스트 스타일 | 13px 이상 전부 적용 ✅ · 10~12px 중심으로 **65건** 미적용 |
| 색상 | 미바인딩 39건 (대부분 도메인 컬러) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

---

## 점검 필요 사항

> 아래 토큰·스타일·네이밍·구조 개선 제안과 건수는 과거 점검 기록이에요. 이번에는 사용 가이드·예제와 페이지 구성을 업데이트했으며 마스터 전체의 토큰·구조를 새로 점검하거나 재설계하지 않았어요. 현재 사용 기준은 가이드라인·Usage를 우선해요.

### 1. `Property 1` / `Property` / `Step` 속성명 11건

같은 개념에 **세 가지 이름**이 붙어 있습니다.

**진행 상태 3단계** (`Disabled` / `Available` / `Completed`)

| 속성명 | 컴포넌트 |
| --- | --- |
| `Property 1` | `.primitive / … / Collect` · `/ Quiz` · `/ News` · `/ Check-In / Checkbox` |
| `Property` | `.primitive / … / Check-In / Button` (순서도 `Available` 먼저) |
| `Step` | `.primitive / … / Personality-Test` |

**위치 인덱스**

| 속성명 | 컴포넌트 | 값 |
| --- | --- | --- |
| `Property` | `.primitive / … / Personality-Test` | `1` · `2` · `3` |
| `Step` | `.primitive / … / Check-In / Button` | `1` · `2` · `3` · `4` |
| `Property 1` | `.primitive / … / Lottery` | `Left` · `Center` · `Right` |

**`Personality-Test`와 `Check-In / Button`은 `Property`와 `Step`의 의미가 정확히 뒤바뀌어 있습니다.** 한쪽은 `Property`가 위치·`Step`이 상태, 다른 쪽은 그 반대입니다. 같은 페이지 안에서 가장 혼동을 부르는 지점입니다.

**단계 개수**

| 속성명 | 컴포넌트 | 값 |
| --- | --- | --- |
| `Property 1` | `Progress Stepper` (Master) | `5` · `10` |

권장 정리안:

| 현재 | 제안 |
| --- | --- |
| 상태 3단계 → `Property 1` / `Property` / `Step` | **`State`** |
| 위치 → `Property` / `Step` / `Property 1` | **`Step`** |
| 단계 개수 → `Property 1` | **`Count`** 또는 **`Steps`** |

이름만 바꾸는 작업이지만 **`Property` ↔ `Step` 교차 사용**이 있어, 한 컴포넌트씩 값을 확인하며 진행해야 합니다.

### 2. 마스터와 Child Item 이름이 어긋남

| Master | Child Item |
| --- | --- |
| `Progress Stepper` | `.primitive / Progress Stepper / Search` |

나머지 10쌍은 모두 이름을 공유합니다. Master를 **`Progress Stepper / Search`**로 바꾸면 일관됩니다.

다만 이 Master는 이름에 서비스명이 없어 **페이지 전체를 대표하는 기본형으로 읽힐 수 있는** 위치입니다. 실제로 범용 Stepper로 쓸 의도였는지, 검색 전용인지에 따라 결정이 갈립니다.

### 3. `Purlpe` 오타 — ✅ 완료

| 컴포넌트 | 속성 | 값 |
| --- | --- | --- |
| `Progress Stepper / Express` `9204:10150` | `Color` | ~~`Purlpe`~~ → **`Purple`** · `Blue` · `Orange` |
| `.primitive / … / Express` `9188:34316` | `Color` | `Disabled` · `Purple` · `Blue` · `Orange` · `Primary` |

Master만 오타였고 Child Item은 정상이었습니다. 인스턴스 0건이라 교체 영향 없이 수정했습니다.

[Button](syrup-button-components.md)의 `Coner`→`Corner`, [Card](syrup-card-components.md)의 `Viariant`→`Variant` 등 지금까지 고친 오타와 같은 성격입니다.

### 4. 로컬 토큰과 이름이 같은 외부 변수 — ✅ 완료

`.primitive / … / News`의 `Gold` 레이어가 **외부 라이브러리의 `color/third_pastel_coral`**에 묶여 있었습니다.

| 구분 | 변수명 | 컬렉션 |
| --- | --- | --- |
| 수정 전 | `color/third_pastel_coral` | **외부** (`semantic tokens`) |
| 수정 후 | `Color/Third_Pastel_Coral` | `global` (로컬, 유일한 로컬 컬렉션) |

값은 같지만 외부 라이브러리가 바뀌면 이 파일이 따라 흔들립니다. **원본 1곳을 교체해 인스턴스 2곳까지 3건 모두 해소**됐습니다.

> **파일 전체 조사 결과**: 이 파일에는 로컬 변수 컬렉션이 **`global` 하나(변수 110개)** 뿐인데, 파일 전체에 **외부 변수 바인딩이 4,557건** 있습니다. 이 가운데 `paragraphSpacing/0`·`paragraphIndent/0` 4,152건은 텍스트 노드에 자동으로 붙는 기본값이고, `Spec docs/*` 265건은 보드 주석 영역입니다. **나머지 약 140건이 실제 정리 대상**입니다.
>
> | 외부 변수 | 건수 |
> | --- | --- |
> | `fontFamilies/pretendard` · `letterSpacing/3` · `fontSize/1·2` · `fontWeights/*` · `lineHeights/10` | 78 |
> | `Color/Gray_White` (로컬과 **동명**) | 9 |
> | `Color/Opacity_Black_100` (로컬과 **동명**) | 5 |
> | `spacing/spacing_50·200·300·400` | 16 |
> | `typeset_lg_medium/*` | 10 |
> | `border/thumbnail_border` | 4 |
> | `color/third_pastel_coral` (로컬과 동명) | 3 |
> | `styles/scrim20` | 2 |
>
> 타이포 계열 78건은 앞서 기록한 **"텍스트 스타일 없이 외부 타이포 변수만 바인딩된 18개 노드"**([Ticker](syrup-design-tokens.md) 15 · [Bottom Info](syrup-bottom-info-components.md) 2 · [List Header](syrup-list-header-components.md) 1)의 실체입니다.
>
> 이전 문서들의 "외부 토큰" 집계는 변수의 `remote` 플래그에 의존했는데, **이 변수들은 `remote`가 `false`로 읽혀 누락**됐습니다. 로컬 변수 ID 목록과 대조하는 방식이 정확합니다. 이 수치는 [syrup-design-tokens.md](syrup-design-tokens.md)에 반영이 필요합니다.

### 5. 미바인딩 색상 39건

| 색상 | 건수 | 사용처 | 성격 |
| --- | --- | --- | --- |
| `#1F80FF` | 8 | `.primitive / … / Lottery` 단계 점 | [Card](syrup-card-components.md)에서도 6건 — **파일 전체 14건 이상** |
| `#9D50FF` | 5 | Express 보라 | 도메인 컬러 |
| `#50ABFF` | 5 | Express 파랑 | 도메인 컬러 |
| `#FF5252` | 4 | Search `Badge` 배경 | — |
| `#CA8CF7` | 3 | Express 연보라 | 도메인 컬러 |
| `#7D7CFF` | 3 | Express 남보라 | 도메인 컬러 |
| `#6F7581` | 3 | Quiz `Line` 트랙 | 다크 UI |
| `#F43437` | 2 | — | — |
| `#5950F6` | 2 | Express | 도메인 컬러 |
| `#545B69` | 1 | **Quiz 배경** | 다크 UI |
| `#F2EBFB` · `#CEB3F0` · `#DFEDFA` | 각 1 | Express 배경·게이지 | 도메인 컬러 |
| `#D8D8D8` | 1 | — | `Gray_750`(#DDDDDD)과 근사 |

**Express 계열 21건은 서비스 고유 컬러**로, [Label Metric](syrup-label-components.md)·[Product Grid](syrup-product-grid-components.md)에서 도메인 컬러를 토큰화 대상에서 제외한 기준을 따르면 그대로 두는 쪽입니다.

판단이 필요한 것은 나머지입니다.

- **`#545B69` + `#6F7581`** — Quiz의 다크 배경/트랙 2종. 파일 내 유일한 다크 UI라 토큰을 만들지, 단일 사용으로 둘지 결정이 필요합니다.
- **`#1F80FF`** — Card와 중복이라 이미 토큰 후보로 올라온 색입니다.
- **`#D8D8D8`** — `Gray_750`(#DDDDDD)과 3 차이. 의도적 구분이 아니라면 토큰으로 바꿀 수 있습니다.

### 6. 미바인딩 수치 (패딩 · 간격 · 라운드) — ✅ 일부 완료

| 값 | 전체 건수 | 원본 노드 | 대응 토큰 | 상태 |
| --- | --- | --- | --- | --- |
| **패딩 10** | 42 | **6** | `Spacing/250` | ✅ 완료 |
| **Gap 10** | 12 | **2** | `Spacing/250` | ✅ 완료 |
| **라운드 23** | 6 | **4** | `Corner radius/circle` | ✅ 완료 |
| 패딩 0.5 | 17 | — | 없음 | 중앙 정렬 보정 — 대상 아님 |
| 패딩 11 | 6 | — | 없음 | 보류 |
| 패딩 35 | 2 | — | 없음 | 보류 |
| Gap −6 / −3 | 5 / 4 | — | — | 단계 겹침 — 의도 |
| Gap 3·13·14·18·33·41·61 | 각 1 | — | 없음 | 보류 |

라운드 23은 대상이 전부 40 × 40 원형이라 23이 이미 반지름(20)을 넘깁니다. `circle`로 바꿔도 **보이는 모양이 바뀌지 않습니다.**

> **측정 주의 — 전체 건수와 원본 노드 수는 다릅니다.**
>
> 처음 집계한 42 / 12 / 6건은 **인스턴스가 원본에서 상속받은 값까지 센 수치**였습니다. 실제 수정이 필요한 원본 노드는 6 / 2 / 4건이고, 원본을 고치면 상속분은 자동으로 따라옵니다.
>
> 인스턴스 내부 노드에 직접 바인딩하면 **불필요한 오버라이드**가 생기므로, 조상에 `INSTANCE`가 있는 노드는 제외하고 작업했습니다. 수정 후 재스캔에서 세 항목 모두 **0건**입니다.
>
> [Grid List](syrup-grid-list-components.md)·[Card](syrup-card-components.md)에서 `findAllWithCriteria`가 중첩 인스턴스를 **덜 세어** 문제였다면, 이번은 반대로 **더 센** 경우입니다. 색상·토큰 집계는 "원본 노드 수"와 "화면에 보이는 횟수"를 구분해 읽어야 합니다.

### 7. 텍스트 스타일 미적용 66건

보드 장식 4건을 뺀 컴포넌트 내부 기준입니다.

| 크기/굵기 | 건수 | 판단 |
| --- | --- | --- |
| 11 Medium | 19 | 방침상 제외 |
| 11 Bold | 11 | 방침상 제외 |
| 11 Regular | 6 | 방침상 제외 |
| 10 Bold | 7 | 방침상 제외 |
| 10 ExtraBold | 5 | 방침상 제외 |
| **12 Bold** | **12** | 토큰 없음 — 판단 필요 |
| **12 Medium** | **5** | 토큰 없음 — 판단 필요 |
| ~~14 Regular~~ | ~~1~~ | ✅ **`b400_14_regular` 적용 완료** |

10~11px 48건은 당시 점검에서 제외한 기록이에요. 현재 11 크기의 토큰도 존재하므로 ‘10~11px은 모두 토큰화 대상이 아니다’라는 공통 규칙으로 적용하지 않아요.

14 Regular 1건은 `Progress Stepper / Quiz`의 「**알림받는 중**」이었고, `b400_14_regular`를 연결했습니다. 남은 미적용은 **65건**입니다.

**12px 17건**은 위치가 둘로 갈립니다.

| 분류 | 건수 | 내용 |
| --- | --- | --- |
| 12 Bold | 12 | `Progress Stepper`(Search) 단계 라벨 「첫번째」~「열번째」 10건 + 「애플에어팟 3세대」 2건 |
| 12 Medium | 5 | `Check-In` 「미션 N개」 4건 + `Check-In / List Item` 1건 |

12px에는 `c100_12_regular` 하나만 있습니다. [Grid List](syrup-grid-list-components.md)에서 `12 Bold` 토큰화를 보류한 건이 있어, **같이 판단하는 편이 효율적**입니다.

### 8. 폰트 굵기 ExtraBold · SemiBold

| 굵기 | 건수 |
| --- | --- |
| Pretendard Bold | 140 |
| Pretendard Medium | 43 |
| Pretendard Regular | 37 |
| **Pretendard ExtraBold** | **5** |
| **Pretendard SemiBold** | **2** |

SemiBold 2건은 보드 장식(40px)이라 제외 대상이고, **ExtraBold 5건(10px)은 컴포넌트 내부**입니다.

[Card](syrup-card-components.md)에서도 같은 사안이 남아 있어, **타이포 스케일에 ExtraBold를 넣을지 함께 결정**하는 것이 좋습니다.

### 9. 마스터 11종 전부 인스턴스 0건

**2026-10-12의 과거 기록이에요.** 현재 Guidelines·Usage에는 인스턴스가 있으므로 미사용이거나 변경 영향이 없다는 뜻이 아니에요.

| 구분 | 인스턴스 |
| --- | --- |
| Master 11종 | **전부 0** |
| Child Item 13종 | Progress Stepper 페이지 **내부에서만** 사용 |

Progress Stepper는 **서비스 화면에 직접 들어가는 완성 블록**이라, 다른 컴포넌트 보드에 끌어다 쓸 일이 거의 없습니다. [Loader](syrup-loader-components.md)·[Lottie](syrup-lottie-components.md)와 같은 이유입니다.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

### 10. 레이어명 정리 — ✅ 완료 (138건)

`Steeper` → `Stepper` 오타 **64건**에 이어, 기본 이름·소문자·스네이크 케이스 **74건**을 정리했습니다.

#### 기본 이름 → 의미 부여 (40건)

| 변경 전 | 변경 후 | 위치 | 건수 | 근거 |
| --- | --- | --- | --- | --- |
| `Frame 1171277246` | `Icon` | Personality-Test | 9 | 단계 이미지 + 금액 텍스트 묶음 |
| `Frame 1171277555` | `Check` | Personality-Test | 9 | 16 × 16, 완료 표시 자리 |
| `Vector 66` | `Special` | Express | 6 | `Special=True` variant에만 존재 (78 × 78 `#F2F2F2`) |
| `Vector 66 (Stroke)` | `Special Outline` | Express | 6 | 같은 조건 (88 × 88 흰색 외곽) |
| `Frame 1171277247` | `Dot` | Lottery | 6 | 12 × 12, 단계 점 |
| `Frame 1171276892` | `Dot` | Collect | 3 | 8 × 8, 단계 점 |
| `Frame 1171276891` | `Content` | Collect | 3 | 금액 + 버튼 묶음 |
| `Frame 1171276632` | `Header` | News | 1 | 288 × 22, 타이틀 + Indicator |
| `Frame 1171276632` | `Title` | News | 1 | 160 × 22 (2겹 중첩 해소) |
| `Frame 1171276634` | `Badge` | `.primitive / … / Quiz` | 1 | 25 × 15 `Gray_100` 배경 + 「받기」 |
| `Frame 1171277120` | `Check-In Items` | 보드 | 1 | Check-In Child Item 3종 묶음 |

#### 소문자 → 대문자 (33건)

| 변경 전 | 변경 후 | 건수 |
| --- | --- | --- |
| `sub text` | `Sub Text` | 12 |
| `time` | `Time` | 5 |
| `title` | `Title` | 4 |
| `text` | `Text` | 3 |
| `title1` · `title2` | `Title 1` · `Title 2` | 2 |
| `gold` | `Gold` | 1 |

파일 전체 레이어명은 **대문자 시작이 80%**(4,822 : 1,172)이고 `text` 대283/소133 · `title` 대82/소12 · `time` 대33/소5로 대문자가 다수라, 관례에 맞춰 올렸습니다.

#### 스네이크 케이스 (1건)

`Stepper_wrapper` → **`Stepper Wrapper`**

정리 후 재스캔 결과 **기본 이름 0건**입니다.

### ⚠️ 앞선 기록 정정 — 🟧는 오류가 아니라 관례입니다

`🟧syrup_img_personality_test_progress01_on`의 이모지를 정리 대상으로 적었던 것은 **잘못된 판단**이었습니다.

| 접두사 | 파일 전체 건수 |
| --- | --- |
| `🟧` | **100** |
| `🎉` | 5 |

[Product Scroll](syrup-product-scroll-components.md) 15 · Progress Stepper 13 · ❖Components 13 등 **거의 모든 페이지에 걸친 이미지 에셋 표시 관례**입니다. 손대지 않았습니다.

다만 **`_on` 에셋명이 `Disabled` variant에도 그대로 쓰이는 점**은 남아 있습니다. 에셋 자체의 이름이라 판단이 필요합니다.

### 10-1. 남은 레이어명 — `gold_test4`

| 레이어 | 위치 |
| --- | --- |
| `gold_test4 1` | `.primitive / … / Express` |
| `gold_test4 2` | `Progress Stepper / Quiz` |

> **정정 (2026-10-12)** — 처음 이 항목을 파일 전체 **17건**으로 적었는데, 그것은 `gold_test4 1` **하나의 이름만** 센 수치였습니다. `gold_test4 2` · `3` 등을 포함한 실제 합계는 **56건 / 12개 페이지**입니다 → [Swipe 점검 7](syrup-swipe-components.md#7-gold_test4-3--파일-전체-56건)에 페이지별 내역을 정리했습니다.

둘 다 **IMAGE 채움을 가진 실제 에셋**입니다. `test4`라는 작업용 이름이 **파일 전체 56건**으로 퍼져 있어, Progress Stepper의 2건만 고치면 오히려 어긋납니다. [News](#9-progress-stepper--news--922323142--set-2)가 쓰는 `img_gold`가 같은 역할이므로 **파일 전체를 한 번에 맞추는 편**이 낫습니다.

### 10-2. 새로 발견 — 빈 `Check` 프레임 6건

`.primitive / … / Personality-Test`의 `Check` 16 × 16 프레임 9개 중 **6개가 자식 없는 빈 프레임**입니다. 나머지 3개만 `Fill 1 (Stroke)` 벡터를 담고 있습니다.

variant 간 레이어 구성을 맞추려고 빈 자리를 남긴 것으로 보여 **삭제하지 않았습니다.** 의도가 아니라면 6건 제거 대상입니다.

### 11. Express variant 매트릭스 불완전

`.primitive / … / Express`는 `Color`(5) × `Active`(2) × `Special`(2) = **20 중 11개**만 존재합니다 → [21번 표](#21-primitive----express--918834316--set-11)

`Disabled`는 `Active=False, Special=False` 하나뿐이고, `Primary`는 `Active=True, Special=False` 하나뿐입니다. 상태를 나타내는 `Disabled`와 브랜드 색인 `Primary`가 **색상 축에 섞여 들어간 결과**입니다.

Master 쪽은 `Purple`·`Blue`·`Orange` 3색만 노출하므로 `Disabled`·`Primary`는 Master에서 선택할 수 없습니다.

구조를 정리한다면 `Color`는 `Purple`·`Blue`·`Orange` 3색으로 두고, `Disabled`는 `State` 축으로, `Primary`는 별도 판단으로 분리하는 방향입니다. 다만 **variant 11개를 재구성하는 작업**이라 비용이 작지 않습니다.

### 12. 타 페이지·외부 라이브러리 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Bubble](syrup-bubble-components.md) | `Bubble` | 5 |
| [Checkbox](syrup-checkbox-components.md) | `Checkbox` | 4 |
| [Indicator](syrup-indicator-components.md) | `Indicator` · `.primitive / Indicator / Number` | 4 |
| ❖System Components | `Section Header` 2 · `Title Bar` 1 | 3 |
| [Button](syrup-button-components.md) | `Text Button` | 1 |
| [Icon Button](syrup-icon-button-components.md) | `Icon Button / Info` | 1 |
| ❖Components | `Icon / Arrow` | 1 |
| **외부 라이브러리** | `syrup_ico_16_alerm_off_primary` | **1** |
| 외부 아이콘 | `syrup_ico/contents/syrup_ico_24_refresh_gray_400` | 1 |

**외부 라이브러리 인스턴스 1건**(`syrup_ico_16_alerm_off_primary`, `Progress Stepper / Quiz`의 알림 아이콘)은 아이콘 세트 소속이라 [AD](syrup-ad-components.md)와 같은 예외로 둘지 확인이 필요합니다.

### 13. `Active` 옵션 순서 불일치 — ✅ 완료

| 컴포넌트 | `Active` 순서 |
| --- | --- |
| `.primitive / … / Pig` | `False` → `True` |
| `.primitive / … / Movie` | `False` → `True` |
| `.primitive / … / Lottery` | `False` → `True` |
| `.primitive / … / Search` | `False` → `True` |
| `.primitive / … / Express` | `False` → `True` |
| `.primitive / … / Mission` | ~~`True` → `False`~~ → **`False` → `True`** ✅ |

`Mission`만 반대였습니다. Figma는 **첫 variant를 기본값**으로 쓰므로 인스턴스를 새로 놓으면 `Mission`만 활성 상태로 시작했습니다. variant 순서를 맞춰 해소했습니다.

---

## 정리 우선순위

### 이번 업데이트 (2026-11-10)

가이드라인 4개와 Usage A~L을 추가했어요. 상태 변경의 공통 기준은 가이드라인 2번에서 설명하고, 체크인의 수령 전후 문구·체크 변화는 예제 F에 반영했어요. Usage는 가로 한 줄로 정렬했으며 설명에서 사용처·컴포넌트 이름을 제거하고 표현 방식 중심으로 정리했어요. Section 1의 아노테이션은 작업 당시 30개 제거했으며, 이후 Section 1 자체는 사용자가 삭제했어요. 삭제된 참조 화면을 재생성하지 않아요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **155건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | `Purlpe` → `Purple` ([3](#3-purlpe-오타---완료)) | 1건 |
| 2 | 라운드 23 → `Corner radius/circle` ([6](#6-미바인딩-수치-패딩--간격--라운드---일부-완료)) | 원본 4건 (전체 6건 해소) |
| 3 | 패딩 10 · Gap 10 → `Spacing/250` ([6](#6-미바인딩-수치-패딩--간격--라운드---일부-완료)) | 원본 8건 (전체 54건 해소) |
| 4 | 「알림받는 중」 → `b400_14_regular` ([7](#7-텍스트-스타일-미적용-66건)) | 1건 |
| 5 | 외부 `color/third_pastel_coral` → 로컬 ([4](#4-로컬-토큰과-이름이-같은-외부-변수---완료)) | 원본 1건 (전체 3건 해소) |
| 6 | `Steeper` → `Stepper` 오타 ([10](#10-레이어명-정리---완료-138건)) | 64건 |
| 7 | `Mission`의 `Active` 순서 ([13](#13-active-옵션-순서-불일치---완료)) | 1건 |
| 8 | 기본 이름 Frame/Vector → 의미 부여 ([10](#10-레이어명-정리---완료-138건)) | **40건** |
| 9 | 소문자 레이어명 → 대문자 ([10](#10-레이어명-정리---완료-138건)) | **33건** |
| 10 | `Stepper_wrapper` → `Stepper Wrapper` ([10](#10-레이어명-정리---완료-138건)) | 1건 |

재스캔 결과 라운드 23 · 패딩 10 · Gap 10 · 외부 coral · `Steeper` 오타 · `Purlpe` 오타 · 기본 이름 Frame **모두 0건**입니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Property 1`/`Property`/`Step` 통일 11건 ([1](#1-property-1--property--step-속성명-11건)) | **의미 교차 — 확인 필요** | 중간 |
| 2 | Master `Progress Stepper` 이름 ([2](#2-마스터와-child-item-이름이-어긋남)) | 판단 필요 | 낮음 |
| 3 | Quiz `Gauge` 숨김 상태 ([7번 Master](#7-progress-stepper--quiz--920610071)) | 의도 확인 | 낮음 |
| 4 | `#545B69` · `#6F7581` · `#D8D8D8` 토큰화 ([5](#5-미바인딩-색상-39건)) | 판단 필요 | 중간 |
| 5 | 12 Bold / 12 Medium 토큰 ([7](#7-텍스트-스타일-미적용-66건)) | **Grid List와 함께 판단** | 중간 |
| 6 | ExtraBold 5건 ([8](#8-폰트-굵기-extrabold--semibold)) | **Card와 함께 판단** | 중간 |
| 7 | Express variant 매트릭스 ([11](#11-express-variant-매트릭스-불완전)) | 구조 재설계 | 높음 |

모두 결정이 필요한 항목입니다. 별도로 `gold_test4` **파일 전체 56건**([10-1](#10-1-남은-레이어명--gold_test4))과 빈 `Check` 프레임 6건([10-2](#10-2-새로-발견--빈-check-프레임-6건))이 남아 있습니다.

가장 영향이 큰 것은 **[점검 4의 파일 전체 외부 변수 140건](#4-로컬-토큰과-이름이-같은-외부-변수---완료)** 입니다. Progress Stepper에는 3건뿐이지만, 이전 문서들의 외부 토큰 집계가 이 변수들을 놓쳤으므로 [syrup-design-tokens.md](syrup-design-tokens.md) 쪽 수치 갱신이 필요합니다.


## 웹 동작 보완

### 웹 상단 시연 모션 (2026-11-18)
- 웹 시연용이며 서비스 전체의 공통 재생 규칙으로 확대하지 않아요. 기존 5초 일정 속도 시연을 대체해요.
- 초기 500ms 대기 후 1회까지 600ms, 5·10·15회까지 각각 700ms 이동해요. cubic ease-out(1−(1−t)^3)으로 감속하며 목표를 넘지 않아요.
- 1·5·10회에서 각각 500ms 정지해요. 횟수·보상 판정은 원 중심 34·116·198·280px 기준이에요.
- 15회 말풍선은 50금 원 중심(280px)에 멈춰요. 선 게이지만 180ms 동안 끝(314px)까지 채워요. 최종 대기는 도착부터 1200ms이며 이 180ms를 포함해요.
- 도착한 원은 320ms 동안 최대 1.08배로 한 번 강조해요. 주황 배경·흰 글자 전환은 도착과 동시에 시작해 50ms ease-out으로 완료해요. 이전 220ms·120ms 전환은 대체해요.
- 복귀는 900ms quart ease-out으로 빠르게 시작해 서서히 멈춰요. 말풍선·게이지가 함께 돌아오고 게이지 선단은 314→−12px로 이동해요. 둥근 끝과 음수 시작을 유지해 갑자기 나타나거나 사라지지 않아요.
- 일시정지·재생, 화면 밖·숨겨진 탭 정지를 지원해요. 모션 줄이기에서는 0회 정지 상태로 표시하고 원 확대도 하지 않아요.

