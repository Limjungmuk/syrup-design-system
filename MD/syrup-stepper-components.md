# Syrup Design System — Stepper 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Stepper` 페이지 → [Stepper 섹션 `8444:7660`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8444-7660) |
| 섹션 크기 | 1440 × 3164 |
| 컴포넌트 수 | **4개** (Master 1 · Child Item 3) |
| Variant 총수 | **42개** (3 · 4 · 14 · 21) |
| 기준일 | 2026-11-10 (가이드라인·Usage 갱신, 기존 점검 기록 유지) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **단계나 순서를 안내해 사용자가 할 일을 이해할 수 있도록 돕는 컴포넌트예요.**
> 프로세스 진행 흐름을 한눈에 보여주고, 다음 단계에서 할 일을 안내해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `StepperRow / NumberIcon / Thumbnail` | `8444:7749` |
| `StepperRow / NumberIcon` | `8444:7694` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Stepper — Master Component](#1-stepper--master-component)
3. [`StepperRow / NumberIcon / Thumbnail`](#2-primitive--stepperrow--numbericon--thumbnail)
4. [`StepperRow / NumberIcon`](#3-primitive--stepperrow--numbericon)
5. [`.primitive / Stepper / NumberIcon`](#4-primitive--stepper--numbericon)
6. [가이드라인](#가이드라인)
7. [Usage — 사용 예제](#usage--사용-예제)
8. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
9. [설계 규칙 요약](#설계-규칙-요약)
10. [점검 필요 사항](#점검-필요-사항)
11. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 하위 구성 3종으로 이뤄져요. 별도 섹션에 가이드라인 4개와 예제 A~F를 정리했어요. 기존 노드·인스턴스·토큰 집계는 2026-10-12 기준이며, 추가된 사용 화면과 문서 예제는 포함하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 850) | `Stepper` |
| y 1424 | Section Header | (상위 제목) |
| y 1564 | Section Header | (하위 제목) |
| y 1638 | (높이 952) | `.primitive / StepperRow / *` 2종 |
| y 2590 | Section Header | |
| y 2720 | (높이 380) | `.primitive / Stepper / NumberIcon` |
| 별도 섹션 | [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1467) | 가이드라인 4개 |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1468) | 예제 A~F 6개 |

Section Header가 **4개**인데 내용 프레임은 3개입니다. y 1424와 y 1564가 연달아 있어 **상위·하위 2단 제목** 구조로 보입니다.

### 3단 중첩 구조

```
Stepper                                    ← 목록 전체
└─ StepperRow / NumberIcon[ / Thumbnail ]   ← 한 줄
   └─ .primitive / Stepper / NumberIcon    ← 번호 원
```

| # | 이름 | 타입 | Variant 축 | 대표 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Stepper` | Set 3 | `Left` | 272 × 610 | **2** ([Card](syrup-card-components.md)) |
| 2 | `StepperRow / NumberIcon / Thumbnail` | Set 4 | `Title Bold` · `Last Item` + SLOT 6 · BOOLEAN 2 | 272 × 111 | **7** |
| 3 | `StepperRow / NumberIcon` | Set 14 | `Icon Size` · `2 Line` · `Description` · `Last Item` | 272 × 59 | **20** |
| 4 | `.primitive / Stepper / NumberIcon` | Set 21 | `Num` · `Icon Size` | 24 × 24 | **46** |

### 파일에서 가장 널리 쓰이는 primitive

| 컴포넌트 | 사용 페이지 |
| --- | --- |
| `.primitive / Stepper / NumberIcon` | Stepper 36 · [Card](syrup-card-components.md) 6 · [Bottom Sheet](syrup-bottom-sheet-components.md) 3 · [Header](syrup-header-components.md) 1 = **46** |
| `StepperRow / NumberIcon` | Stepper 14 · [Card](syrup-card-components.md) 6 = **20** |
| `.primitive / StepperRow / … / Thumbnail` | Stepper 4 · [Bottom Sheet](syrup-bottom-sheet-components.md) 3 = **7** |

지금까지 문서화한 페이지의 primitive 대부분이 자기 페이지 안에서만 쓰였던 것과 달리, **Stepper의 primitive 3종은 모두 다른 페이지에서 쓰입니다.** 개명·구조 변경 시 영향 범위가 넓습니다.

---

## 1. Stepper — Master Component

**Node** `8444:7665` · Component Set · **3 variants**

| Property | Type | Options |
| --- | --- | --- |
| `Left` | VARIANT | `Thumbnail` · `Number Icon Description` · `Number Icon` |

세로 오토레이아웃 · Padding 0 · Gap 0 — **줄 사이 간격은 각 Row의 아래 Padding이 담당**합니다.

| Variant | 크기 | 구성 |
| --- | --- | --- |
| `Thumbnail` | 272 × 610 | `… / Thumbnail` ×4 (101 · 166 · 166 · 177) |
| `Number Icon Description` | 272 × 393 | `… / NumberIcon` ×7 (59 ×6 + 39) |
| `Number Icon` | 272 × 260 | `… / NumberIcon` ×7 (40 ×6 + 20) |

마지막 행만 높이가 낮은 것은 **`Last Item=True`에서 연결선과 아래 여백이 빠지기** 때문입니다.

세 값 모두 표기가 어긋나 있었고 바로잡았습니다 ✅ → [점검 1](#1-left-값-표기-3건---완료)

---

## 2. `StepperRow / NumberIcon / Thumbnail`

**Node** `8444:7749` · Component Set · **4 variants** · 272 × 111

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Title Bold` | VARIANT | `False` | `False` · `True` |
| `Last Item` | VARIANT | `False` | `False` · `True` |
| `Thumbnail` | BOOLEAN | `true` | — |
| `Description` | BOOLEAN | `true` | — |
| **`title`** | SLOT | — | — |
| **`title2`** | SLOT | — | — |
| **`title3`** | SLOT | — | — |
| **`title4`** | SLOT | — | — |
| **`thumbnail`** | SLOT | — | — |
| **`Slot`** | SLOT | — | — |

**속성이 10개**로 이 파일에서 가장 많습니다. 그중 **6개가 SLOT**이고, 이름이 전부 문제입니다 → [점검 2](#2-속성-이름-6건)

가로 오토레이아웃 · Padding `0 / 0 / 8 / 0` (`Spacing/200`) · Gap 8 (`Spacing/200`)

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `Number` | Frame | 24 × 103 | Gap 4 |
| └ `.primitive / Stepper / NumberIcon` | Instance | 24 × 24 | `Color/Primary_Orange` |
| └ `Line` | Frame | **1.5** × 75 | `Color/Gray_800` — 단계 연결선 |
| `Supporting text` | Frame | 240 × 119 | Padding 하 12 · **Gap 14** |
| └ `thumbnail` | **SLOT** | 240 × 48 | `Color/Gray_White` · Gap 14 |
| &nbsp;&nbsp;└ `🟧syrup_img` | Frame | 240 × 48 | 이미지 자리 |
| └ `Text` | Frame | 240 × 45 | Padding 좌 4 · Gap 8 |
| &nbsp;&nbsp;└ `title4` | **SLOT** | 236 × 19 | Gap 4 |
| &nbsp;&nbsp;└ `Description` | Text | 236 × 18 | 13 Regular `b500_13_regular` `Color/Gray_500` |

`Line` 두께가 **1.5**로, 토큰이 없는 값입니다.

---

## 3. `StepperRow / NumberIcon`

**Node** `8444:7694` · Component Set · **14 variants**

| Property | Type | Options |
| --- | --- | --- |
| `Icon Size` | VARIANT | `S` · `M` · `L` |
| **`2 Line`** | VARIANT | `False` · `True` |
| `Description` | VARIANT | `False` · `True` |
| `Last Item` | VARIANT | `False` · `True` |

가로 오토레이아웃 · Padding `0 / 0 / 20 / 0` (`Spacing/500`) · Gap 10 (`Spacing/250`)

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `Icon` | Frame | 16 × 20 | Padding 상하 **3** |
| └ `.primitive / Stepper / NumberIcon` | Instance | 16 × 16 | `Color/Primary_Orange` |
| `Text` | Frame | 246 × 39 | Gap 2 |
| └ `Title` | Text | 246 × 19 | 15 Medium `t1300_15_medium` `Color/Gray_100` |
| └ `Description` | Text | 246 × 18 | 14 Regular `b400_14_regular` `Color/Gray_300` |

### Variant 매트릭스가 불완전합니다

`Icon Size`(3) × `2 Line`(2) × `Description`(2) × `Last Item`(2) = **24 중 14개**만 존재합니다.

| Icon Size | 2 Line | Description | Last Item | 존재 |
| --- | --- | --- | --- | --- |
| `S` | `True` | **`True`** | F / T | ✅ 2 |
| `S` | `False` | `False` | F / T | ✅ 2 |
| `S` | `True` | `False` | F / T | ✅ 2 |
| `M` | `False` | `False` | F / T | ✅ 2 |
| `M` | `True` | `False` | F / T | ✅ 2 |
| `L` | `False` | `False` | F / T | ✅ 2 |
| `L` | `True` | `False` | F / T | ✅ 2 |
| 그 외 10조합 | | | | **없음** |

**`Description=True`는 `Icon Size=S`에만 있습니다.** `M` · `L`에서 설명문을 쓰려 하면 variant가 없습니다 → [점검 5](#5-variant-매트릭스-불완전)

S·M·L 모두 Description=False에서 `2 Line`의 False·True 조합을 제공해요. Description=True 조합은 현재 S에만 있어요.

---

## 4. `.primitive / Stepper / NumberIcon`

**Node** `8444:7797` · Component Set · **21 variants** — `Num`(7) × `Icon Size`(3) **완전 매트릭스** ✅

| Property | Type | Options |
| --- | --- | --- |
| `Num` | VARIANT | `1` ~ `7` |
| `Icon Size` | VARIANT | `L` · `M` · `S` (드롭다운 표시 순서) — 기본값 **`S`** |

| Icon Size | 크기 | 숫자 스타일 |
| --- | --- | --- |
| `L` | **24 × 24** | 14 Bold `t1050_14_bold` ✅ |
| `M` | **20 × 20** | 10 Bold — 스타일 미적용 |
| `S` | **16 × 16** | 10 Bold — 스타일 미적용 |

세로 오토레이아웃 CENTER/CENTER · Padding 0 · Gap 0
배경 `Color/Primary_Orange` ✅ · 숫자 `Color/Gray_White` ✅
라운드 **`Corner radius/circle`** ✅ → [점검 3](#3-라운드-8333--39건---완료)

단계 번호를 담은 **주황 원** 하나입니다. 이 파일에서 **가장 많이 쓰이는 primitive(46건)**입니다.

`Icon Size` 드롭다운 순서는 `L` → `M` → `S`로 [3번](#3-primitive--stepperrow--numbericon)과 반대지만, **기본 Variant는 `S`로 맞췄어요** → [점검 6](#6-icon-size-옵션-순서가-반대---부분-완료)

---

## 가이드라인

### 1. 안내할 정보에 맞게 설명을 구성해요

순서대로 할 일을 짧게 안내할 때는 Number Icon을 사용해요. 단계별 조건이나 주의 사항을 덧붙일 때는 Number Icon Description으로 제목과 보조 설명을 나눠요.

| 안내 구성 | `Stepper / Left` | 사용 방식 |
| --- | --- | --- |
| 짧은 절차 | `Number Icon` | 번호와 안내 문구 |
| 조건·주의 사항 포함 | `Number Icon Description` | 단계 제목과 보조 설명 |
| UI 자료를 활용한 절차 | `Thumbnail` | 번호·UI 요소·문구를 조합 |

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1469)

### 2. 시각 자료가 필요한 단계에는 Thumbnail을 사용해요

버튼이나 배너의 위치를 설명해야 할 때는 Thumbnail 구성에 필요한 UI 요소를 함께 넣어요. 문구만으로 설명할 수 있으면 Thumbnail=False로 숨겨요. 추가 설명은 필요한 행에만 표시해요.

`Thumbnail` BOOLEAN은 표시 여부, `thumbnail` SLOT은 실제 내용을 넣는 자리예요. 이름의 대소문자와 속성 타입을 구분해요. 제목 강조는 `Title Bold=True`로 설정할 수 있어요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1553)

### 3. 주변 구성에 맞는 번호 크기를 사용해요

번호 아이콘은 S(16), M(20), L(24) 중 주변 문구와 배치 공간에 맞게 선택해요. 같은 안내 묶음에서는 번호 크기를 일관되게 사용하고, 문구가 길면 줄 수에 맞는 행 구성을 선택해요.

| 크기 | 번호 아이콘 | 이번 예제 |
| --- | --- | --- |
| S | 16 × 16 | 조건·보조 설명 |
| M | 20 × 20 | 카드 안의 간결한 안내 |
| L | 24 × 24 | 독립된 절차·사용 안내 |

예제의 사용처를 각 크기의 유일한 허용 위치로 해석하지 않아요. 현재 제공된 Row Variant 조합 안에서 문구와 공간에 맞게 선택해요.

[Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1666)

### 4. 번호 순서를 맞추고 마지막 행을 구분해요

번호는 안내 순서대로 연속해서 표시해요. 중간 행은 Last Item=False, 마지막 행은 Last Item=True로 사용해요. 행 사이 간격은 컴포넌트의 아래 여백을 활용하고, 추가 간격을 중복해서 넣지 않아요.

- 단계 수를 변경하면 마지막 행의 `Last Item`과 번호를 함께 확인해요.
- Thumbnail의 연결선과 행 끝 여백은 해당 Row 구성에 따라 처리해요.
- 단계 번호는 표시 순서예요. 완료 상태나 현재 진행 상태를 뜻하지 않아요.

[Figma 가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1753)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1468)에 안내 목적별 예제 6개를 구성했어요.

| 예제 | 구성 | 설명 |
| --- | --- | --- |
| [A. 짧은 참여 절차](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1794) | Number Icon, L(24), 2단계 | 간단한 참여 방법을 번호와 짧은 문구로 안내해요. 마지막 단계는 Last Item=True로 설정해요. |
| [B. 여러 줄의 사용 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1826) | Number Icon, L(24), 여러 줄 문구 | 설명이 길면 문구 줄 수에 맞는 행을 사용해요. 단계의 순서와 번호를 유지하고 내용이 잘리지 않도록 높이를 확보해요. |
| [C. 카드 안의 간결한 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1869) | Number Icon, M(20), 3단계 | 카드처럼 제한된 공간에서는 주변 문구에 맞는 번호 크기를 사용해요. 예제는 M(20)으로 세 단계를 안내해요. |
| [D. 조건과 보조 설명](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1905) | Number Icon Description, S(16) | 조건이나 주의 사항은 해당 단계의 보조 설명으로 나눠요. 예제는 S(16) 번호와 Number Icon Description 구성을 사용해요. |
| [E. UI 요소를 함께 보여주는 절차](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-1950) | Thumbnail=True, Title Bold=True | 단계 이해에 필요한 배너나 UI 요소를 Thumbnail 슬롯에 넣어요. 전체 화면 대신 설명에 필요한 부분만 사용해요. |
| [F. 이미지 없이 제목을 강조한 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11719-2007) | Thumbnail=False, Title Bold=True | Thumbnail=False로 UI 요소를 숨기고, Title Bold=True로 단계 제목을 강조할 수 있어요. 보조 설명은 필요한 행에만 표시해요. |

예제의 단계 수·문구·혜택은 소재이며, 실제 절차와 조건에 맞춰 구성해요.

## 예제 레이아웃과 AI 사용 기준

- 컴포넌트만 배치하는 경우 슬롯에 직접 넣고 불필요한 `화면` 레이어를 만들지 않아요. 슬롯은 좌측·상단 정렬, 추가 패딩 0으로 구성해요.
- 여러 행을 직접 배치할 때는 슬롯의 간격을 0으로 두고 Row 자체의 아래 여백을 활용해요. 원본 사용 사례에서 재정의된 행 간격을 일률적으로 같은 값으로 덮어쓰지 않아요.
- 제목이 길면 제공된 `2 Line` 구성을 선택하고 실제 문구에 맞는 높이를 확보해요. 문구를 잘라 샘플 높이에 강제로 맞추지 않아요.
- NumberIcon Row의 `Description`은 VARIANT, Thumbnail Row의 `Description`·`Thumbnail`은 BOOLEAN이에요. 같은 이름만 보고 타입을 혼동하지 않아요.
- 현재 NumberIcon Row에서 Description=True 조합은 S에만 있어요. 없는 M·L + Description=True 조합을 임의로 선택하거나 자동 대체에 맡기지 않아요.
- Thumbnail 자료는 절차 이해에 필요한 UI 요소만 사용해요. 전체 서비스 화면을 그대로 넣지 않아요. 이미지 없이 설명할 수 있으면 Thumbnail=False로 숨겨요.
- `title`·`title2`·`title3`·`title4`는 제목 슬롯 이름이에요. 단계 번호나 네 가지 필수 제목이라는 뜻으로 해석하지 않아요. 해당 Row에서 실제 노출되는 슬롯을 확인해 사용해요.
- 번호는 `Num`과 표시 텍스트가 일치하는지 확인하고 순서대로 배치해요. 같은 안내 묶음은 번호 크기를 통일해요.
- Stepper는 절차와 순서 안내예요. Section 1에 함께 등장하는 Progress Stepper의 현재 단계·진행 상태 표현을 Stepper의 규칙으로 혼합하지 않아요.
- 이번 문서화에서는 원본 컴포넌트의 명칭·Variant 구성·미바인딩 값을 변경하지 않았어요. 아래 과거 점검 제안을 확정된 사용 규칙으로 해석하지 않아요.

---

## 설계 규칙 요약

### 줄 간격을 Padding으로 처리

`Stepper`의 Gap은 0이고, **각 Row의 아래 Padding**이 줄 간격을 만듭니다.

| 컴포넌트 | 아래 Padding | 토큰 |
| --- | --- | --- |
| `… / Thumbnail` | 8 | `Spacing/200` ✅ |
| `… / NumberIcon` | 20 | `Spacing/500` ✅ |

`Last Item=True`에서 이 Padding과 연결선이 함께 빠집니다. 목록 끝에 여백이 남지 않는 방식입니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 배경 | `Color/Primary_Orange` · `Color/Gray_White` ✅ |
| 텍스트 색 | `Gray_100` · `Gray_300` · `Gray_500` · `Gray_White` ✅ |
| 연결선 색 | `Color/Gray_800` ✅ |
| 텍스트 스타일 | `t1300_15_medium` · `b400_14_regular` · `b500_13_regular` · `t1050_14_bold` ✅ |
| Padding | `Spacing/200` · `Spacing/500` ✅ — **3 ×6건 미바인딩** |
| Gap | `Spacing/200` · `Spacing/250` ✅ — **14 ×8건 미바인딩** |
| 라운드 | `Corner radius/circle` ✅ |
| 미바인딩 색상 | **0건** ✅ |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |
| 스타일 미적용 텍스트 | 14건 (전부 10 Bold) |

색은 전부 토큰에 묶여 있고, **수치 쪽에만 미바인딩이 남아 있습니다.**

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Section Header` 4 · `Title Bar` 1 | 5 |

컴포넌트 내부에서 다른 페이지를 참조하는 인스턴스가 **0건**입니다. 외부 라이브러리도 **0건**입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번에는 가이드라인·Usage와 사용 기준을 갱신했으며, 파일 전체의 인스턴스·토큰·스타일 건수는 재집계하지 않았어요. 슬롯의 현재 사용 맥락은 위 사용 기준을 우선해요.

### 1. `Left` 값 표기 3건 — ✅ 완료

| 변경 전 | 변경 후 | 문제였던 점 |
| --- | --- | --- |
| `ThumbNail` | **`Thumbnail`** | 중간 대문자 N |
| `Number icon` | **`Number Icon`** | `icon` 소문자 |
| `Number icon Desription` | **`Number Icon Description`** | **`Description` 오타** + `icon` 소문자 |

`Desription`은 **`c`가 빠진 오타**였습니다. 같은 컴포넌트 세트 안의 `Description` BOOLEAN 속성은 철자가 맞아 더 눈에 띄던 부분입니다.

`Stepper` 마스터의 인스턴스는 [Card](syrup-card-components.md) 2건이고, Figma가 값 개명을 자동으로 따라갑니다.

> **부수 효과** — 값을 개명하자 속성 옵션 순서가 **레이어 순서대로 다시 계산**됐습니다.
>
> | 시점 | 옵션 순서 |
> | --- | --- |
> | 개명 전 | `ThumbNail` · `Number icon` · `Number icon Desription` |
> | 개명 후 | `Thumbnail` · `Number Icon Description` · `Number Icon` |
>
> 레이어 순서가 `Thumbnail` → `Number Icon Description` → `Number Icon`이라 그대로 반영됐습니다. **이 동작이 [점검 6](#6-icon-size-옵션-순서가-반대---부분-완료)의 한계를 이해하는 단서**가 됩니다.

### 2. 속성 이름 6건

`StepperRow / NumberIcon / Thumbnail`의 속성 10개 중 6개가 문제입니다.

| 속성 | 타입 | 문제 |
| --- | --- | --- |
| **`thumbnail`** | SLOT | **`Thumbnail` BOOLEAN과 대소문자만 다름** |
| `title` | SLOT | 소문자 |
| `title2` | SLOT | 소문자 + 번호 |
| `title3` | SLOT | 소문자 + 번호 |
| `title4` | SLOT | 소문자 + 번호 |
| `Slot` | SLOT | **타입 이름을 그대로 쓴 이름** |

#### 가장 심각한 것은 `Thumbnail` / `thumbnail`

```
Thumbnail = BOOLEAN   ← 썸네일 표시 여부
thumbnail = SLOT      ← 썸네일 내용
```

**속성 패널에 `Thumbnail`과 `thumbnail`이 나란히 보입니다.** 대소문자만 다르고 역할이 달라, 어느 것이 무엇인지 구분할 단서가 이름에 없습니다.

[Search Field](syrup-search-field-components.md)의 `Property 1` → `State`, [Result](syrup-result-components.md)의 `Icon` 중복과 같은 성격이지만 **이쪽이 더 헷갈립니다.**

#### `title` ~ `title4`의 의미를 모르겠습니다

2026-10-12에는 title4만 확인됐지만, 현재 Section 1과 새 예제에는 Title Bold=True 구성의 `title`·`title2` 슬롯도 사용돼요. 슬롯 이름의 번호를 단계 번호로 해석하거나 미사용이라고 단정해 삭제하지 않아요. 필요한 제목 슬롯은 현재 행의 구성을 확인해 사용해요.

| 제안 | 조건 |
| --- | --- |
| 쓰이는 것만 남기고 `Title`로 개명 | `title`~`title3`이 실제로 미사용일 때 |
| 각각 역할을 드러내는 이름으로 | 용도가 따로 있을 때 |

**용도 확인이 필요해 손대지 않는 편이 안전합니다.**

### 3. 라운드 83.33 × 39건 — ✅ 완료

`.primitive / Stepper / NumberIcon`의 **21개 variant 전부**와 이를 쓰는 인스턴스 노드 18개에 `83.33332824707031`이 들어 있었습니다.

**원본 21건을 `Corner radius/circle`에 바인딩해 인스턴스 18건까지 39건 모두 해소**됐습니다. 재스캔 결과 남은 83.33은 **0건**입니다.

| 크기 | 건수 | Figma 적용값 |
| --- | --- | --- |
| 24 × 24 | 15 | 12 (반지름으로 제한) |
| 20 × 20 | 11 | 10 |
| 16 × 16 | 13 | 8 |

Figma는 라운드를 **가로·세로의 절반까지만** 적용하므로, 83.33은 세 크기 모두에서 **완전한 원**이 됩니다.

`Corner radius/circle`(100)로 바꿔도 **똑같이 완전한 원**입니다. 21개 원본만 바꾸면 인스턴스 18건이 따라옵니다.

> **모양이 바뀌지 않는 이유** — 21개 variant가 전부 정사각(24·20·16)이고, 83.33과 100 둘 다 각 크기의 절반을 넘습니다. 제한값이 같으므로 결과도 같습니다.
>
> [Progress Stepper](syrup-progress-stepper-components.md)의 `라운드 23 → circle` 4건과 같은 판단입니다. 반대로 [Result](syrup-result-components.md)에서는 **라운드를 0으로 지우는 변경**이 테두리를 사각형으로 만들어 되돌린 일이 있었습니다. **값을 올리는 것과 지우는 것은 다릅니다.**

83.33은 원본 아이콘을 비정수 배율로 축소할 때 생긴 값으로 보입니다.

### 4. 미바인딩 수치

| 값 | 건수 | 위치 | 대응 토큰 |
| --- | --- | --- | --- |
| ~~라운드 83.33~~ | ~~39~~ | `.primitive / Stepper / NumberIcon` | **바인딩 완료** ✅ |
| Gap 14 | 8 | `Supporting text` 4 · `thumbnail` 4 | **없음** (12 · 16 사이) |
| Padding 3 | 6 | `Icon` · `Frame 1` · `Frame 2` 상하 | **없음** |
| 선 두께 1.5 | 1 | `Line` (단계 연결선) | **없음** |

라운드 39건은 처리됐고, 나머지 세 값은 **대응 토큰이 없어** 판단이 필요합니다.

Gap 14는 `Spacing/300`(12)과 `Spacing/400`(16) 사이입니다. Padding 3은 아이콘(16)을 줄 높이(20)에 맞추는 보정값이라 토큰 대상이 아닙니다.

### 5. Variant 매트릭스 불완전

`StepperRow / NumberIcon`은 **24조합 중 14개**만 있습니다 → [3번 표](#3-primitive--stepperrow--numbericon)

| 빠진 조합 | 영향 |
| --- | --- |
| `Icon Size=M·L` + `Description=True` (4조합) | **`M`·`L`에서 설명문을 쓸 수 없음** |
| `Icon Size=M·L` + `2 Line=False, Description=True` 등 | — |
| `Icon Size=S` + `2 Line=False, Description=True` (2조합) | — |

Figma는 없는 조합을 선택하면 **임의의 다른 variant로 대체**하므로, 의도적 생략이라면 축을 나누는 편이 안전합니다.

다만 **variant 14개를 재구성하는 작업**이고 인스턴스가 20건이라 비용이 작지 않습니다. `Description`을 `Icon Size=S` 전용으로 둘 의도였는지 먼저 확인이 필요합니다.

### 6. `Icon Size` 옵션 순서가 반대 — ⚠️ 부분 완료

| 컴포넌트 | 옵션 순서 | 기본 variant |
| --- | --- | --- |
| `StepperRow / NumberIcon` | `S` → `M` → `L` | `Icon Size=S` |
| `.primitive / Stepper / NumberIcon` | **`L` → `M` → `S`** (그대로) | ~~`Icon Size=L`~~ → **`Icon Size=S`** ✅ |

**실질적 문제였던 기본값은 맞췄습니다.** `.primitive / Stepper / NumberIcon`의 레이어 순서를 `S`(7개) → `M`(7개) → `L`(7개)로 바꿔, 인스턴스를 새로 놓을 때 안팎이 모두 `S`로 시작합니다.

#### 드롭다운 표시 순서는 바꾸지 못했습니다

레이어를 재정렬해도 속성 패널의 옵션 목록은 **`L` · `M` · `S` 그대로**입니다.

| 조치 | 옵션 순서 재계산 |
| --- | --- |
| 값 **개명** ([점검 1](#1-left-값-표기-3건---완료)) | **됨** ✅ |
| 레이어 **재정렬** (이번 건) | **안 됨** |

Figma는 VARIANT 속성의 옵션 순서를 자체적으로 들고 있고, **값을 개명할 때만 레이어 순서 기준으로 다시 만듭니다.** 플러그인 API에 옵션 순서를 직접 바꾸는 수단은 없습니다.

| 선택지 | 내용 | 위험 |
| --- | --- | --- |
| A | 현행 유지 — 기본값은 맞았고 표시 순서만 다름 | 없음 |
| B | 값을 `S`→`Small`→`S` 식으로 왕복 개명해 재계산 유도 | **인스턴스 46건이 두 번 따라가야 함** |
| C | Figma UI에서 직접 variant 순서 조정 | 수작업 |

B는 46개 인스턴스의 variant 선택이 두 번 연쇄 변경되는 방식이라 **권하지 않습니다.** 표시 순서만 남은 문제라 A가 무난합니다.

[Progress Stepper](syrup-progress-stepper-components.md)의 `Mission` `Active` 순서 건은 variant가 2개뿐이라 재정렬만으로 해결됐지만, **이번처럼 옵션 목록 자체를 바꿔야 하는 경우는 한계가 있습니다.**

### 7. `2 Line` 속성명이 숫자로 시작

| 현재 | 제안 |
| --- | --- |
| `2 Line` | `Two Line` 또는 `Multiline` |

Figma가 막지는 않지만, **숫자로 시작하는 속성명은 이 파일에서 유일**합니다. 코드로 옮길 때 식별자로 쓸 수 없는 형태이기도 합니다.

우선순위는 낮습니다.

### 8. 네임스페이스가 두 갈래

| 컴포넌트 | 네임스페이스 |
| --- | --- |
| `.primitive / **StepperRow** / NumberIcon / Thumbnail` | `StepperRow` |
| `.primitive / **StepperRow** / NumberIcon` | `StepperRow` |
| `.primitive / **Stepper** / NumberIcon` | `Stepper` |

같은 페이지의 primitive인데 **`StepperRow`와 `Stepper`로 갈립니다.** 또 `StepperRow` · `NumberIcon` 모두 **붙여쓰기**라, 파일 관례(띄어쓰기)와 다릅니다.

| 현재 | 제안 |
| --- | --- |
| `StepperRow / NumberIcon / Thumbnail` | `.primitive / Stepper / Row / Thumbnail` |
| `StepperRow / NumberIcon` | `.primitive / Stepper / Row` |
| `.primitive / Stepper / NumberIcon` | `.primitive / Stepper / Number` |

**인스턴스가 73건**([구성 한눈에 보기](#파일에서-가장-널리-쓰이는-primitive))이고 [Card](syrup-card-components.md) · [Bottom Sheet](syrup-bottom-sheet-components.md) · [Header](syrup-header-components.md)에 걸쳐 있어, 개명 시 **인스턴스 이름 동반 변경 여부 확인**이 필요합니다.

[Search Field](syrup-search-field-components.md)의 `.primitive / Result / Search / Search` 개명은 인스턴스 3건이 자동으로 따라왔습니다. 같은 방식이 적용될 것으로 보이나 **건수가 24배**입니다.

### 9. 레이어명 정리 — ✅ 부분 완료 (6건)

| 변경 전 | 변경 후 | 위치 | 건수 | 근거 |
| --- | --- | --- | --- | --- |
| `num` | **`Number`** | `… / Thumbnail` | 4 | 소문자 — 번호 원 + 연결선 묶음 |
| `Frame 1` | **`Icon`** | `… / NumberIcon` | 1 | 기본 이름 — 다른 variant의 `Icon`과 동일 역할 |
| `Frame 2` | **`Icon`** | `… / NumberIcon` | 1 | 같음 |

`Frame 1` · `Frame 2`는 **안에 `.primitive / Stepper / NumberIcon` 인스턴스를 담고 Padding 상하 3을 가진** 구조라, 다른 variant의 `Icon` 프레임과 역할이 같은 것을 확인하고 이름을 맞췄습니다.

정리 후 **기본 이름 0건 · 정리 대상 소문자명 0건**입니다.

#### 남은 2건 — SLOT 속성과 묶여 있음

| 레이어 | 연결된 속성 |
| --- | --- |
| `thumbnail` | `thumbnail` SLOT |
| `title4` | `title4` SLOT |

레이어명을 바꾸면 속성명과 어긋나므로 **[점검 2](#2-속성-이름-6건)와 함께 판단해야 합니다.** 손대지 않았습니다.

### 10. 스타일 미적용 10 Bold 14건

| 위치 | 건수 |
| --- | --- |
| `.primitive / Stepper / NumberIcon` `Icon Size=M` · `S` | **14** |

`Icon Size=L`(24px)만 `t1050_14_bold`가 적용돼 있고, `M`(20px) · `S`(16px)의 숫자는 **10 Bold로 스타일 없이** 들어가 있습니다.

**10~11px은 토큰화하지 않는다는 기존 방침**에 따라 제외합니다. [Progress Stepper](syrup-progress-stepper-components.md) 48건 · [Product Grid](syrup-product-grid-components.md) 등과 같은 처리입니다.

---

## 정리 우선순위

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **28건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | `Desription` → `Description` ([1](#1-left-값-표기-3건---완료)) | 1건 |
| 2 | 라운드 83.33 → `Corner radius/circle` ([3](#3-라운드-8333--39건---완료)) | 원본 **21건** (전체 39건 해소) |
| 3 | `ThumbNail` · `Number icon` 표기 ([1](#1-left-값-표기-3건---완료)) | 2건 |
| 4 | `Icon Size` 기본 variant → `S` ([6](#6-icon-size-옵션-순서가-반대---부분-완료)) | **부분** — 드롭다운 표시 순서는 못 바꿈 |
| 5 | 레이어명 `num` · `Frame 1` · `Frame 2` ([9](#9-레이어명-정리---부분-완료-6건)) | **6건** |

정리 후 **라운드 83.33 0건 · 기본 이름 0건 · 정리 대상 소문자명 0건**입니다.

> **알아둘 점 — VARIANT 옵션 순서는 개명으로만 다시 계산됩니다.**
>
> `Left` 값을 개명했더니 옵션 순서가 레이어 순서대로 재계산됐지만, `Icon Size`는 레이어를 재정렬해도 `L` · `M` · `S` 그대로였습니다. 플러그인 API에 옵션 순서를 직접 바꾸는 수단이 없습니다. 자세한 내용은 [점검 6](#6-icon-size-옵션-순서가-반대---부분-완료)에 적었습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `thumbnail` SLOT → `Thumbnail` 중복 해소 ([2](#2-속성-이름-6건)) | **판단 필요** | 낮음 |
| 2 | `title`~`title4` 용도 확인 ([2](#2-속성-이름-6건)) | **확인 필요** | — |
| 3 | `2 Line` → `Two Line` ([7](#7-2-line-속성명이-숫자로-시작)) | 판단 필요 | 낮음 |
| 4 | `Icon Size` 드롭다운 표시 순서 ([6](#6-icon-size-옵션-순서가-반대---부분-완료)) | 현행 유지 권장 | — |
| 5 | 네임스페이스 통일 ([8](#8-네임스페이스가-두-갈래)) | **인스턴스 73건 영향** | 중간 |
| 6 | Gap 14 · Padding 3 · 선 두께 1.5 ([4](#4-미바인딩-수치)) | 판단 필요 | 중간 |
| 7 | Variant 매트릭스 ([5](#5-variant-매트릭스-불완전)) | 구조 재설계 · 인스턴스 20건 | 높음 |

가장 헷갈리는 것은 **[점검 2의 `Thumbnail` / `thumbnail`](#2-속성-이름-6건)** 입니다. 대소문자만 다른 두 속성이 패널에 나란히 보입니다.

주의할 점은 **[점검 8의 네임스페이스](#8-네임스페이스가-두-갈래)** 입니다. 정리하면 좋지만 인스턴스가 73건에 [Card](syrup-card-components.md) · [Bottom Sheet](syrup-bottom-sheet-components.md) · [Header](syrup-header-components.md)까지 걸쳐 있어, **이 페이지에서 영향 범위가 가장 넓은 변경**입니다.
