# Syrup Design System — Banner 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Banner` 페이지 → [Banner 섹션 `8937:77046`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8937-77046) |
| 섹션 구성 | `Banner` 1440×1374 → `Guidelines` 960×1094 → `Usage` 1760×500 (가로 일렬) |
| 기준일 | 2026-11-04 (컷을 컴포넌트 인스턴스로 교체 · 색상 강조형 추가 / 토큰 정리: 2026-09-21) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **사용자에게 주요 정보나 혜택을 강조하여 안내하는 컴포넌트에요.**
> 프로모션, 이벤트, 서비스 안내 등 중요한 콘텐츠를 노출할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Banner / Images` | `8937:79669` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Banner — Master Component](#1-banner--master-component)
3. [Child Item — Banner / Images](#2-child-item--banner--images)
4. [설계 규칙 요약](#설계-규칙-요약)
5. [Usage](#usage)
6. [Guidelines](#guidelines)
7. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Banner` | **Component (단일)** | 없음 — BOOLEAN·SLOT으로 제어 | 328 × 86 |
| 2 | `Banner / Images` | Component Set | `Variant` 9종 | 70 × 70 |

Dialog·Alert·Badge와 달리 **Banner 본체에는 variant가 없습니다.** 표시 요소는 BOOLEAN 프로퍼티로, 이미지는 SLOT으로 갈아 끼우는 구조입니다.

---

## 1. Banner — Master Component

**Node** `8937:80935` · Component (단일) · **328 × 86**

### Properties

| Property | Type | Default | 역할 |
| --- | --- | --- | --- |
| `Image` | SLOT | — | 좌측 70 × 70 이미지 영역 |
| `Arrow` | BOOLEAN | `true` | 우측 이동 화살표 노출 |
| `Indicator` | BOOLEAN | `true` | 우상단 페이지 인디케이터 노출 |

### 내부 구조

| 영역 | 크기 | Padding (T/R/B/L) | Gap | 비고 |
| --- | --- | --- | --- | --- |
| 루트 `Banner` | 328 × 86 | 0 | 0 | VERTICAL · `Corner radius/400` (16) |
| `syrup_img_banner_` | 328 × 86 | `Spacing/200`(8) / `Spacing/300`(12) / `Spacing/200`(8) / `Spacing/400`(16) | `Spacing/200` (8) | HORIZONTAL · 배경 `Color/Gray_White` |
| └ `Image+Text` | 272 × 70 | 0 | `Spacing/100` (4) | HORIZONTAL |
| &nbsp;&nbsp;&nbsp;└ `Image` | 70 × 70 | — | — | **SLOT** — Images 컴포넌트 삽입 |
| &nbsp;&nbsp;&nbsp;└ `Text` | 198 × 42 | 0 | `Spacing/100` (4) | VERTICAL · `Title` + `Text` |
| └ `Icon / Arrow` | 20 × 20 | — | — | `Arrow` 프로퍼티로 토글 |
| `Indicator` | 16 × 13 | — | — | `Indicator` 프로퍼티로 토글 |

좌우 패딩이 **좌 16 / 우 12**로 다릅니다. 우측 화살표 아이콘의 여백을 시각적으로 보정한 것으로 보입니다.

### 텍스트

