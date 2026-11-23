# Syrup Design System — Toast 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Toast` 페이지 → [Toast 섹션 `8502:5439`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8502-5439) |
| 섹션 크기 | 1440 × 1404 |
| 컴포넌트 수 | **2개** (Master 1 · Child Item 1) |
| Variant 총수 | **4개** (2 · 2) |
| 기준일 | 2026-11-10 (가이드라인 3개·Usage A~C·배경색 통일 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) |

> **간단한 메시지를 잠시 동안 화면에 표시하는 피드백 컴포넌트에요.**
> 작업 완료나 오류 등의 상태를 빠르게 알려줄 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Toast / Icon / Image` | `8502:6461` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Toast — Master Component](#1-toast--master-component)
3. [`Toast / Icon / Image`](#2-primitive--toast--icon--image)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)
9. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 섹션과 Guidelines, Usage로 구성해요. 기존 노드 30개·텍스트 6개 및 아래 보드 집계는 2026-11-02 기록으로, 새 가이드라인·예제를 포함한 현재 페이지 전체 집계가 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 366) | `Toast` 1종 |
| y 940 | Section Header | Child Items |
| y 1080 | (높이 260) | `Toast / Icon / Image` 1종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Toast` | Set 2 | **`2 Line`** | 300 × 62 / 300 × 44 | **0** |
| 2 | `Toast / Icon / Image` | Set 2 | `Icon` | 20 × 20 | 1 (Toast 내부) |

속성명 두 개가 어긋나 있었고, `Property 1` → `Icon`은 바로잡았습니다 ✅ → [점검 1](#1-속성명-2건---1건-완료)

---

## 1. Toast — Master Component

**Node** `8502:10441` · Component Set · **2 variants**

| Property | Type | Options |
| --- | --- | --- |
| **`2 Line`** | VARIANT | `True` · `False` |

### 공통 스펙

| 항목 | 값 | 토큰 |
| --- | --- | --- |
| 폭 | 기본 **300** · 대상 영역에 맞춰 사용 (배치 예제는 300 / 320) | — |
| 배경 | **`#222222` · 채우기 불투명도 80%** | **직접 값 사용 · 컬러 토큰 미연결** |
| 라운드 | 16 | `Corner radius/400` ✅ |
| 좌우 Padding | 20 | `Spacing/500` ✅ |
| Gap | 4 | `Spacing/100` ✅ |
| 문구(`Message`) | 15 Medium `t1300_15_medium` ✅ · `Color/Gray_White` ✅ · **가운데 정렬** |
| 줄 간격 | 19px | — |

어두운 반투명 배경 위에 흰 글씨를 올린 **떠 있는 알림 바**입니다.

### 두 variant의 구조

| 항목 | `2 Line=True` | `2 Line=False` |
| --- | --- | --- |
| 높이 | **62** (FIXED) | **44** (FIXED) |
| 레이아웃 방향 | **VERTICAL** | **HORIZONTAL** |
| 상하 Padding | **57** (현재 저장값 · 높이 62 고정 및 가운데 정렬) | **12** (`Spacing/300` ✅) |
| 아이콘 | **없음** | **`Toast / Icon / Image` 20 × 20** |
| 문구 | 「광고 누르고, 광고 페이지에서 5초 이상 …」 (2줄, 38 높이) | 「3금을 적립 받았어요!」 (1줄, 19 높이) |

레이아웃 방향 · 여백 처리 방식 · 아이콘 유무가 달라요. → [점검 2](#2-두-variant의-구조가-다름)

---

## 2. `Toast / Icon / Image`

**Node** `8502:6461` · Component Set · **2 variants** · 모두 **20 × 20** · 오토레이아웃 없음

| Property | Type | Options |
| --- | --- | --- |
| `Icon` | VARIANT | `Firecracker` · `Gold` |

| Variant | 자식 | 크기 | 위치 |
| --- | --- | --- | --- |
| `Firecracker` | `Firecracker` (IMAGE) | **20 × 20** | x 0, y 0 |
| `Gold` | `Gold` (IMAGE) | **20 × 10** | x 0, **y 5** |

**`Gold`는 높이가 절반(10)** 이고 세로 가운데에 놓입니다. 원본 에셋의 가로세로 비율 차이로 보입니다.

레이어명이 variant 값과 같아 **역할이 바로 읽힙니다.** 이 페이지에서 유일하게 이름이 제대로 붙은 부분입니다.

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-502)

### 1. 문구 길이에 맞는 줄 수를 사용해요

짧은 안내나 완료 메시지는 한 줄로 표시하고, 조건 설명이 길면 두 줄로 나누어 보여줘요.
문구가 잘리거나 읽기 어렵게 줄어들지 않도록 2 Line 유형을 선택해요.

- 비교: 한 줄 안내 · `2 Line=False` / 두 줄 안내 · `2 Line=True`
- [가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-504)

### 2. 안내 목적에 맞는 아이콘을 사용해요

한 줄로 리워드 참여를 안내할 때는 Gold, 적립 완료를 알릴 때는 Firecracker 아이콘을 사용해요.
두 줄로 조건을 설명하는 경우에는 아이콘 없이 문구만으로 안내해요.

- 비교: 참여 안내 · Gold / 적립 완료 · Firecracker
- [가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-657)

### 3. 안내할 대상 아래에 배치해요

광고나 콘텐츠에 대한 안내는 대상 요소 아래에 16 간격을 두고 배치해요.
Toast의 폭은 대상 영역에 맞추고, 서로 겹치지 않도록 배치해요.

- ETMS: 폭 300, 대상 아래 16 간격 · 콘텐츠 카드: 폭 320, 대상 아래 16 간격
- 이 기준은 예제의 대상 아래 배치 패턴을 설명해요. 화면 하단 고정 오프셋으로 해석하지 않아요.
- [가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-812)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-503)

