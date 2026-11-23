# Syrup Design System — Text Button 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Text Button` 페이지 → [Text Button 섹션 `8795:6990`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8795-6990) |
| 섹션 크기 | 1440 × 1594 |
| 컴포넌트 수 | **1개** |
| Variant 총수 | **80개** (완전 매트릭스) |
| 기준일 | 2026-11-10 (가이드라인 4개·Usage A~F 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **텍스트를 중심으로 구성된 버튼 컴포넌트에요.**
> 화면 내 보조적인 행동이나 추가 이동을 유도해야 하는 영역에 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Text Button — Master Component](#1-text-button--master-component)
3. [가이드라인](#가이드라인)
4. [Usage — 사용 예제](#usage--사용-예제)
5. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [점검 필요 사항](#점검-필요-사항)
8. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 섹션은 1440 × 1594이며 사용 문서는 Guidelines와 Usage로 구성해요. 기존 노드 295개·텍스트 83개와 파일 전체 인스턴스 20건/8개 페이지는 2026-10-12 점검 기록으로, 이후 추가된 Section 1·가이드라인·예제를 포함한 현재 집계가 아니에요. 마스터는 Child Item 없이 80개 베리언트로 구성되어 있어요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 956) | `Text Button` 1종 |

| # | 이름 | 타입 | Variant 축 | 인스턴스 |
| --- | --- | --- | --- | --- |
| 1 | `Text Button` | **Set 80** | `Color`(5) × `Size`(4) × `Underline`(2) × `Bold`(2) + `Arrow` BOOLEAN | **20** (8개 페이지) |

5 × 4 × 2 × 2 = **80 완전 매트릭스**입니다. 이 파일에서 손꼽히게 큰 Component Set입니다.

### 파일 전반에서 쓰입니다

| 페이지 | 건수 |
| --- | --- |
| [Card](syrup-card-components.md) | 6 |
| [List Row](syrup-list-row-components.md) | 4 |
| [Alert](syrup-alert-components.md) · [Bottom Info](syrup-bottom-info-components.md) | 각 3 |
| [Bottom CTA](syrup-bottom-cta-components.md) · [Button](syrup-button-components.md) · [List Header](syrup-list-header-components.md) · [Progress Stepper](syrup-progress-stepper-components.md) | 각 1 |
| **합계** | **20건 / 8개 페이지** |

위 표는 당시 사용량 기록이에요. 현재 다른 컴포넌트 페이지에도 예제가 추가되어 있으므로 파일 전체 사용량을 뜻하지 않아요. 변경 시 최신 인스턴스와 텍스트 오버라이드를 확인해요.

---

## 1. Text Button — Master Component

**Node** `8853:14938` · Component Set · **80 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Color` | VARIANT | `Gray_100` | `Primary_Orange` · `Secondary_Blue` · `Gray_100` · `Gray_400` · `Gray_600` |
| `Size` | VARIANT | `XS` | `XS` · `S` · `M` · **`XL`** |
| `Underline` | VARIANT | `False` | `False` · `True` |
| `Bold` | VARIANT | `False` | `False` · `True` |
| `Arrow` | BOOLEAN | `true` | — |

공통 — 가로 오토레이아웃 MIN / CENTER · **Padding 0 · Gap 0** · 배경 없음

버튼 영역 없이 **글자와 화살표만** 있는 구조라 패딩이 전혀 없습니다.

### Size별 타이포

| Size | 글자 | Regular | Bold | 화살표 |
| --- | --- | --- | --- | --- |
| `XS` | 13 | `b500_13_regular` ✅ | `t1060_13_bold` ✅ | 12 × 12 |
| `S` | 15 | `b300_15_regular` ✅ | `t1000_15_bold` ✅ | 16 × 16 |
| `M` | 17 | `b100_17_regular` ✅ | `t800_17_bold` ✅ | 20 × 20 |
| **`XL`** | **25** | **스타일 미적용** ❌ | `t300_25_bold` ✅ | 24 × 24 |

`XL`의 Regular만 토큰이 없습니다 → [점검 3](#3-xl-regular-스타일-미적용-10건)

**`L`이 없습니다.** `M`(17) 다음이 바로 `XL`(25)로 **8px 건너뜁니다** → [점검 4](#4-size에-l이-없음)

### `Underline`에 따라 구조가 완전히 다릅니다

| Underline | 구조 | 화살표 |
| --- | --- | --- |
| `False` (40개) | `text` TEXT + `Icon / Arrow` INSTANCE | **있음** |
| `True` (40개) | `Text` FRAME ▸ `text` TEXT | **없음** |

`Underline=True`는 **텍스트를 프레임으로 한 겹 감싸고** 그 프레임의 **하단 테두리로 밑줄을 그립니다.**

| 항목 | 값 |
| --- | --- |
| 밑줄 구현 | `Text` 프레임의 `strokeBottomWeight` |
| 밑줄 색 | `Color` 값과 같은 토큰 ✅ (`Gray_100` · `Primary_Orange` 등) |
| 밑줄 두께 | **1 · 1.25 · 1.5 · 2 · 2.5** (Size·Bold에 따라) |
| 텍스트 `textDecoration` | **`NONE`** — 글자 자체의 밑줄은 쓰지 않음 |

글자의 `textDecoration` 대신 프레임 테두리를 쓴 것은 **밑줄 두께와 간격을 조절하기 위한 선택**으로 보입니다.

**`Underline=True` 40개에는 화살표가 아예 없습니다** → [점검 1](#1-underlinetrue에서-arrow가-작동하지-않음)

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-5945)

### 1. 동작을 알 수 있는 문구를 사용해요

연결할 내용이나 실행할 동작이 드러나는 문구를 사용해요.
참여 방법 보기·수정·삭제처럼 사용자가 누른 뒤의 결과를 예상할 수 있도록 표현해요.

- 비교: 내용 확인 / 항목 관리
- [가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-5947)

### 2. 밑줄과 화살표로 클릭할 수 있음을 알려줘요

문장이나 안내 주변에서 링크를 구분할 때는 Underline=True를 사용해요.
화살표를 함께 표시하려면 Underline=False에서 Arrow=True를 사용해요. 밑줄형에는 화살표를 함께 표시하지 않아요.

- 비교: Underline=True · 밑줄 / Underline=False · Arrow=True
- [가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6000)

### 3. 주변 정보에 맞는 크기와 굵기를 사용해요

안내 영역 안의 작은 링크는 XS, 일반적인 보조 동작은 S처럼 주변 텍스트에 맞는 크기를 사용해요.
금액·개수를 크게 보여주며 상세 내용으로 연결할 때는 XL과 Bold=True를 함께 사용할 수 있어요.

- 비교: XS · 안내 영역의 링크 / XL · 금액 상세 보기
- [가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6043)

### 4. 사용 맥락에 맞는 컬러를 사용해요

보관함 이동을 강조할 때는 Primary_Orange, 설정 안내에는 Secondary_Blue 등 사용처에 맞는 컬러를 선택해요.
수정·삭제나 의견 남기기 같은 보조 동작에는 회색 계열을 사용할 수 있어요. 회색을 비활성 상태로 해석하지 않아요.

- 비교: Primary_Orange · 보관함 이동 / Gray_400 · 보조 동작
- [가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6090)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-5946)

| 예제 | 설명 | 구성 | 링크 |
| --- | --- | --- | --- |
| A. 추가 내용 확인 | 참여 방법처럼 본문과 관련된 추가 내용을 확인해요. 짧은 문구와 화살표를 함께 사용해 연결되는 내용을 알려줘요. | 참여 방법 보기 · S · Gray_100 · Underline=False · Arrow=True | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6132) |
| B. 보관함 이동 | 내 쿠폰함처럼 관련된 보관함으로 이동해요. Primary_Orange와 밑줄을 사용한 링크로 보여줘요. | 내 쿠폰함 · S · Primary_Orange · Underline=True | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6150) |
| C. 안내에서 설정 연결 | 안내 내용을 확인한 뒤 필요한 설정으로 이동해요. Alert 안에서 XS 크기의 밑줄 링크를 함께 사용해요. | Alert + 위치 설정하기 · XS · Secondary_Blue · Underline=True | [C](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6167) |
| D. 항목 수정과 삭제 | 목록 항목을 수정하거나 삭제할 때 사용해요. 두 동작을 짧은 문구로 구분하고 각 항목과 함께 배치해요. | 수정 / 삭제 · S · Gray_400 · Underline=False · Arrow=False · 구분선 1 | [D](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6192) |
| E. 금액 상세 보기 | 금액이나 개수 자체를 눌러 상세 내용을 확인해요. XL 크기와 굵은 글자로 수치를 보여주고 화살표를 함께 표시해요. | 이번 달(보조 텍스트) + 10,000금 · XL · Gray_100 · Bold=True · Arrow=True | [E](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6219) |
| F. 의견 남기기 | 서비스에 대한 의견을 작성하는 화면으로 연결해요. Gray_400과 밑줄을 사용해 보조 동작으로 보여줘요. | 지금 할 일에 의견 남기기 · S · Gray_400 · Underline=True | [F](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11801-6241) |

## 예제 레이아웃과 AI 사용 기준

- Guidelines 섹션은 960 × 1164, Usage는 2560 × 356이에요. 기존 섹션과 동일한 흰 배경·모서리 24를 사용해요.
- Slot은 폭 360, 패딩 0, 좌측·상단 정렬, 높이 Hug예요. 제목·설명 끝과 Slot 사이 간격은 50이에요. Usage의 설명 높이를 맞춰 예제 시작점을 정렬했어요.
- 단일 버튼은 Slot 안에 직접 배치해요. C는 설정 이동의 문맥에 필요한 Alert만, D는 수정·삭제와 구분선만, E는 수치의 의미를 설명하는 ‘이번 달’ 텍스트만 함께 사용했어요. 전체 서비스 화면은 복제하지 않았어요.
- 수정·삭제 묶음의 간격은 기존 요소의 8을 유지했어요. 이 값은 해당 묶음의 예제이며 모든 Text Button 사이의 공통 간격으로 확대하지 않아요.
- Text Button 마스터는 패딩 0인 고유 규격을 사용해요. Slot 패딩 0은 문서 컨테이너 설정으로, 다른 컴포넌트의 내부 패딩을 제거하라는 규칙이 아니에요.
- Arrow는 BOOLEAN이며 실제 속성 키는 `Arrow#8853:0`이에요. Color·Size·Underline·Bold는 VARIANT 속성이에요. Underline=True에는 화살표 레이어가 없어 Arrow=True라도 표시되지 않아요.
- 밑줄 링크와 화살표 링크는 모두 이동에 사용될 수 있어요. 밑줄은 실행 전용, 화살표는 이동 전용처럼 사용처를 임의로 배타 분류하지 않아요.
- 안내 영역의 XS, 보조 동작의 S, 수치 상세 보기의 XL Bold는 확인한 사용 예제예요. M이 사용 불가하거나 삭제 대상이라는 뜻이 아니에요.
- Color는 시각적 표현을 선택하는 속성이에요. 회색 버튼이 Disabled라는 뜻이 아니며, 현재 마스터에 별도의 Disabled·Hover·Pressed 속성이 있다고 가정하지 않아요.
- Primary_Orange와 Secondary_Blue의 적용은 현재 예제의 사용 맥락을 설명해요. 모든 설정 링크가 반드시 파랑이어야 한다는 새 공통 규칙으로 확대하지 않아요.
- 금액·개수의 샘플 수치는 교체 가능한 데이터예요. XL Bold Text Button을 단순 숫자 레이블로 바꾸어 상세 보기 동작을 누락하지 않아요.
- Section 1의 아노테이션 54개를 제거했어요. 예제 구성은 기존 컴포넌트를 재사용했으며 마스터의 색상·크기·구조를 변경하지 않았어요.

---

## 설계 규칙 요약

> 아래 토큰·스타일 건수는 기존 마스터 보드 점검 기록이에요. 이번 작업은 사용 가이드와 예제 추가이며 마스터 전체 토큰 재점검 결과는 아니에요.

### Color 값이 토큰 이름 그대로입니다

| Color 값 | 대응 토큰 |
| --- | --- |
| `Primary_Orange` | `Color/Primary_Orange` |
| `Secondary_Blue` | `Color/Secondary_Blue` |
| `Gray_100` · `Gray_400` · `Gray_600` | `Color/Gray_*` |

variant 이름만 봐도 **어떤 토큰이 적용되는지 바로 알 수 있습니다.** 다른 컴포넌트가 `Default` · `Primary` 같은 역할 이름을 쓰는 것과 다른 방식입니다.

| 장점 | 단점 |
| --- | --- |
| 추적이 쉽고 오해가 없음 | 토큰 이름이 바뀌면 variant 이름도 함께 바꿔야 함 |
| 디자이너가 색을 바로 고를 수 있음 | 역할(강조·보조·비활성)이 이름에 드러나지 않음 |

**의도적 선택으로 보여 변경 대상으로 두지 않았습니다.**

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| 텍스트 색 | `Primary_Orange` · `Secondary_Blue` · `Gray_100` · `Gray_400` · `Gray_600` ✅ |
| 밑줄 색 | 위와 동일 토큰 ✅ |
| 텍스트 스타일 | 7종 적용 ✅ — **`XL` Regular 10건 미적용** |
| Padding · Gap | 전부 0 — 바인딩 불필요 |
| 미바인딩 색상 | **0건** ✅ |
| 미바인딩 수치 | **0건** ✅ (보드 영역 제외) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

**색은 80개 variant 전부 토큰에 묶여 있습니다.** 남은 것은 `XL` Regular 스타일 하나뿐입니다.

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖Components | **`Icon / Arrow`** | **40** |
| ❖System Components | `Title Bar` 1 · `Section Header` 1 | 2 |

화살표를 자체 primitive로 두지 않고 **공용 아이콘을 가져다 씁니다.** 외부 라이브러리 인스턴스는 **0건**입니다.

---

## 점검 필요 사항

> 아래 네이밍·스타일·구조 개선 제안은 과거 점검 기록이에요. 현재 사용 기준은 가이드라인과 Usage를 따라요. 마스터 베리언트와 속성명은 이번에 변경하지 않았어요.

### 1. `Underline=True`에서 `Arrow`가 작동하지 않음

| Underline | variant 수 | `Arrow` 속성 연결 |
| --- | --- | --- |
| `False` | 40 | **40건 전부 연결** ✅ |
| `True` | 40 | **0건** ❌ |

`Arrow`는 BOOLEAN 속성(기본 `true`)이고 **속성 패널에는 항상 보입니다.** 그런데 `Underline=True`를 고르면 화살표 레이어 자체가 없어 **토글해도 아무 일이 일어나지 않습니다.**

#### 사용자가 겪는 상황

1. Text Button을 놓고 `Arrow`를 켭니다 → 화살표가 보입니다
2. `Underline`을 `True`로 바꿉니다 → **화살표가 사라집니다**
3. `Arrow`를 다시 켜봅니다 → **아무 변화가 없습니다**

[Search Field](syrup-search-field-components.md)의 `Dot` 속성도 같은 유형이었는데, 그쪽은 **의도된 설계**로 확인됐습니다. 이 건도 **"밑줄 버튼에는 화살표를 쓰지 않는다"는 의도**일 수 있습니다.

| 선택지 | 내용 |
| --- | --- |
| A | 현행 유지 — 밑줄 버튼에 화살표를 쓰지 않는 것이 의도라면 |
| B | `Underline=True` 40개에도 화살표 추가 — **variant 40개를 수정** |

현재 사용 가이드에서는 밑줄과 화살표를 함께 표시하지 않는 기존 구조를 따르기로 정리했어요. 화살표가 필요하면 Underline=False에서 Arrow=True를 사용해요. 이 문서 업데이트에서 B안을 적용하거나 마스터를 변경하지 않았어요.

### 2. `Frame 1171277140` 1건

`Underline=True` 40개 variant의 텍스트 래퍼 프레임 이름입니다.

| 레이어명 | 건수 |
| --- | --- |
| `Text` | **39** |
| **`Frame 1171277140`** | **1** |

딱 하나만 기본 이름입니다 — **`Color=Primary_Orange, Size=XL, Underline=True, Bold=True`**.

Figma는 variant를 바꿀 때 **같은 이름의 레이어끼리 오버라이드를 이어받으므로**, 이 조합으로 바꾸면 텍스트 수정이 끊길 수 있습니다.

**`Text`로 바꾸면 됩니다. 모양은 바뀌지 않습니다.**

[Tab Bar](syrup-tab-bar-components.md)의 아이콘 인스턴스 레이어명 1건과 같은 유형입니다.

### 3. `XL` Regular 스타일 미적용 10건

| Size | Regular | Bold |
| --- | --- | --- |
| `XS` | `b500_13_regular` ✅ | `t1060_13_bold` ✅ |
| `S` | `b300_15_regular` ✅ | `t1000_15_bold` ✅ |
| `M` | `b100_17_regular` ✅ | `t800_17_bold` ✅ |
| **`XL`** | **없음** ❌ (25 Regular) | `t300_25_bold` ✅ |

네 사이즈 중 **`XL` Regular만 토큰이 없습니다.** `Color` 5종 × `Underline` 2종 = **10건**입니다.

25px는 **13px 하한보다 훨씬 크고 시스템이 관리해야 할 크기**라, 10~11px을 제외해 온 기준과 다릅니다. `XL` Bold에는 `t300_25_bold`가 이미 있으므로 **Regular 짝만 비어 있는 상태**입니다.

| 선택지 | 내용 |
| --- | --- |
| A | **`b?_25_regular` 토큰 신설** — Bold와 짝을 맞춤 |
| B | 현행 유지 — `XL` Regular를 쓰지 않을 계획이라면 |

**토큰 신설이 필요한 사안**이라 판단이 필요합니다.

### 4. `Size`에 `L`이 없음

| Size | 글자 크기 | 간격 |
| --- | --- | --- |
| `XS` | 13 | — |
| `S` | 15 | +2 |
| `M` | 17 | +2 |
| **`XL`** | **25** | **+8** |

`XS` → `S` → `M`은 2px씩 올라가다가 **`M` → `XL`에서 8px 건너뜁니다.** 사이에 들어갈 `L`이 비어 있습니다.

| 해석 | 판단 |
| --- | --- |
| `L`(19 또는 21)이 필요한데 빠짐 | 추가 검토 |
| `XL`이 제목용 특수 크기라 간격이 큰 것이 정상 | 이름을 `Title` 등으로 바꾸는 편이 정확 |

`XL`만 쓰임새가 다르다면 **크기 스케일이 아니라 역할 이름**이 어울립니다. 다만 `Size` 축의 다른 값과 섞여 있어 **지금 이름이 오해를 부릅니다.**

현재 Section 1에서는 XS·S 및 금액·개수 상세 보기용 XL Bold가 확인되었어요. 이번 가이드에는 그 사용처를 반영했으며, M을 제거하거나 L을 추가하지 않았어요.

### 5. 밑줄 두께 5종

| 두께 | 비고 |
| --- | --- |
| 1 | — |
| **1.25** | 비정수 |
| 1.5 | — |
| 2 | — |
| **2.5** | 비정수 |

Size와 Bold 조합에 따라 밑줄 두께가 달라집니다. 글자 크기에 비례해 굵어지는 방식으로 **설계 의도는 분명합니다.**

이 파일에는 **선 두께 토큰 자체가 없으므로**(토큰은 `Color` · `Spacing` · `Corner radius` 3종) 바인딩 대상이 아닙니다.

1.25 · 2.5는 비정수지만 **밑줄은 반픽셀 차이가 실제로 보이는 요소**라 의도적 값으로 보입니다. 변경 대상이 아닙니다.

### 6. `text` 소문자 레이어명 80건

| 레이어명 | 건수 | 위치 |
| --- | --- | --- |
| **`text`** | **80** | 모든 variant의 텍스트 |
| `Text` | 39 | `Underline=True`의 래퍼 프레임 |

**소문자 `text`와 대문자 `Text`가 한 컴포넌트 안에 공존합니다.** `Underline=True`에서는 `Text` 프레임 안에 `text` 텍스트가 들어가는 구조라, 레이어 패널에서 대소문자로만 구분됩니다.

| 제안 | 내용 |
| --- | --- |
| `text` → `Label` | 래퍼 `Text`와 확실히 구분 |
| `text` → `Text`, 래퍼 → `Underline` | 역할을 이름에 반영 |

80건을 한 번에 바꾸는 작업이고 **인스턴스 20건에 텍스트 오버라이드가 걸려 있을 수 있어** 주의가 필요합니다.

> **참고** — 레이어명 `Vector 34` 40건도 있으나, `Icon / Arrow` **인스턴스 내부**라 이 페이지의 정리 대상이 아닙니다.

### 7. 인스턴스 20건 — 2026-10-12 기록

| 페이지 | 건수 |
| --- | --- |
| [Card](syrup-card-components.md) | 6 |
| [List Row](syrup-list-row-components.md) | 4 |
| [Alert](syrup-alert-components.md) · [Bottom Info](syrup-bottom-info-components.md) | 각 3 |
| [Bottom CTA](syrup-bottom-cta-components.md) · [Button](syrup-button-components.md) · [List Header](syrup-list-header-components.md) · [Progress Stepper](syrup-progress-stepper-components.md) | 각 1 |

위 수치는 과거 컴포넌트 보드 점검 기준이에요. 현재 Section 1과 Guidelines·Usage 및 다른 페이지에 추가된 예제는 포함하지 않으므로 최신 사용량이나 변경 영향 범위로 해석하지 않아요.

| 영향 | 설명 |
| --- | --- |
| variant 이름 변경 | 인스턴스의 선택값이 따라가야 함 |
| 레이어명 변경 ([6](#6-text-소문자-레이어명-80건)) | 텍스트 오버라이드가 끊길 수 있음 |
| 구조 변경 ([1](#1-underlinetrue에서-arrow가-작동하지-않음)) | 20건 모두 영향 |

**이 페이지는 변경 비용이 다른 페이지보다 큽니다.**

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 이번 업데이트 (2026-11-10)

가이드라인 4개와 Usage A~F, 사용 유형·밑줄과 화살표·크기와 굵기·컬러 기준 및 Figma 링크를 추가했어요. Section 1의 아노테이션 54개를 제거하고 잔여 0개를 확인했어요. 기존 마스터 80개와 속성명은 유지했어요.

### 과거 점검의 후속 제안

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `Frame 1171277140` → `Text` ([2](#2-frame-1171277140-1건)) | **모양 안 바뀜 · 오버라이드 연결** | 낮음 |
| 2 | `XL` Regular 토큰 신설 ([3](#3-xl-regular-스타일-미적용-10건)) | **토큰 추가 — 판단 필요** | 중간 |
| 3 | `text` → `Label` 등 80건 ([6](#6-text-소문자-레이어명-80건)) | **인스턴스 20건 영향** | 중간 |
| 4 | `Size`의 `L` 공백 ([4](#4-size에-l이-없음)) | **스케일 설계 판단** | 중간 |
| 5 | `Underline=True`의 `Arrow` ([1](#1-underlinetrue에서-arrow가-작동하지-않음)) | 현재 사용 기준 유지 · 구조 변경은 별도 판단 | 높음 |
| — | 밑줄 두께 5종 ([5](#5-밑줄-두께-5종)) | 의도된 값 — 제외 | — |
| — | `Color` 값이 토큰명 ([설계 규칙](#color-값이-토큰-이름-그대로입니다)) | 의도된 선택 — 제외 | — |

**바로 처리 가능한 것은 1번 하나뿐입니다.** 토큰 적용이 이미 깨끗하고(미바인딩 색·수치 0건), 남은 과제가 대부분 **설계 판단**입니다.

현재 `Underline=True`에서는 화살표가 표시되지 않는 구조를 사용 기준으로 문서화했어요. 속성 패널의 Arrow 값만 보고 표시 여부를 판단하지 않아요. 구조 개선이 필요하면 기존 인스턴스에 미치는 영향을 별도로 확인해요.

토큰 면에서는 **[점검 3의 `XL` Regular](#3-xl-regular-스타일-미적용-10건)** 가 유일한 빈칸입니다. 25px는 시스템이 관리해야 할 크기이고 Bold 짝은 이미 있어, **Regular만 비어 있는 상태**입니다.
