# Syrup Design System — Search Field 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Search Field` 페이지 → [Search Field 섹션 `8480:32971`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8480-32971) |
| 섹션 크기 | 1440 × 1454 |
| 컴포넌트 수 | **2개** (Master 1 · Child Item 1) |
| Variant 총수 | **4개** |
| 기준일 | 2026-11-10 (가이드라인·Usage·Dot 미션 기준 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **텍스트 입력을 통해 콘텐츠를 검색할 수 있는 입력 필드예요.**
> 사용자가 원하는 항목을 빠르게 찾을 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Search Field — Master Component](#1-search-field--master-component)
3. [`.primitive / Search Field / Icon`](#2-primitive--search-field--icon)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)
9. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 돋보기 아이콘 1종으로 구성돼요. 별도 섹션에 가이드라인 3개와 예제 A~E를 정리했어요. 기존 노드·인스턴스·토큰 집계는 2026-10-12 기준이며 추가된 사용 화면과 예제까지 포함한 최신 통계는 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 448) | `Search Field` 1종 |
| y 1022 | Section Header | Child Items |
| y 1162 | (높이 228) | `.primitive / Search Field / Icon` 1종 |
| 별도 섹션 | [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2543) | 가이드라인 3개 |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2544) | 예제 A~E 5개 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Search Field` | Set 3 | `State` + `Dot` BOOLEAN | 328 × 56 | **0** |
| 2 | `.primitive / Search Field / Icon` | Component | — | 28 × 28 | 3 (페이지 내부) |

검색창 하나와 돋보기 아이콘 하나가 전부입니다. 두 컴포넌트 이름이 모두 어긋나 있었고 바로잡았습니다 → [점검 1](#1-컴포넌트-이름-2건---완료)

---

## 1. Search Field — Master Component

**Node** `8493:878` · Component Set · **3 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Placeholder` | `Placeholder` · `Typing` · `Typed` |
| `Dot` | BOOLEAN | `true` | — |

### 공통 레이아웃 — 세 variant가 완전히 동일

| 항목 | 값 | 토큰 |
| --- | --- | --- |
| 크기 | **328 × 56** | — |
| 레이아웃 | 가로 오토레이아웃 MIN / CENTER | — |
| Padding | `16 / 16 / 16 / 16` | `Spacing/400` ✅ |
| Gap | 10 | `Spacing/250` ✅ |
| 배경 | 흰색 | `Color/Gray_White` ✅ |
| 라운드 | 10 | `Corner radius/250` ✅ |
| **테두리** | **주황 1px** | **`Color/Primary_Orange`** ✅ |

**프레임 속성은 세 variant가 한 글자도 다르지 않습니다.** 차이는 내부 요소에만 있습니다.

### variant별 차이

| Variant | 텍스트 색 | `Dot` | `Close` 아이콘 |
| --- | --- | --- | --- |
| `Placeholder` | `Color/Gray_400` | 미션 상태에 따라 표시 | — |
| `Typing` | `Color/Gray_100` | 숨김 | — |
| `Typed` | `Color/Gray_100` | 숨김 | **`Icon / Close` 20 × 20** |

`Typing`과 `Typed`의 유일한 차이는 **Close 아이콘 하나**입니다.

### 레이어 구조

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `Content` | Frame | 258 × 22 | Gap 10 |
| └ `Text` | Frame | 258 × 22 (Typed는 228) | Gap 4 |
| &nbsp;&nbsp;└ `Placeholder` | Text | 85 × 22 | 17 Medium `t1100_17_medium` |
| &nbsp;&nbsp;└ `Dot` | Ellipse | 6 × 6 | `Color/Primary_Orange` |
| └ `Icon / Close` | Instance | 20 × 20 | `Typed`에만 존재 |
| `.primitive / Search Field / Icon` | Instance | 28 × 28 | 돋보기 |