| 예제 | 설명 | 구성 | 링크 |
| --- | --- | --- | --- |
| A. 리워드 참여 안내 | 페이지 방문으로 받을 수 있는 리워드를 안내해요. 한 줄 문구에 Gold 아이콘을 함께 사용해요. | `2 Line=False` · Gold · 「페이지 방문하고 금 받기!」 | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-1008) |
| B. 적립 조건 안내 | 광고 페이지에서 머물러야 하는 시간 등 적립 조건을 안내해요. 두 줄 문구로 필요한 조건을 구체적으로 알려줘요. | `2 Line=True` · 아이콘 없음 · 「광고 누르고, 광고 페이지에서 / 5초 이상 머무르면 금이 적립돼요!」 | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-1085) |
| C. 적립 완료 | 금 적립이 완료되었음을 알려줘요. 적립된 금액과 Firecracker 아이콘으로 결과를 보여줘요. | `2 Line=False` · Firecracker · 「3금을 적립 받았어요!」 | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11776-1160) |

## 예제 레이아웃과 AI 사용 기준

- Guidelines 섹션: 960 × 1286 · Usage 섹션: 1360 × 378. 기존 섹션과 동일한 흰 배경·모서리 24를 사용해요.
- 예제 Slot은 폭 360, 패딩 0, 좌측·상단 정렬, 높이 Hug예요. Toast만 필요한 곳은 별도 ‘화면’ 래퍼 없이 직접 배치해요.
- 제목·설명 영역 끝과 Slot의 간격은 50이에요. 실제 Toast의 폭은 300이며 가이드라인 3의 카드 예제만 320이에요.
- 안내 문구와 완료 문구는 같은 Toast의 사용 목적을 구분한 예제예요. 별도 마스터를 만들지 않아요.
- `2 Line`은 Toast의 VARIANT 속성이고 `Icon`은 하위 아이콘 컴포넌트의 VARIANT 속성이에요. 상위 Toast에 없는 아이콘 속성을 임의로 가정하지 않아요.
- 배경은 모든 예제와 마스터에서 **`#222222` · 채우기 불투명도 80%**로 유지해요. `Opacity_Black_100`이나 불투명한 회색으로 대체하지 않아요.
- 노출 시간·자동 닫힘 시간·동시 노출 우선순위는 이번 정적 패턴에서 확인하지 않았으므로 임의의 수치를 규칙으로 추가하지 않아요.
- Section 1의 아노테이션은 작업 시 4개 제거했어요. 현재 페이지는 마스터·Guidelines·Usage로 구성되어 있어요.

