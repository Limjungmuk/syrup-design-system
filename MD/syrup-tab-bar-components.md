# Syrup Design System — Tab Bar 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Tab Bar` 페이지 → [Tab Bar 섹션 `8444:9297`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8444-9297) |
| 섹션 크기 | 1440 × 2128 |
| 컴포넌트 수 | **3개** (Master 1 · Child Item 2) |
| Variant 총수 | **16개** (2 · 4 · 10) |
| 기준일 | 2026-11-10 (가이드라인 3개·Usage A~C 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **앱 하단에 고정되어 주요 탭 간 이동을 지원하는 내비게이션 영역이에요.**
> 모으기·지금·쇼핑적립·MY·전체 등 주요 화면 간 전환에 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Tab Bar — Master Component](#1-tab-bar--master-component)
3. [`.primitive / Tab Bar / Tab Item`](#2-primitive--tab-bar--tab-item)
4. [`.primitive / Tab Bar / Icons`](#3-primitive--tab-bar--icons)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)
10. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 하위 구성 2종을 유지하고, 별도 섹션에 가이드라인 3개와 Usage A~C를 정리했어요.

기존 마스터 섹션 집계는 높이 2,128 · 노드 **170개** · 텍스트 **26개**예요. 노드·인스턴스·파일 전체 수치는 2026-10-12 점검 기록이며, 이후 추가된 사용 화면과 문서 예제는 포함하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 402) | `Tab Bar` 1종 |
| y 976 · y 1116 | Section Header ×2 | (상위 · 하위 제목) |
| y 1190 | (높이 376) | `.primitive / Tab Bar / Tab Item` |
| y 1566 | Section Header | |
| y 1696 | (높이 368) | `.primitive / Tab Bar / Icons` |

### 3단 구조

```
Tab Bar  (Home Indicator = True | False)
└─ .primitive / Tab Bar / Tab Item  ×5   (Selected · Red Dot · Show Tooltip)
   └─ .primitive / Tab Bar / Icons        (Resource 5종 × State)
```

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Tab Bar` | Set 2 | `Home Indicator` | 360 × 84 / 360 × 58 | **0** |
| 2 | `.primitive / Tab Bar / Tab Item` | Set 4 | `Selected` · `Red Dot` + `Show Tooltip` | 48 × 58 | 10 |
| 3 | `.primitive / Tab Bar / Icons` | Set 10 | `Resource` · `State` | 24 × 24 | 14 |

속성명 세 개가 어긋나 있었고 모두 바로잡았습니다 ✅ → [점검 1](#1-속성명-3건---완료)

---

## 1. Tab Bar — Master Component

**Node** `8444:9302` · Component Set · **2 variants**

| Property | Type | Options |
| --- | --- | --- |
| `Home Indicator` | VARIANT | `True` · `False` |

홈 인디케이터 영역을 포함할지 고르는 속성이에요. 기기명만으로 고르지 않고 배치할 화면의 하단 환경에 맞춰 사용해요.

| Home Indicator | 크기 | 구조 |
| --- | --- | --- |
| `True` | **360 × 84** | `Tab Bar` 프레임(58) + `.utill / iOS Home Button`(26) |
| `False` | **360 × 58** | Tab Item 5개 **직접** |

공통 — 배경 `Color/Gray_White` ✅ · **DROP_SHADOW** · Padding 좌우 16 (`Spacing/400`) · Gap 24 (`Spacing/600`)

### 두 variant의 구조가 다릅니다

| Home Indicator | 최상위 자식 | 정렬 |
| --- | --- | --- |
| `True` | `Tab Bar` 프레임 **한 겹 더** → 그 안에 Tab Item 5개 | **SPACE_BETWEEN** |
| `False` | Tab Item 5개가 **바로** | **MIN** |

래퍼 유무와 정렬이 모두 다릅니다. Tab Item 폭도 **65.6 vs 46.4**로 벌어집니다 → [점검 2](#2-home-indicator-variant의-구조-불일치)

### 숨겨진 툴팁

두 variant 모두 `Tooltip`(이전 `Frame 3468129`) 42 × 20이 **숨김**으로 들어 있습니다.

| 항목 | 값 |
| --- | --- |
| 배경 | `Color/Secondary_Red` ✅ · 라운드 `circle` ✅ |
| 문구 | 「할시간!」 11 Regular **스타일 미적용** · `Color/Gray_White` |
| Padding | `4 / 4 / 5 / 5` — 상하좌우 비대칭 |

상위 Tab Bar의 이 Tooltip에는 표시를 제어하는 `Show Tooltip` 속성이 없어요. 아래 Tab Item의 `Show Tooltip`과 별개의 요소예요. 실제 사용 화면에서는 숨겨져 있어 이번 가이드라인·Usage에는 포함하지 않았어요.

---

## 2. `.primitive / Tab Bar / Tab Item`

**Node** `8444:9330` · Component Set · **4 variants** · 48 × 58

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Selected` | VARIANT | `True` | `True` · `False` |
| `Red Dot` | VARIANT | `False` | `False` · `True` |
| `Show Tooltip` | BOOLEAN | `false` | — |

세로 오토레이아웃 · Padding `6 / 0 / 7 / 0` (상 `Spacing/150` ✅ · **하 7 미바인딩**) · Gap 0

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `.primitive / Tab Bar / Icons` | Instance | 28 × 28 | 탭 아이콘 |
| `Label` | Text | 28 × 17 | 12 Regular `c100_12_regular` ✅ |
| `Red Dot` | Ellipse | 6 × 6 | `Color/Primary_Orange` ✅ · `Red Dot` 속성으로 토글 |
| `Tooltip` | Frame | 75 × 26 | **숨김** · `Show Tooltip`으로 토글 |
| └ `Bubble` | Frame | 75 × 22 | `Color/Primary_Orange` ✅ · 라운드 `circle` ✅ · Padding `2.5 / 10 / 3.5 / 10` |
| &nbsp;&nbsp;└ `Text` | Text | 55 × 16 | 「찜하고 금 받기」 10 Medium **스타일 미적용** |
| &nbsp;&nbsp;└ `Vector 34` | Vector | 3 × 6 | **숨김** |
| └ `Tail` ▸ `Triangle` | Vector | 9 × 7 | 말풍선 꼬리 `Color/Primary_Orange` ✅ |

| Selected | 라벨 색 |
| --- | --- |
| `True` | `Color/Gray_100` ✅ |
| `False` | `Color/Gray_400` ✅ |

`Selected=True, Red Dot=True`만 아이콘 인스턴스의 레이어명이 달랐고 맞추었습니다 ✅ → [점검 3](#3-아이콘-인스턴스-레이어명-1건---완료)

---

## 3. `.primitive / Tab Bar / Icons`

**Node** `8444:9374` · Component Set · **10 variants** = `Resource`(5) × `State`(2) **완전 매트릭스** ✅ · 모두 24 × 24

| Property | Type | Options (표시 순서) |
| --- | --- | --- |
| `Resource` | VARIANT | **`05all` · `01pig` · `04wallet` · `02alarm` · `03shopping`** |
| `State` | VARIANT | `True` · `False` |

| Resource | `State=True` | `State=False` | 자식 구성 |
| --- | --- | --- | --- |
| `01pig` | 24.01 × 21.84 | 24.01 × 21.84 | `Vector` |
| `02alarm` | 21 × 21.19 | 21 × 21.19 | `Union` ▸ `Vector` ×3 |
| `03shopping` | 19.19 × 21.59 | 19.19 × 21.59 | `Vector` |
| **`04wallet`** | **20 × 20** | **20.38 × 20** | `Vector` |
| `05all` | 20 × 20 | 20 × 20 | `Union` ▸ `01` · `02` · `03` · `04` (9 × 9) |

| State | 아이콘 색 |
| --- | --- |
| `True` | `Color/Gray_100` ✅ |
| `False` | `Color/Gray_500` ✅ |

`04wallet`만 두 상태의 **폭이 0.38 다릅니다** → [점검 5](#5-04wallet-폭-불일치---완료)

`Resource` 옵션의 **표시 순서가 번호와 맞지 않습니다** → [점검 4](#4-resource-옵션-표시-순서)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-656) · 2026-11-10 기준

### 1. 주요 메뉴와 현재 위치를 일관되게 보여줘요

모으기·지금·쇼핑적립·MY·전체의 순서와 아이콘을 유지해 앱의 주요 메뉴를 탐색해요.
현재 화면에 해당하는 항목만 Selected=True로 표시하고, 나머지는 Selected=False로 구분해요.

- 비교: 모으기 선택 / MY 선택
- [Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-658)

### 2. Red Dot은 선택 여부와 별도로 표시해요

Red Dot은 각 탭의 서비스 조건에 따라 표시해요. 선택 상태를 나타내는 Selected와 별도로 관리해요.
탭을 선택했다는 이유만으로 Dot을 켜거나 끄지 않고, 해당 안내의 표시 조건을 따라요.

- 비교: 지금 선택 · Red Dot=False / 지금 선택 · Red Dot=True
- [Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-887)

### 3. 하단 환경에 맞게 홈 인디케이터를 사용해요

홈 인디케이터 영역이 필요하면 Home Indicator=True, 필요하지 않으면 False를 사용해요.
Tab Bar는 화면 하단에 배치하고, 하단 광고를 함께 사용하는 경우에는 광고를 Tab Bar 위에 두어요.

- 비교: 홈 인디케이터 없음 · False / 홈 인디케이터 포함 · True
- [Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-1151)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-657) · A~C 순서

| 예제 | 설명 | 구성 | Figma |
| --- | --- | --- | --- |
| A. 기본 메뉴 탐색 | 화면 하단에서 앱의 주요 메뉴를 탐색해요. 현재 화면에 해당하는 항목을 선택 상태로 보여줘요. | 모으기 선택, Home Indicator=False인 Tab Bar 1개 | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-1359) |
| B. 선택 상태와 Red Dot | 지금과 쇼핑적립처럼 안내가 있는 탭에 Red Dot을 표시해요. Dot이 있는 항목도 선택·미선택 상태를 각각 표현할 수 있어요. | 모으기 선택 + 지금·쇼핑적립 Dot / 지금 선택 + 지금 Dot인 Tab Bar 2개 비교 | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-1447) |
| C. 하단 광고와 함께 배치 | 하단 광고는 Tab Bar 위에 배치해요. 광고와 메뉴 영역을 구분하고 Tab Bar의 항목을 가리지 않도록 해요. | 높이 80의 광고 + 높이 58의 Tab Bar를 세로로 배치 | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11771-1637) |

B의 두 구성은 Red Dot과 선택 상태의 독립적인 조합을 보여주는 예제예요. 탭 선택 전후의 Dot 해제 순서나 서비스 동작을 정의하는 연속 화면은 아니에요. C의 광고 소재는 두 영역의 위치 관계를 설명하기 위한 보조 요소예요.

---

## 예제 레이아웃과 AI 사용 기준

### 문서 배치

| 항목 | 현재 구성 |
| --- | --- |
| Guidelines 섹션 | **960 × 1032**, 가이드라인 3개 |
| Usage 섹션 | **1360 × 454**, 예제 A~C |
| 섹션 스타일 | 원본 Tab Bar 섹션과 동일한 흰 배경, 모서리 **24**, 테두리 없음. 색상·모서리 토큰 연결 유지 |
| Slot | 폭 **360**, 패딩 **0**, 좌측·상단 정렬, 내용에 맞춘 높이 |
| 기본 Tab Bar | **360 × 58**, Home Indicator=False |
| 홈 인디케이터 포함 Tab Bar | **360 × 84**, Home Indicator=True |
| 예제 B | Tab Bar 2개를 간격 **16** · `Spacing/400`으로 비교 배치 |
| 예제 C | 광고 **360 × 80** 위, Tab Bar **360 × 58** 아래, 두 요소 사이 간격 **0** · `Spacing/0` |
| 설명과 Slot 사이 | **50**, 예제끼리 시각 요소의 시작 높이를 맞춤 |

예제 B의 두 Tab Bar 사이 16은 문서 비교를 위한 간격이에요. 실제 화면에 Tab Bar 두 개를 동시에 배치하라는 규칙이 아니에요. 360 폭과 섹션 크기 역시 현재 예제 배치 수치이며 모든 화면에 고정 적용하는 값은 아니에요.

### 컴포넌트 선택과 상태

- 앱 주요 화면을 오가는 Tab Bar와 같은 화면의 콘텐츠를 구분하는 [Tab](syrup-tab-components.md)을 구분해 사용해요.
- 주요 메뉴의 순서는 모으기 → 지금 → 쇼핑적립 → MY → 전체예요. 기존 Tab Bar 인스턴스를 사용하고 항목의 이름·순서·아이콘을 임의로 바꾸지 않아요.
- 상위 Tab Bar의 VARIANT 속성은 `Home Indicator`예요. `Selected`와 `Red Dot`은 하위 Tab Item의 VARIANT 속성이며, 상위에 `SelectedIndex` 같은 속성이 있다고 가정하지 않아요.
- 아이콘의 `Resource`는 모으기=`01pig`, 지금=`02alarm`, 쇼핑적립=`03shopping`, MY=`04wallet`, 전체=`05all`이에요. 드롭다운 표시 순서를 화면 메뉴 순서로 해석하지 않아요.
- 선택 항목은 한 개로 표시해요. Tab Item의 `Selected`와 중첩 아이콘의 `State`가 서로 맞는지 확인하고, 색상만 임의로 덮어써서 선택 상태를 만들지 않아요.
- `Red Dot`은 선택 여부와 별개예요. 확인해야 할 안내의 구체적인 의미·표시·해제 시점은 탭별 서비스 조건을 따라요. 다른 컴포넌트의 Dot 사용 조건을 그대로 가져오지 않아요.
- 홈 인디케이터가 필요한 경우 기존 True variant의 하단 영역을 사용해요. 별도의 홈 인디케이터를 중복 추가하거나 False variant의 높이만 늘려 표현하지 않아요. variant 전환 뒤 항목 상태가 유지됐는지도 확인해요.
- Tab Bar는 화면 하단에 배치하고 하단 광고는 그 위에 배치해요. 문서 예제에서는 위치 관계에 필요한 광고만 포함하고 전체 제품 화면은 복제하지 않았어요.
- `Show Tooltip`은 Tab Item의 BOOLEAN 속성(`Show Tooltip#8444:0`)이에요. 현재 Section 1에서는 false로 사용되며 이번 가이드라인·Usage에는 툴팁 사용 사례를 추가하지 않았어요. 숨겨진 문구를 근거로 모든 항목에 툴팁을 켜지 않아요.
- Slot에는 Tab Bar 또는 필요한 광고 인스턴스를 직접 배치해요. 불필요한 ‘화면’ 프레임과 Slot 패딩을 추가하지 않아요.
- Section 1의 아노테이션은 점검 시점부터 **0개**였고, 추가 작업 후에도 0개를 확인했어요.
- 현재 시럽 토큰과 기존 컴포넌트 스타일을 유지해요. 아래의 기존 구조·미바인딩 수치 개선 제안은 과거 점검 기록이며, 이번 사용 가이드 추가와 별개의 사항이에요.

---

## 설계 규칙 요약

### 선택 표현

| 요소 | `Selected=True` | `Selected=False` |
| --- | --- | --- |
| 아이콘 | `Color/Gray_100` | `Color/Gray_500` |
| 라벨 | `Color/Gray_100` | `Color/Gray_400` |

**색만으로 구분합니다.** [Tab](syrup-tab-components.md)이 세 타입 모두 글자 굵기를 함께 바꾼 것과 다릅니다. 탭바는 라벨이 12px로 작아 굵기 변화를 쓰기 어려운 사정이 있어 보입니다.

아이콘과 라벨의 비선택 색이 **`Gray_500` / `Gray_400`으로 다른 점**은 확인이 필요합니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 배경 · 아이콘 · 라벨 색 | `Gray_White` · `Gray_100` · `Gray_400` · `Gray_500` · `Primary_Orange` · `Secondary_Red` ✅ |
| 라운드 | `Corner radius/circle` ✅ — **2 ×8건 미바인딩** |
| Padding | `Spacing/150` · `250` · `400` ✅ — **7 ×14 · 5 ×4 · 2.5/3.5 ×4 미바인딩** |
| Gap | `Spacing/100` · `600` ✅ |
| 텍스트 스타일 | `c100_12_regular` ✅ — **미적용 6건** |
| 미바인딩 색상 | **0건** ✅ |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

색은 전부 토큰에 묶여 있고 **수치 쪽에만 미바인딩이 남아 있습니다.**

### 타 페이지·외부 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Section Header` 4 · `Title Bar` 1 | 5 |
| **외부 라이브러리** | **`.utill / iOS Home Button`** | **1** |

외부 인스턴스 1건의 이름에 **`utill` 오타**가 있습니다 → [점검 8](#8-utill-오타--외부-라이브러리)

---

## 점검 필요 사항

> 아래는 2026-10-12에 작성한 구조·토큰·네이밍 점검 기록이에요. 2026-11-10에는 사용 가이드라인·Usage를 추가했어요. 기존 집계와 미바인딩 수치, 개선 제안은 현재 페이지 전체에 대한 새 점검 결과나 확정된 사용 규칙이 아니에요.

### 1. 속성명 3건 — ✅ 완료

| 컴포넌트 | 변경 전 | 변경 후 | 문제였던 점 |
| --- | --- | --- | --- |
| `Tab Bar` | **`아이폰`** | **`Home Indicator`** | 한글 속성명 |
| `.primitive / … / Icons` | `state` | **`State`** | 소문자 |
| `.primitive / … / Tab Item` | `Red dot` | **`Red Dot`** | 두 번째 단어 소문자 |

#### `아이폰` → `Home Indicator`로 정한 이유

지금까지 문서화한 39개 페이지 중 **속성명에 한글을 쓴 것은 이 하나뿐**이었습니다. 값은 `True`/`False` 영문이라 한 속성 안에 한글·영문이 섞여 있었습니다.

의미도 "아이폰이냐"가 아니라 **"홈 인디케이터 영역을 붙이느냐"**입니다. `True`일 때 붙는 것이 `.utill / iOS Home Button` 26px 바이고, 안드로이드에도 같은 역할의 제스처 바가 있습니다.

| 후보 | 판단 |
| --- | --- |
| **`Home Indicator`** | **채택** — 붙는 요소를 정확히 가리킴 |
| `Safe Area` | 노치·상단까지 포함하는 더 넓은 개념이라 과함 |
| `아이폰` | 기기명이라 안드로이드에서 쓸 때 어긋남 |

variant 이름도 `Home Indicator=True` · `Home Indicator=False`로 따라 바뀌었습니다.

`Resource` 값(`01pig` 등)은 **에셋 파일명을 따른 것**으로 보여 손대지 않았습니다 → [점검 4](#4-resource-옵션-표시-순서)

### 2. `Home Indicator` variant의 구조 불일치

| Home Indicator | 최상위 자식 | 정렬 | Tab Item 폭 |
| --- | --- | --- | --- |
| `True` | **`Tab Bar` 프레임** → Tab Item 5개 | **SPACE_BETWEEN** | 65.6 |
| `False` | Tab Item 5개 **직접** | **MIN** | 46.4 |

세 가지가 동시에 다릅니다.

#### 왜 문제인가

| 영향 | 설명 |
| --- | --- |
| 오버라이드 단절 | `Home Indicator`를 바꾸면 Tab Item 5개의 아이콘·라벨 수정이 유지되지 않음 |
| 정렬 차이 | `False`는 `MIN`(왼쪽 정렬) — 탭바는 보통 균등 배분 |
| 폭 차이 | 같은 360 폭인데 Tab Item이 65.6 / 46.4로 다름 |

**`False`의 `MIN` 정렬이 특히 의심스럽습니다.** 5개 탭을 왼쪽부터 붙여 놓고 Gap 24로 띄우는 방식이라, `True`의 SPACE_BETWEEN과 결과가 다릅니다.

| 선택지 | 내용 |
| --- | --- |
| A | `False`도 래퍼 프레임을 두고 SPACE_BETWEEN으로 통일 |
| B | `True`의 래퍼를 없애고 양쪽 평평하게 |
| C | 현행 유지 |

모양이 바뀔 수 있어 디자인 확인이 필요해요. 과거 인스턴스 0건을 현재 변경 영향이 없다는 근거로 사용하지 않아요.

### 3. 아이콘 인스턴스 레이어명 1건 — ✅ 완료

`.primitive / Tab Bar / Tab Item` 네 variant의 아이콘 자리입니다.

| Variant | 변경 전 레이어명 | 참조 원본 |
| --- | --- | --- |
| `Selected=True, Red Dot=False` | `.primitive / Tab Bar / Icons` | `8444:9374` |
| `Selected=False, Red Dot=False` | `.primitive / Tab Bar / Icons` | `8444:9374` |
| **`Selected=True, Red Dot=True`** | ~~`.primitive / Tab Bar / Tab Item / Tab Bar Icons`~~ → **통일** ✅ | `8444:9374` |
| `Selected=False, Red Dot=True` | `.primitive / Tab Bar / Icons` | `8444:9374` |

**참조하는 원본은 네 개 모두 같았습니다.** 인스턴스의 **레이어명만** 하나 달랐습니다.

Figma는 variant를 바꿀 때 **같은 이름·같은 위치의 레이어끼리 오버라이드를 이어받으므로**, 이름이 다른 하나만 연결이 끊겼습니다. `Red Dot`을 토글하면 아이콘 선택(`Resource`)이 초기화될 수 있었습니다.

**이름을 맞춰 해소했고 모양은 바뀌지 않았습니다.**

[Tab](syrup-tab-components.md)의 Rounded 사례와 닮았지만, 그쪽은 **타입 자체가 달랐고**(인스턴스 vs 프레임) 이쪽은 **이름만** 달랐습니다.

### 4. `Resource` 옵션 표시 순서

| 구분 | 순서 |
| --- | --- |
| 레이어 순서 | `01pig` → `02alarm` → `03shopping` → `04wallet` → `05all` ✅ |
| **옵션 표시 순서** | **`05all` → `01pig` → `04wallet` → `02alarm` → `03shopping`** |

값에 번호를 붙여 순서를 정했는데 **드롭다운에서는 뒤섞여 보입니다.**

[Stepper](syrup-stepper-components.md)에서 확인한 대로 **레이어 재정렬로는 표시 순서가 바뀌지 않고, 값을 개명해야만 다시 계산**됩니다.

[점검 1](#1-속성명-3건---완료)에서 `Resource` 값 개명을 함께 진행한다면 **순서도 자연히 정리**됩니다.

### 5. `04wallet` 폭 불일치 — ✅ 완료

| State | 수정 전 | 수정 후 |
| --- | --- | --- |
| `True` | 20 × 20 | 20 × 20 |
| `False` | **20.38 × 20** | **20 × 20** ✅ |

다른 네 Resource는 두 상태의 크기가 같은데 `04wallet`만 0.38 차이가 났습니다.

24 × 24 틀 안에서 가운데 정렬되므로 **화면 차이는 0.19px**로 보이지 않았습니다. [Switch](syrup-switch-components.md)의 폭 42.48 → 42 건과 같은 성격입니다.

### 6. 미바인딩 수치

| 값 | 건수 | 위치 | 대응 토큰 |
| --- | --- | --- | --- |
| **Padding 7** | **14** | `Tab Item` 하단 | **없음** (6=`150` · 8=`200` 사이) |
| 라운드 2 | 8 | `Icons` ▸ `05all` ▸ `01`~`04` | **없음** (최소 4=`100`) |
| Padding 5 | 4 | `Tooltip` 하·좌 | **없음** |
| Padding 2.5 · 3.5 | 각 4 | `Bubble` 상·하 | **없음** (비정수) |

**전부 토큰이 없는 값**이라 바로 바인딩할 수 있는 것이 없습니다.

#### Padding 7이 가장 많습니다

Tab Item의 상단은 6(`Spacing/150`)인데 **하단만 7**입니다. 아이콘 28 + 라벨 17 + 상하 패딩 = 58을 맞추려다 나온 값으로 보입니다.

| 선택지 | 내용 |
| --- | --- |
| A | 상하 모두 6(`Spacing/150`)으로 — **높이가 57로 1px 줄어듦** |
| B | 현행 유지 |

**높이가 바뀌므로 디자인 확인이 필요합니다.**

`Bubble`의 2.5 / 3.5도 비정수 비대칭입니다. [Tab](syrup-tab-components.md)의 4.8 / 3.6과 같은 유형입니다.

### 7. 레이어명 정리 — ✅ 완료 (22건)

| 변경 전 | 변경 후 | 위치 | 건수 |
| --- | --- | --- | --- |
| `label_1` | **`Label`** | `Tab Item` | 4 |
| `Reddot` | **`Red Dot`** | `Tab Item` | 4 |
| `Frame 3466478` | **`Bubble`** | `Tab Item` ▸ `Tooltip` | 4 |
| `text` | **`Text`** | `Tab Item` ▸ `Tooltip` | 4 |
| `Frame 1171276964` | **`Tail`** | `Tab Item` ▸ `Tooltip` | 4 |
| `Frame 3468129` | **`Tooltip`** | `Tab Bar` | 2 |

`Reddot`은 속성명 `Red Dot`과 표기를 맞췄습니다. 정리 후 **기본 이름(`Frame N`) 0건**입니다.

#### `Vector` · `Union`은 정리 대상이 아닙니다

기본 이름처럼 보여 파일 전체 분포를 세어봤습니다.

| 이름 | 파일 전체 |
| --- | --- |
| `Vector` | **738** |
| `Union` | **100** |
| `Triangle` | 10 |

[Switch](syrup-switch-components.md)의 `Oval`(237건) · [Progress Stepper](syrup-progress-stepper-components.md)의 `🟧`(100건)와 같이 **파일 관례**이므로 손대지 않았습니다.

#### 남은 2종

| 레이어 | 건수 | 이유 |
| --- | --- | --- |
| `Vector 34` | 4 | **3 × 6 숨김 벡터 · 역할 불명** — 추측해서 이름 붙이지 않음 |
| `01` · `02` · `03` · `04` | 8 | `05all` 아이콘의 격자 4칸 — **Figma 기본 이름이 아니라 의도적 번호**로 판단 |

`Vector 34`는 `Tooltip` ▸ `Bubble` 안에 숨겨진 3 × 6 벡터입니다. 무엇을 그리려던 것인지 보드에서 확인되지 않아 **그대로 뒀습니다.**

### 8. `.utill` 오타 — 외부 라이브러리

| 인스턴스 | 상태 |
| --- | --- |
| `.utill / iOS Home Button` | **외부 라이브러리** (`remote=true`) |

**`util`의 철자가 틀렸습니다.** 다만 이 파일이 아니라 **외부 라이브러리에 있는 컴포넌트**라 여기서 고칠 수 없습니다.

[AD](syrup-ad-components.md)의 외부 스타일 4건을 예외로 둔 것과 같이, **라이브러리 소유자에게 전달할 사항**입니다.

### 9. 스타일 미적용 텍스트 6건

| 크기/굵기 | 건수 | 위치 |
| --- | --- | --- |
| 10 Medium | 4 | `Tab Item` ▸ `Tooltip` ▸ 「찜하고 금 받기」 |
| 11 Regular | 2 | `Tab Bar` ▸ `Tooltip` ▸ 「할시간!」 |

이 항목은 당시 툴팁 텍스트 스타일 점검에서 제외했던 기록이에요. 현재는 11 크기의 글자 토큰도 존재하므로, 이를 ‘10~11px 전체가 토큰화 대상이 아니다’라는 공통 사용 규칙으로 확대하지 않아요. 툴팁은 이번 사용 예제에 포함하지 않았어요.

### 10. 인스턴스 현황 — 2026-10-12 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Tab Bar` | **0** |
| `.primitive / Tab Bar / Tab Item` | 10 (Tab Bar 페이지 내부) |
| `.primitive / Tab Bar / Icons` | 14 (Tab Bar 페이지 내부) |

탭바는 **앱 하단에 고정되는 화면 단위 요소**라 다른 컴포넌트 보드에 끌어다 쓸 일이 없습니다. [Result](syrup-result-components.md) · [Search Field](syrup-search-field-components.md) · [Swipe](syrup-swipe-components.md)와 같은 상황입니다.

당시에는 Tab Bar 마스터 인스턴스가 0건으로 집계됐지만 현재는 Section 1과 가이드라인·Usage에 인스턴스가 있어요. 위 수치를 현재 사용량이나 구조 변경 영향 범위로 해석하지 않아요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 문서 업데이트 완료 (2026-11-10)

가이드라인 3개와 Usage A~C, Figma 링크, 선택 상태와 Red Dot의 독립적인 사용 기준, Home Indicator 선택, 광고와 Tab Bar의 위치 관계를 반영했어요. 기존 섹션 스타일과 최소한의 보조 요소로 구성한 예제 배치 기준도 추가했어요. 마스터의 구조와 속성명은 이번 문서 작업에서 수정하지 않았어요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **27건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | 아이콘 인스턴스 레이어명 ([3](#3-아이콘-인스턴스-레이어명-1건---완료)) | 1건 · **오버라이드 연결 복구** |
| 2 | `state` → `State` · `Red dot` → `Red Dot` ([1](#1-속성명-3건---완료)) | 2건 |
| 3 | **`아이폰` → `Home Indicator`** ([1](#1-속성명-3건---완료)) | 1건 · **파일 유일 한글 속성명 해소** |
| 4 | 레이어명 정리 ([7](#7-레이어명-정리---완료-22건)) | **22건** |
| 5 | `04wallet` 폭 20.38 → 20 ([5](#5-04wallet-폭-불일치---완료)) | 1건 |

정리 후 **기본 이름 0건 · 한글 속성명 0건 · 소문자 속성명 0건**입니다.

### 확인하고 제외한 것

| 항목 | 파일 전체 | 판단 |
| --- | --- | --- |
| `Vector` · `Union` · `Triangle` | 738 · 100 · 10 | **파일 관례** — 정리 대상 아님 |
| `01`~`04` (격자 4칸) | — | **의도적 번호** — Figma 기본 이름 아님 |
| `Vector 34` 4건 | — | 숨김 3 × 6 · **역할 불명이라 추측 보류** |

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Home Indicator` variant 구조 통일 ([2](#2-home-indicator-variant의-구조-불일치)) | **모양 바뀔 수 있음** | 중간 |
| 2 | Padding 7 통일 ([6](#6-미바인딩-수치)) | **높이 1px 변화** | 중간 |
| 3 | `Resource` 값 개명 ([1](#1-속성명-3건---완료) · [4](#4-resource-옵션-표시-순서)) | 에셋명 확인 필요 | 중간 |
| 4 | `.utill` 오타 ([8](#8-utill-오타--외부-라이브러리)) | **외부 라이브러리 — 전달 사항** | — |
| 5 | 스타일 미적용 6건 ([9](#9-스타일-미적용-텍스트-6건)) | 과거 제외 기록 — 현재 토큰 기준 재확인 필요 | — |

**이름 관련 문제는 모두 해소됐습니다.** 남은 1·2번은 고치면 모양이 바뀌므로 디자인 확인이 선행돼야 합니다.

가장 큰 사안은 **[점검 2의 `Home Indicator` variant](#2-home-indicator-variant의-구조-불일치)** 입니다. 래퍼·정렬·폭이 모두 달라 오버라이드가 끊기는데, 특히 `False`의 **`MIN`(왼쪽 정렬)** 이 탭바의 균등 배분과 어긋나 보입니다. 현재 사용 화면과 문서 예제의 참조를 함께 확인한 뒤 변경해야 해요.

`.utill` 오타는 외부 라이브러리 소유자에게 전달할 사항입니다.