이전엔 `Frame 1`이 **같은 이름으로 2겹 중첩**돼 있었습니다 → [점검 5](#5-레이어명과-중첩-구조---완료-12건)

---

## 2. `.primitive / Search Field / Icon`

**Node** `8600:34656` · Component · **28 × 28** · 오토레이아웃 없음 · 배경 없음 · 라운드 0

| 레이어 | 타입 | 크기 | 채움 | 테두리 |
| --- | --- | --- | --- | --- |
| `Search` | Group | 17.5 × 17.07 | — | — |
| └ `Magnifier` | Group | 17.5 × 17.07 | — | — |
| &nbsp;&nbsp;└ `Circle` | Ellipse | 14.39 × 14.39 | 없음 | `Color/Primary_Orange` **1.931px** |
| &nbsp;&nbsp;└ `Handle` | Vector | 4.89 × 4.33 | 없음 ✅ | `Color/Primary_Orange` **1.931px** |

원(`Circle`) + 손잡이(`Handle`)로 그린 **돋보기**입니다. 색은 테두리로만 입히고 채움은 쓰지 않습니다.

레이어명 4건과 숨겨진 채움은 정리했고([점검 2](#2-btn_serach-오타---완료) · [3](#3-보이지-않는-잔존-채움---완료) · [5](#5-레이어명과-중첩-구조---완료-12건)), **선 두께 1.931**만 남았습니다 → [점검 4](#4-선-두께-1931)

---

## 가이드라인

### 1. 입력 상태에 맞는 State를 사용해요

입력 전에는 Placeholder로 검색할 대상이나 혜택을 안내하고, 검색어를 입력한 상태는 Typing으로 표시해요. 입력값 지우기 버튼이 필요한 상태는 Typed를 사용해요. 세 상태의 주황 테두리는 동일하게 유지해요.

| `State` | 용도 | 텍스트 / 보조 기능 |
| --- | --- | --- |
| `Placeholder` | 입력 전 안내 | 검색 대상·혜택 문구, 해당 미션 상태에 따른 Dot |
| `Typing` | 검색어가 입력된 상태 | 실제 입력값을 진한 색상으로 표시 |
| `Typed` | 입력값 지우기 기능 제공 | 실제 입력값과 Close 버튼 표시 |

`Typed`를 검색 결과 로딩 완료나 미션 완료 상태로 해석하지 않아요. 지우기 버튼과 검색 아이콘은 서로 다른 동작이에요.

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2545)

### 2. 찜하기 미션이 완료되지 않았을 때 Dot을 표시해요

쇼핑적립 탭에서 검색 후 찜하기 미션이 완료되지 않았으면 Dot=True로 표시해요. 미션을 완료하고 금을 받은 후에는 안내 문구를 바꾸고 Dot=False로 숨겨요. Dot은 Placeholder 상태에서만 표시해요.

| 쇼핑적립 탭의 상태 | 안내 문구 | `Dot` |
| --- | --- | --- |
| 1일 1회 찜하기 미션·금 받기 전 | 상품 찜하고 매일 3금 받으세요 | `True` |
| 미션 완료·금 받기 후 | 금 받는 상품을 검색해보세요 | `False` |

Dot은 일반적인 문구 강조나 필수 입력 표시가 아니라 **쇼핑적립 탭의 검색 후 찜하기 미션 미완료 표시**예요. 다른 검색창에 장식 목적으로 켜지 않아요. Typing·Typed에서는 Dot이 보이지 않으며, 입력 시작만으로 미션이 완료됐다고 판단하지 않아요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2612)

### 3. 검색 보조 요소는 필드 밖에 배치해요

최근·추천 검색어는 Search Field 아래에 별도로 배치해 검색을 도와요. 찜처럼 검색과 다른 기능은 필드 밖에 두고, 함께 배치하는 요소를 고려해 검색창 폭을 조정해요.

추천 검색어는 별도 Chip 요소로 구성하고, 찜 기능도 필드 내부 검색 아이콘과 구분해요. 필드의 높이 56과 내부 구성은 유지하면서 배치 공간에 맞춰 폭을 조정해요.

[Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2663)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2544)에 상태와 보조 기능에 따른 예제 5개를 구성했어요.

