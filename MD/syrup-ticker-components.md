# Syrup Design System — Ticker 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Ticker` 페이지 → [`Ticker` 섹션 `10664:5817`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10664-5817) |
| 섹션 크기 | 1440 × 1218 |
| 컴포넌트 수 | **3개** |
| Variant 총수 | **4개** (1 · 2 · 1) |
| 기준일 | 2026-11-10 (가이드라인 2개·Usage A~C 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **짧은 정보를 한정된 영역에서 순차적으로 보여주는 컴포넌트에요.**
> 당첨 후기나 실시간 정보처럼 여러 내용을 흐르거나 전환하며 지속적으로 보여줄 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Ticker / Flip](#1-ticker--flip)
3. [Ticker / Marquee / Inline](#2-ticker--marquee--inline)
4. [Ticker / Marquee / Card](#3-ticker--marquee--card)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)
10. [정리 우선순위](#정리-우선순위)
11. [Figma Make 프로토타입](#figma-make-프로토타입)

---

## 구성 한눈에 보기

마스터 섹션(1440 × 1218)과 Guidelines, Usage, Section 1로 구성해요. 기존 노드 68개·텍스트 35개 및 아래 인스턴스 0건은 2026-10-12의 마스터 보드 점검 기록이며, 새 사용 화면과 가이드라인·예제를 포함한 현재 페이지 전체 집계가 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 580) | 컴포넌트 3종 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Ticker / Flip` | Component | — | 360 × 36 | **0** |
| 2 | `Ticker / Marquee / Inline` | Set 2 | **`Property 1`** | 360 × 50 | **0** |
| 3 | `Ticker / Marquee / Card` | Component | — | 806 × 142 | **0** |

### 세 가지 노출 방식

| 컴포넌트 | 방식 | 생김새 |
| --- | --- | --- |
| `Flip` | 위아래로 넘김 | 한 줄 · 높이 36 · 연보라 배경 |
| `Marquee / Inline` | 가로로 흐름 | 한 줄 내용과 반복 연결용 Row 2 · 높이 50 · 파스텔 블루 배경 |
| `Marquee / Card` | 카드가 가로로 흐름 | M 카드 4장 · 높이 142 고정 |

섹션명이 `Tiker` 오타였고 `Ticker`로 수정됐습니다 ✅ → [점검 1](#1-섹션명-tiker-오타---완료)

---

## 1. Ticker / Flip

**Node** `10664:5908` · Component · **360 × 36** · 속성 없음

가로 오토레이아웃 CENTER / CENTER · Padding `9 / 16 / 9 / 16` (좌우 `Spacing/400` ✅ · **상하 9 미바인딩**) · Gap 8 (`Spacing/200` ✅)
배경 **`#EAEAFF`** (미바인딩)

| 레이어 | 타입 | 내용 |
| --- | --- | --- |
| `Leading` | Frame | Gap 2 (`Spacing/50` ✅) |
| └ `Emoji` | Text | 13 Regular `b500_13_regular` ✅ · `Color/Gray_200` ✅ |
| └ `Highlight` | Text | 12 **Bold** · **`#694ACF`** · **스타일 미적용** |
| `Nickname` | Text | 12 Regular · `Color/Gray_200` ✅ · **스타일 미적용** |
| `Review` | Text | 12 Regular · `Color/Gray_200` ✅ · **스타일 미적용** |

텍스트 3개가 모두 **스타일 없이 외부 타이포 변수에 묶여** 있습니다 → [점검 3](#3-외부-타이포-변수-15건--60개-바인딩)

레이어명이 텍스트 내용 그대로였고, 역할 이름으로 정리했습니다 ✅ → [점검 8](#8-레이어명-정리---완료-29건)

---

## 2. Ticker / Marquee / Inline

**Node** `10664:5850` · Component Set · **2 variants** · **360 × 50**

| Property | Options |
| --- | --- |
| **`Property 1`** | **`Default` · `Variant2`** |

**Figma 자동 생성명 그대로**입니다 → [점검 2](#2-property-1--variant2-자동-생성명)

배경 `Color/Third_Pastel_Blue` ✅

| Variant | 오토레이아웃 | Padding | Gap |
| --- | --- | --- | --- |
| `Default` | **가로 MIN / MIN** | `16 / 12 / 16 / 12` | 20 |
| **`Variant2`** | **없음** | — | — |

**두 variant는 흐름의 시작·이동 후 위치를 표현하며 레이아웃 방식이 달라요.** → [점검 4](#4-variant2에-오토레이아웃이-없음)

### 가로 흐름을 위해 같은 내용을 두 번 배치해요

| 레이어 | 내용 |
| --- | --- |
| `Row 1` | `Leading`(`Emoji` + `Nickname`) + `Highlight` + `Review` |
| `Row 2` | **위와 완전히 동일** |

가로로 흐르는 마퀴 효과를 위해 **같은 줄을 두 번 배치**한 구조입니다. 현재 프로토타입은 Default → Variant2로 5초 LINEAR Smart Animate 후 즉시 Default로 돌아가도록 연결되어 있어요. Row 1과 Row 2는 화면에 두 줄로 쌓는 용도가 아니에요.

### Padding·Gap이 외부 변수에 묶여 있습니다

| 항목 | 바인딩 |
| --- | --- |
| Padding 16 / 12 | ~~`[외부] spacing/spacing_400` · `spacing_300`~~ → **로컬 `Spacing/400` · `Spacing/300`** ✅ |
| Gap 20 · 8 · 2 | ~~`[외부] spacing/*`~~ → **로컬 `Spacing/500` · `200` · `50`** ✅ |

같은 페이지의 `Flip`과 `Card`는 로컬 `Spacing/*`를 쓰는데 `Inline`만 외부였고, 로컬로 교체했습니다 ✅ → [점검 5](#5-외부-spacing-변수-18건---완료)

---

## 3. Ticker / Marquee / Card

**Node** `10664:5915` · Component · **806 × 142 고정** · 상위 컴포넌트 속성 없음 (2026-11-25 확인)

가로 오토레이아웃 · Padding 0 · Gap 10 (`Spacing/250`) · 라운드 12 (`Corner radius/300`)

| 레이어 | 건수 | 내용 |
| --- | --- | --- |
| 후기 아이템 (현재 세트 이름 `Grid Scroll`) | 4 | **Size=M · 194 × 142 고정** · `Color/Third_Pastel_Blue` · 라운드 8 |

- 후기 아이템 세트 `12450:4229`에서 M 원본 `12450:4230`을 사용해요. 기존 문서의 `Grid Scroll / Scroll Item / Review`와 같은 후기 아이템 계열이에요.
- 현재 네 아이템 `10664:5916`~`10664:5919`는 모두 `Size=M`이에요. 전체 길이는 194 × 4 + 10 × 3 = 806이에요. 이 길이는 가로로 흐를 콘텐츠 길이이며 화면의 표시 폭이 아니에요.
- 테스트 후기 4개는 공백·문장부호 포함 각 100자이며 실제 당첨자 인용이 아니에요.
- M 본문은 폭 170, Pretendard 13 Regular / 행간 16, 최대 7줄(112), 초과 끝 말줄임이에요. 사방 패딩 12와 닉네임·당첨일 구성을 유지해요. S는 142 × 110, 폭 118·최대 4줄의 기존 소형 규격이에요.
- **금한돈 당첨 후기** 작성 조건이 **최소 50자·최대 100자**로 바뀌면서 최대 100자를 표시할 목적으로 M을 추가했어요. 입력 최소·최대 검증과 표시 최대 7줄은 별도 기준이에요. 수동 줄바꿈 등으로 줄 수가 넘으면 말줄임이 적용될 수 있어요.
- `Grid Scroll / Winner` 묶음은 현재 서비스에서 사용하지 않아요. 현재 후기 표시는 Ticker 안에서 M 아이템으로 구성하며, 기존 S·110 높이를 그대로 적용하지 않아요.
- 현재 100자 테스트 후기 4개는 모두 6줄이에요. 카드 높이는 문구 길이에 관계없이 142를 유지하고 내부 Ticker는 806 × 142로 구성해요. 최신 피그마 M 원본은 높이 142·FIXED로 확인했으며 자동 높이를 사용 기준으로 적용하지 않아요. 웹 등의 별도 표시 창은 화면 폭에 맞춰 Clip하고, 높이는 M 카드가 잘리지 않도록 142를 확보해요. 과거 문서의 312 × 110 표시 창 높이는 현재 M에 사용하지 않아요.

> 2026-11-25 갱신: 금한돈 당첨 후기 최소 50자·최대 100자 및 후기 아이템 Size=M 반영. 아래 과거 점검 기록의 규격·건수는 당시 기준이에요.

## 웹 예제의 드래그 동작 (2026-11-25)

Inline·Card는 자동으로 흐르다가 마우스·터치·펜 드래그 시 현재 위치에서 정지하고, 손의 이동에 따라 실제 콘텐츠 위치가 바뀌어요. 드래그를 놓은 뒤 2초 후 해당 위치에서 자동 흐름을 이어가요. 일시정지 버튼·모션 줄이기·비활성 탭에서는 자동 재생하지 않아요. Flip에는 드래그를 적용하지 않아요. 이는 웹/React 예제의 동작이며 Figma 이미지가 직접 재생되는 것은 아니에요. React 다운로드의 useMarqueeDrag.ts·marquee-drag.js·타입 선언을 함께 사용해요.

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2005)

### 1. 정보의 양과 보여주는 방식에 맞는 유형을 사용해요

한 항목씩 간결하게 보여줄 때는 Flip, 한 줄 내용을 가로로 이어 보여줄 때는 Marquee / Inline을 사용해요.
닉네임·당첨 정보·후기를 함께 구성해 어떤 내용인지 알 수 있도록 해요.

- 비교: Flip · 한 항목 안내 / Marquee / Inline · 한 줄 흐름
- [가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2007)

### 2. 표시 영역 안에서 내용이 이어지도록 구성해요

후기를 여러 줄로 보여줄 때는 Marquee / Card를 사용해요. 카드의 닉네임·당첨일·본문 구성을 유지하고, 현재 금한돈 당첨 후기는 Size=M(194 × 142, 본문 최대 7줄)을 사용해요.
한 줄 유형은 줄바꿈으로 높이를 늘리지 않고, 가로로 이어지는 내용은 표시 영역 밖으로 넘치지 않도록 처리해요.

- 비교: Inline · 한 줄 표시 영역 / Card · 여러 줄 후기
- [가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2049)

---

### 3. 후기의 길이와 사용 목적에 맞는 크기를 선택해요

짧은 후기 요약은 S, 최대 100자의 금한돈 당첨 후기는 M을 사용해요. 금한돈 당첨 후기 티커는 글자 수와 관계없이 M으로 통일하고, 내용이 짧아도 카드 높이 142를 유지해요.

실제 S(142×110)·M(194×142) 인스턴스를 나란히 비교해요. 두 크기는 고정 높이를 유지하며, 같은 금한돈 당첨 후기 티커 안에서 글자 수에 따라 S와 M을 섞지 않아요.

- [Figma 가이드라인](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12478-514)
- [D. 후기 크기 비교 · S / M](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=12478-563)

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2006)

| 예제 | 설명 | 구성 | 링크 |
| --- | --- | --- | --- |
| A. 당첨 소식 요약 | 닉네임과 당첨 소식, 후기 일부를 짧게 보여줘요. Flip을 사용해 한 항목을 한 줄로 구성해요. | `Ticker / Flip` · 360 × 36 | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2106) |
| B. 한 줄 후기 흐름 | 닉네임·당첨 정보·후기를 한 줄로 이어 보여줘요. Marquee / Inline으로 표시 영역 안에서 내용이 가로로 흐르게 해요. | `Ticker / Marquee / Inline` · Default · 360 × 50 | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2124) |
| C. 카드형 후기 흐름 | 닉네임과 당첨일, 여러 줄 후기를 카드에 담아 보여줘요. Marquee / Card로 여러 후기를 가로로 이어 구성해요. | `Ticker / Marquee / Card` · Size=M · 높이 142 고정 | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11784-2149) |

## 예제 레이아웃과 AI 사용 기준

- Guidelines 섹션은 960 × 748, Usage 섹션은 1360 × 426이에요. 기존 섹션과 동일한 흰 배경·모서리 24를 사용해요.
- Slot은 폭 360, 패딩 0, 좌측·상단 정렬, 높이 Hug로 구성했어요. 별도 ‘화면’ 래퍼 없이 Ticker 인스턴스를 직접 배치해요.
- 제목·설명 영역 끝과 Slot 사이는 50이에요. Usage의 설명 높이를 맞춰 세 예제가 같은 높이에서 시작해요.
- Flip과 Inline은 폭 360을 유지해요. Card 예제는 Section 1의 표시 폭 312를 유지하고 인스턴스에 Clip content를 적용했어요.
- Card는 194 × 142 고정 M 카드 4개를 간격 10으로 담아 806 × 142로 구성해요. 문구가 짧아도 높이를 줄이지 않아요. 화면별 표시 폭과 가로 반복 콘텐츠 길이를 구분하고, M을 S 폭으로 일괄 축소하지 않아요.
- Card 예제의 오른쪽에 다음 카드 일부가 보이는 것은 이어지는 내용을 보여주는 구성이에요. 모든 카드를 정적인 예제 한 화면에 맞춰 넣지 않아요.
- Slot 바깥으로 콘텐츠가 흘러 인접 예제를 가리지 않도록 Ticker 표시 영역에서 처리해요. 마스터의 Clip content 설정은 이번에 변경하지 않았어요.
- Inline의 Row 1 / Row 2는 반복 흐름을 위한 같은 내용이에요. 두 줄짜리 레이아웃이나 서로 다른 데이터 유형으로 해석하지 않아요.
- Inline은 Default에서 Variant2로 5초 LINEAR Smart Animate 후 즉시 복귀하는 기존 연결을 보존했어요. 이는 현재 Inline 프로토타입의 설정이며 다른 유형의 공통 속도로 확대하지 않아요.
- Flip과 Card는 현재 Design 마스터에 직접 연결된 전환이 없어요. 사용 목적을 소개하는 정적 예제이며 애니메이션 구현이 새로 완료되었다는 뜻은 아니에요. Flip의 별도 Make 기록은 아래에 유지했어요.
- 닉네임·당첨 금액·당첨일·후기 내용은 교체 가능한 샘플이에요. 샘플 문구를 고정 운영 규칙으로 사용하지 않아요.
- Section 1의 아노테이션 9개를 제거하고 잔여 0개를 확인했어요.

---

## 설계 규칙 요약

> 이 절의 토큰·스타일·외부 바인딩 건수는 2026-10-12 점검 기록이에요. 이번 작업은 사용 문서 추가이며 전체 토큰 재점검 결과가 아니에요.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 텍스트 색 | `Color/Gray_200` ✅ — **`#694ACF` · `#1F80FF` 미바인딩** |
| 배경 | `Color/Third_Pastel_Blue` ✅ — **`#EAEAFF` 미바인딩** |
| Padding · Gap | **전량 로컬 `Spacing/*`** ✅ — `Flip` 상하 9만 미바인딩 |
| 라운드 | **전량 바인딩** ✅ (`Corner radius/200` · `300`) |
| 텍스트 스타일 | `b500_13_regular` 5건만 ✅ — **미적용 15건** |
| **외부 타이포 변수** | **60개 바인딩 / 15개 노드** |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

**이 페이지는 토큰 정리가 가장 덜 된 축입니다.** 35개 텍스트 중 20개만 토큰 스타일을 쓰고, 나머지 15개는 **외부 라이브러리 변수에 직접 묶여** 있습니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Grid Scroll](syrup-grid-scroll-components.md) | `Grid Scroll / Scroll Item / Review` | **4** |
| ❖System Components | `Title Bar` 1 · `Section Header` 1 | 2 |

외부 라이브러리 **인스턴스**는 0건이지만, **외부 변수 바인딩 78건은 과거 점검 기록**이에요. 현재 전체 건수로 해석하지 않아요.

---

## 점검 필요 사항

> 아래 구조·네이밍·토큰 제안은 과거 점검 기록이에요. 현재 확인된 Inline 전환 구조와 새 사용 기준은 가이드라인 및 애니메이션 해석 항목을 우선해요.

### 1. 섹션명 `Tiker` 오타 — ✅ 완료

| 항목 | 값 |
| --- | --- |
| 페이지명 | `Ticker` |
| 섹션명 | ~~`Tiker`~~ → **`Ticker`** ✅ |
| 컴포넌트명 | `Ticker / *` |

**`c`가 빠진 오타**였고 사용자가 수정했습니다.

[Stepper](syrup-stepper-components.md)의 `Desription`, [Search Field](syrup-search-field-components.md)의 `btn_serach`, [Tab](syrup-tab-components.md)의 `tilte`와 같은 성격입니다.

### 2. `Property 1` = `Variant2` 자동 생성명

```
Property 1 = Default | Variant2
```

**속성명과 값 모두 Figma가 자동으로 붙인 이름**입니다. [Swipe](syrup-swipe-components.md)에서 같은 문제를 `State = Default · Dragging · Near Complete · Expired`로 정리한 적이 있습니다.

두 variant는 같은 내용을 사용하지만 **Row의 가로 위치와 레이아웃 방식이 달라요**. Default는 x=12 / 367, Variant2는 x=-343 / 12로 이동하고 두 상태가 전환으로 연결되어 있어요 → [점검 4](#4-variant2에-오토레이아웃이-없음)

| 선택지 | 내용 |
| --- | --- |
| A | `Variant2`를 삭제 — 내용이 같고 레이아웃만 깨진 상태라면 |
| B | 역할을 확인해 `State` · `Layout` 등으로 개명 |

2026-11-10 확인 결과 `Variant2`는 가로 이동 후 상태로 사용되고 있어요. 내용이 같다는 이유로 삭제하거나 자동 레이아웃으로 바꾸지 않아요. 현재 사용 화면과 가이드라인·예제에 인스턴스가 있으므로 변경 영향도 함께 확인해야 해요.

### 3. 외부 타이포 변수 15건 — 60개 바인딩

이 페이지의 **가장 큰 사안**입니다.

| 외부 변수 | 바인딩 수 |
| --- | --- |
| `fontSize/1` | 15 |
| `fontFamilies/pretendard` | 15 |
| `letterSpacing/3` | 15 |
| `fontWeights/fontweight-400` | 10 |
| `fontWeights/fontweight-700` | 5 |
| **합계** | **60개 / 15개 노드** |

15개 노드는 **전부 12px 텍스트**이고, **스타일 미적용 15건과 정확히 같은 노드**입니다.

| 크기/굵기 | 건수 |
| --- | --- |
| 12 Regular | 10 |
| 12 Bold | 5 |

#### 이것이 앞서 기록한 "18개 노드"의 실체입니다

[Progress Stepper](syrup-progress-stepper-components.md) 문서에 **"텍스트 스타일 없이 외부 타이포 변수만 바인딩된 18개 노드"**를 기록해 뒀는데, 그중 **Ticker가 15건**으로 대부분입니다.

| 페이지 | 건수 |
| --- | --- |
| **Ticker** | **15** |
| [Bottom Info](syrup-bottom-info-components.md) | 2 |
| [List Header](syrup-list-header-components.md) | 1 |

#### 왜 문제인가

| 영향 | 설명 |
| --- | --- |
| 외부 라이브러리 의존 | 라이브러리가 바뀌면 이 파일의 글자가 따라 흔들림 |
| 토큰 체계 이탈 | 파일의 텍스트 스타일(`c100_12_regular` 등)을 쓰지 않음 |
| 추적 어려움 | 스타일 패널에 아무것도 표시되지 않음 |

12px에는 **`c100_12_regular` 토큰이 있습니다.** 12 Regular 10건은 바로 적용 가능합니다.

12 Bold 5건은 **토큰이 없어** [Grid List](syrup-grid-list-components.md) · [Progress Stepper](syrup-progress-stepper-components.md)에서 보류한 `12 Bold` 토큰화 건과 함께 판단해야 합니다.

> **주의** — 텍스트 스타일을 적용해도 **외부 변수 바인딩은 자동으로 풀리지 않습니다.** [Card](syrup-card-components.md)에서 `typeset_xs_bold` 스타일을 떼어낸 뒤 외부 변수 10건이 남아 있던 일이 있었습니다. **스타일 적용 + 변수 해제를 함께** 해야 합니다.

### 4. `Variant2`에 오토레이아웃이 없음

| Variant | 레이아웃 | Padding | Gap |
| --- | --- | --- | --- |
| `Default` | **가로 MIN / MIN** | `16 / 12 / 16 / 12` | 20 |
| `Variant2` | **없음** (절대 배치) | — | — |

반복되는 내용은 두 variant가 같고 크기는 모두 360 × 50이에요. 다만 Row의 가로 위치가 달라 이동 전후 상태를 표현해요. 현재 레이어명은 `Row 1` · `Row 2`예요.

| 해석 | 판단 |
| --- | --- |
| 애니메이션 중간 상태를 절대 배치로 표현 | 의도 — 유지 |
| 오토레이아웃을 실수로 해제 | 복구 필요 |
| 쓰이지 않는 잔존 variant | 삭제 대상 |

2026-11-10에는 두 variant의 Row 위치 변경과 CHANGE_TO 연결을 확인했어요. 절대 배치가 있다는 이유만으로 레이아웃 오류로 판단하지 않아요. 속성명을 정리하더라도 전환 대상과 반복 연결을 보존해야 해요.

### 5. 외부 spacing 변수 18건 — ✅ 완료

`Ticker / Marquee / Inline`의 Padding·Gap이 **외부 라이브러리 변수**에 묶여 있었습니다.

| 변경 전 (외부) | 변경 후 (로컬) | 건수 |
| --- | --- | --- |
| `spacing/spacing_400` | `Spacing/400` | 4 |
| `spacing/spacing_300` | `Spacing/300` | 4 |
| `spacing/spacing_200` | `Spacing/200` | 4 |
| `spacing/spacing_50` | `Spacing/50` | 4 |
| `spacing/spacing_500` | `Spacing/500` | 1 |
| `spacing/spacing_100` | `Spacing/100` | 1 |
| **합계** | | **18** |

같은 페이지의 `Flip`·`Card`는 로컬을 쓰는데 `Inline`만 체계가 달랐습니다.

**교체 전 토큰 값이 같은지 하나씩 대조했고**(예: 외부 `spacing_400`=16, 로컬 `Spacing/400`=16), 값이 다르면 건너뛰도록 했습니다. 보류된 건은 없습니다.

보드 영역의 `Spec docs/margin` 2건은 컴포넌트가 아니라 제외했습니다.

[Search Field](syrup-search-field-components.md)에서 외부 `color/third_pastel_coral`을 로컬로 교체한 것과 같은 방식입니다.

### 6. 라운드 12 미바인딩 1건 — ✅ 완료

| 컴포넌트 | 라운드 | 토큰 |
| --- | --- | --- |
| `Ticker / Marquee / Card` | 12 | **`Corner radius/300` = 12** ✅ |

값이 같은 토큰이 있는데 묶여 있지 않았습니다. **토큰 값이 12인지 확인한 뒤** 바인딩했고, 모양은 바뀌지 않았습니다.

### 7. 미바인딩 색상 3종

| 색 | 건수 | 위치 | 성격 |
| --- | --- | --- | --- |
| **`#1F80FF`** | 4 | `Inline` ▸ 「100만금 당첨」 | **[Card](syrup-card-components.md) 6건 · [Progress Stepper](syrup-progress-stepper-components.md) 8건과 같은 색** |
| `#EAEAFF` | 1 | `Flip` 배경 | 연보라 |
| `#694ACF` | 1 | `Flip` ▸ 「금한돈 당첨」 | 보라 |

#### `#1F80FF`가 파일 전체로 번지고 있습니다

| 페이지 | 건수 |
| --- | --- |
| [Progress Stepper](syrup-progress-stepper-components.md) | 8 |
| [Card](syrup-card-components.md) | 6 |
| **Ticker** | **4** |
| **합계** | **18건 이상** |

세 페이지에 걸쳐 **18건 이상** 쓰이는데 토큰이 없습니다. **토큰 신설을 진지하게 검토할 단계**입니다.

`#EAEAFF` · `#694ACF`는 `Flip` 전용 보라 계열로, 각 1건씩이라 도메인 색으로 두는 쪽이 무난합니다.

### 8. 레이어명 정리 — ✅ 완료 (29건)

| 변경 전 | 변경 후 | 건수 | 근거 |
| --- | --- | --- | --- |
| `Frame 1171276927` | **`Leading`** | 5 | 이모지 + 앞 텍스트 묶음 |
| `🎉` | **`Emoji`** | 5 | 이모지 하나가 이름 |
| `조*주님` | **`Nickname`** | 5 | 샘플 데이터가 이름 |
| `진짜 제가 당첨될 줄…` | **`Review`** | 5 | 문장 전체가 이름 |
| `100만금 당첨` | **`Highlight`** | 4 | 강조 문구 |
| `Frame 3468158` · `Frame 3468159` | **`Row 1`** · **`Row 2`** | 2 · 2 | 마퀴 반복 줄 |
| `금한돈 당첨` | **`Highlight`** | 1 | 강조 문구 |

**텍스트 내용이 그대로 레이어명**이던 것을 역할 이름으로 바꿨습니다. [Text Field](syrup-text-field-components.md)의 `970303` · `총 보유 SCON Credit`과 같은 유형이었습니다.

정리 후 **기본 이름 0건**입니다.

`Highlight`는 `Flip`의 「금한돈 당첨」과 `Inline`의 「100만금 당첨」이 같은 역할(색이 다른 강조 문구)이라 한 이름으로 묶었습니다.

### 9. 인스턴스 현황 — 과거 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Ticker / Flip` · `Marquee / Inline` · `Marquee / Card` | **전부 0** |

티커는 **화면 상단이나 목록 사이에 끼워 넣는 요소**라 다른 컴포넌트 보드에 들어갈 일이 적습니다.

위 0건은 과거 집계예요. 현재 Section 1에 유형별 인스턴스 3개, Guidelines에 4개, Usage에 3개가 있으므로 개명·구조 변경의 영향이 없다고 해석하지 않아요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 이번 업데이트 (2026-11-10)

가이드라인 2개와 Usage A~C, 유형 선택·표시 영역·반복 구조의 해석 기준 및 Figma 링크를 추가했어요. Section 1의 아노테이션 9개를 제거했고, 마스터와 기존 프로토타입 연결은 변경하지 않았어요. 과거 인스턴스 0건과 Variant2 삭제 가능성에 대한 설명도 현재 확인 결과에 맞춰 보완했어요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **48건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | 섹션명 `Tiker` → `Ticker` ([1](#1-섹션명-tiker-오타---완료)) | **사용자 직접 처리** |
| 2 | 라운드 12 → `Corner radius/300` ([6](#6-라운드-12-미바인딩-1건---완료)) | 1건 |
| 3 | 외부 `spacing/*` → 로컬 `Spacing/*` ([5](#5-외부-spacing-변수-18건---완료)) | **18건** |
| 4 | 레이어명 정리 ([8](#8-레이어명-정리---완료-29건)) | **29건** |

정리 후 **기본 이름 0건 · 외부 spacing 변수 0건 · 미바인딩 라운드 0건**입니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | 12 Regular → `c100_12_regular` 10건 ([3](#3-외부-타이포-변수-15건--60개-바인딩)) | **스타일 적용 + 변수 해제** | 중간 |
| 2 | 12 Bold 5건 ([3](#3-외부-타이포-변수-15건--60개-바인딩)) | **토큰 신설 판단 — Grid List와 함께** | 중간 |
| 3 | `Property 1` · `Variant2` ([2](#2-property-1--variant2-자동-생성명) · [4](#4-variant2에-오토레이아웃이-없음)) | **전환 구조 보존 후 네이밍 판단** | 낮음 |
| 4 | `#1F80FF` 토큰 신설 ([7](#7-미바인딩-색상-3종)) | **파일 전체 18건 — 함께 판단** | 중간 |
| 5 | `Flip` 상하 Padding 9 | 토큰 없음 | — |

남은 핵심은 **[점검 3의 외부 타이포 변수 15건](#3-외부-타이포-변수-15건--60개-바인딩)** 입니다. 파일 전체 18건 중 15건이 여기 몰려 있어, 정리하면 **파일 전체의 외부 타이포 의존이 대부분 해소**됩니다.

다만 **스타일을 적용해도 외부 변수는 자동으로 풀리지 않으므로**([Card](syrup-card-components.md) 선례), 두 작업을 함께 해야 합니다.

---

## Figma Make 프로토타입

> 기존 문서에 기록된 별도 프로토타입 정보예요. 이번 업데이트에서는 해당 Make 파일의 코드·타이밍을 다시 검증하지 않았어요. 아래 수치를 Ticker 전체의 공통 재생 규칙으로 적용하지 않아요.

`Ticker / Flip`의 동작은 **Figma Make 프로토타입**으로 구현돼 있습니다.

| 항목 | 값 |
| --- | --- |
| 이름 | **3D Flip Transition Text** |
| URL | [figma.com/make/iyTQEEOFTp8qms3TPNsAYU](https://www.figma.com/make/iyTQEEOFTp8qms3TPNsAYU/3D-Flip-Transition-Text) |
| 스택 | React 19 · Vite 8 · Tailwind CSS v4 · TypeScript 5.7 |
| 핵심 파일 | `src/ReviewFlipBanner.tsx` (272줄) · `src/App.tsx` |
| 폰트 | Pretendard **Bold(700)** · **Regular(400)** woff2 — `@font-face`로 직접 로드 |

### 컴포넌트 API

```ts
type ReviewItem = {
  name: string        // 「조*주님」
  highlight?: string  // 「금한돈 당첨」
  review: string      // 「진짜 제가 당첨될 줄 몰랐는데 너무 좋아요...」
}

type ReviewFlipBannerProps = {
  items: ReviewItem[]
  intervalMs?: number     // 기본 2500 — 전환 주기
  durationMs?: number     // 기본 450  — 전환 길이
  rotationDeg?: number    // 기본 70   — X축 회전 각도
  perspectivePx?: number  // 기본 500  — 원근 깊이
  className?: string
  style?: React.CSSProperties
}
```

### 전환 타이밍

```
0.45초 플립  →  약 2.05초 정지  →  다음 항목
└──────────── 2.5초 주기 ────────────┘
```

| 값 | 설정 |
| --- | --- |
| `intervalMs` | **2500** (`setInterval`) |
| `durationMs` | **450** (`setTimeout`) |
| 정지 시간 | 2500 − 450 = **2050ms** |
| 이징 | **`cubic-bezier(0.4, 0, 0.2, 1)`** (transform · opacity 동일) |

### 3D 플립 구조

두 슬롯이 **항상 겹쳐 렌더링**되고 transform·opacity만 바뀝니다.

| 슬롯 | `idle` | `flipping` |
| --- | --- | --- |
| **현재** (`zIndex: 2`) | `translateY(0) rotateX(0deg)` · opacity **1** | `translateY(-5px) rotateX(70deg)` · opacity **0** |
| **다음** (`zIndex: 1`) | `translateY(5px) rotateX(-70deg)` · opacity **0** | `translateY(0) rotateX(0deg)` · opacity **1** |

현재 항목은 **위로 밀리며 뒤로 눕고**, 다음 항목은 **아래에서 올라오며 정면을 향합니다.**

| 속성 | 값 |
| --- | --- |
| 컨테이너 | `perspective: 500px` · `overflow: hidden` |
| 각 슬롯 | `transformStyle: preserve-3d` · `transformOrigin: 50% 50%` |
| | `backfaceVisibility: hidden` · `willChange: transform, opacity` |
| | `pointerEvents: none` |

### 3단계 phase — 깜빡임을 막는 장치

```
idle  →  flipping  →  settling  →  idle
         (450ms)      (2 프레임)
```

| Phase | 하는 일 |
| --- | --- |
| `idle` | 정지 |
| `flipping` | 두 슬롯이 transform·opacity 전환 |
| **`settling`** | **인덱스를 올리고 `transition: none`으로 즉시 리셋** |

> **개발 중 실제로 겪은 문제입니다.** 처음에는 `isAnimating` 불리언 하나로 만들었는데, 전환이 끝나는 순간 **인덱스 증가와 플래그 해제가 같은 렌더에 묶여** 「다음」 슬롯이 새 내용으로 바뀌면서 transform·opacity 리셋까지 애니메이션돼 **깜빡임**이 생겼습니다.
>
> `settling` 단계에서 **transition을 꺼 리셋을 즉시 적용**하고, `requestAnimationFrame` 2번 뒤 `idle`로 돌아가는 방식으로 해결했습니다.

### 컨테이너 스펙 — Figma와 대조

| 항목 | Figma `Ticker / Flip` | Figma Make | 일치 |
| --- | --- | --- | --- |
| 높이 | **36** | `height: 36` | ✅ |
| 좌우 패딩 | **16** (`Spacing/400`) | `paddingLeft/Right: 16` | ✅ |
| 배경 | **`#EAEAFF`** (미바인딩) | `backgroundColor: "#EAEAFF"` | ✅ |
| 폭 | 360 (고정) | `width: "100%"` | 반응형으로 구현 |
| 상하 패딩 | **9** (미바인딩) | 없음 — `height: 36` + 세로 가운데 정렬 | 방식 다름 |

Figma가 **상하 Padding 9로 높이를 만든** 반면, Make는 **높이 36을 고정하고 가운데 정렬**로 같은 결과를 냅니다. [점검 6](#6-라운드-12-미바인딩-1건---완료)에서 Padding 9를 "토큰 없음"으로 남겨뒀는데, **구현에서는 애초에 쓰지 않습니다.**

### 텍스트 간격 — Figma 대조로 수정된 이력

| 구간 | Figma | Make 초기 | 수정 후 |
| --- | --- | --- | --- |
| `Emoji` → `Highlight` | **2** (`Spacing/50`) | 4 ❌ | **2** ✅ |
| `Highlight` → `Nickname` | 8 (`Spacing/200`) | 8 ✅ | 8 |
| `Nickname` → `Review` | 8 (`Spacing/200`) | 8 ✅ | 8 |

Figma 구조(`gap-[8px]` 바깥 · `gap-[2px]` 이모지 묶음)와 대조해 **이모지 간격 4 → 2로 교정**한 이력이 남아 있습니다.

### 반응형 규칙

| 상황 | 동작 |
| --- | --- |
| 내용이 짧으면 | `width: fit-content` — 내용만큼만 차지하고 **가운데 정렬** |
| 내용이 길면 | `maxWidth: 100%`까지만 확장 |
| 그래도 넘치면 | **후기 텍스트만** 줄어들며 `…` 처리 |

| 요소 | 설정 |
| --- | --- |
| contentRow | `inline-flex` · `width: fit-content` · `maxWidth: 100%` · `whiteSpace: nowrap` |
| `Emoji` | `flexShrink: 0` · `fontSize: 13` · `lineHeight: 1` |
| `Review` | `flexShrink: 1` · `textOverflow: ellipsis` |

이모지·강조·이름은 **줄어들지 않고**, 후기만 잘립니다.

### 색 — Figma와 대조

| 요소 | Figma | Make | 토큰 |
| --- | --- | --- | --- |
| 배경 | `#EAEAFF` | `#EAEAFF` | **없음** → [점검 7](#7-미바인딩-색상-3종) |
| 강조(`Highlight`) | `#694ACF` | `#694ACF` | **없음** → [점검 7](#7-미바인딩-색상-3종) |
| 본문(`Nickname`·`Review`) | `Color/Gray_200` | `#464646` | **`Color/Gray_200` = #464646** ✅ |

**세 색이 Figma와 정확히 일치**합니다. 다만 배경·강조색은 Figma 쪽에 토큰이 없어, 토큰을 만들면 **Make 쪽 하드코딩도 함께 정리**할 수 있습니다.

### Figma와 Make의 차이

| 항목 | Figma | Make |
| --- | --- | --- |
| 데이터 | 샘플 **1건** 고정 | `items` 배열 **3건** (조*주님 · 김*현님 · 이*민님) |
| 폭 | 360 고정 | `100%` 반응형 |
| 상태 | 정적 1컷 | `idle`/`flipping`/`settling` 3단계 |
| 항목 전환 | 없음 | 2.5초 주기 순환 |

Figma 컴포넌트는 **한 컷의 정지 화면**이고, 실제 동작·타이밍·반응형 규칙은 모두 이 Make 프로토타입에 있습니다. **두 곳을 함께 봐야 전체가 파악됩니다.**
