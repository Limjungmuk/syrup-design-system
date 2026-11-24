# Syrup Design System — Bottom CTA 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Bottom CTA` 페이지 → [Bottom CTA 섹션 `8633:6089`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8633-6089) |
| 섹션 구성 | `Bottom CTA` 1440×2319 → `Usage` 3360×660 → `Guidelines` 960×1542 (가로 일렬) |
| 기준일 | 2026-11-03 (컷을 컴포넌트 인스턴스로 교체 · Usage 8패턴 · Guidelines 4규칙) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면 하단에 고정되어 있는 주요 행동 버튼 영역이에요.**
> 다음 단계로 이동하거나 핵심 결정을 유도할 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Bottom CTA — Master Component](#1-bottom-cta--master-component)
3. [Button Area](#2-button-area)
4. [Upper Item](#3-upper-item)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

페이지는 **Master Component → Child Item(Button Area · Upper Item)** 구조입니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Bottom CTA` | **Component (단일)** | 없음 — BOOLEAN 2개로 제어 | 360 × 154 |
| 2 | `.primitive / Bottom CTA / Button Area` | Component Set | `Buttons` 3종 | 360 × 56 · 120 |
| 3 | `.primitive / Bottom CTA / Upper Item` | Component Set | `Type` × `Highlight` 4종 | 360 × 42~44 |

Banner처럼 **본체에는 variant가 없고** 표시 요소를 BOOLEAN으로 켜고 끄는 구조입니다.

---

## 1. Bottom CTA — Master Component

**Node** `8663:6168` · Component (단일) · **360 × 154**

### Properties

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Upper Item` | BOOLEAN | `true` | 버튼 위 보조 영역 노출 |
| `Top Gradient` | BOOLEAN | `true` | 상단 페이드 그라데이션 노출 |

### 내부 구조

| 영역 | 크기 | Padding (T/R/B/L) | Gap | 비고 |
| --- | --- | --- | --- | --- |
| 루트 `Bottom CTA` | 360 × 154 | 0 | 0 | VERTICAL |
| `Top Gradient` | 360 × 36 | — | — | 흰색 **투명 → 불투명** 선형 그라데이션 |
| `Container` | 360 × 118 | 0 / 0 / `Spacing/500`(20) / 0 | 0 | VERTICAL · 배경 `Color/Gray_White` |
| └ `Upper Item` | 360 × 42 | — | — | `Upper Item` 프로퍼티로 토글 |
| └ `Button Area` | 360 × 56 | — | — | |

### Top Gradient

스크롤되는 본문이 CTA 뒤로 지나갈 때 경계를 흐리게 하는 페이드 레이어입니다.

| 항목 | 값 |
| --- | --- |
| 타입 | `GRADIENT_LINEAR` |
| Stop 0 | #FFFFFF · **알파 0%** · position 0 |
| Stop 1 | #FFFFFF · **알파 100%** · position 1 |
| 바인딩 | `Semantic/Background/Default` ⚠️ (외부 라이브러리) |

하단 20px 패딩(`Spacing/500`)은 홈 인디케이터 등 하단 안전 영역을 비워 두기 위한 여백으로 보입니다.

---

## 2. Button Area

**Node** `8664:6044` · Component Set · 3 variants

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Buttons` | VARIANT | `1 Button` | `1 Button` · `2 Buttons (Vertical)` · `2 Buttons` |

### Variants

공통으로 폭 360, 좌우 패딩 `Spacing/400`(16), 상하 패딩 0입니다.

| Variant | 크기 | 레이아웃 | Gap | 버튼 구성 |
| --- | --- | --- | --- | --- |
| `1 Button` | 360 × 56 | HORIZONTAL | 0 | Primary 328 × 56 |
| `2 Buttons (Vertical)` | 360 × 120 | VERTICAL | `Spacing/200` (8) | 위 Secondary · 아래 **Primary** |
| `2 Buttons` | 360 × 56 | HORIZONTAL | `Spacing/200` (8) | 좌 Secondary 160 · 우 **Primary** 160 |

### 버튼 공통 스펙

| 항목 | 값 |
| --- | --- |
| 높이 | 56 |
| Padding | `Spacing/50`(2) / `Spacing/700`(28) |
| Gap | `Spacing/100` (4) |
| Radius | `Corner radius/250` (10) |
| 라벨 | `t800_17_bold` |

### 버튼 위계

| 위계 | 배경 | 라벨 색 |
| --- | --- | --- |
| **Primary** | `Color/Primary_Orange` (#FF6315) | `Color/Gray_White` |
| **Secondary** | `Color/Gray_900` (#F2F2F2) | `Color/Gray_200` (#464646) |

주 액션 위치는 **세로형에서 아래, 가로형에서 오른쪽**입니다. Dialog의 Button Area와 동일한 규칙이고 색상 토큰도 같습니다.

---

## 3. Upper Item

**Node** `8668:30964` · Component Set · 4 variants

버튼 위에 놓이는 보조 영역입니다. 공통으로 폭 360, 패딩 `0 / Spacing/600(24) / Spacing/600(24) / Spacing/600(24)`, gap 0입니다.

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Description` | `List` · `Description` · `Text Button` |
| `Highlight` | VARIANT | `True` | `False` · `True` |

### Variants

| Variant | 크기 | 내용 | 타이포 | 색상 |
| --- | --- | --- | --- | --- |
| `Description, Highlight=True` | 360 × 42 | 설명 문구 | `t1350_14_medium` | `Color/Primary_Orange` |
| `Description, Highlight=False` | 360 × 42 | 설명 문구 | `b400_14_regular` | `Color/Gray_400` |
| `List, Highlight=False` | 360 × 44 | `Bottom Sheet / Body / List / List Item` 인스턴스 | — | — |
| `Text Button, Highlight=False` | 360 × 43 | `Text Button` 인스턴스 | — | — |

- `Highlight=True`는 문구를 `Color/Primary_Orange`로 강조하고 Medium 두께를 씁니다.
- `List` variant는 **Bottom Sheet 컴포넌트의 List Item을 그대로 재사용**합니다. 내부 gap `Spacing/400`(16), 우측 Arrow 아이콘 16 × 16.
- 샘플 문구: "추가 설명이 여기 들어갑니다"

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | **360 고정** |
| 기본 높이 | 154 (Upper Item + 버튼 1개 기준) |
| 배경 | `Color/Gray_White` |
| 상단 페이드 | 36px 흰색 그라데이션 |
| 하단 여백 | `Spacing/500` (20) |
| 버튼 영역 좌우 여백 | `Spacing/400` (16) |
| Upper Item 여백 | `Spacing/600` (24) |
| 버튼 높이 · 모서리 | 56 · `Corner radius/250` (10) |
| 버튼 라벨 | `t800_17_bold` |
| 주 액션 | `Color/Primary_Orange` + `Color/Gray_White` |
| 보조 액션 | `Color/Gray_900` + `Color/Gray_200` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11105:9486`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11105-9486) · 3360 × 660 |
| 구성 | 8패턴 · 폭 360 · 높이는 내용에 맞춰 228~460 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-03).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 세로 간격은 50입니다.

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **A** | 단일 버튼 | 행동이 하나일 때 쓰는 기본형이에요. | `Bottom CTA` | 112 |
| **B** | 설명 + 강조 | 버튼 위에 안내 문구를 두고 숫자나 핵심어를 강조해요. | `Bottom CTA` | 154 |
| **C** | 2 버튼 (가로) | 두 행동을 좌우로 나란히 둬요. 왼쪽이 보조, 오른쪽이 주 행동이에요. | `Bottom CTA` | 112 |
| **C-2** | 2 버튼 (가로) · 비활성 | 진행 조건을 충족하지 못한 경우 주요 행동을 비활성화해요. 이전 단계로 돌아가는 행동은 유지해요. | `Bottom CTA` + `Text Field / Text Area` | 222 |
| **D** | 2 버튼 (세로) | 이용 조건에 따라 선택할 수 있는 두 가지 행동을 세로로 배치해요. | `Bottom CTA` | 176 |
| **E** | 설명 + 강조 없음 | 주요 행동 전에 추가 안내가 필요하지만 강조하지 않아도 되는 경우 사용해요. | `Bottom CTA` | 154 |
| **F** | 텍스트 버튼 + 주요 행동 | 주요 행동 외에 보조 행동이 필요한 경우, 상단에 텍스트 버튼을 배치해요. | `Bottom CTA` | 155 |
| **G** | 그라디언트 없음 | 키보드가 올라온 상태에서는 하단 그라데이션을 제거하고 버튼을 배치해요. | `Bottom CTA` + `Keypad` | 344 |

맥락 요소를 함께 넣은 건 **C-2**와 **G** 둘뿐입니다. C-2는 "진행 조건"이 입력창이라 입력창이 없으면 왜 비활성인지 알 수 없고, G는 키보드가 올라온 상태 자체가 패턴의 전제입니다. 나머지 여섯은 `Bottom CTA` 하나로 충분합니다.

**F는 Upper Item을 `Type=Text Button`으로 쓰는 패턴입니다.** B · E가 쓰는 `Type=Description`이 **읽는 내용**이라면, F의 `Text Button`은 **누르는 보조 행동**입니다 (「친구에게도 알려주기」 + 「도전하기」). 둘 다 Upper Item 영역을 쓰지만 성격이 달라 패턴을 나눴습니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11135:24`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11135-24)** (960 × 1542) 에 Do / Don't 한 쌍으로 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 `Do` · `Don't` **슬롯**이 좌우로 들어갑니다. Do / Don't 표시는 슬롯 이름이 대신합니다.

### 1. Upper Item을 켰으면 내용을 채우세요

버튼 위에 추가 안내나 보조 행동이 필요한 경우 Upper Item을 사용해요. 사용하지 않을 때는 Upper Item을 숨겨주세요.

| | 내용 |
| --- | --- |
| **Do** | 「이벤트 기간에만 받을 수 있어요」처럼 **안내 문구를 채운다**. 보조 행동이면 `Type=Text Button` (Usage **F**) |
| **Don't** | Upper Item을 켠 채 문구를 비워 **42px 빈 줄만** 남긴다 |

### 2. 2버튼은 왼쪽이 보조, 오른쪽이 주 행동

버튼을 가로로 두 개 배치할 때는 왼쪽 보조 행동에 `Weak`, 오른쪽 주요 행동에 `Fill`을 사용해요.

| | 왼쪽 | 오른쪽 |
| --- | --- | --- |
| **Do** | `Weak` 「이전」 | `Fill` 「다음」 |
| **Don't** | **`Fill`** 「이전」 | `Fill` 「다음」 — 주 행동이 둘이라 어디를 눌러야 할지 알기 어려워요 |

### 3. 비활성은 Weak + Disabled로 만드세요

비활성 버튼은 색상을 직접 변경하지 않고, `Variant=Weak`와 `Disabled=True`를 적용해요.

| | 설정 | 결과 |
| --- | --- | --- |
| **Do** | `Variant=Weak` · `Disabled=True` | 배경 `Gray_900` · 글자 `Gray_600` |
| **Don't** | `Variant=Fill` + 배경을 **수동으로 회색** | 흰 글자가 남아 눌리는 버튼처럼 보여요 |

수동으로 칠하면 **토큰 연결이 끊기고**, 비활성 색이 바뀔 때 따라오지 않습니다.

### 4. 행동의 관계에 따라 버튼 배치를 구분해요

이전/다음처럼 서로 연결된 단계 이동은 가로로, 이용 조건에 따라 선택하는 서로 다른 행동은 세로로 배치해요.

| | 두 행동의 관계 | 배치 |
| --- | --- | --- |
| **Do** | 이용 조건에 따라 갈리는 서로 다른 행동 | **세로** (`2 Buttons (Vertical)`) |
| **Don't** | 같은 두 행동을 좌우로 밀어넣음 | 가로 — 문구가 160px 버튼에 꽉 차요 |

배치와 무관하게 **보조는 `Weak`, 주 행동은 `Fill`** 입니다. 가로(`C`)와 세로(`D`)가 **둘 다 `Weak` + `Fill`** 이라 버튼 variant로는 구분되지 않습니다. 그래서 위계를 **배치가 표현하는 관계**로 정의했습니다.

> 이전 판의 규칙 「키보드가 올라오면 Top Gradient를 끄세요」는 Guidelines에서 뺐습니다. 지키지 않으면 깨지는 규칙이라기보다 **상황별 형태**라, Usage **G. 그라디언트 없음**으로 옮겼습니다.

---

## 점검 필요 사항

### 1. ✅ Variant 이름에 제어문자 (2026-10-01 제거 완료)

`Buttons=2 Buttons (Vertical)` variant의 이름에 보이지 않는 **U+0008 (BACKSPACE)** 문자가 들어 있었습니다. 실제 이름은 `2 ␈Buttons (Vertical)` 형태였습니다.

Figma 화면에서는 정상으로 보이지만 다음 상황에서 문제가 됩니다.

- 코드에서 `Buttons=2 Buttons (Vertical)` 문자열로 variant를 지정하면 **매칭 실패**
- 컴포넌트 목록을 JSON으로 내보낼 때 파서가 깨지거나 값이 어긋남
- 문서에 복사해 붙이면 눈에 띄지 않는 깨진 문자가 함께 따라옴

제어문자를 제거해 `variantOptions`가 `["1 Button", "2 Buttons (Vertical)", "2 Buttons"]`로 정리되었습니다.

#### ✅ 파일 전체 제어문자 일괄 정리 (2026-10-01 · 총 14건)

이 건을 고치면서 전수 조사한 결과 같은 문제가 더 있어 **파일 전체를 함께 정리**했습니다.

**Variant 이름 — 4건** (코드에서 문자열 매칭이 실패하므로 영향이 큽니다)

| 페이지 | Node | 정리된 이름 | 문자 |
| --- | --- | --- | --- |
| Bottom CTA | `8681:22669` | `Buttons=2 Buttons (Vertical)` | U+0008 |
| Bottom Sheet | `8686:11125` | `Buttons=2 Buttons (Vertical), Weak Button=Gray_900` | U+0008 |
| Grid Scroll | `8958:77647` | `Variant=네이버플러스스토어` | U+001D |
| List Row | `9354:10305` | `Type=금모으는쿠폰` | U+001D |

**일반 레이어 이름 — 10건**

| 페이지 | 건수 | 이름 | 문자 |
| --- | --- | --- | --- |
| Text Field | 6 | `field` | U+0008 |
| AD | 2 | `syrup_ico_40_floating_close_enabled_gray_400` | U+0008 |
| Foundation | 1 | `weight` | U+0008 |
| List Row | 1 | `head` | U+0008 |

Bottom Sheet의 건은 **이 컴포넌트와 같은 `2 Buttons (Vertical)` 패턴**이라 같은 작업 중에 복사되며 번진 것으로 보입니다. Text Field의 `field` 6건도 한 레이어를 복제하며 퍼진 형태입니다.

U+0008은 BACKSPACE, U+001D는 GROUP SEPARATOR로 둘 다 화면에 표시되지 않습니다. AD 섹션 Title Bar에서 발견된 U+2028(LINE SEPARATOR)과 같은 계열의 문제입니다.

### 2. ✅ `Description, Highlight=False`의 텍스트 스타일 미적용 (2026-10-01 적용 완료)

`Highlight=True`와 같은 설명 문구인데 한쪽만 스타일이 적용되어 있지 않았습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 스타일 | **없음** | `b400_14_regular` |
| 크기 · 두께 | 14 Regular | 14 Regular (유지) |
| line-height | **19** | **18** |
| letter-spacing | −0.5 | −0.5 (유지) |
| variant 높이 | 43 | **42** |

**`b400_14_regular`를 선택한 이유** — 현재 값의 두께(Regular)와 letter-spacing(−0.5)이 그대로 맞고 line-height만 1px 달랐습니다. `Highlight=True`가 쓰는 `t1350_14_medium`을 적용하면 두께가 Medium으로 바뀌어, 강조 여부를 두께로 구분하던 설계가 무너집니다.

이로써 두 variant의 높이가 42로 맞춰졌고 `Highlight` 축은 **색과 두께**로만 구분됩니다.

| Variant | 스타일 | 두께 | 색 |
| --- | --- | --- | --- |
| `Highlight=True` | `t1350_14_medium` | Medium | `Color/Primary_Orange` |
| `Highlight=False` | `b400_14_regular` | Regular | `Color/Gray_400` |

### 3. ✅ Top Gradient가 외부 토큰에 바인딩 (2026-10-01 교체 완료)

`Top Gradient`의 그라데이션이 외부 라이브러리 토큰 **`Semantic/Background/Default`**(#FFFFFF)에 묶여 있었습니다. `Color/Gray_White`와 값이 동일해 무손실로 교체했습니다.

| Stop | Position | 색 | 알파 | 바인딩 |
| --- | --- | --- | --- | --- |
| 0 | 0 | #FFFFFF | **0%** | 없음 (그대로 유지) |
| 1 | 1 | #FFFFFF | 100% | `Semantic/Background/Default` → **`Color/Gray_White`** |

바인딩은 **불투명 stop에만** 걸려 있었고 투명 stop은 묶여 있지 않아, 페이드 효과가 그대로 유지됩니다. 스크린샷으로 확인했습니다.

이 건은 2026-09-21 외부 토큰 일괄 교체에서 **빠져 있었습니다.** 당시 스크립트가 `SOLID` 페인트만 처리했는데 이 노드는 `GRADIENT_LINEAR`라 대상에서 제외되었습니다. 파일 전체에 남아 있던 `Semantic/Background/Default` 1건이 바로 이 노드였고, 이제 **0건**입니다.

> 그라데이션 stop의 변수 바인딩은 `fills[i].gradientStops[j].boundVariables.color`에 저장됩니다. `SOLID` 페인트의 `setBoundVariableForPaint`와 경로가 달라, 토큰 감사 스크립트를 쓸 때 별도 처리가 필요합니다.

### 4. Variant 조합 공백

`Type` 3종 × `Highlight` 2종 = 6조합 중 **4개만** 존재합니다.

| 없는 조합 | 비고 |
| --- | --- |
| `List` + `Highlight=True` | — |
| `Text Button` + `Highlight=True` | — |

`Highlight`는 사실상 `Description`에만 적용되는 축입니다. 의도된 제한이면 컴포넌트 설명에 남겨 두는 편이 좋습니다.

### 5. 다른 컴포넌트에 대한 의존

`Upper Item`의 `List` variant가 **`Bottom Sheet / Body / List / List Item`** 을 인스턴스로 사용합니다. Bottom Sheet 컴포넌트를 수정하면 Bottom CTA에도 영향이 갑니다.

재사용 자체는 바람직하지만, 이름이 `Bottom Sheet` 계열이라 Bottom CTA 쪽에서 추적하기 어렵습니다. 공용 List Item으로 승격하거나 의존 관계를 명시해 두는 편이 안전합니다.

### 6. `Highlight=False`의 정상 사용 예제가 없습니다

[Usage의 `E`](#usage)(`Description` · `Highlight=False`)는 **쓰이고는 있지만 제대로 쓰인 화면을 찾지 못했습니다.** 수집한 화면 중 이 조합을 쓴 것은 Upper Item 텍스트가 **공백 한 칸(" ")** 으로 비어 있었고, 그게 [Guidelines 1번](#1-upper-item을-켰으면-내용을-채우세요)의 Don't가 됐습니다.

그래서 Usage의 `E` 컷과 Guidelines 1번의 Do 샘플은 **수집본이 아니라 새로 만든 것**입니다.

| 판단이 필요한 것 | 내용 |
| --- | --- |
| 쓰임새가 있는가 | 강조 없는 설명만 필요한 화면이 실제로 있는지 |
| 없다면 | [점검 4](#4-variant-조합-공백)의 `Highlight` 축 정리와 함께 판단 |

`Highlight=False`는 [점검 2](#2--description-highlightfalse의-텍스트-스타일-미적용-2026-10-01-적용-완료)에서 텍스트 스타일을 맞춰 둔 조합이라, **스펙은 정상이고 쓰임새만 미확인**입니다.

> 2026-11-03 — `Text Button` + `Highlight=False`는 [Usage의 `F`](#usage)로 쓰임새가 확인됐습니다. 미확인으로 남은 건 **`Description` + `Highlight=False`**(`E`)와 **`List`** 두 가지입니다.

### 7. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 컴포넌트 미바인딩 radius · padding · gap | **0건** |
| 미바인딩 padding (페이지) | `100` 6건 — 문서 보드 레이아웃 프레임 |
| 스타일 미적용 텍스트 | **0건** |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 7 · paragraph 계열 1 — 둘 다 전역 이슈 |

**컴포넌트 자체의 spacing · radius · 색상 · 타이포가 전부 Syrup 토큰과 로컬 스타일로 정리되어 있습니다.** 1 · 2 · 3번은 2026-10-01에 모두 처리했고, 남은 항목은 4번(variant 조합 공백)과 5번(Bottom Sheet 의존)처럼 **구조에 대한 판단이 필요한 건**뿐입니다.

### 8. ✅ 페이지 잔여 노드 정리 (2026-11-03 완료)

컷을 인스턴스로 바꾸면서 남아 있던 `원본 컷 (정리 전)` 섹션(6960 × 1085 · 컷 17개)과 `Usage` 섹션 밖에 떠 있던 낱개 인스턴스 `11241:48244`를 지웠습니다. 페이지에는 이제 `Bottom CTA` · `Usage` · `Guidelines` 세 섹션만 있습니다.

`Usage` · `Guidelines` 템플릿은 `❖System Components` 페이지에 그대로 둡니다 — 다른 컴포넌트 페이지에서도 쓰는 공용 템플릿입니다.