| 예제 | 구성 | 설명 |
| --- | --- | --- |
| [A. 입력 전 검색 안내](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2751) | `State=Placeholder`, `Dot=False` | 검색할 대상이나 혜택을 Placeholder 문구로 안내해요. 예제는 Dot=False로 간결하게 표시해요. |
| [B. 검색어 입력 상태](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2777) | `State=Typing`, 검색어 “커피” | 검색어가 입력된 상태는 Typing으로 표시해요. 입력값을 안내 문구와 구분해 진한 색상으로 보여줘요. |
| [C. 입력값 지우기](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2803) | `State=Typed`, 검색어 “커피” | 입력한 검색어를 지울 수 있는 상태는 Typed를 사용해요. 지우기 버튼과 검색 아이콘의 역할을 구분해요. |
| [D. 추천 검색어와 함께 사용](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2834) | Search Field + 별도 추천 검색어 | Search Field 아래에 추천 검색어를 함께 배치해요. 입력 필드와 추천 검색어는 별도 요소로 구성해요. |
| [E. 찜 기능과 함께 사용](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11698-2886) | Search Field + 별도 찜 기능, `Dot=True` | 검색창 옆에 찜 기능을 별도로 배치해요. 예제는 찜하기 미션 미완료 상태로, 안내 문구와 Dot을 함께 표시해요. |

미션 완료 전후의 안내 문구와 Dot 비교는 가이드라인 2에서 확인해요. 예제 A의 일반 입력 전 안내와 E의 미션 미완료 안내는 모두 Placeholder지만 Dot의 사용 맥락이 달라요.

## 예제 레이아웃과 AI 사용 기준

- 단독 Search Field는 슬롯에 직접 배치해요. 불필요한 `화면` 레이어와 슬롯 패딩을 추가하지 않고 좌측·상단 정렬로 구성해요.
- 추천 검색어·찜 기능처럼 관계가 있는 요소를 함께 배치할 때만 필요한 오토레이아웃 프레임을 사용해요. 컴포넌트 내부 패딩은 유지해요.
- 상태와 무관하게 주황 테두리를 유지해요. 임의로 비활성 회색 테두리나 별도 Focused 상태를 만들지 않아요.
- `Dot`은 기본값이 true여도 모든 Placeholder에 표시하지 않아요. 쇼핑적립 탭의 해당 미션 상태를 확인해 사용해요.
- `Typing`·`Typed`에 Dot이 안 보이는 것은 표시 구조예요. 실제 미션 완료 여부나 리워드 지급 여부는 입력 상태와 별도로 판단해요.
- `Typed`는 지우기 기능이 있는 입력값 표시 구성이에요. 검색 완료 여부·키보드 표시 여부·실시간 검색 동작을 Variant 이름만으로 추정하지 않아요.
- 기본 폭 328은 샘플 규격이에요. 주변 요소와 부모 폭에 맞춰 인스턴스 폭을 조정하되 높이 56과 검색·지우기 아이콘을 유지해요.
- 예제의 검색어·추천 검색어·혜택은 소재예요. 미션 안내의 1일 1회·3금은 첨부 UI 정의에 따른 현재 내용이며 다른 검색 기능의 보상 규칙으로 확대하지 않아요.

---

## 설계 규칙 요약

### 상태 표현

| 상태 | 테두리 | 텍스트 | 보조 요소 |
| --- | --- | --- | --- |
| `Placeholder` (입력 전) | 주황 | `Gray_400` (흐림) | 쇼핑적립 찜하기 미션 미완료 시 Dot |
| `Typing` (입력 중) | 주황 | `Gray_100` (진함) | — |
| `Typed` (입력값 지우기 제공) | 주황 | `Gray_100` | Close 버튼 |

