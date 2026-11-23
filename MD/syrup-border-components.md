# Syrup Design System — Border 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Border` 페이지 → [Border 섹션 `9094:42146`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9094-42146) |
| 섹션 구성 | `Border` 1440×911 → `Guidelines` 960×1708 → `Usage` 960×888 (가로 일렬) |
| 기준일 | 2026-11-04 (컷을 컴포넌트 인스턴스로 교체 / 토큰 정리: 2026-09-21) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **요소의 경계나 구분을 명확히 보여주는 컴포넌트에요.**
> 컨테이너나 콘텐츠 구획을 구분해야 하는 경우에 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Border — Master Component](#1-border--master-component)
3. [Usage](#usage)
4. [Guidelines](#guidelines)
5. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

지금까지 문서화한 컴포넌트 중 **가장 단순한 구성**입니다. Child Item 없이 컴포넌트셋 하나뿐입니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Border` | Component Set | `Height` 2종 | 360 × 1 · 360 × 10 |

---

## 1. Border — Master Component

**Node** `10301:5605` · Component Set · 2 variants

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Height` | VARIANT | `Thick` | `Thin` · `Thick` |

### Variants

| Variant | 크기 | 배경 | Radius | 용도 |
| --- | --- | --- | --- | --- |
| `Height=Thin` | 360 × **1** | `Color/Gray_850` (#EDEDED) | 0 | 리스트 행 사이의 얇은 구분선 |
| `Height=Thick` | 360 × **10** | `Color/Gray_950` (#F6F6F7) | 0 | 섹션 사이를 나누는 두꺼운 구획 바 |

### 구조

- 내부 자식 레이어가 없습니다. 컴포넌트 자체의 `fills`로 선을 표현합니다.
- 오토레이아웃 없음. 폭·높이 모두 **`FIXED`** 입니다.
- 두 variant 모두 색상이 `Color/*` 베리어블에 바인딩되어 있습니다.

> **2026-09-21 변경** — variant 이름을 정정하고 1px 선의 색상을 교체했습니다.
>
> | 항목 | 변경 전 | 변경 후 |
> | --- | --- | --- |
> | 1px variant 이름 | `Height=Thick` | **`Height=Thin`** |
> | 10px variant 이름 | `Height=Default` | **`Height=Thick`** |
> | 1px variant 색상 | `Color/Gray_950` (#F6F6F7) | **`Color/Gray_850`** (#EDEDED) |
>
> 이름이 실제 두께와 반대로 붙어 있던 문제와, 1px 선이 흰 배경에서 보이지 않던 문제를 함께 해결했습니다. 10px variant는 면적이 넓어 구획이 충분히 인지되므로 `Color/Gray_950`을 유지했습니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11194:22`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11194-22) · 960 × 924 |
| 구성 | 2패턴 · 폭 360 · 높이 425 · 724 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-04).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 가로 간격은 40입니다.

**Border는 맥락이 없으면 아무것도 보여 주지 못합니다.** 생김새가 10px 회색 면 하나뿐이라, 단독 컷은 회색 띠 한 줄입니다. 보여 줄 것이 모양이 아니라 **자리**이기 때문에 두 컷 모두 앞뒤 블록을 함께 담았습니다.

| | 패턴 | 설명 | 슬롯에 담은 것 | 슬롯 높이 |
| --- | --- | --- | --- | --- |
| **A** | 새 영역의 시작 | 새 콘텐츠 영역이 시작되는 바로 위에 배치해요. 앞선 콘텐츠와 구분해 새로운 영역의 시작을 알려줘요. | `Border` + 묶음 1개 | 309 |
| **B** | 묶음 사이 | 성격이 다른 콘텐츠 묶음 사이에 배치해요. 각 묶음이 별개의 영역임을 보여줘요. | 묶음 + `Border` + 묶음 | 608 |

**A는 `Border`가 맨 위에 있고, B는 가운데 있습니다.** 이 차이가 두 패턴의 전부이며, 제품 파일에서도 구조로 그렇게 갈립니다 (아래 실측).

### 컷을 이루는 것

컷의 뼈대는 **제품 화면의 묶음 구조를 그대로 옮긴 것**입니다. 레이어 이름(`Frame 1171277328` · `Title` · `Frame 1171276960`)까지 제품 파일과 같아, 실제 화면에서 떼어 온 자리 그대로입니다.

| 역할 | 쓴 것 | 크기 |
| --- | --- | --- |
| 구분선 | **`Border` ▸ `Height=Thick`** — 문서화 대상 | 360 × 10 |
| 묶음 | 흰 바탕 프레임 (`Frame 1171277328` · `1171277329`) | 360 × 299 |
| └ 제목 영역 | `Title` 프레임 — 상하 여백 20 · 좌우 24 | 360 × 64 |
| &nbsp;&nbsp;&nbsp;└ 제목 | `List Header` ▸ `Padding=0` · `Title Acc=Info` · `Tailing Acc=AD` | 312 × 24 |
| └ 본문 영역 | `Frame 1171276960` — 아래 여백 24 | 360 × 235 |
| &nbsp;&nbsp;&nbsp;└ 상품 | `Product Grid / Naver` ▸ `Variant=2column` (`Grid List Item` 2개) | 360 × 211 |

묶음 문구는 제품 화면과 같은 **「11번가 상품 추천」 · 「쿠팡 상품 추천」**이고, A에는 쿠팡 묶음 하나만 들어갑니다.

**묶음 프레임 자체가 흰 바탕입니다.** `Thick`의 색이 `Color/Gray_950`(#F6F6F7)이라 **흰 배경에서만 또렷**하기 때문에, 컷이 섹션 배경에 기대지 않습니다 → [점검 7](#7-thick의-대비는-흰-배경-전용입니다)

### 제품 파일 실측 (2026-11-04)

제품 파일 [`Syrup_App`](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i/Syrup_App) 기준 **15건**입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 중첩 | 다른 컴포넌트 안 | **0** |
| | 직접 배치 | **15** |
| variant | `Height=Thick` | **15 / 15** |
| 높이 | `10` | **15 / 15** |
| 폭 | 360 | 12 |
| | 320 · 402 · 720 | 각 1 |

**중첩이 0건이라 Border는 늘 디자이너가 직접 놓습니다.** [Banner](syrup-banner-components.md)와 같고 [Badge](syrup-badge-components.md)와 반대입니다. 다만 Banner와 달리 **컷에는 맥락이 필요합니다** — 직접 놓는다는 것과 혼자서 읽힌다는 것은 다른 이야기입니다.

자리는 앞뒤 형제 노드로 판정했습니다.

| 자리 | 판정 | 건수 |
| --- | --- | --- |
| **A — 컨테이너의 첫 자식** | 앞 형제 없음 | **7** |
| **B — 블록과 블록 사이** | 앞뒤 형제 모두 있음 | **8** |
| 컨테이너의 마지막 자식 | 뒤 형제 없음 | **0** |

**「맨 뒤」는 이번에도 0건입니다.** Border는 영역을 열거나 가르는 자리에만 쓰이고, 닫는 데에는 쓰이지 않습니다.

> 다만 **A의 7건이 서로 다른 7개 자리는 아닙니다.** 6건이 「파워쇼핑」 블록 앞 한 자리를 폭만 바꿔 복제한 것(360 셋 · 320 · 402 · 720)이고, 나머지 1건이 「네이버 플레이스」 앞입니다. B의 8건도 「오늘의 상품 검색」 6 · PLACE SA 1 · 「쇼핑 적립」 1입니다. **자리의 가짓수로 세면 A 2곳 · B 3곳**입니다. 건수가 자리 수를 부풀리고 있다는 점은 감안해야 합니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11194:29`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11194-29)** (960 × 1828) 에 Do / Don't 한 쌍으로 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 `Do` · `Don't` **슬롯**이 좌우로 들어갑니다. 세로 간격은 100입니다.

**네 컷 모두 Usage **B**와 같은 묶음을 씁니다** — 「11번가 상품 추천」 + `Border` + 「쿠팡 상품 추천」([컷을 이루는 것](#컷을-이루는-것) 참고). 묶음이 같으니 **규칙마다 달라지는 것이 `Border` 하나로 좁혀집니다** — 1은 폭, 2는 개수입니다.

### 1. 컨테이너의 전체 폭을 채워요

높이는 10으로 유지하고, 너비는 컨테이너에 맞춰요.
좌우 여백 없이 배치해 영역 사이의 경계가 명확하게 보이도록 해요.

| | 내용 |
| --- | --- |
| **Do** | 컨테이너 폭 그대로 — `360 × 10` |
| **Don't** | 좌우를 16씩 띄워 `328 × 10` — 양옆에 흰 틈이 남음 |

두 컷은 묶음 두 개 사이에 `Border`를 끼운 **완전히 같은 구성**이고, 차이는 `Border`의 폭 하나입니다. Don't에서는 좌우 끝에 흰 틈이 남아 구획이 묶음 폭을 다 끊지 못합니다.

제품 파일 15건의 폭은 **320 · 360 · 402 · 720** 네 가지인데 **높이는 전부 10**입니다. 폭은 화면을 따라가고 높이는 고정이라는 뜻입니다. 지금은 그 폭을 손으로 맞추고 있습니다 → [점검 4](#4-폭이-fixed-360)

### 2. 서로 다른 콘텐츠 묶음 사이에 사용해요

같은 묶음에 속한 항목 사이에는 Border를 넣지 않아요.
하나의 묶음이 서로 다른 영역으로 나뉘어 보일 수 있어요.

| | `Border` 개수 | 놓인 자리 |
| --- | --- | --- |
| **Do** | **1개** | 「11번가 상품 추천」과 「쿠팡 상품 추천」 **사이** |
| **Don't** | **3개** | 묶음 사이 + 각 묶음의 **제목과 상품 사이** |

Don't에서는 제목이 묶음에서 떨어져 나와 두 묶음이 네 덩어리로 보입니다. 같은 컴포넌트를 더 썼을 뿐인데 영역의 뜻이 바뀝니다.

항목 사이를 나눠야 한다면 10px 면이 아니라 1px 선(`Thin`)의 자리입니다. 다만 `Thin`은 아직 쓰인 적이 없습니다 → [점검 5](#5-thin이-한-번도-쓰이지-않았습니다)

---

## 점검 필요 사항

### 1. ✅ Variant 이름이 실제 값과 반대 (2026-09-21 정정 완료)

`Thick`(두꺼운)이 1px, `Default`가 10px로 **이름이 실제 두께와 반대**였습니다. 처음 쓰는 사람이 틀린 쪽을 고르기 쉬운 상태였습니다.

| 실제 높이 | 변경 전 이름 | 변경 후 이름 |
| --- | --- | --- |
| 1px | `Thick` | **`Thin`** |
| 10px | `Default` | **`Thick`** |

이름 충돌을 피하려고 1px을 먼저 `Thin`으로 바꾼 뒤 10px을 `Thick`으로 옮겼습니다. 프로퍼티 기본값은 `Thick`(10px)으로, 변경 전 `Default`가 가리키던 것과 같은 variant입니다.

### 2. ✅ 1px 선의 대비가 지나치게 낮음 (2026-09-21 수정 완료)

`Color/Gray_950`(**#F6F6F7**)은 흰 배경(#FFFFFF)과 채널 차이가 **9/255 (약 3.5%)** 뿐이라, 1px 선이 흰 배경에서 사실상 보이지 않았습니다.

| Variant | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Thin` (1px) | `Color/Gray_950` #F6F6F7 | **`Color/Gray_850` #EDEDED** |
| `Thick` (10px) | `Color/Gray_950` #F6F6F7 | 유지 |

`Gray_850`은 흰 배경과 채널 차이 **18/255 (약 7%)** 로 두 배 진해집니다. 파일 내에서 직접 그려진 얇은 구분선들이 쓰던 값과도 일치합니다.

10px variant는 면적이 넓어 옅은 색으로도 구획이 인지되므로 `Color/Gray_950`을 그대로 두었습니다.

> **구분선 표준 토큰은 `Color/Gray_850`으로 확정되었습니다** (2026-09-21). 이전에 토큰 문서에서 `Color/Gray_750`(#DDDDDD)에 붙어 있던 "구분선 · 보더" 용도 메모는 `Gray_850`으로 옮겼습니다. [syrup-design-tokens.md](syrup-design-tokens.md)의 Gray Scale 표 참고.

### 3. 사용처 — 「0건」 정정 (2026-11-02)

이전에 **「인스턴스가 파일 전체에 하나도 없다」** 고 적었는데, 이는 **디자인 시스템 파일만 본 것**이었습니다. 제품 파일 [`Syrup_App`](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i/Syrup_App)을 함께 보면 다릅니다.

| 파일 | 건수 |
| --- | --- |
| 디자인 시스템 | 0건 (수집 컷 제외) |
| **제품 `Syrup_App`** | **15건** · 3개 페이지 |

15건 **전부 `Height=Thick`** 이고, main component key가 현재 컴포넌트(`a84fc04b9...`)와 일치합니다. 구버전 참조는 없습니다.

**15건 모두 다른 컴포넌트에 중첩되지 않은 직접 배치**입니다 (2026-11-04 재확인). 상위 컴포넌트에 딸려 오는 경우가 없어, Border를 손보면 영향 범위가 이 15곳으로 한정됩니다.

> 제품 파일에서 14건이 레이어명 `Border`로, 1건만 `Height=Thick`으로 잡혔습니다. **원격 인스턴스의 이름 표기 차이일 뿐** 서로 다른 컴포넌트가 아닙니다 — key 전체를 대조해 확인했습니다. 원격 컴포넌트를 variant 이름으로 세는 스크립트는 이 때문에 결과가 갈릴 수 있습니다.

따라서 1번·2번(이름 혼동, 낮은 대비)이 채택을 막고 있었다는 추정은 **근거가 약합니다.** 쓰이고는 있었고, 다만 디자인 시스템 파일 쪽에 예제가 없었을 뿐입니다.

### 4. 폭이 FIXED 360

`layoutSizingHorizontal`이 `FILL`이 아니라 **`FIXED` 360**입니다. 폭이 다른 컨테이너에 넣으면 매번 수동으로 리사이즈해야 합니다.

**실제로 그러고 있습니다.** 제품 파일 15건의 폭이 네 가지로 갈립니다.

| 폭 | 건수 |
| --- | --- |
| 360 | 12 |
| 320 · 402 · 720 | 각 1 |

높이는 15건 모두 10으로 유지됩니다. 폭만 손으로 맞추고 있다는 뜻이라, `FILL`로 바꾸면 그 수고가 사라집니다. 다만 `FILL`은 오토레이아웃 컨테이너 안에서만 동작하므로 사용 맥락을 함께 정해야 합니다.

**네 가지 폭은 전부 화면 폭입니다** (2026-11-04). 같은 화면을 폭만 바꿔 복제한 것이라, 320 · 360 · 402 · 720은 제각각 틀어진 값이 아니라 기기별 변형입니다. [Banner](syrup-banner-components.md)·[AD](syrup-ad-components.md)에서도 같은 패턴이 나왔습니다. 그래서 이 항목은 **이탈이 아니라 `FILL`이 없어서 생기는 수작업**의 문제입니다.

### 5. `Thin`이 한 번도 쓰이지 않았습니다

`Height=Thin`(360 × 1, `Color/Gray_850`)은 **디자인 시스템 파일과 제품 파일 양쪽 모두 0건**입니다. 쓰이는 것은 `Thick` 15건뿐입니다.

| 선택지 | 내용 |
| --- | --- |
| A | 유지 — 항목 사이 구분선 자리가 아직 비어 있음 ([Guidelines 2](#2-서로-다른-콘텐츠-묶음-사이에-사용해요)) |
| B | 제거 — [Chip](syrup-chip-components.md)의 `Primary` variant를 0건 확인 후 삭제한 선례 |

`Thin`의 대비 문제는 [점검 2](#2--1px-선의-대비가-지나치게-낮음-2026-09-21-수정-완료)에서 이미 고쳤습니다. **고친 뒤에도 쓰이지 않은 것인지, 고친 사실이 알려지지 않은 것인지**부터 확인하는 편이 좋습니다. 지금 화면에서 항목 사이 구분선은 Border 대신 손으로 그려지고 있습니다.

### 6. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 컴포넌트 색상 | `Color/Gray_950` 바인딩 완료 |
| 미바인딩 radius · padding · gap | **0건** |
| 스타일 미적용 / 원격 스타일 텍스트 | **0건** (텍스트 없음) |
| 페이지 잔여 | padding `100` 2건 · `Spec docs/margin` 2건 · `Spec docs/width` 1건 — 전부 문서 레이아웃용 |

컴포넌트 자체는 토큰이 깔끔하게 적용되어 있습니다. 남은 문제는 **네이밍과 색상 선택** 쪽입니다.

### 7. `Thick`의 대비는 흰 배경 전용입니다

[점검 2](#2--1px-선의-대비가-지나치게-낮음-2026-09-21-수정-완료)에서 `Thin`의 색을 `Color/Gray_850`(#EDEDED)으로 올렸지만, **`Thick`은 `Color/Gray_950`(#F6F6F7) 그대로**입니다. 면적이 넓어 옅은 색으로도 구획이 인지된다는 판단이었습니다.

| Variant | 색 | 흰 배경과의 채널 차이 |
| --- | --- | --- |
| `Thin` (1px) | `Color/Gray_850` #EDEDED | 18 / 255 (약 7%) |
| `Thick` (10px) | `Color/Gray_950` #F6F6F7 | **9 / 255 (약 3.5%)** |

면적이 넓은 것은 맞지만, **배경이 흰색일 때만 성립하는 전제**입니다. Usage 컷을 만들면서 확인한 것이 이것입니다 — 조금이라도 회색이 깔린 배경 위에서는 10px 면이 배경에 묻혀 사라집니다. 그래서 컷의 묶음 프레임에 흰 바탕을 깔았습니다.

제품 파일 15건은 전부 흰 배경 위라 지금은 문제가 되지 않습니다. 다만 **회색 배경을 쓰는 화면이 생기면 `Thick`은 그 자리에서 보이지 않습니다.** 배경색을 가리지 않는 값으로 올릴지, 「흰 배경 전용」을 명시할지 정해 두는 편이 좋습니다.

### 8. ✅ 원본 컷 정리 (2026-11-04 완료)

컷을 컴포넌트 인스턴스로 바꾸면서 모아 둔 `원본 컷 (정리 전)` `11238:409`(4960 × 1085 · 컷 12개)를 **삭제했습니다.** 페이지에 남은 섹션은 `Border` · `Guidelines` · `Usage` 셋입니다.

### 9. 섹션 밖에 떠 있는 노드

| 노드 | 위치 | 내용 |
| --- | --- | --- |
| `Frame 1171277546` `11325:53815` | 섹션 밖 `(3823, 284)` | `INSTANCE` 360 × 102 |

어느 섹션에도 속하지 않고 `Usage` 오른쪽 바깥에 떠 있습니다. 컷을 세우는 과정에서 남은 것으로 보여 지우면 됩니다. [Banner](syrup-banner-components.md)의 `러비`와 같은 성격입니다.

### 10. 컷의 묶음 너비가 358입니다

`Guidelines` 네 컷의 묶음 프레임이 슬롯 너비에 맞춰 **358**(360 − 슬롯 테두리 1px × 2)인데, 그 사이의 `Border`는 **360 고정**입니다. 묶음보다 좌우로 1px씩 넓습니다.

슬롯 테두리와 겹치는 자리라 눈에 띄지는 않지만, **규칙 1이 「컨테이너의 전체 폭을 채운다」를 보여 주는 컷**이라 엄밀히는 `Border`도 묶음과 같은 358이어야 맞습니다. `Border`를 `FILL`로 바꾸면 자동으로 맞춰집니다 — [점검 4](#4-폭이-fixed-360)에서 다루는 `FIXED` 폭 문제가 문서 안에서 그대로 드러난 사례입니다.