---

## 설계 규칙 요약

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 문구 색 | `Color/Gray_White` ✅ |
| 텍스트 스타일 | `t1300_15_medium` ✅ · **미적용 0건** |
| 라운드 | `Corner radius/400` ✅ |
| Padding · Gap | `Spacing/100` · `300` · `500` ✅ |
| 배경 | **`#222222` · 80% 직접 값** · `Opacity_Black_100`으로 대체하지 않아요 |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |
| 외부 변수 | **0건** ✅ (보드 영역 `Spec docs` 제외) |

배경은 시각적 일치를 위해 `#222222` · 80%를 직접 지정해요. 과거의 ‘미바인딩 0건’ 기록은 현재 상태를 뜻하지 않아요. → [배경색 확인](#3-배경색-확인--2026-11-10)

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Section Header` 2 · `Title Bar` 1 | 3 |

컴포넌트 내부에서 다른 페이지를 참조하는 인스턴스가 **0건**이고, 외부 라이브러리도 **0건**입니다. 이 파일에서 가장 독립적인 컴포넌트 중 하나입니다.

---

## 점검 필요 사항

> 아래 네이밍·구조 제안은 과거 점검 기록이에요. 현재 확정된 사용 기준은 가이드라인·Usage와 배경색 확인 항목을 따라요. 마스터 구조 개선은 이번 작업에 포함하지 않았어요.

### 1. 속성명 2건 — ✅ 1건 완료

| 컴포넌트 | 변경 전 | 변경 후 | 상태 |
| --- | --- | --- | --- |
| `Toast / Icon / Image` | **`Property 1`** | **`Icon`** | ✅ 완료 |
| `Toast` | **`2 Line`** | `Two Line` 등 | **보류 — Stepper와 함께 판단** |

#### `Property 1` → `Icon` ✅

값은 `Firecracker` · `Gold`로 의미가 분명한데 **속성명만 자동 생성명 그대로**였습니다. 값이 아이콘 종류이므로 `Icon`으로 바꿨고, variant 이름도 `Icon=Firecracker` · `Icon=Gold`로 따라왔습니다.

[Swipe](syrup-swipe-components.md) · [Ticker](syrup-ticker-components.md)는 값까지 `Variant2`였던 것과 달리 **이름만 고치면 되는 경우**였습니다.

#### `2 Line` — 보류

숫자로 시작하는 속성명은 [Stepper](syrup-stepper-components.md)의 `2 Line`과 **파일에서 단 둘뿐**입니다. Figma가 막지는 않지만 코드로 옮길 때 식별자로 쓸 수 없는 형태입니다.

두 페이지가 같은 이름을 쓰므로 **함께 정리하는 편**이 좋아 보류했습니다.

### 2. 두 variant의 구조가 다름

현재 `True`의 저장된 상하 Padding은 57이에요. 아래 Padding 0 기반 계산은 과거 점검 기록이며 현재 규격으로 복사하지 않아요. 두 variant 모두 높이가 FIXED이므로 문구 길이를 확인하고 유형을 선택해요.

| 항목 | `2 Line=True` | `2 Line=False` |
| --- | --- | --- |
| 레이아웃 방향 | **VERTICAL** | **HORIZONTAL** |
| 상하 Padding | **0** | **12** (`Spacing/300`) |
| 높이 | 62 (FIXED) | 44 (FIXED) |
| 아이콘 | **없음** | 있음 |

#### 여백을 만드는 방식이 둘로 갈립니다

| Variant | 계산 |
| --- | --- |
| `2 Line=False` | Padding 12 + 문구 19 + Padding 12 ≈ **44** |
| `2 Line=True` | Padding **0** + 문구 38 → 높이 **62로 고정**, 남는 24를 가운데 정렬로 분배 |

**두 결과 모두 상하 여백 12**로 같지만, 한쪽은 Padding으로 다른 쪽은 **고정 높이 + 가운데 정렬**로 만듭니다.

`2 Line=True`는 높이 62로 고정되어 있어 **문구가 3줄로 늘어나면 잘릴 수 있어요.** `False` 역시 높이 FIXED이므로 문구가 늘어나면 자동으로 안전하게 확장된다고 가정하지 않아요.

| 선택지 | 내용 |
| --- | --- |
| A | `True`도 Padding 12로 통일하고 높이 HUG — **문구 길이에 안전해짐** |
| B | 현행 유지 — 2줄 고정이 전제라면 |

**A를 권하지만 높이가 62 → 62(동일)로 계산돼 모양은 바뀌지 않을 가능성이 높습니다.** 다만 세로 정렬 방식이 바뀌므로 확인이 필요합니다.

#### 아이콘이 1줄에만 있습니다

`2 Line=True`에는 아이콘 레이어 자체가 없어, **2줄 토스트에서는 아이콘을 쓸 수 없습니다.**

| 해석 | 판단 |
| --- | --- |
| 2줄은 안내문 전용이라 아이콘을 쓰지 않음 | 의도 — 유지 |
| 아이콘이 필요한데 빠짐 | 추가 필요 |

[Text Button](syrup-text-button-components.md)의 `Underline=True`에 화살표가 없던 것, [Tab](syrup-tab-components.md)의 Rounded 아이콘 구조와 같은 유형입니다. 현재 사용 기준에서는 두 줄 조건 안내는 아이콘 없이 문구로 표현해요.

또한 레이아웃 방향이 다르면 **variant를 바꿀 때 오버라이드가 이어지지 않을 수 있습니다.**

### 3. 배경색 확인 — 2026-11-10

기존 MD의 색상 수치 `#222222` @80%는 맞게 기록되어 있었어요. 다만 배경을 `Color/Gray_100`에 바인딩했다고 적은 설명은 현재 직접 값 사용 방식에 맞춰 수정했어요.

- 현재 기준: **배경 채우기 `#222222`, 채우기 불투명도 80%, 레이어 전체 불투명도 100%**.
- 마스터 2개와 가이드라인·예제의 Toast 9개, 총 11개를 같은 값으로 통일하고 별도 조회로 확인했어요.
- `Color/Gray_100`의 RGB 자체는 `#222222`와 같아요. 그러나 이번 기준은 토큰 연결 없이 위 값을 직접 사용하는 방식이에요.
- `Color/Opacity_Black_100`은 **`#000000` · 75%**이므로 대체하지 않아요. 흰 배경에서 기존 Toast는 약 `#4E4E4E`, 이 토큰은 약 `#404040`으로 보여요.
- 투명도는 배경 채우기에만 적용해요. 텍스트와 아이콘까지 흐려지는 레이어 전체 불투명도 80%로 구현하지 않아요.
- 흰 배경 위 합성색 `#4E4E4E`를 불투명 배경값으로 저장하지 않아요. 실제 배경색에 따라 합성 결과가 달라져요.

과거 바인딩 과정에서 채우기 불투명도가 100%로 바뀐 기록이 있었어요. 앞으로도 색상뿐 아니라 채우기 불투명도·토큰 연결을 함께 확인해요. 특정 API가 항상 투명도를 바꾼다고 일반화하지 않아요.

### 4. 레이어명이 내용과 전혀 다름 — ✅ 완료 (2건)

| 변경 전 | 실제 내용 | 변경 후 |
| --- | --- | --- |
| **`2022년 3월 21일 Syrup 혜…`** | 「광고 누르고, 광고 페이지에서 5초 이상 …」 | **`Message`** ✅ |
| **`2022년 3월 21일 Syrup 혜…`** | 「3금을 적립 받았어요!」 | **`Message`** ✅ |

두 variant의 **유일한 텍스트 레이어** 이름이 「2022년 3월 21일 Syrup 혜택…」으로, **실제 문구와 아무 관련이 없었습니다.**

다른 화면에서 복제해 오면서 이름이 그대로 남은 것으로 보입니다. [Text Field](syrup-text-field-components.md)의 `총 보유 SCON Credit`(Text Area 본문인데 내용은 「자유롭게 의견을 작성해…」)와 **같은 유형**입니다.

역할 이름 `Message`로 바꿔 **문구가 바뀌어도 어긋나지 않습니다.**

### 5. `Gold` 아이콘 비율

| Variant | 자식 크기 | 프레임 대비 |
| --- | --- | --- |
| `Firecracker` | **20 × 20** | 꽉 참 |
| `Gold` | **20 × 10** | **세로 절반** (y 5로 가운데) |

두 아이콘이 같은 20 × 20 프레임을 쓰는데 내용 높이가 다릅니다. 원본 에셋의 비율 차이로 보이며, **세로 가운데 정렬로 처리**돼 있어 화면상 문제는 없습니다.

다만 `Firecracker`와 나란히 놓으면 **금 아이콘이 상대적으로 작아 보입니다.** 의도인지, 에셋을 20 × 20에 맞춰 다시 만들지 판단이 필요합니다.

[Badge](syrup-badge-components.md)에서 **원본 아이콘 크기를 맞춰 축소 지정을 없앤 선례**가 있습니다.

### 6. 인스턴스 현황 — 과거 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Toast` | **0** |
| `Toast / Icon / Image` | 1 (Toast 내부) |

토스트는 **화면 위에 잠시 떠올랐다 사라지는 요소**라 정적인 컴포넌트 보드에 배치할 일이 거의 없습니다. [Loader](syrup-loader-components.md) · [Dim](syrup-dim-components.md)과 같은 성격입니다.

위 0건은 과거 집계예요. 현재는 가이드라인·Usage에 Toast 인스턴스 9개가 있으므로 구조 변경의 영향이 없다고 해석하지 않아요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 이번 업데이트 (2026-11-10)

가이드라인 3개·Usage A~C와 연결 링크를 추가하고, 배경을 `#222222` · 80% 직접 값으로 통일했어요. Section 1은 현재 페이지에서 제거된 상태이며, 원본 화면을 재생성하지 않았어요.

### ✅ 완료 (2026-11-02)

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | 배경색 → `Color/Gray_100` ([3](#3-배경색-확인--2026-11-10)) | 2건 · **투명도 80% 복구 필요했음** |
| 2 | 레이어명 → `Message` ([4](#4-레이어명이-내용과-전혀-다름---완료-2건)) | 2건 |
| 3 | `Property 1` → `Icon` ([1](#1-속성명-2건---1건-완료)) | 1건 |

위 내용은 당시 정리 기록이에요. 현재 배경은 직접 값으로 사용하므로 미바인딩 0건이라는 설명을 현재 상태에 적용하지 않아요.

> **1번은 한 번에 끝나지 않았습니다.** `setBoundVariableForPaint`가 채움의 투명도를 80% → 100%로 떨어뜨려, 투명도를 다시 넣어 복구했습니다. 자세한 내용은 [배경색 확인](#3-배경색-확인--2026-11-10)에 적었습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `2 Line` → `Two Line` ([1](#1-속성명-2건---1건-완료)) | **Stepper와 함께 판단** | 낮음 |
| 2 | `2 Line=True`의 Padding·높이 처리 ([2](#2-두-variant의-구조가-다름)) | **구조 통일 — 확인 필요** | 중간 |
| 3 | 2줄에 아이콘 추가 여부 ([2](#2-두-variant의-구조가-다름)) | **의도 확인 필요** | 중간 |
| 4 | `Gold` 아이콘 비율 ([5](#5-gold-아이콘-비율)) | 에셋 판단 | 낮음 |
| — | 투명도 80% 토큰화 ([3](#3-배경색-확인--2026-11-10)) | 스케일 신설 — 보류 | — |

배경의 직접 값 사용은 이번에 정한 기준이에요. 나머지 과거 토큰 점검 수치를 현재 페이지 전체 재점검 결과로 해석하지 않아요.

가장 실질적인 사안은 **[점검 2의 구조 불일치](#2-두-variant의-구조가-다름)** 입니다. 두 variant가 레이아웃 방향 · 여백 방식 · 아이콘 유무에서 모두 달라, `2 Line=True`는 **문구가 3줄로 늘어나면 잘립니다.** 2줄 고정이 전제인지 확인이 필요합니다.