**상태 구분을 텍스트 색과 아이콘 유무로만** 하고, 테두리는 쓰지 않습니다 → [점검 6](#6-세-상태-모두-주황-테두리---디자인-의도)

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 배경 | `Color/Gray_White` ✅ |
| 테두리 | `Color/Primary_Orange` ✅ |
| 라운드 | `Corner radius/250` ✅ |
| Padding | `Spacing/400` ✅ |
| Gap | `Spacing/250` ✅ |
| 텍스트 색 | `Color/Gray_400` · `Color/Gray_100` ✅ |
| 텍스트 스타일 | `t1100_17_medium` 적용 ✅ · **미적용 0건** |
| 아이콘 색 | `Color/Primary_Orange` ✅ |
| 원격 텍스트 스타일 | **0건** ✅ |
| 미바인딩 색상 | **0건** ✅ (숨겨진 채움 1건 제외) |
| 미바인딩 수치 | **0건** ✅ (보드 영역 Padding 100 제외) |
| 줄 구분자(U+2028/9) | **0건** ✅ |

[Result](syrup-result-components.md)와 함께 **토큰 적용이 가장 깨끗한 페이지**입니다. 컴포넌트 내부에 미바인딩 값이 하나도 없습니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Section Header` 2 · `Title Bar` 1 | 3 |
| ❖Components | `Icon / Close` | 1 |

외부 라이브러리 인스턴스는 **0건**입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번 갱신은 가이드라인·Usage와 Dot의 미션 기준 문서화이며, 파일 전체의 토큰·스타일·인스턴스 수는 재집계하지 않았어요. 과거 통계와 검토 제안을 현재 사용 규칙과 구분해요.

### 1. 컴포넌트 이름 2건 — ✅ 완료

| 변경 전 | 변경 후 | 문제였던 점 |
| --- | --- | --- |
| `SearchField` | **`Search Field`** | 붙여쓰기 — 페이지명과 불일치 |
| `.primitive / Result / Search / Search` | **`.primitive / Search Field / Icon`** | `Result` 네임스페이스 + `Search / Search` 중복 |

`SearchField`는 파일에서 **유일하게 붙여 쓴 컴포넌트명**이었습니다. 다른 컴포넌트는 [Product Grid](syrup-product-grid-components.md) · [List Row](syrup-list-row-components.md) · [Bottom Sheet](syrup-bottom-sheet-components.md)처럼 모두 띄어 씁니다.

Child Item 쪽이 더 심각했습니다. **`Result` 밑에 있지만 [Result](syrup-result-components.md) 페이지가 아니라 Search Field 페이지에 놓여** 있었습니다.

| 페이지 | primitive 네임스페이스 |
| --- | --- |
| [Result](syrup-result-components.md) | `.primitive / Result / Icon / Empty` · `Result / Icon / Image` |
| Search Field | ~~`.primitive / Result / Search / Search`~~ → `.primitive / Search Field / Icon` ✅ |

Result에서 복제해 만들며 경로가 남은 것으로 보입니다. 인스턴스 3건은 **이름이 원본을 따르고 있어 자동으로 함께 바뀌었습니다.**

### 2. `btn_serach` 오타 — ✅ 완료

| 변경 전 | 변경 후 |
| --- | --- |
| `btn_serach` | **`Search`** |

`search`의 철자가 틀려 있었습니다. 내부 레이어명이라 인스턴스 영향은 없습니다.

철자만 고칠지, 표기 방식까지 맞출지 판단하기 위해 **`btn_` 접두사가 파일 관례인지 세어봤습니다.**

| 접두사 | 파일 전체 건수 | 판단 |
| --- | --- | --- |
| `btn_` | **4** | 관례 아님 |
| `syrup_` · `img_` · `🟧` | 수십~100건 | **관례** ([Progress Stepper](syrup-progress-stepper-components.md) 참고) |

4건뿐이라 관례로 보기 어려워, **대문자 시작 · 역할을 드러내는 이름** 기준에 맞춰 `Search`로 바꿨습니다. `syrup_`·`img_`·`🟧`처럼 수십 건 이상인 접두사였다면 `btn_search`로 철자만 고쳤을 것입니다.

[Progress Stepper](syrup-progress-stepper-components.md)의 `Steeper`→`Stepper` 64건, [Button](syrup-button-components.md)의 `Coner`→`Corner`, [Card](syrup-card-components.md)의 `Viariant`→`Variant`와 같은 성격입니다.

### 3. 보이지 않는 잔존 채움 — ✅ 완료

`Handle`(이전 `Line`) 벡터에 채움이 하나 남아 있었습니다.

| 속성 | 값 | 조치 |
| --- | --- | --- |
| 채움 | `#D8D8D8` · **`visible: false`** | **제거** ✅ |
| 테두리 | `Color/Primary_Orange` | 유지 |

꺼져 있어 화면에 영향이 없었고, 감사에서도 미바인딩 색으로 잡히지 않던 값입니다. `#D8D8D8`은 **이 파일에 대응 토큰이 없는 값**이라(`Color/Gray_750`이 #DDDDDD로 3 차이) 남겨둘 이유가 없었습니다.

같은 색이 [Progress Stepper](syrup-progress-stepper-components.md)에서도 미바인딩 1건으로 발견됐습니다.

### 4. 선 두께 1.931

| 레이어 | 선 두께 |
| --- | --- |
| `Ellipse 2` | **1.9310344457626343** |
| `Line` | **1.9310344457626343** |

원본 아이콘을 **비정수 배율로 축소한 흔적**입니다. 2px로 그린 29px 아이콘을 28px로 줄이면 2 × (28 ÷ 29) = 1.931이 나옵니다.

| 선택지 | 내용 |
| --- | --- |
| A | 선 두께를 **2**로 맞춤 — 두께가 아주 미세하게 굵어짐 |
| B | 그대로 유지 |

화면에서 0.07px 차이는 보이지 않지만, **값이 소수점 16자리로 남아 있는 것 자체**가 다른 아이콘과 다릅니다.

### 5. 레이어명과 중첩 구조 — ✅ 완료 (12건)

| 변경 전 | 변경 후 | 위치 | 건수 | 근거 |
| --- | --- | --- | --- | --- |
| `Frame 1` (바깥) | `Content` | `Search Field` | 3 | 텍스트 묶음 + Close 배치 |
| `Frame 1` (안쪽) | `Text` | `Search Field` | 3 | 문구 + Dot 묶음 |
| `placeholder` | `Placeholder` | `Search Field` | 3 | 소문자 |
| `btn_serach` | `Search` | `Icon` | 1 | 오타 + 스네이크 표기 |
| `Group 2338` | `Magnifier` | `Icon` | 1 | 돋보기 전체 |
| `Ellipse 2` | `Circle` | `Icon` | 1 | 돋보기 원 |
| `Line` | `Handle` | `Icon` | 1 | 돋보기 손잡이 |

**같은 이름 `Frame 1`이 2겹 중첩**돼 있던 것이 가장 읽기 어려운 지점이었습니다.

#### 바깥 프레임은 유지했습니다

| Variant | 바깥 `Content` | 안쪽 `Text` |
| --- | --- | --- |
| `Placeholder` | 258 × 22 | **258 × 22** |
| `Typing` | 258 × 22 | **258 × 22** |
| `Typed` | 258 × 22 | 228 × 22 |

`Typed`에서만 안쪽이 좁아지는데, **Close 아이콘(20) + Gap(10)만큼** 줄어든 결과입니다. 즉 바깥 프레임은 「텍스트 묶음 + Close」를 가로로 배치하는 역할을 합니다.

`Typed`에서는 역할이 있고 나머지 둘에서는 없지만, **variant 간 레이어 구성을 맞추려면 세 곳 모두 있어야** 합니다. 제거하지 않았습니다.

#### 남은 중첩 — `Icon`의 그룹 2겹

| 레이어 | 크기 |
| --- | --- |
| `Search` (Group) | 17.5 × 17.07 |
| └ `Magnifier` (Group) | **17.5 × 17.07** |

바깥·안쪽 그룹의 크기가 **완전히 같아** 한 겹은 불필요합니다. 그룹 해제는 좌표에 영향을 줄 수 있어 손대지 않았습니다.

### 6. 세 상태 모두 주황 테두리 — ✅ 디자인 의도

`Placeholder` · `Typing` · `Typed` 전부 테두리가 **`Color/Primary_Orange` 1px**입니다.

> **의도된 설계입니다.** 검색창이 잘 보이게 해달라는 요청이 있어 **상태와 무관하게 항상 강조**하도록 정했습니다.

같은 파일의 Text Field 쪽은 둘로 갈립니다.

| 컴포넌트 | 비활성 | 활성 |
| --- | --- | --- |
| `Text Field / Text Area` | `Color/Gray_800` | `Color/Primary_Orange` |
| `Text Field / Task` | `Color/Primary_Orange` | `Color/Primary_Orange` |
| **`Search Field`** | **`Color/Primary_Orange`** | `Color/Primary_Orange` |

`Text Area`는 입력 전 회색 → 입력 시 주황으로 바뀌지만, **`Search Field`는 `Task`와 같이 항상 주황**입니다. 포커스 전후가 테두리로 구분되지 않는 대신 **텍스트 색(`Gray_400` → `Gray_100`)으로 구분**합니다.

**변경 대상이 아닙니다.**

### 7. `Dot` 속성은 `Placeholder` 전용 — ✅ 디자인 의도

| Variant | `Dot` 레이어 | 속성 연결 |
| --- | --- | --- |
| `Placeholder` | 보임 | **`visible:Dot`** ✅ |
| `Typing` | 숨김 | 없음 |
| `Typed` | 숨김 | 없음 |

> Dot은 쇼핑적립 탭의 검색 후 찜하기 미션 미완료 표시예요. 표시 구조는 Placeholder에만 연결돼요. 미션 완료·금 받기 후에는 문구를 변경하고 Dot=False로 숨겨요.

`Typing` · `Typed` 상태에서는 안내 문구 대신 입력값을 표시하므로 Dot도 숨겨져요. 이는 미션 완료를 뜻하지 않아요. Placeholder로 돌아오면 실제 미션·금 받기 상태에 맞춰 문구와 Dot을 표시해요.

알아둘 점 하나 — Figma의 BOOLEAN 속성은 **Component Set 전체에 걸리므로** `Typing` · `Typed`를 선택해도 속성 패널에 `Dot` 스위치가 계속 보입니다. 거기서는 켜도 변화가 없습니다. Figma의 동작 방식이라 바꿀 수 없고, **설계상의 문제는 아닙니다.**

**변경 대상이 아닙니다.**

### 8. `Property 1` → `State` — ✅ 완료

| 변경 전 | 변경 후 | 값 |
| --- | --- | --- |
| `Property 1` | **`State`** | `Placeholder` · `Typing` · `Typed` |

Text Field가 같은 개념에 **`State`**(`Inactive` · `Focused` · `Typing` · `Complete` · `Error`)를 쓰고 있어 맞췄습니다. variant 이름도 `State=Placeholder` 형태로 따라 바뀌었습니다.

#### 값 이름은 그대로 뒀습니다

값 이름은 Text Field와 다릅니다.

| Search Field | Text Field |
| --- | --- |
| `Placeholder` | `Inactive` |
| `Typing` | `Typing` |
| `Typed` | `Complete` |

**`Typing`만 겹치고 나머지 둘은 다른 말**을 씁니다. 같은 입력 필드 계열이므로 용어를 맞추는 편이 읽기 쉽습니다. 다만 이름을 바꾸면 **검색창 고유의 의미(입력 전 안내문구가 보이는 상태)가 흐려질 수 있어** 판단이 필요합니다.

### 9. 인스턴스 0건 — 과거 집계

| 구분 | 인스턴스 |
| --- | --- |
| `Search Field` | **0** |
| `.primitive / Search Field / Icon` | 3 (Search Field 페이지 내부) |

검색창은 **검색 화면의 상단에 붙는 요소**라 다른 컴포넌트 보드에 끌어다 쓸 일이 거의 없습니다. [Result](syrup-result-components.md) · [Loader](syrup-loader-components.md) · [Progress Stepper](syrup-progress-stepper-components.md)와 같은 상황입니다.

> 이는 2026-10-12의 기존 집계예요. 현재 Section 1과 Usage에 Search Field 사용 사례가 추가되어 현재 사용 여부를 뜻하지 않아요.

### 10. `Typed`의 본문이 「플레이스홀더」 — 기존 마스터 점검

세 variant 모두 텍스트 내용이 **「플레이스홀더」**로 같습니다.

| Variant | 의미 | 현재 텍스트 |
| --- | --- | --- |
| `Placeholder` | 입력 전 안내문구 | 「플레이스홀더」 ✅ |
| `Typing` | 입력 중 | 「플레이스홀더」 |
| `Typed` | 입력 완료 | 「플레이스홀더」 |

텍스트 색은 `Gray_400` → `Gray_100`으로 제대로 바뀌지만, **내용이 그대로라 입력된 상태로 보이지 않습니다.** 보드에서 상태 차이를 읽기 어렵습니다.

기존 마스터 점검 기록이에요. 이번 가이드라인·Usage의 Typing·Typed 예제에는 실제 입력값 형태의 “커피”를 표시해 차이를 설명했어요. 마스터 문구를 변경했다는 뜻은 아니에요.

---

## 정리 우선순위

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **17건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | `btn_serach` → `Search` ([2](#2-btn_serach-오타---완료)) | 1건 |
| 2 | 레이어명 정리 ([5](#5-레이어명과-중첩-구조---완료-12건)) | **12건** |
| 3 | `.primitive / Result / Search / Search` → `.primitive / Search Field / Icon` ([1](#1-컴포넌트-이름-2건---완료)) | 1건 (인스턴스 3건 자동 반영) |
| 4 | `SearchField` → `Search Field` ([1](#1-컴포넌트-이름-2건---완료)) | 1건 |
| 5 | 숨겨진 채움 `#D8D8D8` 제거 ([3](#3-보이지-않는-잔존-채움---완료)) | 1건 |
| 6 | `Property 1` → `State` ([8](#8-property-1--state---완료)) | 1건 |

정리 후 **기본 이름 0건 · `Property 1` 0건 · 소문자 레이어명 0건**입니다.

### 판단 완료

| 항목 | 결론 |
| --- | --- |
| 세 상태 모두 주황 테두리 ([6](#6-세-상태-모두-주황-테두리---디자인-의도)) | **의도** — 검색창이 잘 보이게 해달라는 요청에 따른 설계 |
| `Dot` 속성이 `Placeholder`에만 연결 ([7](#7-dot-속성은-placeholder-전용---디자인-의도)) | **의도** — 쇼핑적립 찜하기 미션 미완료 표시, Placeholder에서만 표시 |

둘 다 변경하지 않습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | 선 두께 1.931 → 2 ([4](#4-선-두께-1931)) | 미세하게 굵어짐 | 낮음 |
| 2 | `Typed` 샘플 문구 ([10](#10-typed의-본문이-플레이스홀더)) | 보드 가독성 | 낮음 |
| 3 | `Icon`의 그룹 2겹 ([5](#5-레이어명과-중첩-구조---완료-12건)) | 좌표 영향 가능 | 낮음 |
| 4 | `State` 값 이름을 Text Field와 맞출지 ([8](#8-property-1--state---완료)) | 판단 필요 | 낮음 |

**토큰은 전부 바인딩돼 있고, 네이밍 정리와 설계 판단이 모두 끝났습니다.**

남은 4건은 모두 선택 사항입니다. 1번은 0.07px 차이라 화면에서 구분되지 않고, 2번은 보드에서 상태 차이를 읽기 쉽게 하는 수준, 3·4번은 지금 상태로도 문제가 없습니다.