| 레이어 | 스타일 | 스펙 | 색상 | 폭 |
| --- | --- | --- | --- | --- |
| `Title` | `t900_16_bold` | 16 / 20 / −0.3 | `Color/Gray_100` (#222222) | FILL |
| `Text` | `b500_13_regular` | 13 / 18 / 0 | `Color/Gray_250` (#555555) | FILL |

둘 다 LEFT 정렬이고 `FILL`이라 배너 폭이 바뀌어도 리플로우됩니다. 두 텍스트 모두 **로컬 텍스트 스타일이 적용**되어 있습니다.

### Indicator

`Indicator` → `.primitive / Indicator / Number` 인스턴스(16 × 13). `1 / 2` 형태로 현재 위치를 표시합니다.

| 요소 | 색상 |
| --- | --- |
| 현재 번호 | `Color/Gray_Black` |
| 구분자 `/` · 총 개수 | `Color/Gray_500` |

텍스트는 11px Regular이며 스타일이 적용되어 있지 않습니다. 다만 이 텍스트는 **Indicator 컴포넌트 소속**이므로 Banner가 아니라 `Indicator` 페이지에서 관리해야 합니다.

---

## 2. Child Item — Banner / Images

**Node** `8937:79669` · Component Set · 전 variant **70 × 70** 고정

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `금받는미션` | 9종 (아래) |

| Variant | 구성 레이어 | 에셋 종류 |
| --- | --- | --- |
| `금받는미션` | `Image` | 프레임 |
| `지금뭐먹지` | `syrup_img_place` | 래스터 |
| `간식데이` | `도장러비 1` + `하트0000 1` + `Frame 3467899` | 래스터 + 프레임 |
| `쇼핑가이드` | `image 3259` + `logo` | 래스터 + **벡터** |
| `Npay` | `3배 1` | 래스터 |
| `첫구매이벤트` | `Group 1171276979` | **벡터 그룹** |
| `황금티켓` | `image 3255` | 래스터 |
| `황금알` | `egg_g` | 래스터 |
| `엔제리너스` | `image 3341` | 래스터 |

- 9종 모두 **오토레이아웃 없이 고정 배치**입니다.
- 대부분 래스터 이미지이고, 벡터가 들어간 것은 `쇼핑가이드`(Syrup 로고)와 `첫구매이벤트` 둘뿐입니다.
- Variant 이름이 전부 **캠페인 고유명**입니다. UI 상태가 아니라 콘텐츠를 variant로 관리하는 구조입니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 크기 | **328 × 86 고정** |
| 모서리 | `Corner radius/400` (16) |
| 배경 | `Color/Gray_White` |
| 패딩 | 8 / 12 / 8 / 16 |
| 이미지 영역 | 70 × 70 (SLOT) |
| 이미지–텍스트 간격 | `Spacing/100` (4) |
| 타이틀 | `t900_16_bold` / `Color/Gray_100` |
| 본문 | `b500_13_regular` / `Color/Gray_250` |
| 선택 요소 | 화살표 20 × 20 · 인디케이터 16 × 13 |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11204:22`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11204-22) · 1760 × 500 |
| 구성 | 4패턴 · 폭 360 · 높이는 내용에 맞춰 202~300 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-04).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 가로 간격은 40입니다.

Banner는 **variant가 없어** 생김새가 하나입니다. 그래서 **몇 장을 어떻게 두는지**로 A~C를 나눴고, 여기에 **색을 바꿔 쓰는 경우**인 D가 붙습니다.

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **A** | 단독 | 묶음에 배너를 한 장만 둬요. 가장 흔한 쓰임이고, 넘겨 볼 게 없으니 인디케이터는 꺼 둬요. | `Banner` × 1 · `Indicator=false` | 86 |
| **B** | 세로 나열 | 성격이 비슷한 배너 두 장을 동시에 보여줄 때 사용해요. 세로로 배치하고 사이 간격은 12로 둬요. 인디케이터는 꺼 둬요. | `Banner` × 2 · 슬롯 간격 **12** | 184 |
| **C** | 캐러셀 | 여러 배너를 한 자리에서 넘겨 보여줄 때 사용해요. 두 장 이상일 때 인디케이터를 켜고, 현재 위치와 전체 장수를 표시해요. | `Banner` × 1 · `Indicator=true` 「1 / 2」 | 86 |
| **D** | 색상 강조형 | 프로모션이나 이벤트를 눈에 띄게 안내할 때 사용해요. 배경색에 맞춰 텍스트와 화살표 색상을 함께 조정해요. | `Banner` × 1 · 배경 **`#ABC436`** · 흰 텍스트 | 86 |

컷에 쓴 문구와 이미지는 제품 화면 그대로입니다 — A는 `엔제리너스`, B는 `황금티켓` + `황금알`, C는 `쇼핑가이드`, D는 `지금뭐먹지`입니다.

**`Arrow`는 네 패턴 모두 `true`입니다.** 끄는 경우가 없어 패턴을 가르는 축이 되지 못하고, 대신 [Guidelines 1](#1-배너에는-화살표를-켜-둬요)로 올라가 있습니다.

### D. 색상 강조형 — 같은 컴포넌트에 색만 덮습니다

마스터는 A~C와 같은 `Banner` [`8937:80935`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8937-80935)입니다. **variant가 아니라 인스턴스 오버라이드**로 만든 형태라, 컴포넌트 쪽에는 색상 축이 없습니다.

| 항목 | 기본형 (A · B · C) | 색상 강조형 (D) |
| --- | --- | --- |
| 카드 배경 | `Color/Gray_White` | **`#ABC436`** — ⚠️ 토큰 없음 |
| 타이틀 | `Color/Gray_100` (#222222) | `Color/Gray_White` (#FFFFFF) |
| 본문 | `Color/Gray_250` (#555555) | `Color/Gray_White` |
| 화살표 | stroke `Color/Gray_200` (#464646) | stroke `Color/Gray_White` |
| 텍스트 스타일 | `t900_16_bold` · `b500_13_regular` | **같음** — 색만 덮음 |
| 이미지 | `Banner / Images` `8937:79669` | **원격 세트 `11190:27555`** |

텍스트 스타일은 그대로 두고 **색만 덮은** 점이 좋습니다. 크기·굵기·자간이 기본형과 어긋나지 않습니다.

**색은 양쪽 다 토큰을 가리킵니다** — 기본형이 `Gray_100`·`Gray_250`·`Gray_200`을 쓰듯, 색상 강조형은 세 곳 모두 `Color/Gray_White`에 바인딩되어 있습니다 (2026-11-04 정리).

남은 것은 둘입니다. 배경 `#ABC436`은 **Syrup 팔레트에 없는 값**이라 바인딩할 토큰이 없고, 이미지가 이 페이지의 로컬 세트가 아니라 **다른 파일의 원격 세트**를 가리킵니다 → [점검 9](#9-색상-강조형--배경색-토큰만-남았습니다) · [점검 1](#1-이미지-공급-경로가-두-갈래)

### 맥락 컴포넌트를 넣지 않았습니다

Badge와 정반대입니다. [Badge](syrup-badge-components.md)는 328건 중 280건이 다른 컴포넌트 안에 들어 있어 다섯 컷 모두 맥락을 끼고 있는데, **Banner는 중첩이 한 건도 없습니다.**

| | 직접 배치 | 다른 컴포넌트 안 |
| --- | --- | --- |
| Banner | **41** | **0** |

배너는 언제나 디자이너가 화면에 직접 놓습니다. 그래서 컷도 **`Banner` 인스턴스만** 담았습니다. 네 패턴을 가르는 것이 장 수 · `Indicator` 값 · 색 세 가지뿐이라, 주변을 두어도 보이는 게 늘지 않습니다.

**B의 두 장은 슬롯의 세로 간격을 12로 바꿔 쌓았습니다.** 래퍼 프레임 없이 슬롯이 직접 간격을 냅니다.

### 제품 파일 실측 (2026-11-04)

제품 파일 [`Syrup_App`](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i/Syrup_App) 전체를 다시 세어 **41건**입니다. 그중 **12건이 「🛍️ 쇼핑적립 아이데이션」 페이지**라, 제품 기준은 **29건**입니다. 아래는 아이데이션을 뺀 29건입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| `Arrow` | `true` | **29 / 29** |
| `Indicator` | `false` | 22 |
| | `true` | 7 — 전부 「쇼핑 적립」 페이지 |
| 한 묶음 안 배너 수 | 1장 | 19묶음 |
| | 2장 | 5묶음 |
| | 3장 이상 | **0** |
| 2장일 때 간격 | `12` | **5 / 5** |

세 가지가 분명합니다. **`Arrow`는 예외가 없고**, **한 묶음은 두 장을 넘지 않으며**, **쌓을 때 간격은 언제나 12**입니다. 앞의 둘은 [Guidelines](#guidelines)로 올렸고, 간격 12는 Usage **B**에 들어 있습니다.

`Indicator=true` 7건은 **전부 「쇼핑 적립」 페이지의 캐러셀**이고, 모두 **묶음 1장**입니다. 캐러셀은 파일 안에서 배너 한 장으로 그리고 장 수는 인디케이터 숫자로만 표시하기 때문입니다. Usage **C**가 그 형태입니다.

> 앞서 「28건」으로 적었던 것은 **아이데이션 페이지를 뺀 수**였습니다. 이번에 한 건이 늘어 29건이 되었습니다.
>
> **색상 강조형은 제품 파일 29건에 없습니다.** 세어 본 배너는 전부 흰 배경입니다. D와 Guidelines 3은 실측이 아니라 **앞으로의 허용 범위를 정한 것**입니다.

### 위치는 규칙이 아닙니다

처음에는 「영역 맨 위」와 「영역 끝」을 패턴으로 나눴다가 **뺐습니다.** 시스템에 정의된 규칙이 아니고, 수집본에서 「맨 위」가 1건뿐이라 **없는 구분을 만든 것**이었습니다.

이번 실측에서도 **자리를 정한 규칙은 나오지 않았습니다** — 쿠폰 화면에서는 리스트 아래, 출석체크에서는 섹션 헤더 아래, 쇼핑 탭에서는 콘텐츠 사이에 들어갑니다. 참고용 관찰이지 지켜야 할 규칙이 아닙니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11204:31`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11204-31)** (960 × 1094) 에 한 쌍씩 들어 있습니다. 규칙이 2개에서 **3개**로 늘었습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다. 세로 간격은 102입니다.

**Banner에 variant가 없어 규칙도 전부 「같은 배너에서 한 가지만 다름」 형태입니다.** 1은 `Arrow`, 2는 `Indicator`, 3은 색입니다.

### 1. 배너에는 화살표를 켜 둬요

배너는 눌러서 다른 화면으로 이동하는 컴포넌트예요.
이동할 수 있음을 알 수 있도록 화살표를 항상 표시해요.

| | 내용 |
| --- | --- |
| **Do** | `Arrow = true` — 오른쪽에 `>` |
| **Don't** | `Arrow = false` — 오른쪽이 비어 눌러지는지 알 수 없음 |

두 컷 모두 `지금뭐먹지` 이미지에 「지금 뭐 먹지? / 맛집과 상품 구경하기」입니다. 제품 파일 **41건이 예외 없이 `true`** 이고, 끈 사례가 하나도 없습니다.

### 2. 인디케이터는 캐러셀에 두 장 이상 있을 때만 켜요

여러 장을 넘겨 보는 캐러셀에서 현재 위치와 전체 장수를 표시해요.
한 장뿐이거나 세로로 나열한 배너에는 인디케이터를 표시하지 않아요.

| | 컷 | 인디케이터 |
| --- | --- | --- |
| **Do** | 캐러셀 — 「쇼핑 적립이 처음이라면?」 | `true` · **「1 / 2」** |
| **Don't** | 한 장뿐인 배너 — 「엔제리너스 라떼게임」 | `true` · **「1 / 1」** |

**두 컷의 차이는 인디케이터 숫자뿐입니다.** 한 장짜리에 켜면 전체 장 수가 자기 자신이라 「1 / 1」이 되는데, 이게 Don't의 증상입니다.

설명이 **「세로로 나열한 배너」까지 짚어 준 점**이 중요합니다. Usage **B**처럼 두 장을 쌓는 것은 「두 장 이상」이지만 넘겨 보는 게 아니라서 인디케이터를 켜지 않습니다. 제품 파일에서도 2장 묶음 5건이 **전부 `false`** 입니다.

인디케이터 숫자는 **기본값이 `1 / 2`** 라 켜는 순간 장 수를 손으로 맞춰야 합니다. 이 텍스트의 스타일 문제는 [점검 5](#5-indicator-숫자-텍스트)에 있습니다.

### 3. 강조가 필요한 배너는 색상을 변경할 수 있어요

프로모션이나 이벤트의 주목도를 높일 때는 배경색과 텍스트 색상을 변경할 수 있어요.
텍스트와 화살표가 배경에서 명확히 보이도록 색상을 함께 조정해요.

| 라벨 | 컷 | 배경 | 텍스트 · 화살표 |
| --- | --- | --- | --- |
| **기본형** | 「지금 뭐 먹지?」 | `Color/Gray_White` | `Gray_100` · `Gray_250` · stroke `Gray_200` |
| **색상 강조형** | 같은 문구 | **`#ABC436`** (토큰 없음) | 셋 다 `Color/Gray_White` |

**이 규칙만 Do / Don't가 아닙니다.** 슬롯 라벨을 「기본형」·「색상 강조형」으로 바꿔 **둘 다 쓸 수 있는 두 경우를 나란히** 놓았습니다. 금지가 아니라 **허용 범위를 정하는 규칙**이라서입니다. Badge 규칙 1과 같은 방식입니다.

규칙이 요구하는 것은 **색을 쌍으로 바꾸는 것**입니다. 배경만 어둡게 하고 텍스트를 #222222로 두면 읽히지 않습니다. 컷의 두 배너는 배경·타이틀·본문·화살표 **네 가지가 모두 함께** 바뀌어 있습니다.

다만 바꿀 수 있는 **색의 범위는 아직 정해지지 않았습니다** → [점검 9](#9-색상-강조형--배경색-토큰만-남았습니다)

---

## 점검 필요 사항

### 1. 이미지 공급 경로가 두 갈래

Banner 본체는 `Image`를 **SLOT**으로 열어 두었고, 동시에 `Banner / Images` **Component Set**도 존재합니다. 신규 캠페인을 추가할 때 두 가지 방법이 가능합니다.

| 방법 | 장점 | 단점 |
| --- | --- | --- |
| Images에 variant 추가 | 목록이 한곳에 모임 | 캠페인마다 컴포넌트가 늘어남 |
| SLOT에 직접 삽입 | 컴포넌트 증식 없음 | 어떤 이미지가 쓰이는지 추적 어려움 |

현재 9개 variant가 모두 캠페인 고유명(`금받는미션` · `황금알` · `엔제리너스` …)이라 **캠페인이 늘수록 계속 증가하는 구조**입니다. 어느 쪽을 표준으로 할지 정해 두는 편이 좋습니다.

#### 세 번째 갈래가 생겼습니다 (2026-11-04)

Usage **D**와 Guidelines **3**의 색상 강조형 배너가 쓰는 이미지는 이 페이지의 세트가 아닙니다.

| | 세트 | 소속 | variant | 프로퍼티 이름 |
| --- | --- | --- | --- | --- |
| A · B · C · 규칙 1 · 2 | `8937:79669` | **로컬** — Banner 페이지 | 9종 | `Variant` |
| **D · 규칙 3 (색상 강조형)** | **`11190:27555`** | **원격** — 다른 파일의 라이브러리 | 8종 (`엔제리너스` 없음) | **`Property 1`** |

**이름이 `Banner / Images`로 똑같습니다.** 레이어 패널에서는 구분되지 않고, 프로퍼티 이름(`Variant` vs `Property 1`)으로만 갈립니다. 제품 화면에서 배너를 복사해 오면서 원격 세트 참조가 함께 딸려 온 것으로 보입니다.

로컬 세트의 인스턴스로 바꿔 끼우면 정리됩니다. `지금뭐먹지`는 양쪽에 다 있어 **같은 그림으로 교체할 수 있습니다.**

### 2. 로고 컬러가 브랜드 토큰과 다름

`Variant=쇼핑가이드`의 `logo` 벡터 5개가 **#FF5700**을 쓰고 있습니다. 브랜드 토큰 `Color/Primary_Orange`는 **#FF6315**로 서로 다른 값입니다.

| 노드 | 크기 |
| --- | --- |
| `SVGID` (`8937:79676`) | 6 × 7 |
| `Vector` (`8937:79677`) | 6 × 9 |
| `Vector` (`8937:79678`) | 6 × 9 |
| `Vector` (`8937:79679`) | 4 × 7 |
| `Vector` (`8937:79680`) | 6 × 7 |

로고 에셋이라 UI 토큰화 대상은 아니지만, **로고 원본의 오렌지와 브랜드 토큰이 다른 값인지** 확인이 필요합니다. AD 컴포넌트에서도 같은 #FF5700이 발견된 적이 있습니다.

### 3. 일러스트 내부 미바인딩 색상

`Variant=첫구매이벤트`의 `Union`(`8937:79688`, 12 × 3)이 **#FCE8E1**을 씁니다. 일러스트 내부 색이라 토큰화 대상은 아닙니다.

### 4. 좌우 패딩 비대칭

좌 `Spacing/400`(16) / 우 `Spacing/300`(12)입니다. 화살표 아이콘의 광학적 여백을 맞춘 의도로 보이나, 의도라면 컴포넌트 설명에 남겨 두는 편이 좋습니다.

### 5. Indicator 숫자 텍스트

11px Regular에 텍스트 스타일이 적용되어 있지 않습니다. Syrup의 11px은 `c200_11_regular`(11 / 16 / −0.3)인데 이 텍스트는 line-height AUTO / letter-spacing 0입니다. **Indicator 컴포넌트 소속**이므로 해당 페이지에서 함께 정리해야 합니다.

### 6. 폭은 화면 폭을 따라갑니다 — 높이 1건만 이탈 (2026-11-04 재측정)

컴포넌트는 `328 × 86`이지만 제품 파일 29건의 실제 치수는 이렇습니다.

| 폭 | 건수 | | 높이 | 건수 |
| --- | --- | --- | --- | --- |
| 328 | 17 | | 86 | **28** |
| 288 | 5 | | **75.5** | **1** |
| 370 | 3 | | | |
| 688 | 3 | | | |
| 600 | 1 | | | |

**폭이 갈리는 이유는 화면 폭입니다.** 한 부모 프레임 안에 같은 화면이 폭만 바꿔 여러 벌 들어 있습니다 — 「금 모으는 쿠폰」 4건이 한 프레임 안에서 328 · 688 · 288 · 328이고, 「출석체크」 5묶음도 328 · 370 · 688 · 288 · 328입니다. 좌우 여백 16씩을 빼면 **288 = 320폭 · 328 = 360폭 · 370 = 402폭** 화면입니다.

**손으로 줄인 게 아니라 컨테이너를 따라간 것**이라, 폭은 이탈이 아닙니다. 「288 · 370은 왜 다른지 확인이 필요하다」고 남겨 두었던 항목은 이것으로 **해소**되었습니다.

**높이 `75.5` 1건은 여전히 이탈입니다.** 나머지 28건이 모두 86인데 한 건만 어긋났습니다. Banner는 [Border](syrup-border-components.md)·[AD](syrup-ad-components.md)와 달리 **높이 86이 고정**이어야 하는 컴포넌트입니다.

### 7. 페이지 잔여물 (2026-11-04 갱신)

| 노드 | 상태 |
| --- | --- |
| `Frame 3467848` `11190:28539` (`COMPONENT`) | ✅ **사라졌습니다** — 페이지의 로컬 컴포넌트 세트는 `Banner / Images` 하나뿐입니다 |
| `원본 컷 (정리 전)` `11238:636` | ✅ **삭제되었습니다** — 컷 14개와 함께 정리되었습니다 |
| `러비` `8937:81045` | ✅ **삭제되었습니다** — 섹션 밖에 떠 있던 캐릭터 일러스트 조각 ([점검 10](#10--레이어-이름--페이지-잔여물-정리-2026-11-04-완료)) |

**세 건 모두 정리되어 페이지에 잔여물이 없습니다.**

### 8. 토큰 상태 (2026-11-04 갱신)

| 항목 | 결과 |
| --- | --- |
| 미바인딩 radius | **0건** |
| 미바인딩 gap | **0건** |
| 미바인딩 padding | 4건 — 섹션 레이아웃 프레임(`100`), 컴포넌트와 무관 |
| 미바인딩 fill | 일러스트·로고 내부 6건 (위 2 · 3번) + **색상 강조형 배경 2건** (아래 9번) |
| 스타일 미적용 / 원격 스타일 텍스트 | **0건** |
| 외부 토큰 | `Spec docs/margin` 4 · paragraph 계열 2 (전역 이슈) |

**컴포넌트 자체의 spacing · radius · 타이포는 전부 Syrup 토큰과 로컬 스타일로 정리되어 있습니다.** 색상도 2026-11-04에 바인딩을 마쳐, 남은 미바인딩은 **일러스트 내부와 `#ABC436` 배경뿐**입니다.

### 9. 색상 강조형 — 배경색 토큰만 남았습니다

Usage **D**와 Guidelines **3**의 색상 강조형은 `Banner` 마스터의 인스턴스에 **색을 직접 덮어** 만든 것입니다. variant가 아니라 오버라이드입니다.

| 덮어쓴 값 | 토큰 | 상태 |
| --- | --- | --- |
| 타이틀 `#FFFFFF` | `Color/Gray_White` | ✅ **바인딩 완료** (2026-11-04) |
| 본문 `#FFFFFF` | `Color/Gray_White` | ✅ 완료 |
| 화살표 stroke `#FFFFFF` | `Color/Gray_White` | ✅ 완료 |
| 카드 배경 `#ABC436` | ❌ **없음** | 팔레트에 같은 값도, 가까운 초록 계열도 없음 |

흰색 세 곳은 값이 `Color/Gray_White`와 같아 **무손실로 바인딩**했습니다. 두 인스턴스(Usage D · 규칙 3) 모두 적용해 **6건**입니다. 이제 기본형이 `Gray_100`·`Gray_250`·`Gray_200`을 가리키듯 강조형은 세 곳 모두 `Gray_White`를 가리켜, **양쪽이 토큰 대 토큰으로 대응**합니다.

**배경 `#ABC436`만 바인딩하지 못했습니다.** 변수 컬렉션 `global`의 색상 31개를 전부 확인했지만 같은 값이 없고, 근사한 초록 계열도 없습니다. 없는 토큰을 만드는 것은 팔레트를 늘리는 결정이라 손대지 않았습니다.

Guidelines 3이 「변경할 수 있어요」라고 **허용하는** 규칙이라, 범위를 정해 두지 않으면 캠페인마다 제각각의 색이 생깁니다. 방향은 둘입니다.

| 방향 | 내용 |
| --- | --- |
| **토큰 + variant** | 강조 배경색을 팔레트에 올리고 `Banner`에 색상 축을 추가. 쓸 수 있는 색이 고정됨 |
| **쌍만 고정** | 배경색은 캠페인 자유로 두되, 「텍스트·화살표는 `Color/Gray_White`」처럼 **함께 바뀌어야 하는 쌍**만 규칙으로 못 박음 |

**둘째 방향은 이미 절반 성립합니다** — 텍스트·화살표 쪽이 토큰에 묶였으니, 배경만 캠페인 색으로 두면 규칙이 지켜집니다. 제품 파일 29건에는 색상 강조형이 아직 하나도 없어, 지금 정하면 첫 사례부터 맞출 수 있습니다.

### 10. ✅ 레이어 이름 · 페이지 잔여물 정리 (2026-11-04 완료)

| 항목 | 결과 |
| --- | --- |
| `11304:2826` | `B. 두 개를 연달아` → **`B. 세로 나열`** |
| `11304:2982` | `2. 인디케이터는 넘겨 볼 게 있을 때만 켜요` → **`2. 인디케이터는 캐러셀에 두 장 이상 있을 때만 켜요`** |
| `러비` `8937:81045` | **삭제** — 섹션 밖에 떠 있던 `GROUP`(119.7 × 120.6, 조각 3개) |

레이어 이름 넷과 셋이 모두 화면에 보이는 제목과 같아졌습니다. 페이지 최상위에는 이제 **`Banner` · `Guidelines` · `Usage` 세 섹션만** 남습니다.
