# Syrup Design System — Checkbox 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Checkbox` 페이지 → [Checkbox 섹션 `8506:16134`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8506-16134) |
| 섹션 구성 | `Checkbox` 1440×1258 → `Guidelines` 960×802 → `Usage` 2560×517 (가로 일렬) |
| 기준일 | 2026-11-05 (Usage · Guidelines 신설 / 스펙 정리: 2026-10-01) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **하나 이상의 항목을 선택할 수 있는 입력 컴포넌트에요.**
> 사용자의 선택 값을 입력받아야 하는 화면에서 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Checkbox — Master Component](#1-checkbox--master-component)
3. [Variant=Circle](#2-variantcircle)
4. [Variant=Line](#3-variantline)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

**컴포넌트셋 하나**로만 구성되어 있습니다. Child Item 섹션이 없습니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Checkbox` | Component Set | `Variant` × `Size` × `Checked` × `Disabled` (**32종**) | 16~30 정사각 |

---

## 1. Checkbox — Master Component

**Node** `8506:16085` · Component Set · **32 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Circle` | `Line` · `Circle` |
| `Size` | VARIANT | `XS` | `XS` · `S` · `M` · `L` |
| `Checked` | VARIANT | `True` | `False` · `True` |
| `Disabled` | VARIANT | `False` | `False` · `True` |

### Variant 매트릭스

2 × 4 × 2 × 2 = **32조합이 모두 존재합니다.** Bubble에 이어 **빈칸 없는 완전 매트릭스** 두 번째 사례입니다.

### Size 램프

| Size | 크기 | 원형 테두리 두께 |
| --- | --- | --- |
| `XS` | 16 × 16 | 1 |
| `S` | 20 × 20 | 1 |
| `M` | 24 × 24 | 1 |
| `L` | 30 × 30 | 1 |

**실제 획(stroke)은 `Circle` + `Checked=False`의 `Oval` 테두리뿐이며, 네 사이즈 모두 `1`로 고정**입니다. 크기가 커져도 테두리가 두꺼워지지 않습니다.

체크마크(`Fill` · `list/checkmark_selected`)는 **획이 아니라 면으로 그려지는 벡터**입니다. 사이즈별로 벡터를 확대·축소하므로 작은 사이즈에서는 자연히 가늘어집니다.

모든 variant는 **오토레이아웃 없이 고정 크기**입니다.

> 체크마크 레이어의 `strokeWeight` 속성이 사이즈별로 0.67 / 0.83 / 1 / 1.25로 잡혀 있지만, **stroke 페인트가 없어 렌더링에는 영향이 없습니다.** 벡터를 스케일할 때 속성만 따라간 값입니다.

---

## 2. Variant=Circle

원형 박스 안에 체크를 넣는 전통적인 체크박스입니다. 레이어는 `Oval`(배경/테두리) + `Fill`(체크마크)입니다.

| Checked | Disabled | `Oval` | `Fill` (체크마크) |
| --- | --- | --- | --- |
| `True` | `False` | fill `Color/Primary_Orange` | `Color/Gray_White` |
| `True` | `True` | fill `Color/Gray_850` | `Color/Gray_White` |
| `False` | `False` | stroke `Color/Gray_700` | — (레이어 없음) |
| `False` | `True` | stroke `Color/Gray_850` | — |

- 선택 상태는 **면으로 채우고**, 미선택 상태는 **테두리만** 그립니다.
- 미선택일 때 `Fill` 레이어 자체가 존재하지 않습니다.

---

## 3. Variant=Line

박스 없이 **체크마크 하나**(`list/checkmark_selected (Stroke)`)로만 상태를 표현합니다. 목록에서 선택 표시를 할 때 쓰는 형태입니다.

| Checked | Disabled | 체크마크 색 | Opacity |
| --- | --- | --- | --- |
| `True` | `False` | `Color/Primary_Orange` | 100% |
| `True` | `True` | `Color/Primary_Orange` | **30%** ⚠️ |
| `False` | `False` | `Color/Gray_700` | 100% |
| `False` | `True` | `Color/Gray_850` | 100% |

미선택 상태에서도 체크마크 레이어가 **사라지지 않고 회색으로 남습니다.** Circle과 달리 "체크 없음"이 아니라 "흐린 체크"로 표현됩니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 크기 | XS 16 · S 20 · M 24 · L 30 (정사각) |
| 테두리 두께 | 1 (전 사이즈 고정, `Circle`+미선택만) |
| 선택 | `Color/Primary_Orange` |
| 미선택 | `Color/Gray_700` |
| 비활성 | `Color/Gray_850` (`Line`+`Checked=True`만 opacity 30%, 의도된 예외) |
| 체크마크 (Circle) | `Color/Gray_White` |
| 레이아웃 | 오토레이아웃 없음, 고정 크기 |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11452:3240`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11452-3240) · 2560 × 517 |
| 구성 | 6패턴 · 폭 360 · 슬롯 높이 31~201 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-05).

**Checkbox는 단독 컷이 한 장도 없습니다.** 16~30px 정사각 하나뿐이라 혼자 두면 상태만 보이고 **무엇을 고르는 것인지**가 드러나지 않습니다. 그래서 여섯 컷 모두 **체크박스를 품는 컴포넌트**를 함께 세웠습니다 — 제품에서도 118건 중 113건이 다른 컴포넌트 안에 들어 있습니다 → [점검 7](#7-checkbox는-거의-전부-다른-컴포넌트-안에-있습니다)

**패턴을 가르는 축은 「어느 컴포넌트에 담기느냐」입니다.** Badge와 같은 방식입니다.

| | 패턴 | 설명 | 담기는 컴포넌트 | Checkbox |
| --- | --- | --- | --- | --- |
| **A** | 항목 선택 | 목록에서 선택한 항목과 선택하지 않은 항목을 구분해요. 같은 목록에서는 체크박스의 크기와 위치를 맞춰요. | `List Row / Todo / Selection` × 2 | `Circle` · **`M`** · `True` ↔ `False` |
| **B** | 약관 동의 | 약관 항목의 동의 상태를 표시해요. 약관 문구와 체크박스를 함께 배치하고, 전문 보기 화살표와 구분해요. | `Bottom Sheet / Body / List / List Item` × 2 | `Circle` · **`S`** · `False` ↔ `True` |
| **C** | 카드형 선택 | 선택한 카드의 체크 표시와 테두리를 함께 강조해요. 단일·복수 선택 여부는 화면의 선택 방식에 따라 정해요. | `Card / My` × 2 (`Selected` ↔ `Default`) | `Circle` · `S` · `True` ↔ `False` |
| **D** | 간결한 선택 목록 | 정렬이나 통신사 선택 목록에서는 선택한 항목을 Line 체크로 표시해요. 선택한 문구의 강조 상태도 함께 맞춰요. | `Bottom Sheet / Body / Selector / Select Item` × 2 | **`Line`** · `M` · `True` |
| **E** | 할 일 상태 | 완료한 항목은 Checked=True로, 아직 실행할 수 없는 항목은 Disabled=True로 표시해요. 완료·미완료·비활성 상태를 구분해요. | `List Row / Todo / Task` × 3 | `Circle` · `M` · 완료 ↔ 미완료 ↔ **`Disabled=True`** |
| **F** | 완료 표시 | Badge나 Bubble 안에서는 완료 상태를 알려주는 표시로 사용해요. 직접 선택하는 체크박스와 구분하고, 크기는 상위 컴포넌트의 기준을 따라요. | `Badge` · `Check=True` / `Bubble` · `Checkbox=true` | **`L`** 30 · **`XS`** 16 |

**여섯 컷이 네 사이즈를 모두 씁니다.** 크기를 고르는 것은 체크박스가 아니라 **담기는 컴포넌트**입니다.

| Size | 크기 | 쓰이는 자리 (Usage) |
| --- | --- | --- |
| `XS` | 16 | `Bubble` 안의 완료 표시 (F) |
| `S` | 20 | 약관 목록 · 카드 (B · C) |
| `M` | 24 | 할 일 목록 · 정렬 목록 (A · D · E) |
| `L` | 30 | `Badge` 안의 완료 표시 (F) |

**F만 「고르는 체크박스」가 아닙니다.** A~E는 눌러서 상태를 바꾸는 입력이지만, F의 둘은 **이미 끝난 일을 알리는 표시**입니다. 누를 수 없고 상태도 바뀌지 않습니다 — 같은 컴포넌트가 입력과 표시 두 가지로 쓰입니다.

**D만 `Variant=Line`입니다.** 박스 없이 체크마크 하나로 선택을 표시하는 형태라, 목록이 길고 글자가 주인공인 자리에서 씁니다. 오른쪽 끝에 체크만 찍고 선택한 줄의 **글자를 주황으로 바꾸는 것**이 한 쌍입니다.

### 제품 실측 (2026-11-05)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 `Checkbox` 인스턴스 **216건**을 전수 조사했습니다. 이 중 98건은 아이데이션 페이지의 것이라, 실제 제품 화면은 **118건**입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 배치 | **다른 컴포넌트 안에 중첩** | **113** |
| | 직접 배치 | **5** |
| `Variant` | `Circle` | **114** |
| | `Line` | **4** |
| `Size` | `M` (24) | 44 |
| | `XS` (16) | 38 |
| | `L` (30) | 21 |
| | `S` (20) | 15 |
| `Checked` | `True` | 68 |
| | `False` | 50 |
| `Disabled` | `False` | 110 |
| | `True` | **8** |
| variant 조합 | 32종 중 사용 | **9종** |

**네 사이즈가 모두 쓰입니다.** `Bubble`이 24종 중 6종만 쓰는 것과 달리, Checkbox는 사이즈 램프를 다 활용합니다 — 담기는 컴포넌트의 크기가 제각각이기 때문입니다.

**품고 있는 컴포넌트는 15종입니다.**

| 품고 있는 컴포넌트 | 건수 |
| --- | --- |
| `List Row / Todo / Selection` | **27** |
| `Badge` | **21** |
| `List Row / Task` | 12 |
| `Card / My` | 10 |
| `.primitive / Progress Stepper / Quiz / Button` | 8 |
| `cp_todo_list` · `List Row / Todo / Task` | 각 6 |
| `변경` · `Progress Stepper / Quiz` | 5 · 4 |
| `List Row / Personality Test` · `Text Field / Todo` · `Dialog` | 각 3 |
| `Bottom Sheet / Body / List / List Item` · `Bubble` | 각 2 |
| `Steeper Item` | 1 |

`Badge` 21건이 눈에 띕니다 — **전부 Usage F의 「완료 표시」** 쪽 쓰임입니다.

**제품에서 쓰이는 조합은 아홉 가지입니다.**

| 조합 | 건수 |
| --- | --- |
| `Circle` / `XS` / `True` | **34** |
| `Circle` / `M` / `False` | 31 |
| `Circle` / `L` / `True` | 21 |
| `Circle` / `M` / `True` | 9 |
| `Circle` / `S` / `False` | 7 |
| `Circle` / `S` / `True` | 4 |
| `Circle` / `M` / `False` / **`Disabled`** | 4 |
| `Circle` / `S` / `False` / **`Disabled`** | 4 |
| `Line` / `XS` / `False` | **4** |

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11452:3525`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11452-3525)** (960 × 802) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**두 규칙 모두 체크박스를 품는 컴포넌트를 함께 세웠습니다.** 1은 `Card / My`(360 × 84), 2는 `List Row / Todo / Task`(328 × 59)입니다.

| 형식 | 규칙 | 슬롯 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| Do / Don't | **1** | `Do` · `Don’t` | `#222222` · **`#FF3E00`** |
| 두 경우 비교 | **2** | 「완료 · 미완료」 · 「비활성」 | `#222222` · **`#222222`** |

2는 **둘 다 정상인 상태**라 Do / Don't로 두지 않았고, [Bottom Sheet 규칙 6](syrup-bottom-sheet-components.md#6-부가-설명은-보조-설명으로-나눌-수-있어요)에서 정한 대로 오른쪽 라벨 색도 검정으로 맞췄습니다.

### 1. 선택 상태는 관련 항목과 함께 표시해요

어떤 항목을 선택했는지 알 수 있도록 체크박스를 문구 가까이에 배치해요.
카드형 항목은 체크 표시와 테두리의 선택 상태를 일치시켜요.

| | 카드 | 체크박스 | 결과 |
| --- | --- | --- | --- |
| **Do** | `Property 1=Selected` (주황 테두리) | **`Checked=True`** | 테두리와 체크가 같은 말을 함 |
| **Don't** | `Property 1=Selected` (주황 테두리) | **`Checked=False`** | 테두리는 선택인데 체크는 비어 있음 |

두 컷 모두 같은 `Card / My`이고 **테두리도 똑같이 선택 상태**입니다. 다른 것은 `Checked` 하나입니다.

**카드형은 선택 표시가 두 군데로 나뉩니다.** 테두리와 체크박스가 각각 독립된 프로퍼티라, 하나만 바꾸면 **한 카드가 선택이면서 미선택**이 됩니다. 둘을 함께 바꾸는 것이 이 규칙입니다.

### 2. 완료와 비활성 상태를 구분해요

완료한 항목은 Checked=True로, 선택하거나 실행할 수 없는 항목은 Disabled=True로 표시해요.
Checked는 사용 맥락에 따라 선택 또는 완료를 뜻해요.

| 라벨 | `State` | Checkbox | 뜻 |
| --- | --- | --- | --- |
| **완료 · 미완료** | `Completed` / `Default` | `Checked=True` / `Checked=False` | 지금 할 수 있고, 했는지 안 했는지를 나타냄 |
| **비활성** | `Disabled` | **`Disabled=True`** | 아직 할 수 없음 — 누를 수 없는 상태 |

**세 상태가 한 줄에서 갈립니다.** 왼쪽 컷은 같은 「물 마시기」를 완료·미완료 두 줄로 세웠고, 오른쪽 컷은 같은 항목의 비활성 상태입니다. 「오전 09:40」처럼 **아직 오지 않은 시각**이 비활성의 이유입니다.

**`Checked=False`와 `Disabled=True`는 다른 말입니다.** 전자는 「아직 안 했다」, 후자는 「지금은 할 수 없다」입니다. 둘 다 빈 원으로 보이지만 테두리 색이 `Color/Gray_700` ↔ `Color/Gray_850`으로 갈리고, 줄 전체의 색도 함께 흐려집니다.

---

## 점검 필요 사항

### 1. ✅ `Variant=LIne` 오타 (2026-10-01 수정 완료)

variant 값이 **`LIne`** 이었습니다. `L` 다음이 소문자 `l`이 아니라 **대문자 `I`** 로, 같은 보드의 축 라벨 텍스트(`Line`)와 표기가 어긋나 있었습니다.

화면상으로는 구분이 거의 안 되지만, 코드에서 `Variant=Line`으로 지정하면 매칭에 실패하는 상태였습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| Variant 값 | `LIne` | **`Line`** |
| 수정된 variant | — | **16개** (`Line` 계열 전부) |
| `variantOptions` | `["LIne", "Circle"]` | `["Line", "Circle"]` |

파일 전체를 조사한 결과 `LIne` 표기는 **이 16개가 전부**였고, 수정 후 잔여 0건입니다.

### 2. ℹ️ 비활성 처리 방식의 차이 — **의도된 설계**

비활성 상태를 표현하는 방법이 variant마다 다릅니다.

| Variant | Checked | 비활성 처리 | 방식 |
| --- | --- | --- | --- |
| `Circle` | `True` | `Oval` fill → `Color/Gray_850` | 색상 토큰 |
| `Circle` | `False` | `Oval` stroke → `Color/Gray_850` | 색상 토큰 |
| `Line` | `False` | fill → `Color/Gray_850` | 색상 토큰 |
| `Line` | **`True`** | fill은 `Color/Primary_Orange` 유지 + **opacity 30%** | **투명도** |

`Line` + `Checked=True`만 오렌지를 그대로 두고 레이어 투명도를 30%로 낮춥니다. **실제 사용처가 있어 의도적으로 이렇게 둔 것이며 통일 대상이 아닙니다.**

다만 투명도 방식은 **뒤 배경이 비칩니다.** 흰 배경에서는 연한 오렌지로 보이지만 색이 있는 배경 위에 놓으면 다르게 보입니다. 배치되는 배경을 염두에 두고 쓰면 됩니다.

### 3. 체크마크 레이어에 의미 없는 `strokeWeight` 값이 남아 있음

체크마크 레이어(`Circle`의 `Fill`, `Line`의 `list/checkmark_selected`)에 사이즈별로 다른 `strokeWeight`가 설정되어 있습니다.

| Size | `strokeWeight` |
| --- | --- |
| `XS` | 0.67 |
| `S` | 0.83 |
| `M` | 1 |
| `L` | 1.25 |

**두 레이어 모두 stroke 페인트가 없어 이 값은 렌더링에 전혀 영향이 없습니다.** 벡터를 사이즈별로 확대·축소하면서 속성만 비례해 따라간 값입니다. 기능상 문제는 없지만, 스펙을 읽는 사람이 "테두리 두께가 사이즈마다 다르다"고 오해할 수 있습니다.

실제 획은 `Circle` + `Checked=False`의 `Oval` 8개뿐이며 전부 `1`입니다.

### 4. 토큰 상태 — 매우 양호

| 항목 | 결과 |
| --- | --- |
| 미바인딩 fill | **0건** |
| 미바인딩 stroke | **0건** |
| 미바인딩 radius · gap | **0건** |
| 미바인딩 padding | `100` 2건 — 문서 보드 레이아웃 프레임 |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 3 — 문서 레이아웃 전용 |

**32개 variant의 모든 색상이 Syrup 토큰에 바인딩되어 있습니다.** 지금까지 문서화한 컴포넌트 중 Banner와 함께 토큰 적용 상태가 가장 깨끗합니다.

### 5. 보드 축 라벨 16건은 스타일 미적용

`XS` · `S` · `M` · `L` · `Circle` · `Line` · `True` · `False` 등 매트릭스 축 라벨 16건이 15px로 스타일 없이 지정되어 있습니다. **컴포넌트가 아니라 문서 보드 표기**라 제품 UI에는 영향이 없습니다.

### 6. 32종 매트릭스 중 제품이 쓰는 조합은 9종입니다

`Variant` × `Size` × `Checked` × `Disabled` = **32조합이 빈칸 없이 다 만들어져 있지만**, 제품 118건이 실제로 쓰는 것은 **9종**입니다.

| 축 | 쓰이는 값 | 쓰이지 않는 값 |
| --- | --- | --- |
| `Size` | **네 가지 모두** (M 44 · XS 38 · L 21 · S 15) | — |
| `Checked` | 둘 다 (True 68 · False 50) | — |
| `Disabled` | 둘 다 (False 110 · True 8) | — |
| `Variant` | `Circle` 114 | `Line`은 **4건뿐** |

**사이즈 램프는 건강합니다.** [Bubble 점검 6](syrup-bubble-components.md#6-24종-매트릭스-중-제품이-쓰는-조합은-6종입니다)처럼 축 하나가 통째로 노는 경우는 없고, 네 축 모두 양쪽 값이 쓰입니다. 조합이 9종인 것은 **`Size`와 다른 축이 서로 맞물려 다니기 때문**입니다 — `L`은 `Badge` 안에서만, `XS`는 `Bubble`과 목록 아이콘에서만 쓰입니다.

**`Line`만 쓰임이 얕습니다.**

| `Line` 4건 | 조합 | 자리 |
| --- | --- | --- |
| 전부 | `Line` / `XS` / `Checked=False` | `⇥ 금 모으는 쇼핑`의 「참여 방법」 목록 |

제품의 `Line`은 **전부 미선택 상태**이고, 선택된 `Line` 체크는 한 건도 없습니다. 선택 표시로 쓰는 자리는 `Bottom Sheet`의 `Select Item`인데, 제품 화면의 정렬·통신사 선택 시트가 아직 선택 상태를 가진 인스턴스를 쓰고 있지 않습니다 ([Usage D](#usage)가 그 쓰임을 보여 줍니다).

### 7. Checkbox는 거의 전부 다른 컴포넌트 안에 있습니다

제품 118건 중 **113건(96%)이 다른 컴포넌트 안에 중첩**되어 있습니다. 직접 배치는 **5건**뿐입니다.

| 컴포넌트 | 중첩 비율 |
| --- | --- |
| **Checkbox** | **113 / 118 (96%)** |
| [Bubble](syrup-bubble-components.md#7-bubble은-대부분-다른-컴포넌트-안에-심겨-있습니다) | 90 / 116 (78%) |
| [Badge](syrup-badge-components.md) | 280 / 328 (85%) |

지금까지 잰 것 중 **가장 높습니다.** Checkbox는 화면에 혼자 놓이는 일이 사실상 없고, 목록 행·카드·배지가 자기 안에 품는 부품입니다.

**그래서 크기와 색을 Checkbox 쪽에서 정하지 않습니다.** 담는 쪽이 `Size`를 고르고, 선택 여부도 담는 쪽의 상태(`State=Completed` · `Property 1=Selected`)와 짝을 맞춰야 합니다 — [Guidelines 1](#1-선택-상태는-관련-항목과-함께-표시해요)이 그 짝이 어긋나는 경우를 다룹니다.
